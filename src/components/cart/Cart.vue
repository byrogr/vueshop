<template>
  <b-table striped :items="cart" :fields="fields">
    <template slot="actions" slot-scope="cell">
      <b-button size="sm" variant="danger" @click.stop="removeProduct(cell.item)">Eliminar</b-button>
    </template>
  </b-table>
</template>

<script>
import { mapGetters, mapMutations, mapState } from "vuex";
export default {
  data() {
    return {
      fields: ["name", "qty", "price", "actions"]
    };
  },
  computed: {
    ...mapState("cart", ["cart"]),
    ...mapGetters("cart", ["totalCost"])
  },
  methods: {
    ...mapMutations("cart", ["removeProduct"])
  }
};
</script>
