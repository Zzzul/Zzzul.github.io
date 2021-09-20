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

        <div class="col-md-12 mt-1">
          <div class="card shadow-sm nes-container is-rounded p-0 is-dark">
            <div class="card-body p-3">
              <p class="my-2">
                Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem.
                Pellentesque in ipsum id orci porta dapibus. Pellentesque in
                ipsum id orci porta dapibus. Vivamus magna justo, lacinia eget
                consectetur sed, convallis at tellus. Vivamus suscipit tortor
                eget felis porttitor volutpat. Nulla porttitor accumsan
                tincidunt. Pellentesque in ipsum id orci porta dapibus. Mauris
                blandit aliquet elit, eget tincidunt nibh pulvinar a. Curabitur
                non nulla sit amet nisl tempus convallis quis ac lectus.
                Curabitur non nulla sit amet nisl tempus convallis quis ac
                lectus. Cras ultricies ligula sed magna dictum porta. Curabitur
                aliquet quam id dui posuere blandit. Curabitur non nulla sit
                amet nisl tempus convallis quis ac lectus.
              </p>
            </div>
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
