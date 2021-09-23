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

        <!-- Post card -->
        <div
          class="col-sm-12 col-md-6 col-lg-4 mb-4"
          v-for="post of posts"
          :key="post.slug"
        >
          <BlogCard :post="post" />
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
