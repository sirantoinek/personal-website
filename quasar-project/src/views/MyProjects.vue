<script setup lang="ts">
  import InfoCard from 'src/components/InfoCard.vue';
  import BulletList from 'src/components/BulletList.vue';
</script>

<template>
  <div class="myProjects">
    <h2 class="header-text">What I've Built</h2>
    <div class="proj-info-cards">
      <InfoCard title="Personal Website" url="https://github.com/sirantoinek/personal-website" style="grid-area: card-1">
        <BulletList>
          <li>This website right here! Built with TypeScript, HTML, CSS, Quasar, and Vue.js.</li>
          <li>Designed with responsiveness and fluidity in mind for an optimal experience across all device form factors.</li>
          <li>Utilizes Vue.js components with slots and props to ensure modularity and styling consistency across views.</li>
        </BulletList>
      </InfoCard>
      <InfoCard title="Open Organizer" url="https://github.com/sirantoinek/OpenOrganizer" style="grid-area: card-2">
        <BulletList>
          <li>A cross-platform desktop reminder and note-taking calendar application built with user control, complete data ownership, and security as core principles with opt-in cloud sync functionality.</li>
          <li>Utilizes a custom security framework featuring full data encryption keeping the server blind to user data.</li>
          <li>Supports complex and optimally stored and generated recurring reminders with the ability to override individual reminders within a recurring series.</li>
          <li>Built with TypeScript, Quasar, Electron, SQLite, Golang, and PostgreSQL.</li>
        </BulletList>
      </InfoCard>
      <InfoCard title="Auto File Organizer" url="https://github.com/sirantoinek/auto-file-organizer" style="grid-area: card-3">
        <BulletList>
          <li>CLI tool that sorts files into a structured directory by type and/or last modified date.</li>
          <li>Supports recursive and top-level only organization, manual runs, auto scheduling, and undo of last operation.</li>
          <li>Built with Java 21, Maven, Apache Commons IO, and JUnit 5; strengthened testing, and file system skills.</li>
        </BulletList>
      </InfoCard>
      <InfoCard title="CT Property Trends" url="https://github.com/sirantoinek/CT-Property-Trends" style="grid-area: card-4">
        <BulletList>
          <li>Full stack application built with JavaScript/React, Leaflet.js, and Oracle DB for Database Systems course.</li>
          <li>Integrated over 1 million real Connecticut property sales records alongside CTDOT geoJSON data to be used in interactive geographic analysis.</li>
          <li>Developed dynamic visualizations, including a color-coded hover map and interactive multi-line graph, to display trends by town, property type, sales price, and year.</li>
          <li>Enabled complex trend analysis supporting data-driven decision-making for users such as homeowners, real estate agents, and property appraisers.</li>
          <li>Followed Agile Scrum with defined sprints and regular scrum meetings to manage tasks and adapt to feedback.</li>
        </BulletList>
      </InfoCard>
    </div>
  </div>
</template>

<style lang="scss">
  .myProjects {
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

  .proj-info-cards {
    display: grid;
    grid-auto-columns: 1fr;
    grid-auto-rows: auto;
    gap: clamp(1rem, 2vw, 2rem);
    grid-template-areas: 
      "card-1"
      "card-2"
      "card-3"
      "card-4";
  }

  @media (max-width: 730px) {
    .myProjects {
      margin-top: 2.5rem;
    }
  }

  @media (min-width: 1200px) {
    .myProjects {
      margin-top: 10rem;
      transition: 150ms;
    }

    .proj-info-cards {
      grid-template-areas: 
        "card-1 card-2"
        "card-3 card-4";
    }
  }
</style>