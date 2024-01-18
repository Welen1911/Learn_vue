<template>
    <div :class="basedClass">
        {{ test }}
        <slot />
    </div>
</template>

<script>
export default {
    props: {
        variant: {
            type: String,
            default: ''
        },
        test: {
            type: String,
            default: 'Test'
        }
    },
    computed: {
        basedClass() {
            return [
                'alert',
                this.variant ? `alert-${this.variant}` : ''
            ];
        }
    }
}
</script>

<style scoped>
.alert {
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