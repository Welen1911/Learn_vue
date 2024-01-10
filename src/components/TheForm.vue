<template>
    <input type="text" :class="{ 'name': size }" v-model="name" @keyup="() => size = nameSize(name)">
    <p>{{ name }}</p>

    <br>
    <select v-model="sports">
        <option value="">Escolha</option>
        <option value="soccer">Futebol</option>
        <option value="Basket">Basquete</option>
        <option value="Motocross">Motocross</option>
        <option value="Triatlo">Triatlo</option>
    </select>
    <p>{{ sports }}</p>
    <br>
    <label for="">Do you want subscribe to our NewsLetter ?</label>
    <input type="radio" v-model="newsLetter" value="yes">Yes
    <input type="radio" v-model="newsLetter" value="no">No
    <p>{{ newsLetter }}</p>
    <br>
    <label for="">What do you wanna to be?</label><br>
    <input type="checkbox" v-model="checkbox" value="Front-End"> Front-End <br>
    <input type="checkbox" v-model="checkbox" value="Back-End"> Back-End <br>
    <input type="checkbox" v-model="checkbox" value="Full-Stack"> Full-Stack <br>
    <input type="checkbox" v-model="checkbox" value="Mobile"> Mobile <br>
    <p>{{ checkbox }}</p>
    <br>
    <label for="">DO YOU WANT TO RECEIVE LOTS AND LOTS OF SPAM ? </label>
    <input type="checkbox" v-model="privacy"> I accept
    <p>{{ privacy }}</p>
    <button @click.once="onClick(name)">Submit</button>
    
    <div @mouseover="onMouseOver" @mouseout="onMouseOut">
        Mouse over
    </div>
    <br>
    <form action="#" @submit.prevent="onSubmit">
        <input type="text" @keyup.enter="$evt => console.log($evt)">
        <button type="submit">Submit</button>
    </form>
</template>

<script>
export default {
    data() {
        return {
            name: 'Welen',
            sports: 'Motocross',
            newsLetter: '',
            checkbox: ['Mobile'],
            privacy: false,
            size: false,
        }
    },
    methods: {
        onClick(msg) {
            return console.log(msg);
        },
        nameSize(name) {
            if (name.length < 2) {
                return true;
            }
            return false;
        },
        onMouseOver() {
            console.log('Over!');
        },
        onMouseOut() {
            console.log('Out!');
        },
        onSubmit() {
            console.log('Submit!');
        }
    }
}
</script>
<style>
.name {
    border-color: red;
}
</style>