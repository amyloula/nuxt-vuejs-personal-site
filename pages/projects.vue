<template>
  <div class="projects">
    <div class="projects__header">
      <img
        class="img"
        src="~/assets/imgs/github.svg"
        alt="React Logo"
        aria-label="React logo"
      />
      <h1>Github repositories</h1>
    </div>
    <div class="content__wrapper">
      <TileComponent v-for="tile in tiles" :key="tile.name" :tileInfo="tile" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '~assets/styles/_variables.scss';

.projects {
  padding-top: 1rem;
  margin: $center-margin;
  position: relative;

  &__header {
    text-align: center;
    font-family: $main-header-font;

    h1 {
      font-size: 2rem;
    }
  }
}
.content__wrapper {
  display: flex;
  flex-wrap: wrap;
  width: 50%;
  margin: $center-margin;
  > img {
    flex: 1;
    justify-content: center;
  }
}
</style>

<script>
import TileComponent from '~/components/Tile.vue'

export default {
  components: {
    TileComponent
  },
  created: function() {
    this.fetchGitRepositories()
  },
  data() {
    return {
      tiles: []
    }
  },
  methods: {
    fetchGitRepositories: function() {
      fetch('https://api.github.com/users/amyloula/repos?sort=updated')
        .then(resp => resp.json())
        .then(resp => {
          resp.forEach(element => {
            this.tiles.push({
              name: element.name,
              url: element.url,
              stars: element.stargazers_count
            })
          })
        })
        .catch(err => console.error(err))
    }
  }
}
</script>
