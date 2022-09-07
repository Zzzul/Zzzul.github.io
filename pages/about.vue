<template>
  <div id="home">
    <desktop-navigation />

    <div class="container">
      <div class="row">
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
        <div class="col-md-12 mb-4">
          <about-contact />
        </div>
      </div>
    </div>

    <Footer />

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
        content: "Mari mengenal lebih dekat tentang saya.",
      },
    ],
  },
}
</script>

