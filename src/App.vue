<template>
  <div id="app">
    <img
      @click="externalCount()"
      alt="Vue logo"
      style="width:350px;"
      src="https://sun9-81.userapi.com/impg/zydtTlwig-GTRpzIuKVOrj277365k5oTsykfPQ/hdLgMbCaoFA.jpg?size=960x1280&quality=95&sign=3145f7c7c31deadaac3c81743855f5e9&type=album"
      >
      <p
        style="font-size: 36px"
      >
        Внешний долг Андрея: <b> {{ debtCount }} $</b>
      </p>
  </div>

</template>

<script>

export default {
  name: 'App',
  data() {
    return {
        debtCount: 1000000,
        timer: null,
    }
  },
  components: {
  },
  
  created() {
    this.startTimer();
  },
  destroyed() {
    this.stopTimer()
  },

  methods: {
    startTimer() {
      let random = Math.floor(Math.random() * 10000) + 1;
      this.timer = setInterval(() => {
        this.debtCount += random;
      }, 100)
    },

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
img {
  width: 150px,
}
</style>
