<template>
  <div id="about">
    <!-- desktop -->
    <div class="d-none d-md-block mb-0">
      <div class="container">
        <div class="row justify-content-center pt-5">
          <div class="col-md-12 mb-4">
            <HeaderDesktop />
          </div>
        </div>
      </div>
    </div>

    <!-- global -->
    <div class="container">
      <div class="row">
        <Breadcrumb>
          <li class="breadcrumb-item"><nuxt-link to="/">Home</nuxt-link></li>
          <li class="breadcrumb-item" aria-current="page">About</li>
        </Breadcrumb>

        <div class="col-md-12">
          <div class="nes-container is-rounded is-dark is-centered p-4">
            <p class="text-light" style="font-size: 12px">
              Lorem ipsum, dolor sit amet consectetur adipisicing elit.
              Recusandae nisi quia incidunt eligendi dolores, delectus adipisci
              laudantium voluptate ut blanditiis! Molestias nemo eius,
              cupiditate voluptas eum numquam recusandae architecto esse.
            </p>
          </div>
        </div>

        <div class="col-md-12 mt-3 mb-3">
          <p class="text-center text-light">~~~</p>
        </div>
      </div>
    </div>

    <!-- mobile -->
    <div class="d-sm-block d-md-none m-0 p-0 mt-4">
      <div class="container pt-5 mb-0 pb-0">
        <HeaderMobile />
      </div>
    </div>
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
        content: "informasi tentang saya",
      },
    ],
  },
}
</script>
