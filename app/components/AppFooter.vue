<script setup lang="ts">
const links = [
  { label: 'LinkedIn', to: 'https://www.linkedin.com/in/alekos-georgudis-eitel-6051b11ba/', target: '_blank' },
  { label: 'Mi Calendario', to: 'https://calendar.app.google/ZtXgscrydwnF4Rir6', target: '_blank' },
  { label: 'GitHub', to: 'https://github.com/LAxBANDA/', target: '_blank' },
  { label: 'WhatsApp', to: 'https://api.whatsapp.com/send?phone=56958056234', target: '_blank' },
  { label: 'Instagram', to: 'https://www.instagram.com/alekosgeorgudis', target: '_blank' }
  // { label: 'Twitter', to: 'https://twitter.com/nuxt_js', target: '_blank' },
  // { label: 'Status', to: '#' },
  // { label: 'Privacy', to: '#' }
]
</script>

<template>
  <UFooter
    :ui="{
      container: 'border-t border-default lg:py-8',
      right: 'gap-x-0 flex-wrap'
    }"
  >
    <template #left>
      <p class="text-sm text-dimmed">
        Desarrollado por Alekos Georgudis • © {{ new Date().getFullYear() }}
      </p>
    </template>

    <template #right>
      <UButton
        v-for="link in links"
        :key="link.label"
        v-bind="link"
        color="neutral"
        variant="link"
        class="font-light"
        size="sm"
      />
    </template>
  </UFooter>
</template>
