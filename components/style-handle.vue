<template>
<SPAn></SPAn>
</template>
<style>
body
{
    margin: 0px
}
@import url('https://fonts.googleapis.com/css?family=Merienda');
*{
    --surface-logo-length:5em;

    --surface_0_background-color:rgba(0,0,0,0);
    --surface_0_padding:10px;
    --surface_0_color:black;
    --surface-0-cariage-length:1em;

    --surface_1_border-radius:16px;
    --surface_1_border:0px;
    --surface_1_box-shadow:0px 0px 9px rgba(61,5,27,0.54);
    --surface_1_padding:20px;
    --surface_1_color:rgba(255,255,255,0.45);
    --surface_1_background-color:rgba(44, 41, 41, 0.5);

    --surface_-1_border-radius:8px;
    --surface_-1_border:0px;
    --surface_-1_color:grey;
    --surface_-1_box-shadow:0px 0px 3px rgba(33, 150, 243, 0.85) inset;
    --surface_-1_padding:1.62em;
    --surface_-1_font-family:'Merienda';
    --surface_-1_font-size:90%;

    --surface_2_background-color: #115555;
    --surface_2_border-radius:8px;
    --surface_2_color:white;
    --surface_2_border:0px;
    --surface_2_padding:12px;
    --surface_2_font-size:102%;
    --surface_2_box-shadow:0px 0px 16px rgba(61,5,27,1.54);
}
*
{
    font-family: 'Aclonica', sans-serif;
    box-sizing: border-box;
    transition: all .2s ease;
}
*::-webkit-scrollbar-track
{
	box-shadow: inset 0 0 6px rgba(0,0,0,0);
	background-color:transparent;
}

*::-webkit-scrollbar
{
	width: 10px;
	background-color: transparent;
}

*::-webkit-scrollbar-thumb
{
	background-color: #000000;
	border: 2px solid #555555;
}

input::placeholder{
    color:var(--surface_-1_color);
    font-family:'Aclonica', sans-serif;
}
.surface_0
{
    background-color:var(--surface_0_background-color);
    color:var(--surface_0_color);
    font-family: 'Aclonica';
    padding:var(--surface_0_padding)
}
.surface_1
{
    
    box-shadow:var(--surface_1_box-shadow);
    border: var(--surface_1_border);
    border-radius: var(--surface_1_border-radius);
    padding: var(--surface_1_padding);
    background: var(--surface_1_color);
}
input,.surface_-1
{
    
    border-radius:var(--surface_-1_border-radius);
    border:var(--surface_-1_border);
    color:var(--surface_0_color);
    text-shadow:0px 0px 0.1px var(--surface_0_color);
    box-shadow:var(--surface_-1_box-shadow);
    padding:var(--surface_-1_padding);
    font-family:var(--surface_-1_font-family);
    font-size:var(--surface_-1_font-size);
}
.surface_2
{
    background-color:var(--surface_2_background-color); 
    color:var(--surface_2_color);
    border:var(--surface_2_border);
    border-radius:var(--surface_2_border-radius);
    padding:var(--surface_2_padding);
    font-size:var( --surface_2_font-size);
    box-shadow:var(--surface_2_box-shadow);
}
button,input
{
    min-width: 7em;
    min-height: 3em;
}
.interactive
{
    cursor: pointer;
}
.interactive:active
{
    box-shadow: none !important;
}
</style>
<script>
export default {
    
}
</script>
