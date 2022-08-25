<template>
  <div id="home">
    <desktop-navigation />

    <div class="container mb-5">
      <div class="row">
        <breadcrumb>
          <li class="breadcrumb-item">
            <nuxt-link to="/" class="text-decoration-none">Home</nuxt-link>
          </li>
          <li class="breadcrumb-item active" aria-current="page">Blog</li>
        </breadcrumb>

        <div class="col-md-12 mt-0 mb-3">
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

        <!-- Desktop -->
        <div v-if="loading" class="d-none d-md-block mt-4">
          <div class="row">
            <div class="col-md-12 mb-3">
              <div class="card bordered p-0">
                <div class="card-body p-4 text-center">
                  <marquee
                    behavior="alternate"
                    onmouseover="this.stop()"
                    onmouseout="this.start()"
                    direction="right"
                    width="20%"
                    >Loading..
                  </marquee>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Mobile -->
        <div v-if="loading" class="d-sm-block d-md-none mt-4">
          <div class="row">
            <div class="col-md-12 mb-3">
              <div class="card bordered p-0">
                <div class="card-body p-5 text-center">
                  <marquee
                    behavior="alternate"
                    onmouseover="this.stop()"
                    onmouseout="this.start()"
                    direction="right"
                    >Loading..
                  </marquee>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Post card -->
        <div
          class="col-md-12 mt-4"
          v-else
          v-for="post of posts"
          :key="post.slug"
        >
          <BlogCard :post="post" />
        </div>

        <div class="text-center mt-4" v-if="postNotFound">
          <p>Post Not Found.</p>
        </div>
      </div>
    </div>

    <Footer />

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
      loading: true,
    }
  },
  methods: {
    async getPostsData() {
      const articles = await this.$content("posts")
        .only(["title", "description", "slug", "color", "tags"])
        .sortBy("ID", "desc")
        .search(this.search)
        .fetch()
        .catch((err) => (this.postNotFound = true))

      if (articles.length < 1) {
        this.postNotFound = true
      } else {
        this.postNotFound = false
      }

      this.loading = false

      this.posts = articles
    },
  },
  created() {
    this.getPostsData()
  },
}
</script>
