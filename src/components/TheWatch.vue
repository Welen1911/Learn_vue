<template>
    <input type="text" v-model="name"><br>
    {{ name }} <br>
    <br>
    
    <input type="text" v-model="user.firstName"><br>
    {{ user.firstName }} <br> 
    <input type="text" v-model="user.lastName"><br>
    {{ user.lastName }} <br>
    
    <select name="" id="" v-model="page">
        <option value="1">1</option>
        <option value="5">5</option>
        <option value="10">10</option>
    </select>
    <br>
    {{ page }}
</template>
<script>
export default {
    data() {
        return {
            name: '',
            page: '1',
            user: {
                firstName: '',
                lastName: ''
            }
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
    methods: {
        saveUser() {
            console.log("Ajax!");
        },
        changePage() {
            console.log("Ajax change page!");
        }
    }
}
</script>