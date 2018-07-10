<template>
  <div class="mint-swipe-item">
    <slot/>
  </div>
</template>

<script>
export default {
  name: 'MtSwipeItem',

  mounted() {
    if (this.$parent) this.$parent.swipeItemCreated(this);
  },

  destroyed() {
    if (this.$parent) this.$parent.swipeItemDestroyed(this);
  },
};
</script>
