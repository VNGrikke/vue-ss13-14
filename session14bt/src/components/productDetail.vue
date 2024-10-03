<template>
  <v-card class="mx-auto" max-width="900">
    <v-row>
      <v-col cols="12" md="6">
        <v-carousel hide-delimiters>
          <v-carousel-item v-for="(image, index) in images" :key="index">
            <v-img :src="image"></v-img>
          </v-carousel-item>
        </v-carousel>
      </v-col>
      <v-col cols="12" md="6">
        <div class="text-h5">Cute Soft Teddybear</div>
        <v-rating value="4" readonly></v-rating>
        <div class="text-h6">$200 <s>$175</s></div>

        <div>Colors:</div>
        <v-radio-group v-model="color">
          <v-radio label="Red" value="red"></v-radio>
          <v-radio label="Yellow" value="yellow"></v-radio>
          <v-radio label="Blue" value="blue"></v-radio>
        </v-radio-group>

        <div>Quantity:</div>
        <v-btn icon small> - </v-btn>
        <span>1</span>
        <v-btn icon small> + </v-btn>

        <v-btn color="success">Buy Now</v-btn>
        <v-btn outlined>Add To Cart</v-btn>
      </v-col>
    </v-row>
  </v-card>
</template>

<script setup>
import { ref } from "vue";

const color = ref("red");

const images = ref([
  "https://pethouse.com.vn/wp-content/uploads/2022/12/anh-meo-anh-long-ngan-9988838880.jpg",
  "https://dean2020.edu.vn/wp-content/uploads/2020/03/anh-meo-32.jpg",
  "https://upanh123.com/wp-content/uploads/2020/11/hinh-anh-con-meo-cute9.jpg",
]);
</script>

<style scoped>
</style>
