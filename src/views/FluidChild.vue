<template>
  <div class="fluid-container">
    <div class="fixed-height-header">
      FIXED HEIGHT HEADER
    </div>
    <div class="fluid-content">
      <div class="fluid-child-a">
        <div class="fixed-grand-child">FLUID-CHILD-A:FIXED-GRAND-CHILD</div>
        <div class="fluid-grand-child">
          <!-- FLUID-CHILD-A:FLUID-GRAND-CHILD -->
          <line-chart />
        </div>
      </div>
      <div class="fluid-child-b">FLUID-CHILD-B</div>
    </div>
  </div>
</template>

<script>
import LineChart from '@/components/LineChart.vue'
export default {
  name: 'FluidChild',
  components: { LineChart }
}
</script>
    LineChart

<style lang="scss" scoped>
.fluid-container{
  width: 100vw;
  height: 100vh;
  // outline: 1px saddlebrown;
  .fixed-height-header{
    height: 60px;
    width: 100%;
    line-height: 60px;
    text-align: center;
    font-size: 21px;
    font-weight: 500;
    background: bisque;
  }
  .fluid-content{
    width: 100%;
    height: calc(100% - 60px);
    background: green;
    // padding: 1rem;
    // display: flex;
    // flex-flow: row nowrap;
    // justify-content: flex-start;
    // align-items: flex-start;

    .fluid-child-a{
      width: 100%;
      height: calc(100% - 200px);
      text-align: center;
      // border: 2px solid darkorange;
      .fixed-grand-child{
        width: 100%;
        height: 200px;
        line-height: 200px;
        text-align: center;
        color: whitesmoke;
        background-color: orangered;
        // margin-bottom: 10px;
      }
      .fluid-grand-child{
        width: 100%;
        height: calc(100% - 200px);
        text-align: center;
        background-color: orchid;
      }
    }
    .fluid-child-b{
      width: 100%;
      height: 200px;
      color: white;
      text-align: center;
      line-height: 200px;
      // border: 2px solid salmon;
    }
  }
}
</style>