<script>
  import Hero from "./Hero.svelte";
  import About from "./About.svelte";
  import Experience from "./Experience.svelte";
  import Contact from "./Contact.svelte";

  export let theme;
</script>

<main class="snap-y">
  <Hero bind:theme />
  <About />
  <Experience />
  <Contact />
</main>
