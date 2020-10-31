<template>
    <section class="single-recipe">
      <h1>TITLE</h1>
      <div>
        <img src="" alt="">
      </div>
      <p>{{ $route.params.id}}</p>

      <p>The recipe description</p>
    </section>
</template>

<script>
export default {
}
</script>

<style scoped>
.single-recipe {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 30px;
}
</style>
