<template lang="html">
  <div class="firm-name-dropdown">

    <div v-if="isCustomers">

      <span :class="{'select is-fullwidth': true, 'is-danger': errors.has('customer') }">
        <select v-validate="'required|not_in:null'" v-model="firm" @change="stateChange()" name="customer">
          <option value=null>Select dropdown</option>
          <option v-for="firm in firms" :value="firm">{{firm.firm_name}}</option>
        </select>
      </span>

      <div class="help is-danger" v-show="errors.has('customer')">
        {{errors.first('customer')}}
      </div>
    </div>
    <div v-if="!isCustomers">
      No Customers
    </div>

  </div>
</template>

<script>
import api from '@/api/main';
export default {
  name: 'firm-name-dropdown',
  created() {
    this.listCustomer();
  },
  data() {
    return {
      firm: null,
      firm_id: null,
      firms: [],
      show: true,
      code: null,
      state_code: null,
      isCustomers: false
    };
  },
  methods: {
    listCustomer() {
      api.listCustomer()
      .then( ( response ) => {
        if(response.data.message == "No Customer") {
          this.isCustomers = false;
        }
        else {
          this.isCustomers = true;
          this.firms = response.data.firms;
        }
      } )
      .catch( ( error ) => {
        console.log( "Error: ", error );
      } )
    },

    stateChange() {
      this.$bus.$emit( 'firm_name_change', {
        firm: this.firm
      } );
    },
  }
}
</script>

<style lang="scss">
.firm-name-dropdown {
  .select.is-fullwidth {
    width: 26rem;
  }
}
</style>
