<template>
    <div class="c-container">
        <h4>{{title}}</h4>
        <p>{{harga}}</p>
    </div>
</template>

<script>
export default {
  name: 'Card',
  props: ['title', 'harga']
}
</script>

<style scoped>
    .c-container{
        height: 200px;
        width: 150px;
        border-radius: 5px;
        border: 1px solid grey;
    }
</style>
