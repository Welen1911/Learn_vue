<template>
    {{ fullName }}
    <button @click="onClick">Clique!</button>
    <br><br>
    <h2>Tarefas pendentes:</h2>
    <div v-for="todo in uncompletedTodos" :key="todo.id">
        <p>{{ todo.title }} <span>{{ todo.completed }}</span></p>
    </div>
    <h2>Tarefas Completadas:</h2>
    <div v-for="todo in completedTodos" :key="todo.id">
        <p>{{ todo.title }} <span>{{ todo.completed }}</span></p>
    </div>
    <h2>Todas as tarefas:</h2>
    <div v-for="todo in todos" :key="todo.id">
        <p><input type="checkbox" v-model="todo.completed"> {{ todo.title }}</p>
    </div>
</template>
<script>
export default {
    data() {
        return {
            user: {
                firstName: 'Jon',
                lastName: 'Snow'
            },
            todos: [
                {
                    "userId": 1,
                    "id": 1,
                    "title": "delectus aut autem",
                    "completed": true
                },
                {
                    "userId": 1,
                    "id": 2,
                    "title": "quis ut nam facilis et officia qui",
                    "completed": false
                },
                {
                    "userId": 1,
                    "id": 3,
                    "title": "fugiat veniam minus",
                    "completed": false
                },
                {
                    "userId": 1,
                    "id": 4,
                    "title": "et porro tempora",
                    "completed": true
                },
                {
                    "userId": 1,
                    "id": 5,
                    "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
                    "completed": false
                }
            ]
        }
    },
    computed: {
        fullName() {
            return `${this.user.firstName} ${this.user.lastName}`;
        },
        uncompletedTodos() {
            return this.todos.filter(todo => !todo.completed);
        },
        completedTodos() {
            return this.todos.filter(todo => todo.completed);
        }
    },
    methods: {
        onClick() {
            console.log(this);
        }
    }
}
</script>