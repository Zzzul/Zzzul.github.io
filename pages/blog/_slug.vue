<template>
  <div id="home">
    <desktop-navigation />

    <div class="container">
      <div class="row">
        <breadcrumb>
          <li class="breadcrumb-item">
            <nuxt-link to="/" class="text-decoration-none">Home</nuxt-link>
          </li>
          <li class="breadcrumb-item">
            <nuxt-link to="/blog" class="text-decoration-none">Blog</nuxt-link>
          </li>
          <li class="breadcrumb-item active" aria-current="page">
            <span v-if="loading">...</span>
            <span v-else>{{ post.slug }}</span>
          </li>
        </breadcrumb>

        <div class="col-md-12 mb-3">
          <div class="card bordered">
            <div class="card-body p-4">
              <div v-if="loading" class="text-center mt-3 mb-1">
                <!-- <h6>Loading..</h6> -->
                <div class="d-none d-md-block">
                  <!-- Desktop -->
                  <marquee
                    behavior="alternate"
                    onmouseover="this.stop()"
                    onmouseout="this.start()"
                    width="20%"
                    direction="right"
                    >Loading..
                  </marquee>
                </div>

                <!-- Mobile -->
                <div class="d-sm-block d-md-none">
                  <marquee
                    behavior="alternate"
                    onmouseover="this.stop()"
                    onmouseout="this.start()"
                    direction="right"
                    width="100%"
                    class="mb-2"
                    >Loading..
                  </marquee>
                </div>
              </div>
              <div v-else>
                <nuxt-content :document="post" />
              </div>
            </div>
          </div>
        </div>

        <div class="col-md-12 mb-3 mt-5" v-if="!loading">
          <div class="card bordered-hover">
            <div class="card-body p-4">
              <h6 class="text-center m-0" style="line-height: 21px">
                Halo, kamu telah mencapai penghujung halaman, terima kasih telah
                membacanya hingga akhir. Semoga harimu menyenangkan.
              </h6>
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
  data() {
    return {
      loading: true,
      post: [],
    }
  },
  head() {
    return {
      title: this.post.title,
      meta: [
        {
          hid: "description",
          name: "description",
          content: this.post.description,
        },
      ],
    }
  },
  async mounted() {
    const post = await this.$content("posts", this.$route.params.slug).fetch()

    this.post = post

    setTimeout(() => {
      this.loading = false
    }, 1000)
  },
}
</script>
