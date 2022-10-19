<script setup>
import { ref, computed } from 'vue'

const arrayTask = ref([]);


const createTask = ()=>{
    // console.log(task.value);
    arrayTask.value.push(task.value)

}








</script>

<template>
  <form>
    <div class="form-group col-md-6">
                        <label>Tarea : </label>
                        <input type="text" class="form-control" v-model="task" name="task" id="task"  placeholder="Agregar tarea" />
     </div>
     <button type="button" @click='createTask()'>Create</button>
  </form>


  <ul>
    <li v-for ="(ta, index) in arrayTask" key="index">
      {{ta}}
      </li>
    </ul>
  




</template>