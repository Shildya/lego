<template>
  <div class="error-container">
    <img class="error-picture" src="/img/lego-robot.jpg" alt="lego-robot.jpg">
    <div class="error-text">
      <h1 class="error-number">Erreur {{ error.statusCode }}</h1>
      <h2 v-if="error.statusCode === 404" class="error-description">Page non trouvée</h2>
      <h2 v-else class="error-description">Erreur inconnue</h2>
      <nuxt-link to="/" class="error-link"><span class="arrow left"></span> retourner à l'accueil</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  props: ['error'],
  layout: 'default'
}
</script>

<style lang="scss" scoped>
.error-container {
  display: flex;
  justify-content: center;;
  align-items: center;
  position: relative;
  height: fit-content;
}

.error-picture {
  height: 280px;
}

.error-text {
  display: flex;
  flex-direction: column;
  justify-content: left;
  margin-left: 40px;
  height: 100%;
}

.error-number {
  font-size: 80px;
  font-weight: bold;
}

.error-description {
  font-size: 40px;
}

.error-link {
  display: flex;
  align-items: center;
  margin-top: 24px;
  padding: 12px 16px;
  border: 2px solid black;
  border-radius: 4px;
  box-sizing: border-box;
  font-weight: $medium;
  text-transform: uppercase;
  text-decoration: none;
  color: black;
  width: fit-content;
  transition: all 0.25s;

  &:hover {
    color: white;
    background-color: black;

    span {
      border: solid white;
      border-width: 0 2px 2px 0;
    }
  }
}

.arrow {
  border: solid black;
  border-width: 0 2px 2px 0;
  display: inline-block;
  padding: 3px;
  transition: all 0.25s;

  &.left {
    margin-right: 8px;
    transform: rotate(135deg);
    -webkit-transform: rotate(135deg);
  }
}
</style>