<template>
    <div class="searchbox-container surface_2">
        <div class="fields-container">
        <div id="label-input-container">
        <labeled-input class=".input-and-label search-input" placeholder="Name" label="Enter Name " along="vertical" ></labeled-input>
        </div>
        <div class='select-container'>
            <select class="js-example-basic-single" name="state">
                <option value="AL">Alabama</option>
                    ...
                <option value="WY">Wyoming</option>
            </select>
   
        </div>   
    </div>    
       
    </div>   
</template>
<script src="https://cdnjs.cloudflare.com/ajax/libs/select2/4.0.6-rc.0/js/select2.min.js"></script>
<script
  src="http://code.jquery.com/jquery-3.3.1.min.js"
  integrity="sha256-FgpCb/KJQlLNfOu91ta32o/NMZxltwRo8QtmkMRdAu8="
  crossorigin="anonymous"></script>
<script>
import labeledInput from "./labeled-input";
export default {
  components:{
    labeledInput
  }
}

</script>
<style scoped>
@import url('https://cdnjs.cloudflare.com/ajax/libs/select2/4.0.6-rc.0/css/select2.min.css');
.searchbox-container
{
    width: 50%;
    background:#3d8af7;  
}
.search-input
{
    background: inherit;
}
.fields-container
{
    margin:auto;
    width: 80%;
}
.search_categories{
  font-size: 13px;
  padding: 10px 8px 10px 14px;
  background: #fff;
  border: 1px solid #ccc;
  border-radius: 6px;
  overflow: hidden;
  position: relative;
}

.search_categories .select{
  width: 120%;
  background-position:80% center;
}

.search_categories .select select{
  background: transparent;
  line-height: 1;
  border: 0;
  padding: 0;
  border-radius: 0;
  width: 120%;
  position: relative;
  z-index: 10;
  font-size: 1em;
}
</style>
