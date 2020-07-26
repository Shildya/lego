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
  position: relative;
  width: 100%;
  height: 72px;
  background-color: $test;
}

.logo {
  @include centerY;
  left: 24px;
}
</style>