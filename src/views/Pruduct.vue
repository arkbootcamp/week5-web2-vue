<template>
    <div>
    <Navbar />
    <h2>hamalaman product</h2>
    <div v-for="product in products" :key="product.id">
        <Card :title="product.name" :harga="product.price"/>
    </div>
    <!-- <Card title="kopi" harga="2000"/>
    <Card title="susu" harga="3000"/> -->
    </div>
</template>

<script>
import Card from '../components/_base/Card'
import Navbar from '../components/_base/Nabar'

export default {
  name: 'Product',
  components: {
    Card,
    Navbar
  },
  data () {
    return {
      products: [
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
