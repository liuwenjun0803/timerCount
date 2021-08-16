<template>
<div id="foot">
    <a href="javascipt:;">
        <img src="../assets/foot-tubiao.png" alt="">
        闹钟
    </a>
    <a href="javascipt:;">
        <img src="../assets/foot-tubiao.png" alt="">
        闹钟
    </a>
    <a href="javascipt:;">
        <img src="../assets/foot-tubiao.png" alt="">
        闹钟
    </a>
    <a href="javascipt:;">
        <img src="../assets/foot-tubiao.png" alt="">
        闹钟
    </a>
</div>

</template>
<script>
export default {
  name: 'Head',
  props: {
    msg: String
  }
}
</script>

<style scoped lang="scss">
  #foot{
    width: 100%;
    height: 100px;
    display: flex;
    width: 100%;
    justify-content: space-around;
    align-items: center;
    background: #111111;
    a{
        display: flex;
        flex-direction: column;
    }
  }
</style>
