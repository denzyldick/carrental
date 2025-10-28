<template>
          <v-card>
            <v-img
              :src="photo"
              class="align-end"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="200px"
              cover
            >
              <v-card-title class="text-white" v-text="model"></v-card-title>
            </v-img>

            <v-card-actions>
              <span class="text-h5">{{price}}</span>
              <v-spacer></v-spacer>

              <v-btn
                color="medium-emphasis"
                icon="mdi-heart"
                size="small"
              ></v-btn>

              <v-btn
                color="medium-emphasis"
                icon="mdi-bookmark"
                size="small"
              ></v-btn>

              <v-btn
                color="medium-emphasis"
                icon="mdi-share-variant"
                size="small"
              ></v-btn>
            </v-card-actions>
          </v-card>
</template>
<script setup>
  const props = defineProps({
        model: String,
        photo: String,
        price: Number,
    }
  );
  </script>


