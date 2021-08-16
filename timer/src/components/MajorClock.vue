<template>
    <div class="clock">
     <span class="m">{{countM}}</span>
     <span>:</span>
     <span class="s">{{countS}}</span>
     <span>.</span>
     <span class="ms">{{countMs}}</span>
    </div>
</template>

<script>
export default {
  name: 'MajorClock',
  data: function () {
    return {
      m: '00',
      s: '0',
      ms: '00',
      time: null
    }
  },
  computed: {
    countMs () {
      if (this.ms >= 1000) {
        if (Math.floor((this.ms - 1000 * Math.floor(this.ms / 1000)) / 10) < 10) {
          return '0' + Math.floor((this.ms - 1000 * Math.floor(this.ms / 1000)) / 10)
        } else {
          return Math.floor((this.ms - 1000 * Math.floor(this.ms / 1000)) / 10)
        }
      } else {
        if (Math.floor(this.ms / 10) < 10) {
          return '0' + Math.floor(this.ms / 10)
        } else {
          return Math.floor(this.ms / 10)
        }
      }
    },
    countS () {
      if (this.s >= 60) {
        if (Math.floor(this.s - 60 * Math.floor(this.s / 60)) < 10) {
          return '0' + Math.floor(this.s - 60 * Math.floor(this.s / 60))
        } else {
          return this.s - 60 * Math.floor(this.s / 60)
        }
      } else {
        if (this.s < 10) {
          return '0' + this.s
        } else {
          return this.s
        }
      }
    },
    countM () {
      if (this.m >= 60) {
        return this.m - 60 * Math.floor(this.m / 60)
      } else {
        return this.m
      }
    }
  },
  watch: {
    ms (newValue) {
      if (newValue % 1000 === 0) {
        this.s++
      }
    },
    s (newValue) {
      if (newValue % 60 === 0) {
        this.m++
      }
    }
  },
  methods: {
    timeRun () {
      this.time = setInterval(() => {
        this.ms = 10 + Number(this.ms)
      }, 10)
    }
  },
  mounted () {
    // this.timeRun()
  }
}
</script>

<style scoped lang="scss">
  .clock{
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #fff;
    span{
      font-size: 80px;
    }
  }
</style>
