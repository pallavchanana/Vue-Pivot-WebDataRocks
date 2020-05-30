<template>
  <div id="app">
    <WebDataRocks report=report toolbar></WebDataRocks>
  </div>
</template>

<script>
import WebDataRocks from './components/WebDataRocks.vue'

export default {
  name: 'app',
  components: {
    WebDataRocks
  },
    data() {
        return {
            report: null
        }
    },
    mounted() {
        this.report = {
            
           
                dataSource: {
            filename: 'https://cdn.webdatarocks.com/data/data.csv'
        },
                "slice": {
        "rows": [
            {
                "uniqueName": "Country"
            },
            {
                "uniqueName": "Category"
            }
        ],
        "columns": [
            {
                "uniqueName": "Business Type"
            },
            {
                "uniqueName": "Measures"
            }
        ],
        "measures": [
            {
                "uniqueName": "Price",
                "aggregation": "sum"
            }
        ]
    },
    "conditions": [
        {
            "formula": "#value > 2000000",
            "measure": "Price",
            "format": {
                "backgroundColor": "#0598df",
                "color": "#FFFFFF",
                "fontFamily": "Arial",
                "fontSize": "12px"
            }
        }
    ]
            }
    }

}
</script>

<style>
</style>


