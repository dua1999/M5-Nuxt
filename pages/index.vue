<script setup>

const {data} = await useFetch('https://yesno.wtf/api');
const image = data.value.image;
const answer = data.value.answer;
console.log(data);

</script>

<template>
  <div>
    <section class="box-border h-100 w-100 p-4 border-0 items-center float-canter object-contain">
    <h1 class="text-center bg-slate-800 text-white h-15 rounded-md text-2xl">Is today a good day?</h1>
      {{ answer }}
      <img :src="image"/> 
    </section>
    <br/>
    
    <section class="flex flex-col-reverse divide-y divide-y-reverse ">
      <AlertBox class="border-2 border-spacing-2 h-14 w-25 text-xl marging" type="success">Success!</AlertBox>
      <AlertBox class="border-2 border-spacing-2 h-14 w-25 text-xl marging" type="info">Info</AlertBox>
      <AlertBox class="border-2 border-spacing-2 h-14 w-25 text-xl marging" type="warning">Careful!</AlertBox>
      <AlertBox class="border-2 border-spacing-2 h-14 w-25 text-xl marging" type="error">Error!</AlertBox>
    </section>
    <section class="grid grid-cols-2 divide-x">
      <img class="sm:mx-0 sm:shrink-0 " src="img/nuxt.png" alt="Nuxt Logo" />
      <img src="img/vue.png" alt="Vue Logo"/>
    </section>
    </div>
  </template>

  <style scoped>
.conent-center{
  align-content: center;
}
</style>