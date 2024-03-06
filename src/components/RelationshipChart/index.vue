<template>
  <div class="container">
    <div ref="chart"></div>

  </div>
</template>

<script>
import {mapGetters} from 'vuex'
import * as echarts from 'echarts'

//https://www.makeapie.cn/echarts_content/xByJm_ypsl.html
export default {
  name: 'RelationshipChart',
  props: {
    dataList: {
      type: Array,
      default: () => {
        return []
      }
    }
  },
  computed:{
  },
  mounted() {
    this.chart = echarts.init(this.$refs.chart)
    this.renderChart()
  },
  data() {
    return {
      chart: null,
      isDialogShow:false,
      entity:{}
    }
  },
  watch:{
  },
  methods: {
    renderChart() {
      const echarts = this.$echarts



      this.chart.setOption(option)
    },

    destroy() {
    }
  }
}
</script>

<style lang="scss" scoped>
.container{
  margin-left: 20%;
  width: 60%;
}
div {
  height: 100%;
  width: 100%;
}
</style>
