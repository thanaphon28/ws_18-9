<template>
<div id = "faculty">
    <h1> คณะ : {{myfaculty}} </h1>
    <h2> สาขา : {{branch}} </h2>

</div>
  
</template>

<script>




export default {
    name : "faculty",
data() {
    return{
        myfaculty : "faculty of science sriracha",
        branch : "IT , Comscience ",

    };
}

}
</script>

<style>
#faculty{
    background-color: orange;
    color: whitesmoke;
}

</style>