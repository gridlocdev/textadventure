<template>
  <v-row
    align="center"
    justify="center"
    class="text-center my-3"
    cols="12"
    no-gutters
  >
    <v-col class="col-5">
      <h4 class="font-weight-medium">Reset Story Progress</h4>
    </v-col>
    <v-col>
      <v-row no-gutters justify="center">
        <v-dialog v-model="dialog" max-width="290">
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              style="width: 60%"
              class="ma-2 myClass"
              v-bind="attrs"
              v-on="on"
              elevation="5"
            >
              Reset Story
            </v-btn>
          </template>
          <v-card>
            <v-card-title style="word-break: normal" class="headline">
              Reset Progress
              <v-spacer /> on the current Story?
            </v-card-title>
            <v-card-text
              >Resetting the story progress will clear your browser's local
              cache, and allow you to start over from the beginning.
            </v-card-text>
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn color="blue darken-1" text @click="dialog = false">
                Return
              </v-btn>

              <v-btn color="blue darken-1" text @click="resetLocalCache()">
                Confirm
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
      </v-row>
    </v-col>
  </v-row>
</template>

<script>
// Component Description:
// This component is in Settings, and is used to reset the application's story state back to default.

export default {
  data() {
    return {
      dialog: false,
    };
  },
  methods: {
    resetLocalCache() {
      // Resets story progress, and navigates back to home.
      this.$store.dispatch("resetStoryProgress");

      this.dialog = false;

      this.$emit("closeSettingsModal");
      this.$router.push({ name: "Start" });
      this.$router.go();
    },
  },
};
</script>

<style>
</style>