<template>
  <b-col md="3">
    <b-card
      :title="name"
      :img-src="pic"
      img-alt="Job-info"
      img-top
      tag="article"
      style="max-width: 20rem"
      class="mb-4"
      footer="Card Footer"
    >
      <b-card-text>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor, nam.
      </b-card-text>
      <b-button variant="primary">Apply</b-button>
    </b-card>
  </b-col>
</template>

<script>
export default {
  name: "jobCard",
  props: ["name", "pic"],
};
</script>

<style scoped></style>
