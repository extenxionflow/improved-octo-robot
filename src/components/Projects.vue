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
          links: ['https://example.com/project-one']
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