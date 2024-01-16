<template>
    <input type="text" v-model="name"><br>
    {{ name }} <br>
    <br>
    
    <input type="text" v-model="user.firstName"><br>
    {{ user.firstName }} <br> 
    <input type="text" v-model="user.lastName"><br>
    {{ user.lastName }} <br>
    
    <select name="" id="" v-model="page" v-if="isPage">
        <option value="1">1</option>
        <option value="5">5</option>
        <option value="10">10</option>
    </select>
    <br>
    {{ page }}
    <br>
    <button @click="this.isPage = !this.isPage">toggle Button</button>
</template>
<script>
export default {
    data() {
        return {
            name: 'Welen',
            page: '1',
            user: {
                firstName: '',
                lastName: ''
            },
            isPage: false
        }
    },
    watch: {
        name(newValue) {
            if (newValue.length >= 3) {
                this.saveUser();
            }
        },
        page() {
            this.changePage();
        },
        user: {
            handler() {
                console.log('User alterado!');
            },
            deep: true
        }
    },
    beforeCreate() {
        console.log("Antes de ser criado!");
        console.log(this.name);
    },
    created() {
        console.log("Criado!");
        console.log(this.name);

    },
    beforeMount() {
        console.log("Antes de ser montado!");
        console.log(this.name);
        window.addEventListener('resize', this.resized);

    },
    mounted() {
        console.log("Montado!");
        console.log(this.name);
        console.log(this.$el);

    },
    beforeUpdate() {
        console.log("Antes de atualizar!");
    },
    updated() {
        console.log("Atualizado!");
    },
    beforeUnmount() {
        console.log('Antes de ser desmontado!');
        console.log(this.name);
        window.removeEventListener('resize', this.resized);
    },
    unmounted() {
        console.log("Desmontado!");
    },
    methods: {
        saveUser() {
            // console.log("Ajax!");
        },
        changePage() {
            // console.log("Ajax change page!");
        },
        resized($evt) {
            console.log($evt);
        }
    }
}
</script>