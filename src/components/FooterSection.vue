<template>
  <footer class="bg-dark-900 text-white py-12">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid md:grid-cols-3 gap-8">
        <!-- Brand Section -->
        <div>
          <h3 class="text-2xl font-bold gradient-text mb-4">Zeeshan Ahmad</h3>
          <p class="text-dark-300 mb-6 leading-relaxed">
            Software Dev Staff Engineer at Quest Software specializing in data intelligence solutions, 
            technical leadership, and enterprise-grade software architecture.
          </p>
          <div class="flex space-x-4">
            <a href="https://github.com/zeeshan-git-repo" class="w-10 h-10 bg-primary-600 rounded-lg flex items-center justify-center hover:bg-primary-700 transition-colors duration-300">
              <i class="fab fa-github"></i>
            </a>
            <a href="https://www.linkedin.com/in/zeeshan-ahmad-0637b8188" class="w-10 h-10 bg-primary-600 rounded-lg flex items-center justify-center hover:bg-primary-700 transition-colors duration-300">
              <i class="fab fa-linkedin"></i>
            </a>            
            <a href="https://mail.google.com/mail/?view=cm&fs=1&to=azeeshan867@gmail.com" target="_blank"  class="w-10 h-10 bg-primary-600 rounded-lg flex items-center justify-center hover:bg-primary-700 transition-colors duration-300">
              <i class="fas fa-envelope"></i>
            </a>
          </div>
        </div>

        <!-- Quick Links -->
        <div>
          <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
          <ul class="space-y-3">
            <li>
              <a href="#home" @click="scrollTo('#home')" class="text-dark-300 hover:text-primary-400 transition-colors duration-300">
                Home
              </a>
            </li>
            <li>
              <a href="#about" @click="scrollTo('#about')" class="text-dark-300 hover:text-primary-400 transition-colors duration-300">
                About
              </a>
            </li>
            <li>
              <a href="#skills" @click="scrollTo('#skills')" class="text-dark-300 hover:text-primary-400 transition-colors duration-300">
                Skills
              </a>
            </li>
            <li>
              <a href="#experience" @click="scrollTo('#experience')" class="text-dark-300 hover:text-primary-400 transition-colors duration-300">
                Experience
              </a>
            </li>
            <li>
              <a href="#projects" @click="scrollTo('#projects')" class="text-dark-300 hover:text-primary-400 transition-colors duration-300">
                Projects
              </a>
            </li>
            <li>
              <a href="#contact" @click="scrollTo('#contact')" class="text-dark-300 hover:text-primary-400 transition-colors duration-300">
                Contact
              </a>
            </li>
          </ul>
        </div>

        <!-- Contact Info -->
        <div>
          <h4 class="text-lg font-semibold mb-4">Get in Touch</h4>
          <div class="space-y-3">
            <div class="flex items-center space-x-3">
              <i class="fas fa-envelope text-primary-400"></i>
              <span class="text-dark-300">azeeshan867@gmail.com</span>
            </div>
            <div class="flex items-center space-x-3">
              <i class="fas fa-phone text-primary-400"></i>
              <span class="text-dark-300">9160667207</span>
            </div>
            <div class="flex items-center space-x-3">
              <i class="fas fa-map-marker-alt text-primary-400"></i>
              <span class="text-dark-300">Hyderabad, India / Remote</span>
            </div>
          </div>

          <!-- Resume Download -->
          <div class="mt-6">
            <a href="/Zeeshan Java Developer Resume.pdf" download="Zeeshan Java Developer Resume.pdf" class="inline-flex items-center px-6 py-3 bg-primary-600 hover:bg-primary-700 text-white font-medium rounded-lg transition-all duration-300 shadow-lg hover:shadow-xl">
              <i class="fas fa-download mr-2"></i>
              Download Resume
            </a>
          </div>
        </div>
      </div>

      <!-- Bottom Section -->
      <div class="border-t border-dark-700 mt-12 pt-8">
        <div class="flex flex-col md:flex-row justify-between items-center">
          <p class="text-dark-400 text-sm">
            © {{ currentYear }} Zeeshan Ahmad. Built with ❤️ using Vue.js and Tailwind CSS.
          </p>
          <div class="flex items-center space-x-6 mt-4 md:mt-0">
            <span class="text-dark-400 text-sm">Made with</span>
            <div class="flex space-x-4">
              <div class="flex items-center space-x-2">
                <i class="fab fa-vuejs text-green-400"></i>
                <span class="text-dark-400 text-sm">Vue.js</span>
              </div>
              <div class="flex items-center space-x-2">
                <i class="fas fa-paint-brush text-blue-400"></i>
                <span class="text-dark-400 text-sm">Tailwind CSS</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
import { computed } from 'vue'

const currentYear = computed(() => new Date().getFullYear())

const scrollTo = (elementId: string) => {
  const element = document.querySelector(elementId)
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
}
</script>
