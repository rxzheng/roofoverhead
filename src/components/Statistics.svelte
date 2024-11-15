<script>
  import { onMount } from 'svelte';
  
  let isGraphVisible = false;
  let isTextVisible = false; // Track the visibility of the text
  
  // Set scroll event listener
  onMount(() => {
    const handleScroll = () => {
      const graphElement = document.querySelector('.graph');
      const textElement = document.querySelector('.text'); // Select the text element
      const graphPosition = graphElement.getBoundingClientRect().top;
      const textPosition = textElement.getBoundingClientRect().top;
  
      // Trigger visibility when graph element is in the viewport
      if (graphPosition < window.innerHeight && !isGraphVisible) {
        isGraphVisible = true;
      }

      // Trigger visibility of the text when further down the page
      if (textPosition < window.innerHeight && isGraphVisible) {
        isTextVisible = true;
      }
    };
  
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<style>
  .statistics {
    font-size: 2rem;
    color: darkorange;
    text-align: center;
    margin-top: 50px;
  }

  .large-text {
    font-size: 3rem;
    color: darkorange;
    margin-top: 20px;
    font-weight: 100;
  }

  .graph {
    font-size: 30rem; /* Adjust size of the icon */
    color: darkorange;
    text-align: center;
    opacity: 0; /* Make it invisible initially */
    transform: translateY(100px); /* Initially position the icon below */
    transition: opacity 1s, transform 1s ease-out;
  }

  .graph-visible {
    opacity: 1;
    transform: translateY(0); /* Move the icon up as it becomes visible */
  }

  .text {
    font-size: 2rem;
    color: darkorange;
    text-align: center;
    opacity: 0; /* Make it invisible initially */
    transform: translateY(50px); /* Initially position the text below */
    transition: opacity 1s, transform 1s ease-out;
    margin-top: 20px;
  }

  .text-visible {
    opacity: 1;
    transform: translateY(0); /* Move the text up as it becomes visible */
  }
</style>

<!-- Font Awesome CDN (add this to your HTML file or include it in the <head> section) -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">

<div class="statistics">
  <h1 class="text-orange-400">Statistics</h1>
  <br><br><br><br>
  <p class="large-text">122,494 people are suffering from homelessness in Australia</p>
  <br><br><br><br>
</div>

<div class="graph" class:graph-visible={isGraphVisible}>
  <i class="fas fa-chart-line"></i>
</div>

<div class="text" class:text-visible={isTextVisible}>
  
  <br><br><br><br><br>
  1 in 7 of people homeless in Australia are under the age of 12.
</div>
