<template>
  <!-- <h1>gg</h1> -->
  <section class="recipes">
    <Recipe
      v-for="r in recipes"
      :key="r.id"
      :thumbnail="r.thumbnail"
      :title="r.title"
      :id="r.id"
      :previewText="r.previewText"
      />
      <!-- <article class="recipe">
        <div class="thumbnail" style="background-image: url('https://www.seriouseats.com/recipes/images/2015/07/20150702-sous-vide-hamburger-anova-primary-1500x1125.jpg')"></div>
        <h1>title</h1>
        <p>some nice text here</p>
      </article> -->

  </section>
</template>

<script>
import Recipe from '@/components/Recipe'

export default {
  components: {
    Recipe
  },
  asyncData () {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
          resolve({
            recipes: [
              {
                id:   "1",
                title: "Delicious Pizza",
                previewText: "Awesome Pizzaa",
                thumbnail: "https://upload.wikimedia.org/wikipedia/commons/a/a3/Eq_it-na_pizza-margherita_sep2005_sml.jpg"
              },
              {
                id:   "2",
                title: "Delicious Burger",
                previewText: "Big Burger",
                thumbnail: "https://www.seriouseats.com/recipes/images/2015/07/20150702-sous-vide-hamburger-anova-primary-1500x1125.jpg"
              }
            ]
          })
      }, 2000)
    })
  }
}
</script>

<style scoped>
.recipes {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
}
.recipe {
  box-sizing: border-box;
  width: 280px;
  padding: 8xp;
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #aaa;
}
.thumbnail {
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 200px;
}
</style>
