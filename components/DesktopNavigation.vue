<template>
  <div class="d-none d-md-block">
    <nav
      class="navbar navbar-expand-lg navbar-light bg-primary mb-5 bordered"
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
              <nuxt-link class="nav-link" to="/" style="font-size: 13px">
                Home
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
  },
}
</script>

