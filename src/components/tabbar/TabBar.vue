<template>
  <div id="tab-bar">
    <slot>

    </slot>
  </div>
</template>

<script>
  export default {
    name: "TabBar"
  }
</script>

<style scoped>
  #tab-bar{
    position: Fixed;
    bottom: 100px;
    left: 0;
    height: 55px;
    display: flex;
    text-align: center;
    background: #ccc;
    width: 100vw;
  }

</style>