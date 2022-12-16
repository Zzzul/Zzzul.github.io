<template>
  <div id="mobile-navigation">
    <div class="d-sm-block d-md-none m-0">
      <br />
      <br />
      <br />
      <!-- <br /> -->
    </div>

    <div class="d-flex d-sm-block d-md-none fixed-bottom justify-content-end me-2" style="bottom: 100px;">
        <div class="form-group">
          <select class="form-select form-select-sm p-1" aria-label=".form-select-sm example" v-model="$colorMode.preference" style="width: 100px; font-size: 10px !important;" id="theme">
            <option value="system">System</option>
            <option value="light">Light</option>
            <option value="dark">Dark</option>
          </select>
        </div>
    </div>

      <div class="d-sm-block d-md-none fixed-bottom bg-primary bordered boder-top mb-2 mx-2">
          <div class="row px-3 py-2">
          <div class="col-3 m-0 p-0">
            <nuxt-link
              class="mb-0 py-2 nav-link text-dark text-center"
              to="/"
              style="font-size: 12px"
            >
              <span class="px-1">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-speedometer" viewBox="0 0 16 16">
                  <path d="M8 2a.5.5 0 0 1 .5.5V4a.5.5 0 0 1-1 0V2.5A.5.5 0 0 1 8 2zM3.732 3.732a.5.5 0 0 1 .707 0l.915.914a.5.5 0 1 1-.708.708l-.914-.915a.5.5 0 0 1 0-.707zM2 8a.5.5 0 0 1 .5-.5h1.586a.5.5 0 0 1 0 1H2.5A.5.5 0 0 1 2 8zm9.5 0a.5.5 0 0 1 .5-.5h1.5a.5.5 0 0 1 0 1H12a.5.5 0 0 1-.5-.5zm.754-4.246a.389.389 0 0 0-.527-.02L7.547 7.31A.91.91 0 1 0 8.85 8.569l3.434-4.297a.389.389 0 0 0-.029-.518z"/>
                  <path fill-rule="evenodd" d="M6.664 15.889A8 8 0 1 1 9.336.11a8 8 0 0 1-2.672 15.78zm-4.665-4.283A11.945 11.945 0 0 1 8 10c2.186 0 4.236.585 6.001 1.606a7 7 0 1 0-12.002 0z"/>
                </svg>
              </span>
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
              <span class="px-1">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-file-earmark-person-fill" viewBox="0 0 16 16">
                  <path d="M9.293 0H4a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V4.707A1 1 0 0 0 13.707 4L10 .293A1 1 0 0 0 9.293 0zM9.5 3.5v-2l3 3h-2a1 1 0 0 1-1-1zM11 8a3 3 0 1 1-6 0 3 3 0 0 1 6 0zm2 5.755V14a1 1 0 0 1-1 1H4a1 1 0 0 1-1-1v-.245S4 12 8 12s5 1.755 5 1.755z"/>
                </svg>
              </span>
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
              <span class="px-1">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-pc-display-horizontal" viewBox="0 0 16 16">
                  <path d="M1.5 0A1.5 1.5 0 0 0 0 1.5v7A1.5 1.5 0 0 0 1.5 10H6v1H1a1 1 0 0 0-1 1v3a1 1 0 0 0 1 1h14a1 1 0 0 0 1-1v-3a1 1 0 0 0-1-1h-5v-1h4.5A1.5 1.5 0 0 0 16 8.5v-7A1.5 1.5 0 0 0 14.5 0h-13Zm0 1h13a.5.5 0 0 1 .5.5v7a.5.5 0 0 1-.5.5h-13a.5.5 0 0 1-.5-.5v-7a.5.5 0 0 1 .5-.5ZM12 12.5a.5.5 0 1 1 1 0 .5.5 0 0 1-1 0Zm2 0a.5.5 0 1 1 1 0 .5.5 0 0 1-1 0ZM1.5 12h5a.5.5 0 0 1 0 1h-5a.5.5 0 0 1 0-1ZM1 14.25a.25.25 0 0 1 .25-.25h5.5a.25.25 0 1 1 0 .5h-5.5a.25.25 0 0 1-.25-.25Z"/>
                </svg>
              </span>
              <br />
              <small class="m-0 p-0" style="font-size: 8px">Projects</small>
            </nuxt-link>
          </div>

          <div class="col-3 m-0 p-0">
            <nuxt-link :class="isBlogRoute()" to="/blog" style="font-size: 12px">
              <span class="px-1">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-stickies-fill" viewBox="0 0 16 16">
                  <path d="M0 1.5V13a1 1 0 0 0 1 1V1.5a.5.5 0 0 1 .5-.5H14a1 1 0 0 0-1-1H1.5A1.5 1.5 0 0 0 0 1.5z"/>
                  <path d="M3.5 2A1.5 1.5 0 0 0 2 3.5v11A1.5 1.5 0 0 0 3.5 16h6.086a1.5 1.5 0 0 0 1.06-.44l4.915-4.914A1.5 1.5 0 0 0 16 9.586V3.5A1.5 1.5 0 0 0 14.5 2h-11zm6 8.5a1 1 0 0 1 1-1h4.396a.25.25 0 0 1 .177.427l-5.146 5.146a.25.25 0 0 1-.427-.177V10.5z"/>
                </svg>
              </span>
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
