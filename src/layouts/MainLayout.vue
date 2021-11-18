<script setup>
import RegisterButton from 'src/components/RegisterButton.vue'
import AccountMenu from 'src/components/AccountMenu.vue'
import UserAvatar from 'src/components/UserAvatar.vue'
</script>

<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title>
          Quasar App
        </q-toolbar-title>

        <RegisterButton
          v-if="false"
          label="register"
          unelevated
          color="secondary"
        />

        <q-btn
          v-else
          round
          dense
        >
          <UserAvatar />
          <AccountMenu />
        </q-btn>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>
