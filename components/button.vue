<template>
    <button><slot></slot></button>
</template>
<style scoped>
    button
    {
    height:2.7em;
    min-width: 5em;
    width: 7vw;
    /*background-color: #115555;*/
    background-color: var(--surface-0-color,red);
    color: white;
    font-weight: bold;
    border-radius: 4px;
    box-shadow: 0px 0px 5px black;
     border: 0px;
    font-size: 1.2em
  }
</style>
<script>
export default {
    props:["text"],
}
</script>