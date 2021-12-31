<template>
  <div id="mobile-navigation">
    <div class="d-sm-block d-md-none">
      <br />
      <br />
      <br />
      <br />
    </div>

    <div
      class="
        d-sm-block d-md-none
        mt-4
        bg-primary
        bordered
        fixed-bottom
        boder-top
      "
      style="margin-top: 110px"
    >
      <div class="row px-3 py-2">
        <div class="col-3 m-0 p-0">
          <nuxt-link
            class="mb-0 py-2 nav-link text-dark text-center"
            to="/"
            style="font-size: 12px"
          >
            <span class="px-1">H</span>
            <br />
            <small class="m-0 p-0" style="font-size: 8px">Home</small>
          </nuxt-link>
        </div>

        <div class="col-3 m-0 p-0">
          <nuxt-link
            :class="isAboutRoute()"
            to="/about"
            style="font-size: 12px"
          >
            <span class="px-1">A</span>
            <br />
            <small class="m-0 p-0" style="font-size: 8px">About</small>
          </nuxt-link>
        </div>

        <div class="col-3 m-0 p-0">
          <nuxt-link
            class="mb-0 py-2 nav-link text-dark text-center"
            to="/projects"
            style="font-size: 12px"
          >
            <span class="px-1">P</span>
            <br />
            <small class="m-0 p-0" style="font-size: 8px">Projects</small>
          </nuxt-link>
        </div>

        <div class="col-3 m-0 p-0">
          <nuxt-link :class="isBlogRoute()" to="/blog" style="font-size: 12px">
            <span class="px-1">B</span>
            <br />
            <small class="m-0 p-0" style="font-size: 8px">Blog</small>
          </nuxt-link>
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
        return "mb-0 py-2 nav-link text-dark text-center nuxt-link-exact-active "
      }

      return "mb-0 py-2 nav-link text-dark text-center"
    },
    isAboutRoute() {
      if (this.$route.name == "about") {
        return "mb-0 py-2 nav-link text-dark text-center nuxt-link-exact-active "
      }

      return "mb-0 py-2 nav-link text-dark text-center"
    },
  },
}
</script>
