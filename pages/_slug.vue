<template>
  <div id="slug">
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
          <li class="breadcrumb-item">
            <nuxt-link to="/blog">Blog</nuxt-link>
          </li>
          <li class="breadcrumb-item" aria-current="page">
            {{ post.slug }}
          </li>
        </Breadcrumb>

        <div class="col-md-12">
          <div class="nes-container is-rounded is-dark p-4 text-light">
            <div v-if="loading" class="text-center mt-3">
              <h6>Loading..</h6>
            </div>
            <div v-else>
              <nuxt-content :document="post" />
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
  data() {
    return {
      title: "",
      description: "",
      loading: true,
      post: [],
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: "description",
          name: "description",
          content: this.description,
        },
      ],
    }
  },
  async mounted() {
    const post = await this.$content("blog", this.$route.params.slug).fetch()

    this.post = post
    this.title = post.title
    this.description = post.description

    setInterval(() => {
      this.loading = false
    }, 500)
  },
}
</script>
