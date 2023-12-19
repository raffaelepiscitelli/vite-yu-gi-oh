<template lang="">
    <header>
        <nav class="navbar bg-body-tertiary">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">
      <img src="../assets/imgs/Yu-Gi-Oh Logo.png" alt="Logo" class="d-inline-block align-text-top">
      {{ title }}
    </a>
  </div>
</nav>
    </header>
</template>
<script>
export default {
    data() {
        return {
            title: 'Yu-Gi-Oh API'
        }
    },
}
</script>
<style lang="scss">
    img {
        height: 3.2rem;
    }
</style>