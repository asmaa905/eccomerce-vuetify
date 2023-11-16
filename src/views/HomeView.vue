<template>
  <v-app>
    <nav-bar></nav-bar>
    <v-main>
      <v-container>
        <v-row>
          <v-col cols="12" sm="12">
            <v-carousel>
              <v-carousel-item v-for="(item , i) in items" :key="i" :src="item.src" cover>
                <v-row>
                  <v-col cols="12" sm="6">
                    <div class="d-flex fill-height justify-center align-center">
                      <h2 class="text-white top">{{ item.title }}</h2><br />
                      <br />
                    </div>
                    <div class="d-flex fill-height justify-center align-center">
                      <p class="text text-white">{{ item.text }}</p>
                    </div>
                    <!-- not appear  -->
                    <div class="d-flex fill-height justify-center align-center">
                      <v-btn style="margin-top:-120px;">Buy Now</v-btn>
                    </div>
                  </v-col>
                </v-row>
              </v-carousel-item>
            </v-carousel>
          </v-col>
          <v-toolbar color="transparent">
            <v-toolbar-title>Popular Products</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn icon="mdi mdi-chevron-left"></v-btn>
            <v-btn icon="mdi mdi-chevron-right"></v-btn>
          </v-toolbar>
          <v-col cols="12" sm="12" class="mt-n10">
            <popular-comp />
          </v-col>
          <v-toolbar color="transparent" class="mt-n10">
            <v-toolbar-title>Featured Products</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn icon="mdi mdi-chevron-left"></v-btn>
            <v-btn icon="mdi mdi-chevron-right"></v-btn>
          </v-toolbar>
          <v-col cols="12" sm="12" class="mt-n10">
            <feature-comp />
          </v-col>
          <v-col cols="12" sm="12" class="mt-n10">
            <client-comp />
          </v-col>
          <v-col cols="12" sm="12" class="mt-n10">
            <v-row>
              <v-col cols="12" sm="4">
                <v-card class="mx-auto my-12 pb-4" max-width="374">
                  <v-row>
                    <v-col cols="12" sm="6">
                      <v-card-item class="mt-10">
                        <v-card-title class="text-center">
                          Smart Watch
                        </v-card-title>
                      </v-card-item>
                      <v-card-text>
                          <div class="text-center">
                            Small pallets, salads & sandwitches
                          </div>
                          <div class="text-center">
                            <v-btn color="black">Buy Now</v-btn>
                          </div>
                      </v-card-text>
                    </v-col>
                    <v-col cols="12" sm="6">
                      <v-img height="250" class="mx-4" src="/footer/10.png"></v-img>
                    </v-col>

                  </v-row>
                </v-card>
              </v-col>
              <v-col cols="12" sm="4" >
                <v-card class="mx-auto my-12 pb-4" max-width="374"  color="red">
                  <v-row>
                    <v-col cols="12" sm="6">
                      <v-card-item class="mt-10">
                        <v-card-title class="text-center">
                          Smart Watch
                        </v-card-title>
                      </v-card-item>
                      <v-card-text>
                          <div class="text-center">
                            Small pallets, salads & sandwitches
                          </div>
                          <div class="text-center">
                            <v-btn color="black">Buy Now</v-btn>
                          </div>
                      </v-card-text>
                    </v-col>
                    <v-col cols="12" sm="6">
                      <v-img height="250" class="mx-4" src="/footer/1.png"></v-img>
                    </v-col>

                  </v-row>
                </v-card>
              </v-col>
              <v-col cols="12" sm="4">
                <v-card class="mx-auto my-12 pb-4" max-width="374">
                  <v-row>
                    <v-col cols="12" sm="6">
                      <v-card-item class="mt-10">
                        <v-card-title class="text-center">
                          Smart Watch
                        </v-card-title>
                      </v-card-item>
                      <v-card-text>
                          <div class="text-center">
                            Small pallets, salads & sandwitches
                          </div>
                          <div class="text-center">
                            <v-btn color="black">Buy Now</v-btn>
                          </div>
                      </v-card-text>
                    </v-col>
                    <v-col cols="12" sm="6">
                      <v-img height="250" class="mx-4" src="/footer/11.png"></v-img>
                    </v-col>

                  </v-row>
                </v-card>
              </v-col>

            </v-row>
          </v-col>
        </v-row>
      </v-container>
      <footer-comp/>
    </v-main>
  </v-app>
</template>
<script>
import NavBar from '@/components/NavBar.vue';
import PopularComp from '@/components/PopularComp.vue';
import FeatureComp from '@/components/FeatureComp.vue';
import ClientComp from '@/components/ClientComp.vue';
import FooterComp from '@/components/FooterComp.vue';
export default {
  data() {
    return {
      items: [
        {
          src:"/images/1.jpg",
          title:"Surface Studio",
          text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus harum eius saepe vitae? Dicta quasi itaque sapiente, molestiae mollitia autem illo veritatis fuga fugit maiores cum corrupti labore consequuntur assumenda?"
        },
        {
          src:"/images/2.jpg",
          title:"Surface Studio",
          text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus harum eius saepe vitae? Dicta quasi itaque sapiente, molestiae mollitia autem illo veritatis fuga fugit maiores cum corrupti labore consequuntur assumenda?"
        },
        {
          src:"/images/3.jpg",
          title:"Surface Studio",
          text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus harum eius saepe vitae? Dicta quasi itaque sapiente, molestiae mollitia autem illo veritatis fuga fugit maiores cum corrupti labore consequuntur assumenda?"
        },
        {
          src:"/images/3.jpg",
          title:"Surface Studio",
          text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus harum eius saepe vitae? Dicta quasi itaque sapiente, molestiae mollitia autem illo veritatis fuga fugit maiores cum corrupti labore consequuntur assumenda?"
        },
      ]
    }
  },
  components:{
    NavBar,
    PopularComp,
    FeatureComp,
    ClientComp,
    FooterComp
  }
}
</script>
<style scoped>
.top {
  margin-top: 100px;
}
.text {
  margin-top:-40px;
  margin-left: 80px;
}
.top-day {
  margin-top: 120px;
}
</style>
