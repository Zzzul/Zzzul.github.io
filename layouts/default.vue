<template>
  <div>
    <Nuxt />
  </div>
</template>

<style>
/* global */
body {
  background-color: #212529;
}

html,
body,
pre,
code,
kbd,
samp {
  font-family: "Press Start 2P", cursive;
}

a.nuxt-link-active {
  border-bottom: none;
}

a.nuxt-link-exact-active {
  border-bottom: 2px solid white;
}

.my-link:hover {
  border-bottom: 2px solid white;
  text-decoration: none;
  -webkit-transform: translateY(3px);
  transform: translateY(3px);
}

a {
  -webkit-transition-duration: 0.3s;
  transition-duration: 0.3s;
  -webkit-transition-property: transform;
  transition-property: transform;
  -webkit-transition-timing-function: ease-out;
  transition-timing-function: ease-out;
}

.my-card,
.my-card-no-hover {
  -webkit-transition-duration: 0.3s;
  transition-duration: 0.3s;
  -webkit-transition-property: transform;
  transition-property: transform;
  -webkit-transition-timing-function: ease-out;
  transition-timing-function: ease-out;
}

.my-card:hover,
.my-card:focus,
.my-card:active {
  -webkit-transform: translateY(5px);
  transform: translateY(5px);
}

h1 {
  font-size: 23px;
}

h2 {
  font-size: 21px;
}

h3 {
  font-size: 19px;
}

h4 {
  font-size: 17px;
}

h5 {
  font-size: 15px;
}

h6 {
  font-size: 13px;
}

p,
.custom-href {
  font-size: 10px;
}

.header-text {
  font-size: 12px;
}

code,
table {
  font-size: 10px !important;
}

h1,
h2,
h3,
h4,
h5,
h6,
p {
  margin-bottom: 15px;
}

/* code {
  font-family: "Courier New", Courier, monospace;
  font-size: 15px;
} */

/* Mobile */
.text-link-bottom {
  font-size: 8px;
}

.title-bottom {
  font-size: 10px;
}

.name-bottom {
  font-size: 15px;
}
</style>
