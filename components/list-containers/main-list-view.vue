<template>
    <div class="surface_1 surface_0 main-list-root">
        <div id="header"></div>
        <div id="body">
            <component :is="'thumb-view'"></component>
        </div>
    </div>
</template>
<style scoped>
    .main-list-root
    {

    }
    #header
    {

    }
</style>
<script>
import thumView from "./thumb-viewer"
export default {
    
}
</script>