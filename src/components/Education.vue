<script setup lang="ts">
interface Education {
  degree: string
  school: string
  period: string
  details: string[]
  gpa?: string
}

const education: Education[] = [
  {
    degree: 'Master of Science in Computer Science',
    school: 'Stanford University',
    period: '2016 - 2018',
    gpa: '3.8/4.0',
    details: [
      'Specialized in Software Engineering and Distributed Systems',
      'Research Assistant in Cloud Computing Lab',
      'Teaching Assistant for Advanced Algorithms course'
    ]
  },
  {
    degree: 'Bachelor of Science in Computer Science',
    school: 'University of California, Berkeley',
    period: '2012 - 2016',
    gpa: '3.9/4.0',
    details: [
      'Dean\'s List all semesters',
      'Senior thesis on Distributed Systems',
      'President of Computer Science Club'
    ]
  }
]
</script>

<template>
  <section class="bg-white rounded-xl shadow-lg p-6 md:p-8 transform hover:scale-[1.01] transition-transform">
    <h2 class="text-2xl font-bold text-gray-800 mb-6 flex items-center">
      <span class="bg-blue-600 w-2 h-8 mr-3 rounded-full"></span>
      Education
    </h2>
    
    <div class="space-y-8">
      <div v-for="(edu, index) in education" :key="index" 
           class="relative pl-6 border-l-2 border-blue-500">
        <div class="absolute w-3 h-3 bg-blue-500 rounded-full -left-[7px] top-2"></div>
        <h3 class="text-xl font-semibold text-gray-800">{{ edu.degree }}</h3>
        <p class="text-blue-600 font-medium">{{ edu.school }} • {{ edu.period }}</p>
        <p v-if="edu.gpa" class="text-gray-600 mt-1">GPA: {{ edu.gpa }}</p>
        <ul class="mt-2 space-y-1">
          <li v-for="(detail, idx) in edu.details" :key="idx"
              class="text-gray-600 flex items-start">
            <span class="text-blue-500 mr-2">•</span>
            {{ detail }}
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>