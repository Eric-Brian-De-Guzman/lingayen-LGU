<template>
  <Bar
    id="my-chart-id"
    :options="chartOptions"
    :data="chartData"
    style="padding: 3%; margin: 2%; height: 450px; width: 100%"
  />
</template>

<script lang="ts">
import { Bar } from "vue-chartjs";
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  BarElement,
  CategoryScale,
  LinearScale
} from "chart.js";

ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale);
export default {
  name: "BarChart",
  components: { Bar },
  data() {
    return {
      chartData: {
        labels: ["January", "February", "March"],
        },
    };
  },
  mounted() {
    axios.get("/stats/users").then((res) => {
      this.stats = [res.data.data.present, res.data.data.late, res.data.data.absent];
    });
  },
  computed: {
    chartData() {
      return {
        labels: ["On Time", "Late", "Absent"],
        datasets: [
          {
            hoverBackgroundColor:["#171717"],
            backgroundColor: ["#808080"],
            data: this.stats
          }
        ]
      };
    },
    chartOptions() {
      return {
        responsive: true,
        maintainAspectRatio: false
      };
    }
  }
};

</script>
