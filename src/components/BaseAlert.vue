<template>
    <div :class="basedClass">
        <slot />
        <button @click="onClick"> X </button>
    </div>
</template>

<script>
export default {
    props: {
        variant: {
            type: String,
            default: ''
        },
       
    },
    computed: {
        basedClass() {
            return [
                'alert',
                this.variant ? `alert-${this.variant}` : ''
            ];
        }
    },
    methods: {
        onClick() {
            this.$emit('close');
            console.log('Clicou!');
        }
    }
}
</script>

<style scoped>
.alert {
    display: flex;
    justify-content: space-between;
    padding: 5px;
    border-radius: 6px;
    color: gray;
    background: #ddd;
}

.alert-sucess {
    background: #42b983;
    color: white;
}

.alert-danger {
    background: red;
    color: white;
}
</style>