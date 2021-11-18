<script setup>
import RegisterButton from 'src/components/RegisterButton.vue'
import AccountMenu from 'src/components/AccountMenu.vue'
import UserAvatar from 'src/components/UserAvatar.vue'
import { ref } from 'vue'

const authenticated = ref(false)
</script>

<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title>
          Quasar App
          <q-btn
            label="toggle authenticated"
            no-caps
            @click="authenticated = !authenticated"
          />
        </q-toolbar-title>

        <q-btn
          v-if="authenticated"
          round
          dense
        >
          <UserAvatar />
          <AccountMenu />
        </q-btn>

        <RegisterButton
          v-else
          label="register"
          unelevated
          color="secondary"
        />
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>
