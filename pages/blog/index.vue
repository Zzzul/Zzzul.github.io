<template>
  <div id="home">
    <desktop-navigation />

    <div class="container">
      <div class="row mt-4 mb-5">
        <breadcrumb>
          <li class="breadcrumb-item">
            <nuxt-link to="/" class="text-decoration-none">Home</nuxt-link>
          </li>
          <li class="breadcrumb-item active" aria-current="page">Blog</li>
        </breadcrumb>

        <!-- Card -->
        <div
          class="col-sm-12 col-md-6 col-lg-4 mb-4"
          v-for="post of posts"
          :key="post.slug"
        >
          <div
            class="card bordered-hover p-0"
            :style="{ 'background-color': post.color }"
          >
            <div class="card-body p-3">
              <nuxt-link
                class="mb-1 mt-1"
                style="font-size: 13px"
                :to="'/blog/' + post.slug"
              >
                {{ post.title }}
                <br />
                <span style="font-size: 9px" class="text-dark">{{
                  post.description
                }}</span>
              </nuxt-link>
            </div>
          </div>
        </div>

        <Footer />
      </div>
    </div>

    <mobile-navigation />
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const posts = await $content("posts", params.slug)
      .only(["title", "description", "slug", "color"])
      .sortBy("createdAt", "desc")
      .fetch()
    return { posts }
  },
  head: {
    title: "Blog",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "Tulisan yang saya buat, biasanya tentang Web Programming",
      },
    ],
  },
}
</script>
