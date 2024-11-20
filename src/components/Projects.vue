<script setup lang="ts">
// ... previous interface and data remain the same ...
</script>

<template>
  <section class="bg-white/80 backdrop-blur-sm rounded-xl shadow-lg p-6 md:p-8">
    <h2 class="text-2xl font-bold text-gray-800 mb-6 flex items-center">
      <span class="bg-gradient-to-r from-violet-500 to-purple-500 w-2 h-8 mr-3 rounded-full"></span>
      Projects
    </h2>
    
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
      <div v-for="project in projects" :key="project.title" 
           class="bg-white/90 rounded-lg overflow-hidden shadow-md hover:shadow-xl transition-all duration-300 hover:scale-[1.02]">
        <div class="h-48 bg-gray-200 relative">
          <div class="absolute inset-0 bg-gradient-to-br from-violet-600/90 via-purple-600/90 to-indigo-600/90 flex items-center justify-center text-white text-xl font-bold p-4 text-center">
            {{ project.title }}
          </div>
        </div>
        
        <div class="p-4">
          <p class="text-gray-600 mb-4">{{ project.description }}</p>
          
          <div class="mb-4 flex flex-wrap gap-2">
            <span v-for="tech in project.technologies" :key="tech"
                  class="px-2 py-1 bg-gradient-to-r from-violet-50 to-purple-50 text-purple-700 rounded-full text-sm border border-purple-100">
              {{ tech }}
            </span>
          </div>
          
          <div class="flex gap-4">
            <a :href="project.demoUrl" target="_blank" 
               class="flex-1 text-center px-4 py-2 bg-gradient-to-r from-violet-600 to-purple-600 text-white rounded-lg hover:from-violet-700 hover:to-purple-700 transition-all duration-300">
              Live Demo
            </a>
            <a :href="project.githubUrl" target="_blank"
               class="flex-1 text-center px-4 py-2 bg-gradient-to-r from-gray-800 to-gray-900 text-white rounded-lg hover:from-gray-900 hover:to-black transition-all duration-300">
              GitHub
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>