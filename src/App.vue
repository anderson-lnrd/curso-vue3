<template>
  <div v-show="showName">
    First name: {{ firstName }} <br>
    Last Name: {{ lastName }}
  </div>
  <div>
    <div
       v-for="(obj, index) in todos" 
       v-bind:key="obj.id" 
       class="todos-item"
    >

      <img 
        v-bind:src="obj.imgSrc"
        v-bind:alt="obj.imgAlt"
      >
      {{ index }} - {{ obj.title }}
    </div>

  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data(){
    return{
      showHeader: true,
      firstName: "Jon",
      lastName: "Snow",
      showName: false,
      accessLevel: "admin",
      todos: [
        {
          "userId": 1,
          "id": 1,
          "title": "delectus aut autem",
          "completed": false,
          "imgSrc:": 'http://placekitten.com/150',
          "imgAlt": "kitten Photo"
        },
        {
          "userId": 1,
          "id": 2,
          "title": "quis ut nam facilis et officia qui",
          "completed": false,
          "imgSrc:": 'http://placekitten.com/150',
          "imgAlt": "kitten Photo"
        },
        {
          "userId": 1,
          "id": 3,
          "title": "fugiat veniam minus",
          "completed": false,
          "imgSrc:": 'http://placekitten.com/150',
          "imgAlt": "kitten Photo"
        },
        {
          "userId": 1,
          "id": 4,
          "title": "et porro tempora",
          "completed": true,
          "imgSrc:": 'http://placekitten.com/150',
          "imgAlt": "kitten Photo"
        },
        {
          "userId": 1,
          "id": 5,
          "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
          "completed": false,
          "imgSrc:": 'http://placekitten.com/150',
          "imgAlt": "kitten Photo"
        }
      ]

    }
  }
}
</script>

<style>
.todos-item{
  background-color: #000;
  margin: 0 0 5px 0;
  padding: 3px 6px;
  color: #fff;

}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
  margin:60px
}
</style>
