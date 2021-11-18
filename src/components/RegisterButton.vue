<script setup>
import { ref } from 'vue'

const showDialog = ref(false)
</script>

<template>
  <q-btn
    v-bind="$attrs"
    @click="showDialog = true"
  >
    <q-dialog v-model="showDialog">
      <q-card>
        <q-card-section>
          Show register form
        </q-card-section>
      </q-card>
    </q-dialog>
  </q-btn>
</template>
