<script>
  import { Link } from "svelte-routing";
  import TextReveal from "../components/TextReveal.svelte";
  import { copyToClipboard } from "../helper";
  import { onMount } from "svelte";

  export let theme;

  $: welcomeMessage =
    theme === "dark" ? 'print("Hey!👋")' : 'print("Hi!🙋‍♂️")';
</script>

<section
  id="home"
  class="relative main bg-gray-100 h-screen flex bg-gradient-to-b dark:from-gray-700 dark:to-gray-900"
>
  <div
    data-aos="slide-down"
    data-aos-delay="700"
    data-aos-duration="700"
    class="absolute top-0 right-0 h-1/2 w-full md:w-1/3 md:h-full moving-gradient-1"
  />

  <section
    data-aos="fade-in"
    data-aos-delay="600"
    class="m-auto pt-5 relative grow max-w-5xl"
  >
    <div
      class="bg-white dark:bg-gray-900 px-5 py-10 lg:py-14 lg:px-10 shadow-2xl"
    >
      <div
        data-aos="flip-up"
        data-aos-delay="600"
        data-aos-duration="700"
        class="bg-purple-400 dark:bg-purple-300 shadow-purple-300/60 shadow-lg w-8 h-1.5 lg:w-10 lg:h-2 ml-0.5 mb-6"
      />
      <h1
        class="mb-3 md:mb-6 font-mono font-black text-2xl md:text-3xl lg:text-5xl text-gray-700 dark:text-white"
      >
        <TextReveal delay={800} once text={welcomeMessage} />
      </h1>
      <p
        class="text-lg md:text-xl lg:text-xl mb-8 font-bold text-gray-500 dark:text-gray-400 ml-1"
      >
        <TextReveal
          delay={1000}
          once
          text="I build and design industry standard web apps. Welcome to my website."
        />
      </p>

      <div
        data-aos="fade-left"
        data-aos-delay="1200"
        data-aos-duration="700"
        class="text-sm text-gray-700 font-semibold font-mono"
      >
        <Link
          to="/resume"
          data-aos="zoom-in"
          data-aos-delay="700"
          class="transition-colors px-4 py-1 mr-3 lg:ml-1 inline-block bg-green-200 shadow-green-300/20 shadow-lg border rounded-sm border-green-400 hover:bg-green-300"
          data-aos-duration="700">View Resume</Link
        >
        <a
          href="#contact"
          class="transition-colors px-4 py-1 inline-block bg-blue-200 shadow-blue-300/20 shadow-lg hover:bg-blue-300 rounded-sm border border-blue-400"
          >Let's talk</a
        >
      </div>
    </div>
  </section>

  <div
    data-aos="slide-up"
    data-aos-delay="1500"
    data-aos-duration="700"
    class="hidden text-xl absolute lg:flex flex-col gap-4 items-center w-4 left-14 bottom-0 text-center text-gray-700 dark:text-gray-50"
  >
    <a
      title="See my GitHub profile"
      aria-label="See my GitHub profile"
      href="https://github.com/PurtucRobert"
      target="_blank"
      class="block"><i class="fab fa-github" /></a
    >
    <a
      title="Connect on LinkedIn"
      aria-label="Connect on LinkedIn"
      href="https://www.linkedin.com/in/purtuc-robert/"
      target="_blank"
      class="block"
    >
      <i class="fab fa-linkedin-in" /></a
    >
    <a
      title="Send me an email"
      aria-label="Send me an email"
      href="mailto:purtuc.robert@gmail.com"
      target="_blank"
      class="block"
    >
      <i class="far fa-envelope" />
    </a>
    <div class="shadow-xl w-4 h-28 bg-gray-700 dark:bg-gray-50" />
  </div>

  <button
    title="Go to about me"
    aria-label="Go to about me"
    data-aos="fade-down"
    data-aos-delay="1500"
    data-aos-duration="700"
    on:click={() => document.getElementById("about").scrollIntoView()}
    class="group text-xl lg:text-3xl py-5 text-gray-700 dark:text-white absolute w-14 mx-auto text-center bottom-20 right-0 left-0"
  >
    <i class="hover-vertical fas fa-angle-down group-hover:pause" />
  </button>
</section>
