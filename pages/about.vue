<template>
  <div id="home">
    <desktop-navigation />

    <div class="container">
      <div class="row mt-4 mb-5">
        <breadcrumb>
          <li class="breadcrumb-item">
            <nuxt-link to="/" class="text-decoration-none">Home</nuxt-link>
          </li>
          <li class="breadcrumb-item active" aria-current="page">About</li>
        </breadcrumb>

        <!-- About -->
        <div class="col-md-12 mb-5">
          <AboutDescription />
        </div>

        <!-- Skills -->
        <div class="col-md-12 mb-3" id="skills">
          <AboutSkill />
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
    title: "Blog",
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

