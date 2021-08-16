<template>
    <div class="box">
      <ul>
        <li v-for='(item,index) in list'
        :key='index'
        >
        {{'计次'+Number(index)}}
        </li>
      </ul>
    </div>
</template>
<script>
export default {
  name: 'splitTimes',
  data: function () {
    return {
      list: [1, 1, 1, 1, 1]
    }
  }
}
</script>
<style scoped lang="scss">
  .box{
    flex: 1;
    width: 100%;
    color: #fff;
    li{
      height: 50px;
      border-bottom: 1px solid rgb(56, 56, 56);
    }
  }
</style>
