<template>
  <div class="heading-small">
    <slot />
  </div>
</template>

<script>
export default {
  name: 'HeadingSmall'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  @import "@bit/lmartim.calamity._variables";
  .heading-small {
    text-align: left;
    
    font-size: $font-size-lg;
    line-height: $line-height-distant;

    font-family: $font-family-highlight;
    font-weight: $font-weight-bold;
    color: $neutral-color-5;
  }
</style>
