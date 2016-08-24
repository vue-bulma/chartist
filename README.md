# Chartist

Chartist component is based on [Chartist](http://gionkunz.github.io/chartist-js/) for Vue Bulma.

## Installation

```
$ npm install vue-bulma-chartist
```

## Examples

```vue
<template>
  <chart :type="'line'" :data="data" :options="options"></chart>
</template>

<script>
import Chart from 'vue-bulma-chartist'

export default {
  components: {
    Chart
  },

  data () {
    return {
      data: {
        labels: ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday'],
        series: [
          [12, 9, 7, 8, 5],
          [2, 1, 3.5, 7, 3],
          [1, 3, 4, 5, 6]
        ]
      },
      options: {
        fullWidth: true,
        chartPadding: {
          right: 40
        }
      }
    }
  }
}
</script>
```

## Badges

![](https://img.shields.io/badge/license-MIT-blue.svg)
![](https://img.shields.io/badge/status-stable-green.svg)

---

> [fundon.me](https://fundon.me) &nbsp;&middot;&nbsp;
> GitHub [@fundon](https://github.com/fundon) &nbsp;&middot;&nbsp;
> Twitter [@_fundon](https://twitter.com/_fundon)
