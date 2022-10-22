<script lang="ts" setup>
import { ref } from 'vue'

const arrayTask = ref([]);


const createTask = ()=>{
    // console.log(task.value);
    arrayTask.value.push(task.value);

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
  <div class="container text-center">
  <div class="row">
    <div class="col">
        <div class="card text-center" style="width: 18rem; margin-bottom: 1%;" v-for ="(ta, index) in arrayTask" key="index">
                 <div class="card-body" >
                 <h5 class="card-title">{{index}}</h5>
                  <p class="card-text">  {{ta}} </p>
    
                  </div>
  
  
        </div>
        
  
  </div>
</div>
   
    </div>
    




</template>