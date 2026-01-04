<template>
  <section id="experience" class="section-padding bg-white dark:bg-dark-900">
    <div class="max-w-7xl mx-auto">
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-dark-900 dark:text-white mb-4">
          Professional <span class="gradient-text">Experience</span>
        </h2>
        <p class="text-lg text-dark-600 dark:text-dark-300 max-w-2xl mx-auto">
          6+ years of professional experience building scalable applications and leading development teams
        </p>
      </div>

      <!-- Experience Timeline -->
      <div class="relative">
        <!-- Timeline Line -->
        <div class="absolute left-1/2 transform -translate-x-px h-full w-0.5 bg-primary-200 dark:bg-primary-800"></div>

        <!-- Experience Items -->
        <div class="space-y-12">
          <div v-for="(experience, index) in experiences" :key="index" 
               :class="['relative flex items-center', index % 2 === 0 ? 'flex-row' : 'flex-row-reverse']">
            
            <!-- Timeline Dot -->
            <div class="absolute left-1/2 transform -translate-x-1/2 w-4 h-4 bg-primary-600 rounded-full border-4 border-white dark:border-dark-900 z-10"></div>
            
            <!-- Content -->
            <div :class="['w-5/12', index % 2 === 0 ? 'pr-8 text-right' : 'pl-8 text-left']">
              <div class="card p-6 hover:shadow-xl transition-all duration-300">
                <div class="flex items-center mb-3" :class="index % 2 === 0 ? 'justify-end' : 'justify-start'">
                  <div class="w-12 h-12 bg-primary-100 dark:bg-primary-900/30 rounded-lg flex items-center justify-center mr-3">
                    <i :class="experience.icon" class="text-primary-600 text-xl"></i>
                  </div>
                </div>
                
                <h3 class="text-xl font-semibold text-dark-900 dark:text-white mb-2">
                  {{ experience.position }}
                </h3>
                <h4 class="text-lg font-medium text-primary-600 mb-2">
                  {{ experience.company }}
                </h4>
                <p class="text-sm text-dark-500 dark:text-dark-400 mb-4">
                  {{ experience.duration }} | {{ experience.location }}
                </p>
                <p class="text-dark-600 dark:text-dark-300 mb-4">
                  {{ experience.description }}
                </p>
                
                <!-- Technologies Used -->
                <div class="flex flex-wrap gap-2" :class="index % 2 === 0 ? 'justify-end' : 'justify-start'">
                  <span v-for="tech in experience.technologies" :key="tech"
                        class="px-3 py-1 bg-primary-100 dark:bg-primary-900/30 text-primary-700 dark:text-primary-300 text-xs rounded-full">
                    {{ tech }}
                  </span>
                </div>
              </div>
            </div>
            
            <!-- Empty space for alternating layout -->
            <div class="w-5/12"></div>
          </div>
        </div>
      </div>

      <!-- Key Achievements -->
      <div class="mt-20 grid md:grid-cols-3 gap-8">
        <div class="card p-6 text-center">
          <div class="w-16 h-16 mx-auto bg-green-100 dark:bg-green-900/30 rounded-xl flex items-center justify-center mb-4">
            <i class="fas fa-code text-2xl text-green-600"></i>
          </div>
          <h3 class="text-lg font-semibold text-dark-900 dark:text-white mb-2">Clean Code Advocate</h3>
          <p class="text-dark-600 dark:text-dark-300 text-sm">
            Implemented best practices and coding standards, reducing bug reports by 40%
          </p>
        </div>
        
        <div class="card p-6 text-center">
          <div class="w-16 h-16 mx-auto bg-blue-100 dark:bg-blue-900/30 rounded-xl flex items-center justify-center mb-4">
            <i class="fas fa-users text-2xl text-blue-600"></i>
          </div>
          <h3 class="text-lg font-semibold text-dark-900 dark:text-white mb-2">Technical Leadership</h3>
          <p class="text-dark-600 dark:text-dark-300 text-sm">
            Promoted through ranks: Trainee → SDE → Staff Engineer, mentoring teams and driving technical excellence
          </p>
        </div>
        
        <div class="card p-6 text-center">
          <div class="w-16 h-16 mx-auto bg-purple-100 dark:bg-purple-900/30 rounded-xl flex items-center justify-center mb-4">
            <i class="fas fa-rocket text-2xl text-purple-600"></i>
          </div>
          <h3 class="text-lg font-semibold text-dark-900 dark:text-white mb-2">Performance Optimization</h3>
          <p class="text-dark-600 dark:text-dark-300 text-sm">
            Optimized applications resulting in 60% improvement in response times
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const experiences = ref([
  {
    position: 'Software Dev Staff Engineer',
    company: 'Quest Software',
    duration: 'April 2024 - Present',
    location: 'Hyderabad / Remote',
    description: 'Promoted to Staff Engineer role, leading technical architecture decisions for erwinDI Intelligence platform. Designing scalable solutions for enterprise data intelligence, mentoring junior developers, and driving best practices across development teams. Leading cross-functional initiatives and technical roadmap planning.',
    technologies: ['Java', 'Spring Boot', 'Vue.js', 'Microservices', 'AWS', 'Technical Leadership'],
    icon: 'fas fa-star'
  },
  {
    position: 'Software Development Engineer',
    company: 'Quest Software',
    duration: 'May 2022 - April 2024',
    location: 'Hyderabad / Remote',
    description: 'Promoted to Software Development Engineer after demonstrating strong technical skills. Led development of key features in erwinDI Intelligence including data lineage tracking, metadata management, and performance optimization. Collaborated with product teams to deliver enterprise-grade solutions.',
    technologies: ['Java', 'Spring Boot', 'Vue.js', 'PostgreSQL', 'ElasticSearch', 'Docker'],
    icon: 'fas fa-laptop-code'
  },
  {
    position: 'Associate Software Engineer',
    company: 'erwin Inc.',
    duration: 'Sept 2019 - April 2022',
    location: 'Hyderabad',
    description: 'Started as Trainee Software Engineer and quickly progressed through learning and delivering quality code. Worked on erwinDI Intelligence platform development, implemented REST APIs, built frontend components, and gained expertise in enterprise data intelligence solutions. Participated in code reviews and agile development processes.',
    technologies: ['Java', 'Spring MVC', 'Vue.js', 'JavaScript', 'SQL', 'Git'],
    icon: 'fas fa-code'
  }
])
</script>
