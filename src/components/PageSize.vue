<template>
      <select class="form-select" @change="changeHandler" v-model="rows">
        <!-- <option value=0 selected>全部</option>
        <option value=3>每頁 3 筆資料</option> -->
        <option value=5 selected>每頁 5 筆資料</option>
        <option value=10>每頁 10 筆資料</option>
</select>
  
</template>
    
<script setup>
import {ref} from 'vue'
const rows = ref(5)
const emit = defineEmits(["PageSizeChange"])

    const changeHandler = ()=>{
        emit("PageSizeChange",rows.value)
    }
</script>
    
<style>
    
</style>