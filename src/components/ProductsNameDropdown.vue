<template lang="html">
  <div class="products-name-dropdown">
    <div class="" v-if="!message">
      <span :class="{'select is-fullwidth': true, 'is-danger': errors.has('product') }">
        <select v-model="product" v-validate="'required|not_in:null'"
        @change="productChange()" name="product">
          <option value=null>Select dropdown</option>
          <option v-for="pro in products" :value="pro">{{pro.product_name}} - {{pro.hsn_code}}</option>
        </select>
      </span>
    </div>
    <div v-if="message == 'No Products'">
      No Products
    </div>
  </div>
</template>

<script>
import api from '@/api/main';
export default {
  inject: ['$validator'],
  name: 'products-name-dropdown',
  created() {
    this.getProducts();
  },
  data() {
    return {
      product: null,
      product_id: null,
      products: [],
      show: true,
      code: null,
      message: ''
    };
  },
  methods: {
    getProducts() {
      api.getProducts()
        .then( ( response ) => {
          if ( response.data.message ) {
            this.message = 'No Products';
          } else {
            this.products = response.data.products;
            this.message = null;
          }
        } )
        .catch( ( error ) => {
          console.log( error );
        } )
    },

    productChange() {
      this.$bus.$emit( 'product_name_change', {
        product: this.product
      } );
    },
  }
}
</script>

<style lang="scss">
.products-name-dropdown {}
</style>
