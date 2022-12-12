<template>
  <div id="home">
    <desktop-navigation />

    <div class="container">
      <div class="row">
        <breadcrumb>
          <li class="breadcrumb-item active text-secondary" aria-current="page">
            Home
          </li>
        </breadcrumb>

        <!-- Card -->
        <div class="col-md-12 mb-4" id="main-content">
          <div class="card bordered">
            <div class="card-body p-5 text-center">
              <h5 class="mb-3">Hai!</h5>
              <h3 class="mb-3">Saya Mohammad Zulfahmi</h3>
              <h4 class="mb-4">Web Developer, Freelance, & Tech enthusiast.</h4>
              <Socmed/>
            </div>
          </div>
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
    title: "Home",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "Hai!, saya Mohammad Zulfahmi dan ini adalah website pribadi saya.",
      },
    ],
  },
}
</script>
