<template>
  <nav class="fixed top-0 w-full z-50 bg-white/80 dark:bg-dark-900/80 backdrop-blur-md border-b border-dark-200 dark:border-dark-700">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center h-16">
        <!-- Logo -->
        <div class="flex-shrink-0">
          <h1 class="text-2xl font-bold gradient-text">Portfolio</h1>
        </div>

        <!-- Desktop Navigation -->
        <div class="hidden md:block">
          <div class="ml-10 flex items-baseline space-x-8">
            <a v-for="item in navigation" 
               :key="item.name"
               :href="item.href"
               class="text-dark-600 dark:text-dark-300 hover:text-primary-600 dark:hover:text-primary-400 px-3 py-2 text-sm font-medium transition-colors duration-300"
               @click="scrollTo(item.href)">
              {{ item.name }}
            </a>
            <a href="/Zeeshan Java Developer Resume.pdf" download="Zeeshan Java Developer Resume.pdf" class="btn-primary text-xs px-4 py-2">
              <i class="fas fa-download mr-1"></i>
              Resume
            </a>
          </div>
        </div>

        <!-- Theme Toggle & Mobile Menu Button -->
        <div class="flex items-center space-x-4">
          <button @click="toggleTheme" 
                  class="p-2 rounded-lg bg-dark-100 dark:bg-dark-800 text-dark-600 dark:text-dark-300 hover:text-primary-600 transition-colors duration-300">
            <i :class="isDark ? 'fas fa-sun' : 'fas fa-moon'"></i>
          </button>
          
          <button @click="mobileMenuOpen = !mobileMenuOpen"
                  class="md:hidden p-2 rounded-lg bg-dark-100 dark:bg-dark-800 text-dark-600 dark:text-dark-300">
            <i :class="mobileMenuOpen ? 'fas fa-times' : 'fas fa-bars'"></i>
          </button>
        </div>
      </div>

      <!-- Mobile Navigation -->
      <div v-show="mobileMenuOpen" class="md:hidden">
        <div class="px-2 pt-2 pb-3 space-y-1 bg-white dark:bg-dark-900 border-t border-dark-200 dark:border-dark-700">
          <a v-for="item in navigation" 
             :key="item.name"
             :href="item.href"
             class="block px-3 py-2 text-base font-medium text-dark-600 dark:text-dark-300 hover:text-primary-600 dark:hover:text-primary-400 transition-colors duration-300"
             @click="scrollTo(item.href); mobileMenuOpen = false">
            {{ item.name }}
          </a>
          <a href="/Zeeshan Java Developer Resume.pdf" download="Zeeshan Java Developer Resume.pdf" 
             class="block px-3 py-2 text-base font-medium text-primary-600 dark:text-primary-400 border-t border-dark-200 dark:border-dark-700"
             @click="mobileMenuOpen = false">
            <i class="fas fa-download mr-2"></i>
            Download Resume
          </a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'

const mobileMenuOpen = ref(false)
const isDark = ref(false)

const navigation = [
  { name: 'Home', href: '#home' },
  { name: 'About', href: '#about' },
  { name: 'Skills', href: '#skills' },
  { name: 'Experience', href: '#experience' },
  { name: 'Projects', href: '#projects' },
  { name: 'Contact', href: '#contact' },
]

const toggleTheme = () => {
  isDark.value = !isDark.value
  document.documentElement.classList.toggle('dark')
  localStorage.setItem('theme', isDark.value ? 'dark' : 'light')
}

const scrollTo = (elementId: string) => {
  const element = document.querySelector(elementId)
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
}

onMounted(() => {
  const savedTheme = localStorage.getItem('theme')
  if (savedTheme === 'dark' || (!savedTheme && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
    isDark.value = true
    document.documentElement.classList.add('dark')
  }
})
</script>
