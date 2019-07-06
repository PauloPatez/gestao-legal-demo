<script>
import {Bar} from 'vue-chartjs'

export default {
  extends: Bar,
  mounted () {
    this.renderChart({
      labels: ['Não', 'Sim', 'Em Adequação', 'Conhecimento', 'ND'],
      datasets: [
        {
          label: 'Requisitos',
          data: [1,2,3,4,5,0],
          backgroundColor: ['#f44336', '#43a047', '#63a4ff', '#ae52d4', '#52c7b8']
        }
      ],
      options: {
        legend: {
          display: false
        }
      }
    }, {responsive: true, maintainAspectRatio: false})

  }
}
</script>