<template>
    <span :class="along+' surface_0'">
      <div id=label>{{label}}</div>
      <input class="surface_-1" :placeholder="placeholder" :type="type"/>
    </span>
</template>
<script>
export default {
    props:["label","placeholder","along"]
}
</script>
<style scoped>
input
{
    height:3em;
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
.horizontal.surface_0
{
    display: grid;
    grid-template-columns: max-content auto;;
    grid-template-rows: auto;
}
.vertical.surface_0
{
    display: grid;
    grid-template-rows:auto;
    grid-template-rows: auto  max-content;
}
</style>
