<template>
    <span :class="along">
      <div id=label>{{label}}</div>
      <input class="surface_-1" :placeholder="placeholder" :type="type"/>
    </span>
</template>
<script>
export default {
    props:["label","placeholder","along","type"]
}
</script>
<style scoped>
input
{
    min-height:3em;
    outline: 0px;
}
#label
{
    justify-self: left;
    align-self: center;
}
.vertical #label
{
    padding-bottom:var(--surface-0-cariage-length);
}
.horizontal
{
    display: grid;
    grid-template-columns: max-content auto;;
    grid-template-rows: auto;
}
.vertical
{
    display: grid;
    grid-template-columns:auto;
    grid-template-rows: auto  max-content;
}
</style>
