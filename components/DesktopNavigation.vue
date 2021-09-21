<template>
  <div class="d-none d-md-block">
    <nav class="navbar navbar-expand-lg navbar-light bg-primary mb-5 bordered">
      <div class="container py-2">
        <nuxt-link
          class="navbar-brand"
          to="/"
          style="border-bottom: none !important"
          >Zul</nuxt-link
        >
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
              <nuxt-link class="nav-link" to="/">Home</nuxt-link>
            </li>

            <li class="nav-item">
              <nuxt-link class="nav-link" to="/about">About</nuxt-link>
            </li>

            <li class="nav-item">
              <nuxt-link class="nav-link" to="/projects">Projects</nuxt-link>
            </li>

            <li class="nav-item">
              <nuxt-link class="nav-link" to="/blog">Blog</nuxt-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>

