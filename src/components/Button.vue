<template>
  <button v-bind:type="type" v-bind:class="className">{{text}}</button>
</template>

<script>
export default {
    props: {
        text: String,
        type: String,
        className: String,
    },
    inheritAttrs: false,
}
</script>

<style>

.button{
    height: 2rem;
    font-size: 1.2rem;
    border-radius: 5px;
    margin: 6px;
    padding: 4px 20px;
}

.blue{
    background-color: rgb(0, 108, 209);
    color: whitesmoke;
}

</style>