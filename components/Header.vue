<template>
  <header>
    <Logo class="logo" />
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="scss" scoped>
header {
  position: fixed;
  top: 0;
  width: 100%;
  height: 72px;
  background-color: $supernova;
  z-index: 12;
}

.logo {
  @include centerY;
  left: 24px;
}
</style>