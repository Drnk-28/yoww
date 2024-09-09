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
   const clrs = ["blue", "violet", "green", "emerald", "lime", "red", "yellow", "indigo", "cyan", "sky", "rose", "pink"]
   const random = clrs[Math.floor(Math.random() * clrs.length)]
</script>

<template>
   <UContainer>
      <UDropdown :items="items" :popper="{ placement: 'bottom-start' }">
         <UButton :color="random" label="DRNK" icon="i-flowbite-bars-from-left-outline" />
      </UDropdown>
      <UCard class="mt-10">
         <div>
            <h1>Hi Guys</h1>
         </div>
      </UCard>
   </UContainer>
</template>
