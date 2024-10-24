
<template>
  <nav class="nav-bar">
    <button class="toggle" @click="$store.commit('toggleButton')">
      <font-awesome-icon class="icon" :icon="['fas', 'bars-staggered']" />
    </button>
  </nav>
</template>

<script>
</script>

<style lang="scss" scoped>
.nav-bar {
  background: #fff;
  width: 100%;
  padding: 20px;
  display: flex;
  justify-content: end;

  button {
    border: none;
    background: transparent;
    cursor: pointer;
  }
  .icon {
    color: #333;
    font-size: 24px;
  }
}
</style>