<template>
  <div id="skeleton-home">
    <!-- Global loading -->
    <div class="col-sm-12 mb-0" v-if="loading">
      <div class="ph-item bordered mb-0 py-5">
        <div class="ph-col-12">
          <div class="ph-row">
            <div class="ph-col-4 empty"></div>
            <div class="ph-col-4 big"></div>
            <div class="ph-col-4 empty"></div>
            <div class="ph-col-4 empty"></div>
            <div class="ph-col-4 big"></div>
            <div class="ph-col-4 empty"></div>

            <div class="ph-col-12 big"></div>
            <div class="ph-col-12 big"></div>

            <div class="ph-col-2 empty"></div>
            <div class="ph-col-8 big"></div>
            <div class="ph-col-2 empty"></div>
          </div>
        </div>

        <!-- Desktop loading -->
        <div class="d-none d-md-block">
          <div class="ph-col-12">
            <div class="ph-row">
              <div class="ph-col-2 empty"></div>
              <div
                class="ph-picture ms-5 me-3"
                style="width: 50px; height: 50px; margin-left: 163px !important"
              ></div>
              <div
                class="ph-picture me-3"
                style="width: 50px; height: 50px"
              ></div>
              <div
                class="ph-picture me-3"
                style="width: 50px; height: 50px"
              ></div>
              <div
                class="ph-picture me-3"
                style="width: 50px; height: 50px"
              ></div>
              <div
                class="ph-picture me-3"
                style="width: 50px; height: 50px"
              ></div>
              <div
                class="ph-picture me-3"
                style="width: 50px; height: 50px"
              ></div>
            </div>
          </div>
        </div>
        <!-- End of loading desktop -->

        <!-- Mobile loading -->
        <div class="d-sm-block d-md-none">
          <div class="ph-col-12">
            <div class="ph-row">
              <div
                class="ph-picture ms-5 me-2"
                style="width: 50px; height: 50px; margin-left: 15px"
              ></div>
              <div
                class="ph-picture me-2"
                style="width: 50px; height: 50px"
              ></div>
              <div
                class="ph-picture me-2"
                style="width: 50px; height: 50px"
              ></div>
              <div
                class="ph-picture me-2"
                style="width: 50px; height: 50px"
              ></div>

              <div class="ph-col-4 empty"></div>
              <div
                class="ph-picture me-2"
                style="width: 50px; height: 50px"
              ></div>
              <div
                class="ph-picture me-2"
                style="width: 50px; height: 50px"
              ></div>
            </div>
          </div>
        </div>
        <!-- End of mobile loading -->
      </div>
      <!-- End of ph-item -->
    </div>
    <!-- End of global loading -->
  </div>
</template>
