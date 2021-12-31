<template>
  <div id="home">
    <desktop-navigation />

    <div class="container mb-3">
      <div class="row mb-4">
        <breadcrumb>
          <li class="breadcrumb-item">
            <nuxt-link to="/" class="text-decoration-none">Home</nuxt-link>
          </li>
          <li class="breadcrumb-item active" aria-current="page">About</li>
        </breadcrumb>

        <!-- About -->
        <div class="col-md-12">
          <about-description />
        </div>

        <div class="mb-5" id="skills"></div>

        <!-- Skills -->
        <div class="col-md-12 mb-5">
          <about-skill />
        </div>

        <!-- Contact -->
        <div class="col-md-12 mb-3">
          <about-contact />
        </div>

        <Footer />
      </div>
    </div>

    <mobile-navigation />
  </div>
</template>

<script>
export default {
  head: {
    title: "About",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "Mari mengenal saya lebih dekat",
      },
    ],
  },
}
</script>

