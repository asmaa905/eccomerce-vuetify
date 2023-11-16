<template>
  <v-row>
    <v-col cols="3"
    v-for="(feature, i) in featured" :key="i">
      <v-card
        class="mx-auto my-12 pb-4"
        max-width="374"
      >
        <v-img height="250" class="mx-4"
        :src="feature.img"></v-img>
        <v-card-item class="mt-n4">
          <v-card-title class="text-center">
            {{ feature.title }}
          </v-card-title>
        </v-card-item>
        <v-card-text>
          <div class="text-center">
            {{ feature.bio }}
          </div>
          <v-row align="center" class="mx-0 mt-2">
            <v-rating :model-value="4.5" color="amber" density="compact" half-increments readonly size="small"></v-rating>
            <v-spacer></v-spacer>
            <div class="text-gray ms-4">{{ feature.price }}</div>
          </v-row>

        </v-card-text>
      </v-card>

    </v-col>
  </v-row>
</template>

<script>
export default {
  data:() => ({
    featured: [
      {
        img: "/featured/1.jpg",
        title:"Apple Mac Book Pro",
        price:"$ 93.359",
        bio:"Apple's 2023 flagship, the 16-inch MacBook Pro, combines proven design with the M2 Max CPU to be a powerful force for processing and creating media, gaming, and high-end professional tasks. (Plus, it lasted nearly 27 hours in our battery test.)"
      },
      {
        img: "/featured/2.jpg",
        title:"Apple Mac Book Pro",
        price:"$ 93.359",
        bio:"Apple's 2023 flagship, the 16-inch MacBook Pro, combines proven design with the M2 Max CPU to be a powerful force for processing and creating media, gaming, and high-end professional tasks. (Plus, it lasted nearly 27 hours in our battery test.)"
      },
      {
        img: "/featured/3.jpg",
        title:"Apple Mac Book Pro",
        price:"$ 93.359",
        bio:"Apple's 2023 flagship, the 16-inch MacBook Pro, combines proven design with the M2 Max CPU to be a powerful force for processing and creating media, gaming, and high-end professional tasks. (Plus, it lasted nearly 27 hours in our battery test.)"
      },
      {
        img: "/featured/4.jpg",
        title:"Apple Mac Book Pro",
        price:"$ 93.359",
        bio:"Apple's 2023 flagship, the 16-inch MacBook Pro, combines proven design with the M2 Max CPU to be a powerful force for processing and creating media, gaming, and high-end professional tasks. (Plus, it lasted nearly 27 hours in our battery test.)"
      }
    ]
  })
}
</script>

<style>

</style>
