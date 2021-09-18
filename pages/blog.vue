<template>
  <div id="blog">
    <!-- desktop -->
    <div class="d-none d-md-block mb-0">
      <div class="container">
        <div class="row justify-content-center pt-5">
          <div class="col-md-12 mb-4">
            <HeaderDesktop />
          </div>
        </div>
      </div>
    </div>

    <!-- global -->
    <div class="container">
      <div class="row">
        <Breadcrumb>
          <li class="breadcrumb-item"><nuxt-link to="/">Home</nuxt-link></li>
          <li class="breadcrumb-item" aria-current="page">Blog</li>
        </Breadcrumb>

        <div
          class="col-sm-12 col-md-6 col-lg-4 mt-1"
          v-for="article of articles"
          :key="article.slug"
        >
          <div
            class="card my-card shadow-sm nes-container is-rounded p-0 is-dark"
          >
            <div class="card-body p-3">
              <nuxt-link
                :to="{ name: 'slug', params: { slug: article.slug } }"
                class="text-primary"
                style="font-size: 12px"
              >
                {{ article.title }}
              </nuxt-link>

              <p class="my-2" style="font-size: 9px">
                {{ article.description }}
              </p>
            </div>
          </div>
        </div>

        <div class="col-md-12 mt-3 mb-3">
          <p class="text-center text-light">~~~</p>
        </div>
      </div>
    </div>

    <!-- mobile -->
    <div class="d-sm-block d-md-none m-0 p-0 mt-4">
      <div class="container pt-5 mb-0 pb-0">
        <HeaderMobile />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  head: {
    title: "Blog",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "semua post yang saya buat",
      },
    ],
  },
  async asyncData({ $content, params }) {
    const articles = await $content("blog", params.slug)
      .only(["title", "description", "slug"])
      .sortBy("createdAt", "asc")
      .fetch()

    return { articles }
  },
}
</script>

