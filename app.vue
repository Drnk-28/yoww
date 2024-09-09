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
  }]
]
   const clrs = ["blue", "violet", "green", "emerald", "lime", "red", "yellow", "indigo", "cyan", "sky", "rose", "pink"]
   const random = clrs[Math.floor(Math.random() * clrs.length)]
</script>

<template>
   <UContainer>
      <UDropdown :items="items" :popper="{ placement: 'bottom-start' }">
         <UButton size="xl" :color="random" icon="i-flowbite-bars-from-left-outline" variant="soft" />
      </UDropdown>
      <UDivider label="HOME" :ui="{ label: 'text-primary-500 dark:text-primary-400' }">

      </UDivider>
      <UCard class="mt-10" :color="random">
         <div>
            <h1>Hi Guys</h1>
            <p>In short, this is my personal site and now or in the future I will probably fill it with content such as photos of my memories, as long as I live in this world.</p>
         </div>
      </UCard>
   </UContainer>
</template>
