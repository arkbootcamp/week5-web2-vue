<template>
  <div>
    <h3 class="title" :class="[warna? warna:'']">nama saya {{fullname}}</h3>
    <h1>count : {{count}}</h1>
    <h5>email: {{email}}</h5>
    <h5>jenis kelamin: {{jk}}</h5>
    <input type="text" v-model="email" >
    <select v-model="warna">
      <option value="kuning">kuning</option>
      <option value="hijau">hijau</option>
      <option value="abu">abu-abu</option>
    </select>
    <button @click="addCount">Tambah 1</button>
    <button @click="minCount(5)">kurang 5</button>
    <button @click="tittleActive">ubah warna</button>
  </div>
</template>

<script>
export default {
  name: 'About',
  data () {
    return {
      count: 0,
      firstName: 'muhd',
      lastName: 'Risano',
      email: '',
      jk: '',
      isActive: false,
      warna: 'kuning'
    }
  },
  methods: {
    addCount () {
      this.count = this.count + 1
    },
    minCount (val) {
      this.count = this.count - val
    },
    changeData (e) {
      this.email = e.target.value
    },
    tittleActive () {
      this.isActive = !this.isActive
    }
  },
  computed: {
    fullname: function () {
      // if (this.firstName.length < 5) {
      //   return 'firstname kurang dari 5'
      // }
      return (this.firstName.length < 5) ? 'kurang dari 5' : ''
    }
  }
}
</script>

<style scoped>
  .title{
    color: blue;
    text-align: center;
  }
  .active {
    color: red;
  }
  .kuning {
    color: yellow;
  }
  .hijau {
    color: green;
  }
  .abu {
    color: gray;
  }
</style>
