<template>
  <b-card
    :title="product.name"
    :img-src="product.picture"
    :img-alt="product.name"
    img-top
    tag="article"
    style="max-width: 30rem;"
    class="mb-2"
  >
    <b-button variant="primary" @click.prevent="add(product)">Añadir al carrito</b-button>
  </b-card>
</template>

<script>
export default {
  props: {
    product: { type: Object, required: true }
  },
  methods: {
    add(product) {
      this.$emit("addToCart", product);
    }
  }
};
</script>

