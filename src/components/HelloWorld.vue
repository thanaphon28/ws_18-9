<template>


<div id = "hello">
  
  <h1>  {{myName}} </h1>
  <p> Tel : {{tel}} </p>
  <p> {{no}} </p>


  <button>click me</button>
  <div class="btn-group" role="group" aria-label="Basic example">
  <button type="button" class="btn btn-primary">Left</button>
  <button type="button" class="btn btn-primary">Middle</button>
  <button type="button" class="btn btn-primary">Right</button>
  <i class="far fa-address-card"></i>
</div>
</div>
  
</template>

<script>
export default {
  name : "hello", 
data() {
  return {
    myName : "Thanaphon Jedsadalak",
    tel: "0657401212",
    no : "6130203209"
  };
}
}
</script>

<style>
.test{
  font-size:  9em;
}
#hello{
  background-color: red;
  color: white;
}


</style>