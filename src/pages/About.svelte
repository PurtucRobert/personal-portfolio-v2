<script>
  import SectionNumber from "../components/SectionNumber.svelte";
  import TextReveal from "../components/TextReveal.svelte";
</script>

<section
  id="about"
  class="overflow-hidden snap-center relative bg-gray-50 bg-gradient-to-b dark:from-gray-800 dark:to-gray-700"
>
  <div
    data-aos="slide-right"
    data-aos-offset="100"
    data-aos-duration="700"
    class="absolute background left-0 w-1/3 lg:w-1/4 h-full moving-gradient-2"
  />

  <SectionNumber
    number="001"
    shaftClasses="bg-gray-100 dark:bg-gray-800"
    textClasses="text-gray-100 dark:text-gray-800"
  />

  <section class="main mb-40 mt-40 lg:mt-64">
    <div
      class="flex flex-col items-center gap-32 lg:gap-20 lg:flex-row justify-center"
    >
      <div class="max-w-xs z-10 flex-1">
        <div
          class="bg-gray-50 dark:bg-gray-300 shadow-2xl overflow-hidden p-3 rounded-sm"
        >
          <img
            loading="lazy"
            data-aos="slide-right"
            data-aos-duration="500"
            data-aos-delay="200"
            src="/images/me.webp"
            alt="A guy (me) posing nearby Corvin Castle in Romania"
          />
        </div>
      </div>

      <div
        class="flex-1 max-w-prose relative bg-white dark:bg-gray-900 px-6 py-6 lg:py-10 lg:px-10 shadow-2xl"
      >
        <div
          class="absolute right-0 -top-20 lg:-top-32 lg:text-right tracking-wide text-5xl md:text-6xl lg:text-7xl font-black text-gray-700 dark:text-gray-200"
        >
          <TextReveal text="ABOUT ME" />
        </div>

        <div
          data-aos="zoom-in-left"
          data-aos-delay="100"
          class="text-gray-600 dark:text-gray-300 lg:text-lg space-y-5"
        >
          <p class="first-letter:text-4xl first-letter:font-bold">
            What's up? I’m Robert, a software engineer based in Romania and
            currently I am working as a backend engineer for Klarna Bank.
          </p>
          <p class="indent-4">
            The passion to create and innovate has always been in me. I strive
            to build quality, clean, intuitive, and robust software with
            attention and deliberation.
          </p>
          <p class="indent-4">
            With a solid 5-year track record in the software industry,my
            expertise thrives in web applications and microservices applied in cybersecurity,
            e-commerce, fintech and legaltech, areas that truly ignite my passion of crafting software.
          </p>
        </div>
      </div>
    </div>
  </section>

  <div
    data-aos="slide-up"
    data-aos-offset="200"
    class="shadow-xl hidden lg:block absolute right-14 bottom-0 w-4 h-28 bg-gray-300 dark:bg-gray-300"
  />
</section>
