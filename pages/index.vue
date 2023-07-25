<template>
  <div id="home">
    <DesktopNavigation />
    <div class="container">
      <div class="row">
        <Breadcrumb>
          <li class="breadcrumb-item active text-secondary" aria-current="page">
            Home
          </li>
        </Breadcrumb>
        <div class="col-md-12 mb-4" id="main-content">
          <div class="card bordered">
            <div class="card-body p-5 text-center">
              <h6 class="mb-3">Hai!</h6>
              <h6 class="mb-3">Saya Mohammad Zulfahmi,</h6>
              <h6 class="mb-4">Dan ini adalah website pribadi milik saya.</h6>
              <Socmed/>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Footer />
    <MobileNavigation />
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
