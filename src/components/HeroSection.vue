<template>
  <section id="home" class="min-h-screen flex items-center justify-center bg-gradient-to-br from-primary-50 to-purple-50 dark:from-dark-900 dark:to-dark-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20">
      <div class="text-center">
        <!-- Profile Image -->
        <div class="mb-8 animate-fade-in">
          <div class="w-48 h-48 mx-auto rounded-full bg-gradient-to-r from-primary-500 to-purple-500 p-1">
            <div class="w-full h-full rounded-full bg-white dark:bg-dark-800 flex items-center justify-center">
              <i class="fas fa-user text-6xl text-primary-600"></i>
            </div>
          </div>
        </div>

        <!-- Introduction -->
        <div class="animate-slide-up">
          <h1 class="text-4xl md:text-6xl font-bold text-dark-900 dark:text-white mb-4">
            Hi, I'm <span class="gradient-text">Zeeshan Ahmad</span>
          </h1>
          <p class="text-xl md:text-2xl text-dark-600 dark:text-dark-300 mb-6 max-w-3xl mx-auto">
            Passionate Full-Stack Developer with 6+ years of experience in Java, Spring Boot, Vue.js, and Cloud Technologies
          </p>
          <p class="text-lg text-dark-500 dark:text-dark-400 mb-8">
            BTech CSE Graduate from MANUU Hyderabad | Software Dev Staff Engineer at Quest Software
          </p>
        </div>

        <!-- CTA Buttons -->
        <div class="flex flex-col sm:flex-row gap-4 justify-center animate-fade-in">
          <a href="/Zeeshan Java Developer Resume.pdf" download="Zeeshan Java Developer Resume.pdf" class="btn-primary">
            <i class="fas fa-download mr-2"></i>
            Download Resume
          </a>
          <button @click="scrollTo('#projects')" class="btn-secondary">
            <i class="fas fa-code mr-2"></i>
            View My Work
          </button>
          <button @click="scrollTo('#contact')" class="btn-secondary">
            <i class="fas fa-envelope mr-2"></i>
            Get In Touch
          </button>
        </div>

        <!-- Social Links -->
        <div class="mt-12 flex justify-center space-x-6 animate-fade-in">
          <a href="https://github.com/zeeshan-git-repo" class="text-2xl text-dark-400 hover:text-primary-600 transition-colors duration-300">
            <i class="fab fa-github"></i>
          </a>
          <a href="https://www.linkedin.com/in/zeeshan-ahmad-0637b8188" class="text-2xl text-dark-400 hover:text-primary-600 transition-colors duration-300">
            <i class="fab fa-linkedin"></i>
          </a>
          <a href="https://mail.google.com/mail/?view=cm&fs=1&to=azeeshan867@gmail.com" target="_blank" class="text-2xl text-dark-400 hover:text-primary-600 transition-colors duration-300">
            <i class="fas fa-envelope"></i>
          </a>
        </div>

        <!-- Scroll Indicator -->
        <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce-slow">
          <i class="fas fa-chevron-down text-2xl text-dark-400"></i>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const scrollTo = (elementId: string) => {
  const element = document.querySelector(elementId)
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
}
</script>
