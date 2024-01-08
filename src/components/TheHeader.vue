<template>
    <header class="header">
        <div v-if="count >= 2">
            Maior ou igual a dois
        </div>
        <div v-else>
            Menor que dois
        </div>
        <button v-on:click="count++">Acrescentar</button>
    </header>
</template>

<script>
    export default {
        data() {
            return {
            count: 0
            }
        }
    }
</script>

<style>
    .header {
        background: #000;
        color: white;
    }
</style>