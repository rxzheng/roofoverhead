<script>
    import { onMount } from 'svelte';
  
    let isGraphVisible = false;
  
    // Set scroll event listener
    onMount(() => {
      const handleScroll = () => {
        const graphElement = document.querySelector('.graph');
        const graphPosition = graphElement.getBoundingClientRect().top;
  
        // Trigger visibility when graph element is in the viewport
        if (graphPosition < window.innerHeight) {
          isGraphVisible = true;
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
      font-size: 1.5rem;
      color: darkorange;
      margin-top: 20px;
    }
  
    .graph {
      font-size: 30rem; /* Adjust size of the icon */
      color: rgb(183, 0, 255);
      text-align: center;
      opacity: 0; /* Make it invisible initially */
      transform: translateY(100px); /* Initially position the icon below */
      transition: opacity 1s, transform 1s ease-out;
    }
  
    .graph-visible {
      opacity: 1;
      transform: translateY(0); /* Move the icon up as it becomes visible */
    }
  </style>
  
  <!-- Font Awesome CDN (add this to your HTML file or include it in the <head> section) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  
  <div class="statistics">
    <h1>Statistics</h1>
    <br><br><br><br>
    <p class="large-text">122,494 people are suffering from homelessness in Australia</p>
    <br><br><br><br>
  </div>
  
  <div class="graph" class:graph-visible={isGraphVisible}>
    <i class="fas fa-chart-line"></i> <!-- Font Awesome graph icon -->
  </div>
  