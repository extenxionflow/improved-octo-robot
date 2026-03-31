<template>
  <div class="projects">
    <transition-group name="fade" tag="div">
      <div v-for="(project, index) in projects" :key="project.id" class="project-card" v-bind:style="{ transitionDelay: (index * 0.1) + 's' }">
        <h3>{{ project.title }}</h3>
        <p>{{ project.description }}</p>
        <p><strong>Tech Stack:</strong> {{ project.techStack.join(', ') }}</p>
        <a v-for="(link, i) in project.links" :key="i" :href="link" target="_blank">Link {{ i + 1 }}</a>
      </div>
    </transition-group>
  </div>
</template>

<script>
export default {
  name: 'Projects',
  data() {
    return {
      projects: [
        {
          id: 1,
          title: 'Project One',
          description: 'Description for project one.',
          techStack: ['Vue', 'CSS', 'HTML'],
          links: ['<template>
  <div class="skills-container">
    <div class="skills-grid">
      <transition-group name="fade" tag="div" class="skills-list">
        <div v-for="(skill, index) in skills" :key="skill.id" class="skill-badge" :style="{ transitionDelay: (index * 0.1) + 's' }">
          <div class="skill-icon">{{ skill.icon }}</div>
          <h3>{{ skill.name }}</h3>
          <p>{{ skill.description }}</p>
          <div class="skill-level">
            <div class="progress-bar" :style="{ width: skill.level + '%' }"></div>
          </div>
          <span class="level-text">{{ skill.level }}%</span>
        </div>
      </transition-group>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data() {
    return {
      skills: [
        { id: 1, name: 'Vue.js', description: 'Frontend Framework', icon: '⚡', level: 95 },
        { id: 2, name: 'React', description: 'UI Library', icon: '⚛️', level: 85 },
        { id: 3, name: 'JavaScript', description: 'Programming Language', icon: '✨', level: 90 },
        { id: 4, name: 'CSS/SCSS', description: 'Styling', icon: '🎨', level: 88 },
        { id: 5, name: 'Node.js', description: 'Backend Runtime', icon: '🟢', level: 80 },
        { id: 6, name: 'Tailwind CSS', description: 'Utility Framework', icon: '🌊', level: 92 }
      ]
    }
  }
}
</script>

<style scoped>
.skills-container {
  width: 100%;
  padding: 2em 0;
}

.skills-grid {
  max-width: 1200px;
  margin: 0 auto;
}

.skills-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2em;
  padding: 0 2em;
}

.skill-badge {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 2em;
  border-radius: 10px;
  text-align: center;
  box-shadow: 0 4px 15px rgba(102, 126, 234, 0.3);
  transition: all 0.3s ease;
  cursor: pointer;
  animation: slideUp 0.6s ease-out both;
}

.skill-badge:hover {
  transform: translateY(-10px);
  box-shadow: 0 8px 25px rgba(102, 126, 234, 0.5);
}

.skill-icon {
  font-size: 3em;
  margin-bottom: 0.5em;
  animation: bounce 0.6s ease-out;
}

.skill-badge h3 {
  font-size: 1.5em;
  margin-bottom: 0.5em;
}

.skill-badge p {
  font-size: 0.9em;
  opacity: 0.9;
  margin-bottom: 1em;
}

.skill-level {
  background-color: rgba(255, 255, 255, 0.2);
  height: 8px;
  border-radius: 10px;
  overflow: hidden;
  margin-bottom: 0.5em;
}

.progress-bar {
  background-color: rgba(255, 255, 255, 0.9);
  height: 100%;
  border-radius: 10px;
  transition: width 1s ease-out;
  animation: growWidth 1s ease-out;
}

.level-text {
  font-size: 0.9em;
  font-weight: bold;
  display: block;
  margin-top: 0.5em;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}

.fade-enter, .fade-leave-to {
  opacity: 0;
}

@keyframes slideUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes bounce {
  0%, 100% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.2);
  }
}

@keyframes growWidth {
  from {
    width: 0;
  }
}

@media (max-width: 768px) {
  .skills-list {
    grid-template-columns: 1fr;
    padding: 0 1em;
  }

  .skill-badge {
    padding: 1.5em;
  }

  .skill-icon {
    font-size: 2.5em;
  }
}
</style>']
        },
        {
          id: 2,
          title: 'Project Two',
          description: 'Description for project two.',
          techStack: ['React', 'JavaScript'],
          links: ['https://example.com/project-two']
        },
        {
          id: 3,
          title: 'Project Three',
          description: 'Description for project three.',
          techStack: ['Angular', 'TypeScript'],
          links: ['https://example.com/project-three']
        },
        {
          id: 4,
          title: 'Project Four',
          description: 'Description for project four.',
          techStack: ['Node.js', 'Express'],
          links: ['https://example.com/project-four']
        },
        {
          id: 5,
          title: 'Project Five',
          description: 'Description for project five.',
          techStack: ['Python', 'Django'],
          links: ['https://example.com/project-five']
        },
      ]
    }
  }
}
</script>

<style scoped>
.projects {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.project-card {
  width: 200px;
  border: 1px solid #ccc;
  margin: 10px;
  padding: 10px;
  border-radius: 5px;
  transition: transform 0.2s;
}

.project-card:hover {
  transform: scale(1.05);
}

.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>