<template>
  <v-carousel
      v-model="activeSlide"
      color="white"
  >
    <template #next>
      <v-icon color="white" size="72px" style="cursor: pointer" @click="updateSlide(1)">mdi-dog</v-icon>
    </template>
    <template #prev>
      <v-icon color="white" size="72px" style="cursor: pointer" @click="updateSlide(-1)">mdi-cat</v-icon>
    </template>
    <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
        cover
    ></v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  data() {
    return {
      activeSlide: 0,
      items: [
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
        },
      ],
    }
  },
  methods: {
    updateSlide(action) {
      if (this.activeSlide === 0 && action === -1) {
        this.activeSlide = 0;
        return;
      }

      if (this.activeSlide === (this.items.length - 1) && action === 1) {
        this.activeSlide = (this.items.length - 1);
        return;
      }

      this.activeSlide += action;
    }
  }
}
</script>