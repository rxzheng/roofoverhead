<script>
  export let steps = [
      {
          name: "Sleep",
          icon: "fa-solid fa-bed",
          description: "Sleepout event where participants experience sleeping outdoors to gain empathy for those experiencing homelessness."
      },
      {
          name: "Music",
          icon: "fa-solid fa-music",
          description: "A music festival dedicated to raising funds for the community, featuring popular artists and an uplifting atmosphere."
      },
      {
          name: "PJ's at Work",
          icon: "fa-solid fa-shirt",
          description: "An opportunity for professionals to raise awareness and support by working in the comfort of their pajamas, promoting relaxation and camaraderie."
      }
  ];
</script>

<main class="flex flex-col flex-1 p-4 text-white">
  <!-- Title Section -->
  <section class="text-center py-8 sm:py-14">
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
          <span class="poppins text-orange-400">Events</span>
      </h2>
  </section>

  <!-- Events Section -->
  <section class="flex flex-col gap-16 py-20 lg:py-32">
      <!-- Sleepout Event -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-10 items-center">
          <div class="text-center lg:text-left flex flex-col gap-4">
              <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                  {steps[0].name}
              </h3>
              <p class="text-base sm:text-lg md:text-xl">
                  {steps[0].description}
              </p>
          </div>
          <div class="relative shadow-2xl">
              <img src="images/sleepout.jpg" alt="Sleepout event" class="object-cover rounded-lg w-full h-auto image-style"/>
          </div>
      </div>

      <!-- Music Festival Event -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-10 items-center lg:flex-row-reverse">
          <div class="text-center lg:text-left flex flex-col gap-4">
              <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                  {steps[1].name}
              </h3>
              <p class="text-base sm:text-lg md:text-xl">
                  {steps[1].description}
              </p>
          </div>
          <div class="relative shadow-2xl">
              <img src="images/music_festival.jpg" alt="Music Festival" class="object-cover rounded-lg w-full h-auto image-style"/>
          </div>
      </div>

      <!-- PJ's at Work Event -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-10 items-center">
          <div class="text-center lg:text-left flex flex-col gap-4">
              <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                  {steps[2].name}
              </h3>
              <p class="text-base sm:text-lg md:text-xl">
                  {steps[2].description}
              </p>
          </div>
          <div class="relative shadow-2xl">
              <img src="images/pjs_at_work.jpg" alt="PJ's at Work" class="object-cover rounded-lg w-full h-auto image-style"/>
          </div>
      </div>
  </section>
</main>

<style>
  main {
      color: #ffffff; /* White text for black background */
  }

  h2, h3 {
      color: #ea580c; /* Orange 400 */
  }

  p {
      line-height: 1.6; /* Enhance readability */
  }

  /* Add rounded edges and orange outline to images */
  .image-style {
      border-radius: 12px; /* Round the edges */
      border: 4px solid #ea580c; /* Orange border */
  }
</style>
