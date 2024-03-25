<template>
  <h1>{{title}}</h1>
</template>

<script>
export default {
props:['title']
}
</script>

<style lang="scss" scoped>

header{
  padding: 24px 32px;
  display: flex;
  justify-content: center;
}
h1{
  font-size: 32px;
  color: var(--tertiary);
  font-weight: 700;
  text-align: center;
  text-transform: uppercase;
  padding-bottom: 8px;
  border-bottom: 5px solid rgb(221, 137, 137) ;
}




</style>