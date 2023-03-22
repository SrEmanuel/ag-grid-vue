<template>
   <ag-grid-vue
        style="width: 35rem; height: 25rem;"
        class="ag-theme-alpine"
        :columnDefs="columnDefs"
        :rowData="rowData">
    </ag-grid-vue>
  
</template>

<script>

import { AgGridVue } from "ag-grid-vue3";
import "ag-grid-community/styles/ag-grid.css"; 
import "ag-grid-community/styles/ag-theme-alpine.css"; 

export default {
    components: {
        AgGridVue
    },
    data(){
        return{
            columnDefs: [
                {sortable: true, filter:true, headerName: "Company", field: 'company'},
                {headerName: "Model", field: 'model'},
                {headerName: "Price", field: 'price'},
            ],
            rowData: [
                {company: 'Toyota', model: 'Celica', price: '35000'},
                {company: 'Ford', model: 'Mondeo', price: '32000'},
                {company: 'Porsche', model: 'Boxter', price: '72000'}
            ]
        }
    }
}
</script>

<style>

</style>