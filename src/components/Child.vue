<template>
<div class="list">
<h1 >{{user?.name}}</h1>
<h1 >{{ user?.category}}</h1>
</div>
<button v-on:click="getAllData(user?.name)">Click me for alert</button>
<h1>{{colors?.name}}</h1>
</template>

<script>
export default {
    name: 'ChildComponent',
    props: {
        user: String,
        getAllData: Function,
        colors: Object,
    },
};
</script>
<style>
.list {
    background-color: lightblue;
    padding: 5px;
    color: blueviolet
}
</style>
