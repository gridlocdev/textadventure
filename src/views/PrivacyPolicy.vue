<template>
  <v-container
    class="animate__animated animate__fadeIn"
    style="animation-duration: 0.25s"
  >
    <v-row justify="space-around">
      <v-icon style="font-size: 6em; margin-top: 0" x-large color="green">
        mdi-lock-check
      </v-icon>
    </v-row>
    <v-row justify="space-around">
      <v-col
        class="col-xs-10 col-sm-9 col-md-8 col-lg-7"
        align="center"
        justify="center"
      >
        <h1>Privacy Policy</h1>
        <v-row class="ma-5">
          No data from this site ever leaves your browser. All progress is saved via cookies in
          your browser's local cache, which is used exclusively to persist your
          story progress through refreshes and when the browser is closed.
        </v-row>
        <v-spacer />
        <v-row class="ma-5">
          If you would like to reset it, click "Reset Story Progress" in
          Settings or you can also reset it through your browser options.
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
// Component Description:
// A page that lists the Privacy Policy for this application.

export default {};
</script>

<style>
</style>