<template>
  <div id="home">
    <desktop-navigation />

    <div class="container">
      <div class="row mt-4 mb-4">
        <breadcrumb>
          <li class="breadcrumb-item">
            <nuxt-link to="/" class="text-decoration-none">Home</nuxt-link>
          </li>
          <li class="breadcrumb-item active" aria-current="page">Blog</li>
        </breadcrumb>

        <div class="col-md-12 mt-0 mb-4">
          <div class="form-group">
            <input
              type="text"
              v-model="search"
              class="form-control"
              placeholder="Search..."
              @keyup="getPostsData"
              @keydown="getPostsData"
            />
          </div>
        </div>

        <!-- Post card -->
        <div class="col-md-12 mt-4" v-for="post of posts" :key="post.slug">
          <BlogCard :post="post" />
        </div>

        <div class="text-center mt-4" v-if="postNotFound">
          <p>Post Not Found.</p>
        </div>

        <Footer />
      </div>
    </div>

    <mobile-navigation />
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
        content:
          "Tulisan yang saya buat dan berharap bisa bermanfaat untuk kamu. biasanya tentang Web Programming/IT",
      },
    ],
  },
  data() {
    return {
      posts: [],
      search: "",
      postNotFound: false,
    }
  },
  methods: {
    async getPostsData() {
      const articles = await this.$content("posts")
        .only(["title", "description", "slug", "color"])
        .sortBy("createdAt", "desc")
        .search(this.search)
        .fetch()
        .catch((err) => (this.postNotFound = true))

      if (articles.length < 1) {
        this.postNotFound = true
      }

      this.posts = articles
    },
  },
  created() {
    this.getPostsData()
  },
}
</script>
