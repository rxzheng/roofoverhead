<script>
    const teamMembers = [
      {
        name: "John",
        description: "A passionate man with a mission.",
        image: "images/man1.webp"
      },
      {
        name: "Jill",
        description:
          "Someone that was once homeless and is willing to do anything to help those in need.",
          image: "images/woman1.webp"
      },
      {
        name: "Jack",
        description: "A great funder of our mission and is very supportive.",
        image: "images/man2.webp"
      },
    ];
  </script>
  
  <style>
    .about-container {
      max-width: 800px;
      margin: auto;
      padding: 2rem;
      text-align: center;
      color:darkorange;
    }
  
    .title {
      font-size: 2rem;
      font-weight: bold;
      margin-bottom: 1rem;
      font-weight:100;
    }
  
    .mission {
      font-size: 1.1rem;
      font-weight: bold;
      margin: 1rem 0;
      line-height: 1.6;
      font-style:oblique;
      font-weight:100;
    }
  
    .team-section {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1.5rem;
      margin-top: 2rem;
    }
  
    .team-box {
      background-color: #333;
      border: 1px solid #444;
      border-radius: 8px;
      padding: 1.5rem;
      width: 250px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      text-align: center;
      color: #fff;
    }
  
    .team-member-name {
      font-size: 1.25rem;
      font-weight: 100;
      margin-bottom: 0.5rem;
    }
  
    .team-member-description {
      font-size: 1rem;
      line-height: 1.5;
      font-weight:100;
    }
  </style>
  
  <div class="about-container">
    <div class="title">About Us</div>
    <div class="mission">
      <p>Roofoverhead Initiative is committed to helping those in need.</p>
      <p>We host music festivals, sleepouts, PJs at Work Days, and other events that matter.</p>
      <br><br><br><br><br><br>
    </div>
    <div class="title">Meet Our Team</div>
    <div class="team-section">
      {#each teamMembers as member}
        <div class="team-box">
          <div class="team-member-name">{member.name}</div>
          <div class="team-member-image"><img src="{member.image}" alt="{member.name}">{member.image}</div>
          <div class="team-member-description">{member.description}</div>
          
        </div>
      {/each}
    </div>
  </div>
  