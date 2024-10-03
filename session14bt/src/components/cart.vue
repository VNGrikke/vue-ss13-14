<template>
  <v-card class="mx-auto" max-width="900">
    <v-card-title>
      <v-tabs v-model="tab" grow>
        <v-tab>Item Cart</v-tab>
        <v-tab>Billing</v-tab>
        <v-tab>Payment</v-tab>
      </v-tabs>
    </v-card-title>

    <v-card-text>
      <v-row>
        <v-col cols="12" md="6">
          <v-img
            src="https://pethouse.com.vn/wp-content/uploads/2022/12/anh-meo-anh-long-ngan-9988838880.jpg"
            max-width="120"
          ></v-img>
          <div>
            <strong>Cute Soft Teddybear</strong>
            <div>size: 8 | Color: Dark Red</div>
          </div>
        </v-col>
        <v-col cols="3" md="2">
          <div>$200</div>
          <s>$175</s>
        </v-col>
        <v-col cols="3" md="2">
          <v-btn icon small> - </v-btn>
          <span>1</span>
          <v-btn icon small> + </v-btn>
        </v-col>
        <v-col cols="3" md="2">$200</v-col>
        <v-col cols="1">
          <v-btn icon>
            <v-icon color="red">mdi-delete</v-icon>
          </v-btn>
        </v-col>
      </v-row>

      <v-divider></v-divider>
      <div class="text-h6">Order Summary</div>
      <v-row>
        <v-col>Sub Total</v-col>
        <v-col>$200</v-col>
      </v-row>
      <v-row>
        <v-col>Discount 5%</v-col>
        <v-col color="error">- $10</v-col>
      </v-row>
      <v-row>
        <v-col>Shipping Charges</v-col>
        <v-col>-</v-col>
      </v-row>
      <v-row class="font-weight-bold">
        <v-col>Total</v-col>
        <v-col>$190</v-col>
      </v-row>

      <v-btn outlined color="error">Continue Shopping</v-btn>
      <v-btn color="success">CheckOut</v-btn>
    </v-card-text>
  </v-card>
</template>

<script setup>
import { ref } from "vue";
const tab = ref(0);
</script>

<style scoped>
</style>
