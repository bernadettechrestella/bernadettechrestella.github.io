<template>
  <v-footer padless color="blue" class="footer">
    <v-col
      class="text-center"
      cols="12"
    >
      {{ new Date().getFullYear() }} — <strong>Bernadette Chrestella</strong>
    </v-col>
  </v-footer>
</template>

<script>
export default {
    name: "Footer"
}
</script>