---
title: First post
description: Ini adalah post pertama menggunakan nuxtjs content module.
slug: first-post
color: '#E0ECE4'
---

# First post

Ini adalah post pertama yang saya buat menggunakan `@nuxtjs/content` yang digenerate dari file markdown `.md`

### Lorem ipsum

dolor sit amet consectetur adipisicing elit. Eveniet debitis, libero recusandae architecto eum ab perspiciatis pariatur reprehenderit eaque saepe aut doloribus ut aperiam nam assumenda nostrum explicabo atque omnis rem sunt blanditiis non! Eaque, quidem. Impedit ducimus assumenda voluptatibus?

#### Vestibulum
 ac diam sit amet quam vehicula elementum sed sit amet dui. Pellentesque in ipsum id orci porta dapibus. Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Donec velit neque, auctor sit amet aliquam vel, ullamcorper sit amet ligula. Nulla porttitor accumsan tincidunt. Sed porttitor lectus nibh. Vivamus suscipit tortor eget felis porttitor volutpat. Donec rutrum congue leo eget malesuada. Proin eget tortor risus. Curabitur non nulla sit amet nisl tempus convallis quis ac lectus. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque in ipsum id orci porta dapibus. Quisque velit nisi, pretium ut lacinia in, elementum id enim.

Dibawah ini adalah coding yang digunakan pada halaman ini

 ```js
 <template>
  <div id="home">
    <desktop-navigation />

    <div class="container">
      <div class="row mt-2 mb-4">
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
    }, 1500)
  },
}
</script>

 ```
