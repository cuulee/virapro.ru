<template>
  <div>
    <cart-products/>
    <orders-history></orders-history>
  </div>
</template>

<script>
  import CartProducts from "../../components/cart/CartProducts";
  import OrdersHistory from "../../components/cart/OrdersHistory";
  export default {
    name: "index",
    components: {OrdersHistory, CartProducts},
    async fetch({store, params}) {
      await store.dispatch('USER_EVENT', 'Страница: Корзина')
    }
  }
</script>

<style scoped>

</style>
