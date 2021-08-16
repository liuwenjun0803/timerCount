<template>
    <div class="box">
        <button>计次</button>
        <div class="dot">
            <span class="kong"></span>
            <span class="shi"></span>
        </div>
        <button>启动</button>
    </div>
</template>
<script>
export default {
  name: 'MajorClock',
  data: function () {
    return {
    }
  }
}
</script>
<style scoped lang="scss">
.box{
    flex: 1;
    width: 100%;
    display: flex;
    justify-content: space-around;
    align-items: center;
    button{
        display: inline-block;
        width: 100px;
        height: 100px;
        border-radius: 50%;
        font-size: 30px;
    }
    .dot{
        display: inline-block;
        span{
            display: inline-block;
            width: 15px;
            height: 15px;
            border-radius: 50%;
            border: 1px solid #fff;
            margin-left: 20px;
        }
        .kong{
            background: transparent;
        }
        .shi{
            background: #eee;
        }
    }

}
</style>
