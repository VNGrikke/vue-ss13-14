<template>
  <v-card class="mx-auto" max-width="500">
    <v-card-title>Basic with Icons</v-card-title>

    <v-card-text>
      <v-text-field
        v-model="form.name"
        label="Name"
        prepend-inner-icon="mdi-account"
        placeholder="John Deo"
      ></v-text-field>

      <v-text-field
        v-model="form.company"
        label="Company"
        prepend-inner-icon="mdi-office-building"
        placeholder="ACME Inc."
      ></v-text-field>

      <v-text-field
        v-model="form.email"
        label="Email"
        prepend-inner-icon="mdi-email"
        placeholder="john.deo"
      ></v-text-field>

      <v-text-field
        v-model="form.phone"
        label="Phone No"
        prepend-inner-icon="mdi-phone"
        placeholder="412 2150 451"
      ></v-text-field>

      <v-textarea
        v-model="form.message"
        label="Message"
        prepend-inner-icon="mdi-message"
        placeholder="Hi, Do you have a moment to talk Jeo?"
      ></v-textarea>
    </v-card-text>

    <v-card-actions>
      <v-spacer></v-spacer>
      <v-btn color="primary">Send</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script setup>
import { ref } from "vue";

const form = ref({
  name: "",
  company: "",
  email: "",
  phone: "",
  message: "",
});
</script>

<style scoped>
</style>


<template>
  <v-card class="mx-auto" max-width="500">
    <v-card-title>Basic Layout</v-card-title>

    <v-card-text>
      <v-text-field
        v-model="form.name"
        label="Name"
        placeholder="John Deo"
      ></v-text-field>

      <v-text-field
        v-model="form.company"
        label="Company"
        placeholder="ACME Inc."
      ></v-text-field>

      <v-text-field
        v-model="form.email"
        label="Email"
        placeholder="john.deo"
      ></v-text-field>

      <v-text-field
        v-model="form.phone"
        label="Phone No"
        placeholder="412 2150 451"
      ></v-text-field>

      <v-textarea
        v-model="form.message"
        label="Message"
        placeholder="Hi, Do you have a moment to talk Jeo?"
      ></v-textarea>
    </v-card-text>

    <v-card-actions>
      <v-spacer></v-spacer>
      <v-btn color="primary">Send</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script setup>
import { ref } from "vue";

const form = ref({
  name: "",
  company: "",
  email: "",
  phone: "",
  message: "",
});
</script>

<style scoped>
</style>
