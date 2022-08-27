<template>
  <div class="d-none d-md-block mb-0">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <nav
            class="
              navbar navbar-expand-lg navbar-light
              bg-primary
              mb-5
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
                  <li class="nav-item">
                    <button @click="toggleTheme" class="btn btn-transparent text-dark me-3 mt-0 mb-0 px-0 pt-1">
                      <svg  xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="currentColor" class="bi bi-cloud-moon" viewBox="0 0 16 16" >
                        <path d="M7 8a3.5 3.5 0 0 1 3.5 3.555.5.5 0 0 0 .625.492A1.503 1.503 0 0 1 13 13.5a1.5 1.5 0 0 1-1.5 1.5H3a2 2 0 1 1 .1-3.998.5.5 0 0 0 .509-.375A3.502 3.502 0 0 1 7 8zm4.473 3a4.5 4.5 0 0 0-8.72-.99A3 3 0 0 0 3 16h8.5a2.5 2.5 0 0 0 0-5h-.027z"/>
                        <path d="M11.286 1.778a.5.5 0 0 0-.565-.755 4.595 4.595 0 0 0-3.18 5.003 5.46 5.46 0 0 1 1.055.209A3.603 3.603 0 0 1 9.83 2.617a4.593 4.593 0 0 0 4.31 5.744 3.576 3.576 0 0 1-2.241.634c.162.317.295.652.394 1a4.59 4.59 0 0 0 3.624-2.04.5.5 0 0 0-.565-.755 3.593 3.593 0 0 1-4.065-5.422z"/>
                      </svg>
                    </button>
                  </li>

                  <li class="nav-item">
                    <nuxt-link class="nav-link" to="/" style="font-size: 13px">
                      Home {{ userTheme }}
                    </nuxt-link>
                  </li>

                  <li class="nav-item">
                    <nuxt-link
                      :class="isAboutRoute()"
                      to="/about"
                      style="font-size: 13px"
                    >
                      About
                    </nuxt-link>
                  </li>

                  <li class="nav-item">
                    <nuxt-link
                      class="nav-link"
                      to="/projects"
                      style="font-size: 13px"
                    >
                      Projects
                    </nuxt-link>
                  </li>

                  <li class="nav-item">
                    <nuxt-link
                      :class="isBlogRoute()"
                      to="/blog"
                      style="font-size: 13px"
                    >
                      Blog
                    </nuxt-link>
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
   mounted() {
    const initUserTheme = this.getTheme() || this.getMediaPreference()
    this.setTheme(initUserTheme)
  },
   data() {
    return {
       userTheme: "light",
    }
  },
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

    toggleTheme() {
      const activeTheme = localStorage.getItem("user-theme")
      if (activeTheme === "light") {
        this.setTheme("dark")
      } else {
        this.setTheme("light")
      }
    },

    getTheme() {
      return localStorage.getItem("user-theme")
    },

    setTheme(theme) {
      localStorage.setItem("user-theme", theme)
      this.userTheme = theme
      document.documentElement.className = theme
    },

    getMediaPreference() {
      const hasDarkPreference = window.matchMedia("(prefers-color-scheme: dark)").matches

      if (hasDarkPreference) {
        return "dark"
      } else {
        return "light"
      }
    },
  },
}
</script>

