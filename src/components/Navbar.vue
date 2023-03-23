<template>
  <v-app-bar app>
    <div class="d-flex align-center">
      <v-img
        alt="Vuetify Logo"
        class="shrink mr-2"
        contain
        src="@/assets/logo.jpg"
        transition="scale-transition"
        width="40"
      />

      {{ $const.APP_NAME }}
    </div>

    <v-spacer />

    <v-btn href="/login" text>
      <span class="mr-2">Login</span>
      <v-avatar color="primary" size="30">
        <v-icon>mdi-account-circle</v-icon>
      </v-avatar>
    </v-btn>
  </v-app-bar>
</template>

<script></script>

<style lang="scss" scoped></style>
