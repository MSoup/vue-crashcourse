<template>
    <button v-bind:style="{background: color}" class="btn" v-on:click="onClick()">{{text}}</button>
</template>

<script>
    export default {
        name: "Button",
        methods: {
            onClick() {
                this.$emit("toggle-add-task");
            }
        },
        props: {
            text: String,
            color: String,
        }
    }
</script>

