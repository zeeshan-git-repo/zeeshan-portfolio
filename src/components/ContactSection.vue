<template>
  <section id="contact" class="section-padding bg-white dark:bg-dark-900">
    <div class="max-w-7xl mx-auto">
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-dark-900 dark:text-white mb-4">
          Get In <span class="gradient-text">Touch</span>
        </h2>
        <p class="text-lg text-dark-600 dark:text-dark-300 max-w-2xl mx-auto">
          I'm always interested in hearing about new opportunities and interesting projects. Let's connect!
        </p>
      </div>

      <div class="grid lg:grid-cols-2 gap-12">
        <!-- Contact Information -->
        <div class="space-y-8">
          <div class="card p-8">
            <h3 class="text-2xl font-semibold text-dark-900 dark:text-white mb-6">
              Let's Start a Conversation
            </h3>
            <p class="text-dark-600 dark:text-dark-300 mb-8 leading-relaxed">
              I'm always open to discussing new opportunities, whether it's a full-time position, 
              freelance project, or just a chat about technology. Feel free to reach out through 
              any of the channels below.
            </p>

            <div class="space-y-6">
              <div class="flex items-center space-x-4">
                <div class="w-12 h-12 bg-primary-100 dark:bg-primary-900/30 rounded-lg flex items-center justify-center">
                  <i class="fas fa-envelope text-primary-600"></i>
                </div>
                <div>
                  <h4 class="font-semibold text-dark-900 dark:text-white">Email</h4>
                  <p class="text-dark-600 dark:text-dark-300">azeeshan867@gmail.com</p>
                </div>
              </div>

              <div class="flex items-center space-x-4">
                <div class="w-12 h-12 bg-primary-100 dark:bg-primary-900/30 rounded-lg flex items-center justify-center">
                  <i class="fas fa-phone text-primary-600"></i>
                </div>
                <div>
                  <h4 class="font-semibold text-dark-900 dark:text-white">Phone</h4>
                  <p class="text-dark-600 dark:text-dark-300">9160667207</p>
                </div>
              </div>

              <div class="flex items-center space-x-4">
                <div class="w-12 h-12 bg-primary-100 dark:bg-primary-900/30 rounded-lg flex items-center justify-center">
                  <i class="fas fa-map-marker-alt text-primary-600"></i>
                </div>
                <div>
                  <h4 class="font-semibold text-dark-900 dark:text-white">Location</h4>
                  <p class="text-dark-600 dark:text-dark-300">Hyderabad, India / Remote</p>
                </div>
              </div>
            </div>

            <!-- Social Links -->
            <div class="mt-8 pt-8 border-t border-dark-200 dark:border-dark-700">
              <h4 class="font-semibold text-dark-900 dark:text-white mb-4">Connect with me</h4>
              <div class="flex space-x-4">
                <a href="https://github.com/zeeshan-git-repo" class="w-10 h-10 bg-primary-600 text-white rounded-lg flex items-center justify-center hover:bg-primary-700 transition-colors duration-300">
                  <i class="fab fa-github"></i>
                </a>
                <a href="https://www.linkedin.com/in/zeeshan-ahmad-0637b8188" class="w-10 h-10 bg-primary-600 text-white rounded-lg flex items-center justify-center hover:bg-primary-700 transition-colors duration-300">
                  <i class="fab fa-linkedin"></i>
                </a>                
                <a href="https://mail.google.com/mail/?view=cm&fs=1&to=azeeshan867@gmail.com" target="_blank" class="w-10 h-10 bg-primary-600 text-white rounded-lg flex items-center justify-center hover:bg-primary-700 transition-colors duration-300">
                  <i class="fas fa-envelope"></i>
                </a>
              </div>
            </div>
          </div>

          <!-- Quick Info Cards -->
          <div class="grid grid-cols-2 gap-4">
            <div class="card p-6 text-center">
              <i class="fas fa-clock text-2xl text-primary-600 mb-2"></i>
              <h4 class="font-semibold text-dark-900 dark:text-white">Response Time</h4>
              <p class="text-dark-600 dark:text-dark-300 text-sm">Within 24 hours</p>
            </div>
            <div class="card p-6 text-center">
              <i class="fas fa-handshake text-2xl text-primary-600 mb-2"></i>
              <h4 class="font-semibold text-dark-900 dark:text-white">Availability</h4>
              <p class="text-dark-600 dark:text-dark-300 text-sm">Open to opportunities</p>
            </div>
          </div>
        </div>

        <!-- Contact Form -->
        <div class="card p-8">
          <h3 class="text-2xl font-semibold text-dark-900 dark:text-white mb-6">
            Send me a message
          </h3>
          
          <form action="https://formspree.io/f/xvgpkwpb" method="POST" @submit="handleSubmit" class="space-y-6">
            <div class="grid md:grid-cols-2 gap-6">
              <div>
                <label class="block text-sm font-medium text-dark-700 dark:text-dark-300 mb-2">
                  First Name *
                </label>
                <input v-model="form.firstName" name="firstName" type="text" required
                       class="w-full px-4 py-3 border border-dark-300 dark:border-dark-600 rounded-lg bg-white dark:bg-dark-800 text-dark-900 dark:text-white focus:ring-2 focus:ring-primary-500 focus:border-transparent transition-all duration-300">
              </div>
              <div>
                <label class="block text-sm font-medium text-dark-700 dark:text-dark-300 mb-2">
                  Last Name *
                </label>
                <input v-model="form.lastName" name="lastName" type="text" required
                       class="w-full px-4 py-3 border border-dark-300 dark:border-dark-600 rounded-lg bg-white dark:bg-dark-800 text-dark-900 dark:text-white focus:ring-2 focus:ring-primary-500 focus:border-transparent transition-all duration-300">
              </div>
            </div>

            <div>
              <label class="block text-sm font-medium text-dark-700 dark:text-dark-300 mb-2">
                Email Address *
              </label>
              <input v-model="form.email" name="_replyto" type="email" required
                     class="w-full px-4 py-3 border border-dark-300 dark:border-dark-600 rounded-lg bg-white dark:bg-dark-800 text-dark-900 dark:text-white focus:ring-2 focus:ring-primary-500 focus:border-transparent transition-all duration-300">
            </div>

            <div>
              <label class="block text-sm font-medium text-dark-700 dark:text-dark-300 mb-2">
                Subject *
              </label>
              <input v-model="form.subject" name="subject" type="text" required
                     class="w-full px-4 py-3 border border-dark-300 dark:border-dark-600 rounded-lg bg-white dark:bg-dark-800 text-dark-900 dark:text-white focus:ring-2 focus:ring-primary-500 focus:border-transparent transition-all duration-300">
            </div>

            <div>
              <label class="block text-sm font-medium text-dark-700 dark:text-dark-300 mb-2">
                Message *
              </label>
              <textarea v-model="form.message" name="message" rows="5" required
                        class="w-full px-4 py-3 border border-dark-300 dark:border-dark-600 rounded-lg bg-white dark:bg-dark-800 text-dark-900 dark:text-white focus:ring-2 focus:ring-primary-500 focus:border-transparent transition-all duration-300 resize-none">
              </textarea>
            </div>

            <!-- Hidden Formspree fields -->
            <input type="hidden" name="_subject" value="New Portfolio Contact from Zeeshan Ahmad's Website">
            <input type="text" name="_gotcha" style="display:none">

            <button type="submit" :disabled="isSubmitting"
                    class="w-full btn-primary disabled:opacity-50 disabled:cursor-not-allowed">
              <span v-if="!isSubmitting">
                <i class="fas fa-paper-plane mr-2"></i>
                Send Message
              </span>
              <span v-else>
                <i class="fas fa-spinner fa-spin mr-2"></i>
                Sending...
              </span>
            </button>
          </form>

          <!-- Success Message -->
          <div v-if="showSuccess" class="mt-6 p-4 bg-green-100 dark:bg-green-900/30 border border-green-200 dark:border-green-800 rounded-lg">
            <p class="text-green-800 dark:text-green-200 text-sm">
              <i class="fas fa-check-circle mr-2"></i>
              Thank you for your message! I'll get back to you soon.
            </p>
          </div>

          <!-- Error Message -->
          <div v-if="showError" class="mt-6 p-4 bg-red-100 dark:bg-red-900/30 border border-red-200 dark:border-red-800 rounded-lg">
            <p class="text-red-800 dark:text-red-200 text-sm">
              <i class="fas fa-exclamation-circle mr-2"></i>
              {{ errorMessage }}
            </p>
          </div>

          <!-- Alternative Contact Methods -->
          <div class="mt-8 pt-6 border-t border-dark-200 dark:border-dark-700">
            <p class="text-sm text-dark-600 dark:text-dark-400 text-center">
              Having trouble with the form? 
              <a href="mailto:azeeshan867@gmail.com?subject=Portfolio Contact&body=Hello Zeeshan," 
                 class="text-primary-600 hover:text-primary-700 font-medium">
                Email me directly
              </a>
              or call <a href="tel:+919160667207" class="text-primary-600 hover:text-primary-700 font-medium">+91 9160667207</a>
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const form = ref({
  firstName: '',
  lastName: '',
  email: '',
  subject: '',
  message: ''
})

const isSubmitting = ref(false)
const showSuccess = ref(false)
const showError = ref(false)
const errorMessage = ref('')

const handleSubmit = (event: Event) => {
  isSubmitting.value = true
  showError.value = false
  showSuccess.value = false
  
  // Allow the form to submit to Formspree
  // Show user feedback
  setTimeout(() => {
    isSubmitting.value = false
    showSuccess.value = true
    
    // Reset form after successful submission
    form.value = {
      firstName: '',
      lastName: '',
      email: '',
      subject: '',
      message: ''
    }
    
    // Hide success message after 5 seconds
    setTimeout(() => {
      showSuccess.value = false
    }, 5000)
  }, 2000)
}
</script>
