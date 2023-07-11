<template>
   <div>
     <h2>About</h2>
     <p>JAI SHREE RAM ! </p>
      <p>api response:</p>
     <div>{{ data }}</div>
   </div>
 </template>
 
 <style scoped>
   h2 {
     margin-bottom: 22px;
     font-size: 38px;
   }
   p {
     margin: 25px 0;
   }
 </style>
 
 <script setup>
    const { data } = await useFetch('/api/currency/INR')
 </script>
