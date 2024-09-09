<template>
   <UContainer>
      <script setup lang="ts">
const items = [
  [{
    label: 'Profile',
    avatar: {
      src: 'https://avatars.githubusercontent.com/u/739984?v=4'
    }
  }], [{
    label: 'Edit',
    icon: 'i-heroicons-pencil-square-20-solid',
    shortcuts: ['E'],
    click: () => {
      console.log('Edit')
    }
  }, {
    label: 'Duplicate',
    icon: 'i-heroicons-document-duplicate-20-solid',
    shortcuts: ['D'],
    disabled: true
  }], [{
    label: 'Archive',
    icon: 'i-heroicons-archive-box-20-solid'
  }, {
    label: 'Move',
    icon: 'i-heroicons-arrow-right-circle-20-solid'
  }], [{
    label: 'Delete',
    icon: 'i-heroicons-trash-20-solid',
    shortcuts: ['⌘', 'D']
  }]
]
</script>

<template>
  <UDropdown :items="items" :popper="{ placement: 'bottom-start' }">
    <UButton color="white" label="Options" trailing-icon="i-heroicons-chevron-down-20-solid" />
  </UDropdown>
</template>

      
      <UCard class="mt-10">
         <template #header>
            <div class="flex justify-between">
               <h1>Welcome to Nuxt UI Starter</h1>
               <ColorScheme>
                  <USelect v-model="$colorMode.preference" :options="['system', 'light', 'dark']" />
               </ColorScheme>
            </div>
         </template>
         <UButton icon="i-heroicons-book-open" to="https://ui.nuxt.com" target="_blank">Open Nuxt UI Documentation</UButton>
      </UCard>
   </UContainer>
</template>
