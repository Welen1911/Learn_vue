<template>
    <input type="text" v-model="name">
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
            }
        }
    }
</script>