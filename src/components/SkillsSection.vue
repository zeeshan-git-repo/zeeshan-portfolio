<template>
  <section id="skills" class="section-padding bg-dark-50 dark:bg-dark-800">
    <div class="max-w-7xl mx-auto">
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-dark-900 dark:text-white mb-4">
          Technical <span class="gradient-text">Skills</span>
        </h2>
        <p class="text-lg text-dark-600 dark:text-dark-300 max-w-2xl mx-auto">
          A comprehensive overview of my technical expertise and the technologies I work with
        </p>
      </div>

      <div class="grid lg:grid-cols-3 gap-8">
        <!-- Backend Technologies -->
        <div class="card p-8">
          <div class="text-center mb-6">
            <div class="w-16 h-16 mx-auto bg-primary-100 dark:bg-primary-900/30 rounded-xl flex items-center justify-center mb-4">
              <i class="fas fa-server text-2xl text-primary-600"></i>
            </div>
            <h3 class="text-xl font-semibold text-dark-900 dark:text-white">Backend Development</h3>
          </div>
          
          <div class="space-y-4">
            <div v-for="skill in backendSkills" :key="skill.name" class="skill-item">
              <div class="flex justify-between items-center mb-2">
                <span class="text-dark-700 dark:text-dark-300 font-medium">{{ skill.name }}</span>
                <span class="text-sm text-primary-600">{{ skill.level }}%</span>
              </div>
              <div class="w-full bg-dark-200 dark:bg-dark-700 rounded-full h-2">
                <div 
                  class="bg-gradient-to-r from-primary-500 to-primary-600 h-2 rounded-full transition-all duration-1000"
                  :style="{ width: skill.level + '%' }"
                ></div>
              </div>
            </div>
          </div>
        </div>

        <!-- Frontend Technologies -->
        <div class="card p-8">
          <div class="text-center mb-6">
            <div class="w-16 h-16 mx-auto bg-green-100 dark:bg-green-900/30 rounded-xl flex items-center justify-center mb-4">
              <i class="fas fa-laptop-code text-2xl text-green-600"></i>
            </div>
            <h3 class="text-xl font-semibold text-dark-900 dark:text-white">Frontend Development</h3>
          </div>
          
          <div class="space-y-4">
            <div v-for="skill in frontendSkills" :key="skill.name" class="skill-item">
              <div class="flex justify-between items-center mb-2">
                <span class="text-dark-700 dark:text-dark-300 font-medium">{{ skill.name }}</span>
                <span class="text-sm text-green-600">{{ skill.level }}%</span>
              </div>
              <div class="w-full bg-dark-200 dark:bg-dark-700 rounded-full h-2">
                <div 
                  class="bg-gradient-to-r from-green-500 to-green-600 h-2 rounded-full transition-all duration-1000"
                  :style="{ width: skill.level + '%' }"
                ></div>
              </div>
            </div>
          </div>
        </div>

        <!-- DevOps & Cloud -->
        <div class="card p-8">
          <div class="text-center mb-6">
            <div class="w-16 h-16 mx-auto bg-purple-100 dark:bg-purple-900/30 rounded-xl flex items-center justify-center mb-4">
              <i class="fas fa-cloud text-2xl text-purple-600"></i>
            </div>
            <h3 class="text-xl font-semibold text-dark-900 dark:text-white">DevOps & Cloud</h3>
          </div>
          
          <div class="space-y-4">
            <div v-for="skill in devopsSkills" :key="skill.name" class="skill-item">
              <div class="flex justify-between items-center mb-2">
                <span class="text-dark-700 dark:text-dark-300 font-medium">{{ skill.name }}</span>
                <span class="text-sm text-purple-600">{{ skill.level }}%</span>
              </div>
              <div class="w-full bg-dark-200 dark:bg-dark-700 rounded-full h-2">
                <div 
                  class="bg-gradient-to-r from-purple-500 to-purple-600 h-2 rounded-full transition-all duration-1000"
                  :style="{ width: skill.level + '%' }"
                ></div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Technology Icons -->
      <div class="mt-16">
        <h3 class="text-2xl font-semibold text-center text-dark-900 dark:text-white mb-8">
          Technologies I Work With
        </h3>
        <div class="grid grid-cols-4 md:grid-cols-6 lg:grid-cols-8 gap-6">
          <div v-for="tech in technologies" :key="tech.name" 
               class="flex flex-col items-center p-4 card hover:scale-105 transition-transform duration-300">
            <i :class="tech.icon" class="text-3xl mb-2" :style="{ color: tech.color }"></i>
            <span class="text-xs text-dark-600 dark:text-dark-400 text-center">{{ tech.name }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const backendSkills = ref([
  { name: 'Java', level: 95 },
  { name: 'Spring Boot', level: 90 },
  { name: 'Spring MVC', level: 88 },
  { name: 'Microservices', level: 85 },
  { name: 'REST API', level: 92 },
  { name: 'SQL', level: 88 },
  { name: 'Apache Kafka', level: 80 },
])

const frontendSkills = ref([
  { name: 'JavaScript', level: 88 },
  { name: 'Vue.js', level: 85 },
  { name: 'HTML5', level: 95 },
  { name: 'CSS3', level: 90 },
  { name: 'TypeScript', level: 80 },
  { name: 'Responsive Design', level: 92 },
])

const devopsSkills = ref([
  { name: 'AWS', level: 82 },
  { name: 'Docker', level: 85 },
  { name: 'CI/CD', level: 80 },
  { name: 'Git', level: 90 },
  { name: 'Linux', level: 75 },
  { name: 'Jenkins', level: 78 },
])

const technologies = ref([
  { name: 'Java', icon: 'fab fa-java', color: '#f89820' },
  { name: 'Spring', icon: 'fas fa-leaf', color: '#6db33f' },
  { name: 'Vue.js', icon: 'fab fa-vuejs', color: '#4fc08d' },
  { name: 'JavaScript', icon: 'fab fa-js-square', color: '#f7df1e' },
  { name: 'Docker', icon: 'fab fa-docker', color: '#2496ed' },
  { name: 'AWS', icon: 'fab fa-aws', color: '#ff9900' },
  { name: 'Git', icon: 'fab fa-git-alt', color: '#f05032' },
  { name: 'SQL', icon: 'fas fa-database', color: '#336791' },
])
</script>

<style scoped>
.skill-item {
  @apply transition-all duration-300 hover:transform hover:scale-105;
}
</style>
