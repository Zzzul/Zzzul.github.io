<template>
  <div class="col-md-12">
    <nav
      style="--bs-breadcrumb-divider: '>'; background-color: #ffff"
      aria-label="breadcrumb"
    >
      <ol class="breadcrumb bordered p-3 mb-5" style="font-size: 12px">
        <slot />
      </ol>
    </nav>
  </div>
</template>
