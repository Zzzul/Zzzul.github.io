<template>
	<div v-if="loading">
	<!-- Desktop -->
        <div  class="d-none d-md-block">
          <div class="row">
            <div class="col-md-4 mb-4">
              <div class="card bordered p-0">
                <div class="card-body p-5">
                  <marquee
                    behavior="alternate"
                    onmouseover="this.stop()"
                    onmouseout="this.start()"
                    direction="right"
                    >Loading..
                  </marquee>
                </div>
              </div>
            </div>

            <div class="col-md-4">
              <div class="card bordered p-0">
                <div class="card-body p-5">
                  <marquee
                    behavior="alternate"
                    onmouseover="this.stop()"
                    onmouseout="this.start()"
                    direction="right"
                    >Loading..
                  </marquee>
                </div>
              </div>
            </div>

            <div class="col-md-4">
              <div class="card bordered p-0">
                <div class="card-body p-5">
                  <marquee
                    behavior="alternate"
                    onmouseover="this.stop()"
                    onmouseout="this.start()"
                    direction="right"
                    >Loading..
                  </marquee>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Mobile -->
        <div class="d-sm-block d-md-none">
          <div class="row">
            <div class="col-md-12 mb-4">
              <div class="card bordered p-0">
                <div class="card-body p-5">
                  <marquee
                    behavior="alternate"
                    onmouseover="this.stop()"
                    onmouseout="this.start()"
                    direction="right"
                    >Loading..
                  </marquee>
                </div>
              </div>
            </div>
          </div>
        </div>
     </div>
</template>

<script>
export default {
  props: ["loading"],
}
</script>