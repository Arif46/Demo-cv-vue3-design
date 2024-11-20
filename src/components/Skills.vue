<script setup lang="ts">
const skills = [
  { name: 'Vue.js', level: 90 },
  { name: 'TypeScript', level: 85 },
  { name: 'JavaScript', level: 90 },
  { name: 'HTML/CSS', level: 85 },
  { name: 'Git', level: 80 },
  { name: 'Node.js', level: 75 }
]
</script>

<template>
  <section class="bg-white/80 backdrop-blur-sm rounded-xl shadow-lg p-6 md:p-8 transform hover:scale-[1.01] transition-transform">
    <h2 class="text-2xl font-bold text-gray-800 mb-6 flex items-center">
      <span class="bg-gradient-to-r from-violet-500 to-purple-500 w-2 h-8 mr-3 rounded-full"></span>
      Skills
    </h2>
    
    <div class="grid grid-cols-1 gap-6">
      <div v-for="skill in skills" :key="skill.name" 
           class="bg-white/90 p-4 rounded-lg hover:shadow-md transition-all duration-300">
        <div class="flex justify-between items-center mb-2">
          <h3 class="font-semibold text-gray-800">{{ skill.name }}</h3>
          <span class="text-purple-600 font-medium">{{ skill.level }}%</span>
        </div>
        <div class="w-full bg-gray-200 rounded-full h-2">
          <div class="bg-gradient-to-r from-violet-500 to-purple-500 h-2 rounded-full transition-all duration-500"
               :style="{ width: `${skill.level}%` }"></div>
        </div>
      </div>
    </div>
  </section>
</template>