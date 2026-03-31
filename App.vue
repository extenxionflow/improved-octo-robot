<template>
  <div>
    <nav>
      <h1>Articwolfglobal's Portfolio</h1>
      <ul>
        <li><a href="#hero">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>

    <section id="hero">
      <h2>Welcome to My Portfolio</h2>
      <p>Creative solutions for modern challenges.</p>
    </section>

    <section id="about">
      <h2>About Me</h2>
      <p>Information about Articwolfglobal.</p>
    </section>

    <section id="projects">
      <h2>Projects</h2>
      <p>Showcasing my work</p>
    </section>

    <section id="skills">
      <h2>Skills</h2>
      <p>A list of my skills.</p>
    </section>

    <section id="contact">
      <h2>Contact Me</h2>
      <p>Get in touch!</p>
    </section>
  </div>
</template>

<script>
export default {
  name: 'App',
};
</script>

<style>
nav {
  background: #333;
  color: #fff;
  padding: 1em;
}
nav ul {
  list-style-type: none;
  padding: 0;
}
nav li {
  display: inline;
  margin-right: 10px;
}
section {
  padding: 20px;
}
</style>