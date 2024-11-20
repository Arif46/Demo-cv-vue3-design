<script setup lang="ts">
import { EnvelopeIcon, PhoneIcon, MapPinIcon } from '@heroicons/vue/24/solid'
</script>

<template>
  <header class="bg-gradient-to-r from-violet-600 via-purple-600 to-indigo-600 text-white shadow-xl">
    <div class="max-w-4xl mx-auto p-8">
      <div class="flex flex-col md:flex-row md:justify-between md:items-center gap-6">
        <div class="space-y-2">
          <h1 class="text-4xl font-bold">John Doe</h1>
          <h2 class="text-xl text-purple-100">Senior Software Developer</h2>
        </div>

        <div class="flex flex-col space-y-3">
          <a href="mailto:john.doe@example.com" class="flex items-center hover:text-purple-200 transition-colors">
            <EnvelopeIcon class="h-5 w-5 mr-2" />
            <span>john.doe@example.com</span>
          </a>
          <a href="tel:+1234567890" class="flex items-center hover:text-purple-200 transition-colors">
            <PhoneIcon class="h-5 w-5 mr-2" />
            <span>+1 234 567 890</span>
          </a>
          <div class="flex items-center">
            <MapPinIcon class="h-5 w-5 mr-2" />
            <span>San Francisco, CA</span>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>