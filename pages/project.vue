<template>
  <div id="project">
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

    <div class="container">
      <div class="row">
        <Breadcrumb>
          <li class="breadcrumb-item"><nuxt-link to="/">Home</nuxt-link></li>
          <li class="breadcrumb-item" aria-current="page">Project</li>
        </Breadcrumb>

        <div class="col-sm-12 col-md-6 col-lg-4 mt-1">
          <div
            class="card my-card shadow-sm nes-container is-rounded p-0 is-dark"
          >
            <div class="card-body p-3">
              <a href="#" style="font-size: 12px">Lorem ipsum dolor</a>
              <p class="my-2" style="font-size: 9px">
                Lorem ipsum dolor, sit amet consectetur adipisicing elit.
                Minima, commodi!
              </p>
            </div>
          </div>
        </div>

        <div class="col-sm-12 col-md-6 col-lg-4 mt-1">
          <div
            class="card my-card shadow-sm nes-container is-rounded p-0 is-dark"
          >
            <div class="card-body p-3">
              <a href="#" style="font-size: 12px">Lorem ipsum dolor</a>
              <p class="my-2" style="font-size: 9px">
                Lorem ipsum dolor, sit amet consectetur adipisicing elit.
                Minima, commodi!
              </p>
            </div>
          </div>
        </div>

        <div class="col-sm-12 col-md-6 col-lg-4 mt-1">
          <div
            class="card my-card shadow-sm nes-container is-rounded p-0 is-dark"
          >
            <div class="card-body p-3">
              <a href="#" style="font-size: 12px">Lorem ipsum dolor</a>
              <p class="my-2" style="font-size: 9px">
                Lorem ipsum dolor, sit amet consectetur adipisicing elit.
                Minima, commodi!
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
    title: "Project",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "kerjaan/project yang saya buat",
      },
    ],
  },
}
</script>
