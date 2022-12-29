<template>
  <div class="container">
    <h1>Shop Watcher</h1>

    <div>
      Black Friday sale
      <strike>Was {{ oldDiscount }}%</strike>
      <strong> Now {{ discount }}% OFF</strong>
    </div>

    <br />
    <a href="#" @click="updateDiscount">Increase Discount!</a>
  </div>
</template>

<script>
export default {
  data() {
    return {
      oldDiscount: 0,
      discount: 5,
    }
  },
  methods: {
    updateDiscount() {
      this.discount = this.discount + 5
    },
  },
  watch: {
    discount(newValue, oldValue) {
      this.oldDiscount = oldValue
    },
  },
}
</script>


<style scoped>

</style>