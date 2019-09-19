
<template>
  <div id="myEcharts"></div>
</template>

<script>

export default {
  name: "earth",
  mounted() {
    this.drawEarth();
  },
  methods: {
    drawEarth() {
      let myEath = this.$echarts.init(document.getElementById("myEcharts"));
      myEath.setOption = {
        backgroundColor: "#000",
        globe: {
          baseTexture: "/assets/world.topo.bathy.jpg",
          heightTexture: "/assets/world.topo.bathy.jpg",
          displacementScale: 0.04,
          shading: "realistic",
          environment: "/assets/world.topo.bathy.jpg",
          realisticMaterial: {
            roughness: 0.9
          },
          postEffect: {
            enable: true
          },
          light: {
            main: {
              intensity: 5,
              shadow: true
            },
            ambientCubemap: {
              texture: ROOT_PATH + "data-gl/asset/pisa.hdr",
              diffuseIntensity: 0.2
            }
          }
        }
      };
    }
  }
};
</script>

<style lang="scss" scoped>
.myEcharts {
  width: 500px;
  height: 500px;
}
</style>