<template>
  <div class="box">
    <monthly-sales-chart
      :labels="labels"
      :selectedYears="selectedYears"
      :datasets="datasets"
    ></monthly-sales-chart>
  </div>
</template>

<script>
import MonthlySalesChart from "./components/MonthlySalesChart";

export default {
  name: "app",
  components: {
    MonthlySalesChart,
  },

  data() {
    return {
      labels: ["Jan", "Feb", "Mar", "Apr", "May"],
      selectedYears: [2017, 2018],
      datasets: {
        2018: {
          label: "2018",
          borderColor: "rgba(50, 115, 220, 0.5)",
          backgroundColor: "rgba(50, 115, 220, 0.1)",
          data: [300, 700, 450, 750, 450],
        },
        2017: {
          label: "2017",
          borderColor: "rgba(255, 56, 96, 0.5)",
          backgroundColor: "rgba(255, 56, 96, 0.1)",
          data: [600, 550, 750, 250, 700],
        },
      },
    };
  },
};
</script>
