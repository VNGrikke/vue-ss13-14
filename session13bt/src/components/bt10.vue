<template>
  <v-card class="mx-auto" max-width="800">
    <v-card-title>Item</v-card-title>
    <v-data-table
      :headers="headers"
      :items="items"
      class="elevation-1"
      item-value="name"
      :items-per-page="5"
    >
      <template v-slot:item.status="{ item }">
        <v-chip :color="getStatusColor(item.status)" dark small>
          {{ item.status }}
        </v-chip>
      </template>
      <template v-slot:footer.page-text> Items per page </template>
    </v-data-table>
  </v-card>
</template>

<script setup>
import { ref } from "vue";

const headers = [
  { text: "Name", value: "name" },
  { text: "Project Name", value: "project" },
  { text: "Post", value: "post" },
  { text: "Status", value: "status" },
  { text: "Budget", value: "budget" },
];

const items = [
  {
    name: "Sunil Joshi",
    project: "Elite Admin",
    post: "Web Designer",
    status: "Active",
    budget: "$3.9",
  },
  {
    name: "Andrew McDownland",
    project: "Real Homes WP Theme",
    post: "Project Manager",
    status: "Pending",
    budget: "$24.5k",
  },
  {
    name: "Christopher Jamil",
    project: "MedicalPro WP Theme",
    post: "Project Manager",
    status: "Completed",
    budget: "$12.8k",
  },
  {
    name: "Nirav Joshi",
    project: "Hosting Press HTML",
    post: "Frontend Engineer",
    status: "Active",
    budget: "$2.4k",
  },
  {
    name: "Micheal Doe",
    project: "Helping Hands WP Theme",
    post: "Content Writer",
    status: "Cancel",
    budget: "$9.3k",
  },
];

const getStatusColor = (status) => {
  switch (status) {
    case "Active":
      return "green";
    case "Pending":
      return "orange";
    case "Completed":
      return "blue";
    case "Cancel":
      return "red";
    default:
      return "grey";
  }
};
</script>

<style scoped>
</style>
