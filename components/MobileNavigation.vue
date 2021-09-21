<template>
  <div
    class="d-sm-block d-md-none mt-5 bg-primary bordered fixed-bottom"
    style="margin-top: 100px"
  >
    <div class="row px-3 py-2">
      <div class="col-3 m-0 p-0">
        <nuxt-link
          class="mb-0 py-2 nav-link text-dark text-center"
          to="/"
          style="font-size: 12px"
        >
          <span class="px-1 active-uri">H</span>
          <br />
          <small class="m-0 p-0 text-link-bottom">Home</small>
        </nuxt-link>
      </div>

      <div class="col-3 m-0 p-0">
        <nuxt-link
          class="mb-0 py-2 nav-link text-dark text-center"
          to="/about"
          style="font-size: 12px"
        >
          <span class="px-1">A</span>
          <br />
          <small class="m-0 p-0 text-link-bottom">About</small>
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
          <small class="m-0 p-0 text-link-bottom">Projects</small>
        </nuxt-link>
      </div>

      <div class="col-3 m-0 p-0">
        <nuxt-link
          class="mb-0 py-2 nav-link text-dark text-center"
          to="/blog"
          style="font-size: 12px"
        >
          <span class="px-1">B</span>
          <br />
          <small class="m-0 p-0 text-link-bottom">Blog</small>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>
