<template>
  <div class="d-none d-md-block mb-0">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <nav
            class="
              navbar navbar-expand-lg navbar-light
              bg-primary
              bordered
            "
            id="desktop-nav"
          >
            <div class="container py-2">
              <nuxt-link
                class="navbar-brand"
                to="/"
                style="border-bottom: none !important"
              >
                M!
              </nuxt-link>
              <button
                class="navbar-toggler bordered-without-shadow"
                type="button"
                data-bs-toggle="collapse"
                data-bs-target="#navbarSupportedContent"
                aria-controls="navbarSupportedContent"
                aria-expanded="false"
                aria-label="Toggle navigation"
              >
                <span class="navbar-toggler-icon"></span>
              </button>
              <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
                  <li class="nav-item custom-nav-item">
                    <nuxt-link class="nav-link" to="/">
                      Home
                    </nuxt-link>
                  </li>

                  <li class="nav-item custom-nav-item">
                    <nuxt-link
                      :class="isAboutRoute()"
                      to="/about"
                    >
                      About
                    </nuxt-link>
                  </li>

                  <li class="nav-item custom-nav-item">
                    <nuxt-link
                      class="nav-link"
                      to="/projects"
                    >
                      Projects
                    </nuxt-link>
                  </li>

                  <li class="nav-item custom-nav-item me-3">
                    <nuxt-link
                      :class="isBlogRoute()"
                      to="/blog"
                    >
                      Blog
                    </nuxt-link>
                  </li>

                  <li class="nav-item">
                    <select class="form-select form-select-sm mt-1 mb-0 px-4 py-1" aria-label=".form-select-sm example"v-model="$colorMode.preference">
                      <option value="system">System</option>
                      <option value="light">Light</option>
                      <option value="dark">Dark</option>
                    </select>
                  </li>
                </ul>
              </div>
            </div>
          </nav>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    isBlogRoute() {
      if (this.$route.name == "blog" || this.$route.name == "blog-slug") {
        return "nav-link nuxt-link-exact-active "
      }

      return "nav-link"
    },
    
    isAboutRoute() {
      if (this.$route.name == "about") {
        return "nav-link nuxt-link-exact-active "
      }

      return "nav-link"
    },

    changeToDarkMode(){
      this.$colorMode.preference = 'dark'
    },

    changeToLightMode(){
      this.$colorMode.preference = 'light'
    }
  },
}
</script>

