<template>
  <div id="home">
    <desktop-navigation />

    <div class="container">
      <div class="row mt-4 mb-5">
        <breadcrumb>
          <li class="breadcrumb-item">
            <nuxt-link to="/" class="text-decoration-none">Home</nuxt-link>
          </li>
          <li class="breadcrumb-item">
            <nuxt-link to="/blog" class="text-decoration-none">Blog</nuxt-link>
          </li>
          <li class="breadcrumb-item active" aria-current="page">
            {{ slug }}
          </li>
        </breadcrumb>

        <div class="col-md-12 mb-4">
          <div class="card bordered">
            <div class="card-body p-4">
              <nuxt-content :document="post" />
            </div>
          </div>
        </div>

        <div class="col-md-12 text-center my-5">~~~</div>
      </div>
    </div>

    <mobile-navigation />
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "",
      description: "",
      slug: "",
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
    const post = await this.$content("posts", this.$route.params.slug).fetch()

    this.post = post
    this.title = post.title
    this.slug = post.slug
    this.description = post.description

    // setInterval(() => {
    //   this.loading = false
    // }, 1000)
  },
}
</script>
