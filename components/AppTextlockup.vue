<template>
  <div class="textlockup">
    <div class="new">
      <slot name="new">FLAVORMAN</slot>
    </div>
    <div class="top">
      <slot name="top"></slot>
    </div>
    <div class="middle">
      <slot name="middle"></slot>
    </div>
    <div class="lower">
      <slot name="lower"></slot>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.textlockup {
  display: grid;
  grid-template-columns: 50px 100px 1fr;
  grid-template-rows: 50px 50px 100px 20px 1fr;
  grid-column-gap: 0px;
  grid-row-gap: 0px;
  margin-top: 2px;
  .new {
    grid-area: 1 / 1 / 5 / 4;
    font-size: 23vmin;
    color: #efefef;
    text-transform: uppercase;
  }
  .top {
    grid-area: 2 / 2 / 3 / 4;
    font-size: 6.5vmin;
    color: #004978;
    font-family: "Effra", -apple-system, BlinkMacSystemFont, "Effra", Roboto,
      "Effra", Arial, sans-serif;
  }
  .middle {
    grid-area: 3 / 3 / 4 / 4;
    font-size: 8.5vmin;
    font-family: "Effra", -apple-system, BlinkMacSystemFont, "Effra", Roboto,
      "Effra", Arial, sans-serif;
  }
  .lower {
    grid-area: 4 / 2 / 5 / 4;
    font-size: 2vmin;
    letter-spacing: 0.2em;
    text-transform: uppercase;
  }
  .img {
    max-width: 950px;
    grid-area: 1 / 3 / 6 / 4;
    img {
      width: 100%;
    }
  }
}

@media screen and (max-width: 650px) {
  .textlockup {
    grid-template-columns: 25px 25px 1fr !important;
    grid-template-rows: 6vmin 5.5vmin 10vmin 20px 1fr !important;
  }
}
</style>