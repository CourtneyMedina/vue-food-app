<template>
  <div class="btn-group" role="group" aria-label="Basic example">
  <button type="button" @click="decrease" class="btn btn-secondary">-</button>
  <input type="text" v-model="quantity" class="form-control" placeholder=0 aria-label="Input" 
  aria-describedby="btnGroupAddon">
  <button type="button" @click="increase" class="btn btn-secondary">+</button>
</div>
</template>

<script>
 
import {ref} from "vue"

export default {
    setup(){
        let quantity = ref(0)

        function increase() {
            quantity.value++
            console.log(quantity.value)
        }

        function decrease() {
            if(quantity.value > 0){
                quantity.value--
                console.log(quantity.value)
            }
        }
        
        return {
            quantity,
            increase,
            decrease,
            }
    }
    
}
</script>

<style>

.btn-group {
    width: 50%;
}
.form-control {
    width: 50%;
}
</style>