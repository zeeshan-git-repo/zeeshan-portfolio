<template>
  <section id="projects" class="section-padding bg-dark-50 dark:bg-dark-800">
    <div class="max-w-7xl mx-auto">
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-dark-900 dark:text-white mb-4">
          Featured <span class="gradient-text">Projects</span>
        </h2>
        <p class="text-lg text-dark-600 dark:text-dark-300 max-w-2xl mx-auto">
          A showcase of my recent work and projects that demonstrate my technical skills and problem-solving abilities
        </p>
      </div>

      <!-- Project Grid -->
      <div class="grid lg:grid-cols-2 gap-8 mb-12">
        <div v-for="project in projects" :key="project.id" 
             class="card overflow-hidden hover:shadow-2xl transition-all duration-500 transform hover:-translate-y-2">
          
          <!-- Project Image -->
          <div class="relative h-48 bg-gradient-to-br from-primary-500 to-purple-600 overflow-hidden">
            <div class="absolute inset-0 flex items-center justify-center">
              <i :class="project.icon" class="text-6xl text-white opacity-30"></i>
            </div>
            <div class="absolute top-4 right-4">
              <span class="px-3 py-1 bg-white/20 backdrop-blur-sm text-white text-xs rounded-full">
                {{ project.type }}
              </span>
            </div>
          </div>

          <!-- Project Content -->
          <div class="p-6">
            <h3 class="text-xl font-semibold text-dark-900 dark:text-white mb-3">
              {{ project.title }}
            </h3>
            <p class="text-dark-600 dark:text-dark-300 mb-4 leading-relaxed">
              {{ project.description }}
            </p>

            <!-- Technologies -->
            <div class="flex flex-wrap gap-2 mb-6">
              <span v-for="tech in project.technologies" :key="tech"
                    class="px-3 py-1 bg-primary-100 dark:bg-primary-900/30 text-primary-700 dark:text-primary-300 text-xs rounded-full">
                {{ tech }}
              </span>
            </div>

            <!-- Features -->
            <div class="mb-6">
              <h4 class="text-sm font-semibold text-dark-900 dark:text-white mb-2">Key Features:</h4>
              <ul class="space-y-1">
                <li v-for="feature in project.features" :key="feature" 
                    class="text-sm text-dark-600 dark:text-dark-300 flex items-start">
                  <i class="fas fa-check text-green-500 mr-2 mt-1 text-xs"></i>
                  {{ feature }}
                </li>
              </ul>
            </div>

            <!-- Project Links -->
           <!-- <div class="flex space-x-4">
              <a href="#" class="flex items-center text-primary-600 hover:text-primary-700 font-medium text-sm transition-colors duration-300">
                <i class="fab fa-github mr-2"></i>
                View Code
              </a>
              <a href="#" class="flex items-center text-primary-600 hover:text-primary-700 font-medium text-sm transition-colors duration-300">
                <i class="fas fa-external-link-alt mr-2"></i>
                Live Demo
              </a>
            </div> -->
          </div>
        </div>
      </div>

      <!-- Additional Projects -->
      <div class="text-center">
        <h3 class="text-2xl font-semibold text-dark-900 dark:text-white mb-8">Other Notable Projects</h3>
        <div class="grid md:grid-cols-3 gap-6">
          <div v-for="project in additionalProjects" :key="project.id" 
               class="card p-6 hover:shadow-lg transition-all duration-300">
            <div class="text-center mb-4">
              <div class="w-12 h-12 mx-auto bg-primary-100 dark:bg-primary-900/30 rounded-lg flex items-center justify-center mb-3">
                <i :class="project.icon" class="text-primary-600 text-xl"></i>
              </div>
              <h4 class="text-lg font-semibold text-dark-900 dark:text-white">{{ project.title }}</h4>
            </div>
            <p class="text-dark-600 dark:text-dark-300 text-sm mb-4">{{ project.description }}</p>
            <div class="flex flex-wrap gap-1 justify-center">
              <span v-for="tech in project.technologies" :key="tech"
                    class="px-2 py-1 bg-dark-100 dark:bg-dark-700 text-dark-600 dark:text-dark-400 text-xs rounded">
                {{ tech }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const projects = ref([
  {
    id: 1,
    title: 'erwinDI Intelligence Platform',
    type: 'Enterprise Data Intelligence',
    description: 'A comprehensive data intelligence platform for enterprise data discovery, lineage tracking, and metadata management. Leading development of core features including data cataloging, automated discovery, and real-time lineage visualization.',
    icon: 'fas fa-database',
    technologies: ['Java', 'Spring Boot', 'Vue.js', 'PostgreSQL', 'ElasticSearch', 'AWS', 'Docker'],
    features: [
      'Automated data discovery and cataloging',
      'Real-time data lineage tracking and visualization',
      'Enterprise metadata management',
      'Advanced search and filtering capabilities',
      'Role-based access control and governance'
    ]
  },
  {
    id: 2,
    title: 'Microservices Data Processing Pipeline',
    type: 'Backend Architecture',
    description: 'Scalable microservices architecture for processing large volumes of enterprise data. Implemented event-driven architecture with message queues for real-time data processing and transformation.',
    icon: 'fas fa-cogs',
    technologies: ['Java', 'Spring Boot', 'Apache Kafka', 'Redis', 'Docker', 'Kubernetes'],
    features: [
      'Event-driven microservices architecture',
      'Real-time data stream processing',
      'Horizontal scaling and load balancing',
      'Circuit breaker and fault tolerance',
      'Comprehensive monitoring and logging'
    ]
  },
  {
    id: 3,
    title: 'API Gateway & Security Layer',
    type: 'Backend Infrastructure',
    description: 'Comprehensive API Gateway solution with authentication, authorization, rate limiting, and monitoring for enterprise microservices ecosystem.',
    icon: 'fas fa-shield-alt',
    technologies: ['Java', 'Spring Cloud Gateway', 'OAuth2', 'JWT', 'Redis', 'Prometheus'],
    features: [
      'Centralized authentication and authorization',
      'Rate limiting and throttling',
      'Request/response transformation',
      'API monitoring and analytics',
      'Load balancing and failover'
    ]
  }
])

const additionalProjects = ref([
  {
    id: 4,
    title: 'Data Lineage Tracker',
    description: 'Advanced data lineage tracking system for enterprise data governance and compliance.',
    icon: 'fas fa-project-diagram',
    technologies: ['Java', 'quasar', 'Vue.js']
  },
  {
    id: 5,
    title: 'Metadata Management API',
    description: 'RESTful API for enterprise metadata management with versioning and change tracking.',
    icon: 'fas fa-code-branch',
    technologies: ['Spring Boot', 'SQLSERVER', 'Swagger', 'Docker']
  },
  {
    id: 6,
    title: 'Real-time Monitoring Dashboard',
    description: 'System monitoring dashboard with real-time metrics and alerting capabilities.',
    icon: 'fas fa-tachometer-alt',
    technologies: ['Vue.js', 'WebSocket', 'Chart.js', 'Redis']
  }
])
</script>
