<template>
  <div class="home">
    <h1> {{active? fistName +" "+ lastName : "nama belum ada"}}</h1>
    <div v-if="active">
      <h2>ini active</h2>
    </div>
    <div v-else>
      <h2>ini tidak active</h2>
    </div>
    <div>{{fistName}}</div>
    <div :id="dataId">test</div>
    <a :href="active ? url:'http://facebook.com'">google</a>
    <br>
    <ul>
      <li v-for="(food, index) in foods" :key="index">{{food.name}} || {{food.price}} || index : {{index}} </li>
    </ul>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  data () {
    return {
      fistName: 'muhammad',
      lastName: 'Risano',
      page: '<h1>hello</h1>',
      active: true,
      dataId: 'coba',
      url: 'http://google.com',
      foods: [
        {
          id: 1, name: 'nasi goreng', price: 4000
        },
        {
          id: 2, name: 'nasi kungi', price: 5000
        },
        {
          id: 3, name: 'kopi', price: 4000
        },
        {
          id: 4, name: 'teh', price: 8000
        }
      ]
    }
  }
}
</script>
<style scoped>
</style>
