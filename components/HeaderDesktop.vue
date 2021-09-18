<template>
  <div id="navbar">
    <nav class="navbar navbar-light navbar-expand-md bg-transparent">
      <button
        class="navbar-toggler ml-1"
        type="button"
        data-toggle="collapse"
        data-target="#collapsingNavbar2"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="navbar-collapse collapse" id="collapsingNavbar2">
        <ul class="navbar-nav mx-auto text-center">
          <li class="nav-item px-4">
            <nuxt-link
              class="nav-link text-light text-decoraion-none my-link active"
              to="/"
              >Home</nuxt-link
            >
          </li>

          <li class="nav-item px-4">
            <nuxt-link
              to="/about"
              class="nav-link text-light text-decoraion-none my-link"
              >About
            </nuxt-link>
          </li>

          <li class="nav-item px-4">
            <nuxt-link
              class="nav-link text-light text-decoraion-none my-link"
              to="/project"
              >Project</nuxt-link
            >
          </li>

          <li class="nav-item px-4">
            <nuxt-link
              class="nav-link text-light text-decoraion-none my-link"
              to="/blog"
              >Blog</nuxt-link
            >
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>
