<template>
  <div id="cv">
    <desktop-navigation />

    <div class="container">
      <div class="row">
        <breadcrumb>
          <li class="breadcrumb-item">
            <nuxt-link to="/" class="text-decoration-none">Home</nuxt-link>
          </li>
          <li class="breadcrumb-item active" aria-current="page">CV</li>
        </breadcrumb>

        <div>
            <embed src="/pdf/cv.pdf" width="100%" height="900px"/>
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
    title: "CV",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "CV dan sertifikat yang telah saya dapatkan.",
      },
    ],
  },
}
</script>

