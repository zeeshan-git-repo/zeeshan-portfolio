<template>
  <section id="about" class="section-padding bg-white dark:bg-dark-900">
    <div class="max-w-7xl mx-auto">
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-4xl font-bold text-dark-900 dark:text-white mb-4">
          About <span class="gradient-text">Me</span>
        </h2>
        <p class="text-lg text-dark-600 dark:text-dark-300 max-w-2xl mx-auto">
          Passionate software developer with a strong foundation in full-stack development and cloud technologies
        </p>
      </div>

      <div class="grid lg:grid-cols-2 gap-12 items-center">
        <!-- About Content -->
        <div class="space-y-6">
          <div class="card p-8">
            <h3 class="text-2xl font-semibold text-dark-900 dark:text-white mb-4">
              <i class="fas fa-user-graduate text-primary-600 mr-3"></i>
              Background
            </h3>
            <p class="text-dark-600 dark:text-dark-300 leading-relaxed mb-4">
              I'm Zeeshan Ahmad, a dedicated software developer with <strong>6+ years</strong> of professional experience
              in building scalable web applications and data intelligence solutions. I hold a <strong>BTech in Computer Science Engineering</strong> 
              from <strong>Maulana Azad National Urdu University, Hyderabad (2019)</strong> and have a passion for creating efficient, maintainable code.
            </p>
            <p class="text-dark-600 dark:text-dark-300 leading-relaxed">
              Currently working as a <strong>Software Dev Staff Engineer</strong> at <strong>Quest Software</strong> on erwin Data Intelligence, 
              a powerful data intelligence platform. I've grown through the ranks from Trainee Software Engineer to Software Development Engineer, 
              and now Software Dev Staff Engineer, demonstrating consistent technical excellence and leadership. My expertise spans across backend development 
              with Java and Spring ecosystem, frontend development with Vue.js, and cloud deployment using AWS and Docker. 
              I thrive in collaborative environments and enjoy solving complex problems.
            </p>
          </div>

          <div class="card p-8">
            <h3 class="text-2xl font-semibold text-dark-900 dark:text-white mb-4">
              <i class="fas fa-rocket text-primary-600 mr-3"></i>
              What I Do
            </h3>
            <div class="grid sm:grid-cols-2 gap-4">
              <div class="flex items-center space-x-3">
                <i class="fas fa-check-circle text-green-500"></i>
                <span class="text-dark-600 dark:text-dark-300">Full-Stack Development</span>
              </div>
              <div class="flex items-center space-x-3">
                <i class="fas fa-check-circle text-green-500"></i>
                <span class="text-dark-600 dark:text-dark-300">Microservices Architecture</span>
              </div>
              <div class="flex items-center space-x-3">
                <i class="fas fa-check-circle text-green-500"></i>
                <span class="text-dark-600 dark:text-dark-300">Cloud Deployment</span>
              </div>
              <div class="flex items-center space-x-3">
                <i class="fas fa-check-circle text-green-500"></i>
                <span class="text-dark-600 dark:text-dark-300">API Development</span>
              </div>
              <div class="flex items-center space-x-3">
                <i class="fas fa-check-circle text-green-500"></i>
                <span class="text-dark-600 dark:text-dark-300">Database Design</span>
              </div>
              <div class="flex items-center space-x-3">
                <i class="fas fa-check-circle text-green-500"></i>
                <span class="text-dark-600 dark:text-dark-300">DevOps & CI/CD</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Statistics -->
        <div class="space-y-6">
          <div class="grid grid-cols-2 gap-6">
            <div class="card p-6 text-center">
              <div class="text-3xl font-bold text-primary-600 mb-2">5+</div>
              <div class="text-dark-600 dark:text-dark-300">Years Experience</div>
            </div>            
            <div class="card p-6 text-center">
              <div class="text-3xl font-bold text-primary-600 mb-2">15+</div>
              <div class="text-dark-600 dark:text-dark-300">Technologies</div>
            </div>
            <div class="card p-6 text-center">
              <div class="text-3xl font-bold text-primary-600 mb-2">10+</div>
              <div class="text-dark-600 dark:text-dark-300">Certifications</div>
            </div>
            <div class="card p-6 text-center">
              <div class="text-3xl font-bold text-primary-600 mb-2">10+</div>
              <div class="text-dark-600 dark:text-dark-300">Projects</div>
            </div>
          </div>

          <!-- Education -->
          <div class="card p-8">
            <h3 class="text-2xl font-semibold text-dark-900 dark:text-white mb-6">
              <i class="fas fa-graduation-cap text-primary-600 mr-3"></i>
              Education
            </h3>
            <div class="border-l-4 border-primary-600 pl-6">
              <h4 class="text-lg font-semibold text-dark-900 dark:text-white">
                Bachelor of Technology - Computer Science Engineering
              </h4>
              <p class="text-primary-600 font-medium mt-1">
                Maulana Azad National Urdu University, Hyderabad
              </p>
              <p class="text-dark-500 dark:text-dark-400 text-sm mt-1">
                Graduated 2019
              </p>
              <p class="text-dark-600 dark:text-dark-300 mt-2">
                Graduated with strong fundamentals in computer science, algorithms, and software engineering principles.
              </p>
            </div>
          </div>

          <!-- Current Focus -->
          <div class="card p-8">
            <h3 class="text-2xl font-semibold text-dark-900 dark:text-white mb-4">
              <i class="fas fa-target text-primary-600 mr-3"></i>
              Current Focus
            </h3>
            <div class="space-y-3">
              <div class="flex items-center space-x-3">
                <i class="fas fa-arrow-right text-primary-600"></i>
                <span class="text-dark-600 dark:text-dark-300">Cloud-Native Applications</span>
              </div>
              <div class="flex items-center space-x-3">
                <i class="fas fa-arrow-right text-primary-600"></i>
                <span class="text-dark-600 dark:text-dark-300">Serverless Architecture</span>
              </div>
              <div class="flex items-center space-x-3">
                <i class="fas fa-arrow-right text-primary-600"></i>
                <span class="text-dark-600 dark:text-dark-300">Container Orchestration</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
// About section component
</script>
