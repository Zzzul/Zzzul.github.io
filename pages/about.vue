<template>
  <div id="home">
    <DesktopNavigation/>
    <div class="container">
      <div class="row">
        <Breadcrumb>
          <li class="breadcrumb-item">
            <nuxt-link to="/" class="text-decoration-none">Home</nuxt-link>
          </li>
          <li class="breadcrumb-item active" aria-current="page">About</li>
        </Breadcrumb>
        <div class="col-md-12">
          <AboutDescription />
        </div>
        <div class="mb-5" id="skills"></div>
        <div class="col-md-12 mb-5">
          <AboutSkill />
        </div>
        <div class="col-md-12 mb-4">
          <AboutContact />
        </div>
      </div>
    </div>
    <Footer />
    <MobileNavigation/>
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

