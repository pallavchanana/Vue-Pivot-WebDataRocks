<template>
  <div id="app">
    <!-- <WebDataRocks report="employeesData" toolbar></WebDataRocks> -->
    <WebDataRocks report=report toolbar></WebDataRocks>

  </div>
</template>

<script>
import WebDataRocks from './components/WebDataRocks.vue'
import employeesData from './data/employees.json'
// import sampleData from './data/Sample.json'

export default {
  name: 'app',
  components: {
    WebDataRocks
  },
    data() {
        return {
            report: null,
            employees: employeesData,
        }
    },
    mounted() {  
        // this.report = {
        //     dataSource: {
        //     data: this.employees
        //     }
        // }     
 }
}
</script>

<style>
</style>


