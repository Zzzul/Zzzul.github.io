<template>
  <div class="col-md-12 mb-5 mt-5">
    <nav
      class="custom-breadcrumb"
      style="--bs-breadcrumb-divider: '>';"
      aria-label="breadcrumb"
    >
      <ol class="ol-breadcrumb px-3 pt-3 pb-0">
        <slot />
      </ol>
    </nav>
  </div>
</template>
