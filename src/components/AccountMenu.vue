<script setup>
function logout () {
  console.log('logout')
}

function changePassword () {
  console.log('changePassword')
}

const menuItems = [
  {
    label: 'Logout',
    handler: logout,
    icon: 'logout'
  },
  {
    label: 'Change Password',
    handler: changePassword,
    icon: 'lock'
  }
]
</script>

<template>
  <q-menu v-bind="$attrs">
    <q-list>
      <q-item
        v-for="item in menuItems"
        :key="item.label"
        clickable
        @click="item.handler"
      >
        <q-item-section side>
          <q-icon :name="item.icon" />
        </q-item-section>
        <q-item-section>{{ item.label }}</q-item-section>
      </q-item>
    </q-list>
  </q-menu>
</template>
