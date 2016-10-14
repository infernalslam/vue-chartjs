<template>
  <div id="app">
    <p class="title">Chart.jS Vue<p>
      <canvas id="graph" width="400" height="400"></canvas>
  </div>
</template>

<script>
import Chart from 'chart.js'
export default {
  components: {
  },
  mounted: function () {
    var ctx = document.getElementById('graph').getContext('2d')
    var bar = new Chart(ctx, {
      type: 'bar',
      data: {
        labels: ['1', '2', '3'],
        datasets: [
          {
            label: '# of Vote',
            data: [12, 45, 67]
          }]
      }
    })
    console.log(bar)
  },
  data () {
    return {
    }
  }
}
</script>

<style>
html {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

#app {
  color: #2c3e50;
  margin-top: -100px;
  max-width: 600px;
  font-family: Source Sans Pro, Helvetica, sans-serif;
  text-align: center;
}

#app a {
  color: #42b983;
  text-decoration: none;
}

.logo {
  width: 100px;
  height: 100px
}
.title {
  color: #72;
  font-size: 50px;
}
</style>
