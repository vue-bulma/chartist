<template>
  <div class="ct-chart"></div>
</template>

<script>
import Chartist from 'chartist'

const types = ['Line', 'Bar', 'Pie']

export default {

  props: {
    type: {
      type: String,
      default: 'Line',
      required: true,
      validator: (value) => types.includes(value)
    },
    data: {
      type: Object,
      required: true,
      default: () => ({})
    },
    options: {
      type: Object,
      default: () => ({})
    },
    responsiveOptions: {
      type: Array,
      default: () => ([])
    }
  },

  data () {
    return {
      chart: null
    }
  },

  mounted () {
    this.chart = new Chartist[this.type](
      this.$el,
      this.data,
      this.options,
      this.responsiveOptions
    )
  },

  watch: {
    data (val) {
      this.$nextTick(() => this.chart.update())
    }
  }
}
</script>

<style lang="scss">
@import '~chartist/dist/scss/chartist';

.ct-chart {
  max-width: 100%;
}
</style>
