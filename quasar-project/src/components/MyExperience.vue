<script setup lang="ts">
  
</script>

<template>
  <div class="myExperience">
    <h2 class="header-text">My Background</h2>
    <div class="info-cards">
      <div class="card" style="grid-area: card-1">
        <h3 class="subheader-text">Education</h3>
        <p class="card-text">
          <strong>University of Florida</strong>
          <br>Bachelor of Science in Computer&nbsp;Science <!-- &nbsp; is a non-breaking space -->
        </p>
        <p class="card-text">
          GPA: 4.0 (Cum Laude)
        </p>
      </div>
      <div class="card" style="grid-area: card-2">
        <h3 class="subheader-text">Experience</h3>
        <ul class="card-text bullet-list">
          <strong>IT Support Technician Intern</strong>, C&W&nbsp;Technologies
          <li class="bullet-text">Diagnosed and resolved hardware and software issues on desktops and laptops.</li>
          <li class="bullet-text">Replaced faulty components in desktops and laptops and performed system upgrades.</li>
          <li class="bullet-text">Installed drivers, recovered user data, and optimized system performance.</li>
          <li class="bullet-text">Updated support tickets and prepared technical reports using Tigerpaw software.</li>
        </ul>
        <ul class="card-text bullet-list">
          <strong>Assembly Technician</strong>, 3D&nbsp;Potter
          <li class="bullet-text">Assembled clay 3D printers and prepared units for shipment.</li>
          <li class="bullet-text">Soldered wire harnesses and flashed firmware onto printer mainboards.</li>
          <li class="bullet-text">Supported R&D of next-gen printers.</li>
          <li class="bullet-text">Led the 3D Potter display at Maker Faire Orlando, generating $5,000+ in sales.</li>
        </ul>
      </div>
      <div class="card" style="grid-area: card-3">
        <h3 class="subheader-text">Certifications</h3>
        <p class="card-text">
          <strong>CompTIA A+</strong>
          <br>(Exp. 07/31/2028)
        </p>
      </div>
      <div class="card" style="grid-area: card-4">
        <h3 class="subheader-text">Skills</h3>
        <p class="card-text">C++, Java, Python, TypeScript, JavaScript, Electron.js, Node.js, Vue.js, JUnit, SQL, x64dbg, Ghidra, Git</p>
        <p class="card-text">Computer Hardware/Software Troubleshooting, Computer Hardware Installation, Technical Support</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
  .myExperience {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
	  position: relative;
    gap: 2rem;
    margin-top: 5rem;
  }

  .header-text {
    font-size: clamp(2rem, 4vw, 4rem);
    margin-top: 2.5rem;
    margin-bottom: 0px;
    line-height: 1;
    white-space: nowrap;
  }

  .info-cards {
    display: grid;
    grid-auto-columns: auto;
    grid-auto-rows: auto;
    gap: clamp(1rem, 2vw, 2rem);
    grid-template-areas: 
    "card-1 card-3"
    "card-2 card-2"
    "card-4 card-4";
  }

  .card {
    display: flex;
    flex-direction: column;
    padding: clamp(1.5rem, 2vw, 2rem);
    background-color: $lm-border;
    border-radius: .5rem;
    text-align: center;
    gap: clamp(1rem, 1.5vw, 1.5rem);
  }

  .subheader-text {
    font-size: clamp(1.75rem, 2.5vw, 2.5rem);
    font-weight: 300;
    margin: 0px;
    line-height: 1;
    white-space: nowrap;
  }

  .card-text {
    font-size: clamp(1rem, 1.25vw, 1.25rem);
    margin: 0px;
  }
  
  .bullet-list {
    padding-left: clamp(1.5rem, 2vw, 2rem);
    text-align: start;
  }

  .bullet-text {
    margin-top: 0.35rem;
  }

  @media (max-width: 600px) {
    .info-cards {
      grid-template-areas: 
      "card-1"
      "card-2"
      "card-3"
      "card-4";
    }
  }

  @media (max-width: 730px) {
    .myExperience {
      margin-top: 2.5rem;
    }
  }

  @media (min-width: 1200px) {
    .myExperience {
      margin-top: 10rem;
      transition: 150ms;
    }

    .info-cards {
      grid-template-columns: fit-content(200px) 1fr;
      grid-template-areas: 
      "card-1 card-2 card-2"
      "card-3 card-2 card-2"
      "card-4 card-4 card-4";
    }
  }
</style>