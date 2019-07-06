<script>
import {Bar} from 'vue-chartjs'

export default {
  extends: Bar,
  mounted () {
    this.renderChart({
      labels: ['Documentos Legais', 'Monitoramento', 'Adequação'],
      datasets: [
        {
          label: 'Vencidas',
          backgroundColor: '#f44336',
          data: [3, 5, 12]
        },
        {
          label: 'Programadas',
          backgroundColor: '#63a4ff',
          data: [1, 4, 8]
        },
        {
          label: 'Atendidas',
          backgroundColor: '#43a047',
          data: [0, 6, 7]
        }
      ],
      scales: {
  yAxes: [
    {
      ticks: {
        min: 0,
        max: this.max,// Your absolute max value
        callback: function (value) {
          return (value / this.max * 100).toFixed(0) + '%'; // convert it to percentage
        },
      },
      scaleLabel: {
        display: true,
        labelString: 'Percentage',
      },
    },
  ],
},
    }, {responsive: true, maintainAspectRatio: false})

  }
}
</script>