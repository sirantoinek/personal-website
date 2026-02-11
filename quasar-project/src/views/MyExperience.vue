<script setup lang="ts">
  import InfoCard from 'src/components/InfoCard.vue';
  import BulletList from 'src/components/BulletList.vue';
</script>

<template>
  <div class="myExperience">
    <h2 class="header-text">My Background</h2>
    <div class="exp-info-cards">
      <InfoCard title="Education" style="grid-area: card-1">
        <p>
          <strong>University of Florida</strong>
          <br>Bachelor of Science in Computer&nbsp;Science <!-- &nbsp; is a non-breaking space -->
        </p>
        <p>GPA: 4.0 (Cum Laude)</p>
      </InfoCard>
      <InfoCard title="Experience" style="grid-area: card-2">
        <BulletList>
          <strong>IT Support Technician Intern</strong>, C&W&nbsp;Technologies
          <li>Diagnosed and resolved hardware and software issues on desktops and laptops.</li>
          <li>Replaced faulty components in desktops and laptops and performed system upgrades.</li>
          <li>Installed drivers, recovered user data, and optimized system performance.</li>
          <li>Updated support tickets and prepared technical reports using Tigerpaw software.</li>
        </BulletList>
        <BulletList>
          <strong>Assembly Technician</strong>, 3D&nbsp;Potter
          <li>Assembled clay 3D printers and prepared units for shipment.</li>
          <li>Soldered wire harnesses and flashed firmware onto printer mainboards.</li>
          <li>Supported R&D of next-gen printers.</li>
          <li>Led the 3D Potter display at Maker Faire Orlando, generating $5,000+ in sales.</li>
        </BulletList>
      </InfoCard>
      <InfoCard title="Certifications" style="grid-area: card-3">
        <p>
          <a href="https://cp.certmetrics.com/comptia/en/public/verify/credential/E901Y92MZH4Q1YS5" class="link-text" target="_blank">
            <strong>CompTIA A+</strong>
          </a>
          <br>(Exp. 07/31/2028)
        </p>
      </InfoCard>
      <InfoCard title="Skills" style="grid-area: card-4">
        <BulletList>
          <strong>Programming Languages</strong>
          <li>C++</li>
          <li>Java</li>
          <li>Python</li>
          <li>TypeScript && JavaScript</li>
          <li>HTML && CSS</li>
        </BulletList>
        <BulletList>
          <strong>Frameworks</strong>
          <li>Vue.js</li>
          <li>Electron.js</li>
          <li>Quasar</li>
          <li>JUnit</li>
        </BulletList>
        <BulletList>
          <strong>Tools & Others</strong>
          <li>Git</li>
          <li>SQLite</li>
          <li>PostgreSQL</li>
        </BulletList>
        <BulletList>
          <strong>IT & Technical Support</strong>
          <li>Computer Hardware/Software Troubleshooting</li>
          <li>Desktop/Laptop Hardware Installation</li>
          <li>Network Troubleshooting</li>
          <li>TeamViewer</li>
          <li>Ticketing Systems (Tigerpaw)</li>
          <li>Windows, Linux, Android</li>
        </BulletList>
      </InfoCard>
    </div>
  </div>
</template>

<style lang="scss">
  .myExperience {
    display: grid;
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

  .exp-info-cards {
    display: grid;
    grid-auto-columns: auto;
    grid-auto-rows: auto;
    gap: clamp(1rem, 2vw, 2rem);
    grid-template-areas: 
      "card-1 card-3"
      "card-2 card-2"
      "card-4 card-4";
  }

  @media (max-width: 600px) {
    .exp-info-cards {
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

    .exp-info-cards {
      grid-auto-columns: 1fr;
    }
  }

  @media (min-width: 1200px) {
    .myExperience {
      margin-top: 10rem;
      transition: 150ms;
    }

    .exp-info-cards {
      grid-template-columns: fit-content(200px) 1fr;
      grid-template-areas: 
        "card-1 card-2 card-2"
        "card-3 card-2 card-2"
        "card-4 card-4 card-4";
    }
  }
</style>