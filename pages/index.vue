<template>
  <div>
    Hello World. 
    <br>
    {{mountain.title}} is {{mountain.height}}
    <br>
    and {{mountain2.title}} is {{mountain2.height}}
    <NuxtLink to="/test">Go to test page</NuxtLink>
  </div>
</template>

<script setup>
const { data: mountain } = await useFetch('https://api.nuxtjs.dev/mountains/aconcagua', { initialCache: false })
const { data: mountain2 } = await useFetch('https://api.nuxtjs.dev/mountains/mount-everest', { initialCache: false })

</script>