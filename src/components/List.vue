<template lang="html">
<div class="list">
  <li>
    <router-link :to="{ name:route }">
      <span class="icon is-small"> <i :class=icon aria-hidden="true"></i> </span>
      <span>{{name}}</span>
    </router-link>
  </li>
</div>
</template>

<script>
export default {
  name: 'list',
  props: ['name', 'icon', 'route'],
  created() {
  }
}
</script>

<style lang="scss">
.list {
  .icon.is-small {
    display: inline;
  }
}
</style>
