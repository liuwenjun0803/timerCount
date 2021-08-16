<template>
  <div id="head">头</div>
</template>

<script>
export default {
  name: 'Head',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  #head{
    width: 100%;
    font-weight: 400;
  }
</style>
