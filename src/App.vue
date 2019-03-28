<template>
  <div id="app" class="mt-5">
    <shop-layout>
      <template slot="products">
        <product-list></product-list>
      </template>
      <template slot="cart">
        <cart/>
      </template>
    </shop-layout>
  </div>
</template>

<script>
import ShopLayout from "@/components/layouts/ShopLayout";
import ProductList from "@/components/products/ProductList";
import Cart from "@/components/cart/Cart";

export default {
  name: "app",
  components: {
    ShopLayout,
    ProductList,
    Cart
  }
};
</script>

