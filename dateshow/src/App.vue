<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>
export default {
  name: "App",

  data(){
    return {
     
    }
  },
  methods:{

  },
  mounted() {
    const resize = () => {
      const clientWidth =
        document.documentElement.clientWidth || document.body.clientWidth;
      const clientHeight =
        document.documentElement.clientHeight || document.body.clientHeight;
      const scale1 = clientWidth / 1920;
      const scale2 = clientHeight / 1080;
      const value = Math.min(scale1, scale2);
      document.querySelector("#app").style.transform = `scale(${value})`;
    };
    window.addEventListener("resize", resize);
    resize();
  }
}
</script>
<style lang="scss">
body {
  background: rgba(0, 22, 34, 1);
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  height: 1080px;
  width: 1920px;
  color: #fff;
  transform-origin: center center;

}
</style>