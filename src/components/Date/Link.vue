<template>

<a :href="link.url">{{link.nameLink}}</a>
  
</template>

<script>
export default {
    name: "Link", 
    props: ['link']

}
</script>

<style>

</style>