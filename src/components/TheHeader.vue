<template>
    <div>
        <h1 :class="classes2" v-if="$slots.title">
            <slot name="title" />         
        </h1>
            <slot name="description" />         
            <slot />         
        
        <h1 :class="{ 'para': true, 'title': false, 'titleHome': isHome }">
            VueJs
        </h1>
        <p :class="paragraph">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas pulvinar, est at placerat viverra, nunc mi
            elementum enim, ac rhoncus quam felis vel ex. Suspendisse maximus orci justo, in lobortis diam lacinia eu. Donec
            scelerisque, diam a dignissim convallis, elit tellus volutpat nulla, a ornare augue orci quis nunc. Donec luctus
            diam metus, ac varius purus viverra eget. In et orci dapibus ligula vehicula feugiat sed at ipsum. Quisque
            facilisis accumsan libero sit amet condimentum. Cras neque est, consequat rutrum venenatis eu, bibendum sed mi.
            Praesent eget mattis urna. Nullam at felis at lectus pulvinar viverra. Nunc urna lacus, varius sed sagittis
            eget, accumsan quis metus. Ut sed vestibulum est, sit amet lacinia libero. In tincidunt quam sed erat aliquet
            facilisis. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis aliquet ornare consequat.
        </p>
        <p :style="lorem">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas pulvinar, est at placerat viverra, nunc mi
            elementum enim, ac rhoncus quam felis vel ex. Suspendisse maximus orci justo, in lobortis diam lacinia eu. Donec
            scelerisque, diam a dignissim convallis, elit tellus volutpat nulla, a ornare augue orci quis nunc. Donec luctus
            diam metus, ac varius purus viverra eget. In et orci dapibus ligula vehicula feugiat sed at ipsum. Quisque
            facilisis accumsan libero sit amet condimentum. Cras neque est, consequat rutrum venenatis eu, bibendum sed mi.
            Praesent eget mattis urna. Nullam at felis at lectus pulvinar viverra. Nunc urna lacus, varius sed sagittis
            eget, accumsan quis metus. Ut sed vestibulum est, sit amet lacinia libero. In tincidunt quam sed erat aliquet
            facilisis. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis aliquet ornare consequat.
        </p>
    </div>
    <div>
        <ul v-for="obj in todos" :key="obj.id" class="todos-item">
            <img v-if="obj.img" :src="obj.img">
            <li>{{ obj.id }} - {{ obj.title }} </li>
        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {

            classes: 'title',
            classes2: 'para',
            isHome: true,
            paragraph: ['text', {
                'para': false
            }],
            lorem: { 'color': 'red', backgroundColor: 'black' },
            todos: [
                {
                    "userId": 1,
                    "id": 1,
                    "title": "delectus aut autem",
                    "completed": false,
                    "img": "https://fakeimg.pl/150x150",
                },
                {
                    "userId": 1,
                    "id": 2,
                    "title": "quis ut nam facilis et officia qui",
                    "completed": false,
                    "img": "https://fakeimg.pl/150x150",
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
    }
}
</script>

<style>
.text {
    color: blueviolet;
}

.h1 {
    font-size: 100px;
}

.titleHome {
    color: aqua;
}

.para {
    font-size: 50px;
}

.title {
    color: blue;
}

.todos-item {
    background: #000;
    margin: 0 0 5px 0;
    padding: 3px 6px;
    color: #fff;

}

.header {
    background: #000;
    color: white;
}
</style>