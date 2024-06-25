<template>
  <!-- Menu -->
  <MenuVue :links="links">
    <span class="prim"> Meiwei Zhang </span>
  </MenuVue>
  <HeroSection id="hero" pic="header.png">
    <template v-slot:welcome>Hello!</template>
    <p>
      I'm Meiwei Zhang, a passionate
      <hi-word>full stack developer</hi-word>
      on a mission to create innovative and impactful software solutions.
      Currently, I'm pursuing a Master of Science in Information Systems at
      Northeastern University.
    </p>
    <p>
      From building dynamic <hi-word>web applications</hi-word> to crafting
      seamless user experiences, I thrive in environments that challenge me to
      think creatively and solve complex problems. Feel free to explore my work
      and reach out if you have any questions or opportunities. Let's create
      something amazing together!
    </p>
    <template v-slot:buttons>
      <simple-button
        class="btn-primary text-white"
        url="https://www.linkedin.com/in/meiwei-zhang/"
        icon="fab linkedin-in"
      >
        Hire me!
      </simple-button>
      <simple-button
        class="btn-outline-secondary"
        url="https://github.com/Mavismeiwei"
        icon="fab github"
      >
        My Code Repo
      </simple-button>
    </template>
  </HeroSection>
  <SkillsGrid id="skills" :skills="skills" />
  <ExperienceTable id="edu-exp" :experience="experience" />
  <AwardsGrid id="awards" :awards="awards" />
  <ProjectsGrid id="projects" :projects="projects" />
  <AboutMe id="about" />
  <FooterVue :links="socials" :copyright="copyright" />
</template>

<script>
import MenuVue from "@/components/shared/AppMenu.vue";
import FooterVue from "@/components/shared/AppFooter.vue";
import HeroSection from "@/components/hero/HeroSection.vue";
import SkillsGrid from "@/components/skills/SkillsGrid.vue";
import ExperienceTable from "@/components/experience/ExperienceTable.vue";
import AwardsGrid from "@/components/awards/AwardsGrid.vue";
import ProjectsGrid from "@/components/projects/ProjectsGrid.vue";
import AboutMe from "@/components/about/AboutMe.vue";

// data to fill components
import skills from "@/data/skills";
import experience from "@/data/experience";
import awards from "@/data/awards";
import projects from "@/data/projects";

import SimpleButton from "@/components/reusable/SimpleButton.vue";
import HiWord from "@/components/reusable/HighlightIt.vue";

export default {
  name: "HomeView",
  data: () => {
    return {
      delay: 100,
      links: [
        {
          name: "home",
          url: "#hero",
        },
        {
          name: "skills",
          url: "#skills",
        },
        {
          name: "experience",
          url: "#edu-exp",
        },
        {
          name: "certificate",
          url: "#awards",
        },
        {
          name: "projects",
          url: "#projects",
        },
        {
          name: "about",
          url: "#about",
        },
      ],
      skills,
      experience,
      awards,
      projects,
      socials: [
        {
          id: 1,
          icon: "fab linkedin-in",
          url: "https://www.linkedin.com/in/meiwei-zhang/",
        },
        {
          id: 2,
          icon: "fab github",
          url: "https://github.com/Mavismeiwei",
        },
      ],
      copyright: "2024 Meiwei Zhang",
    };
  },
  components: {
    MenuVue,
    FooterVue,
    HeroSection,
    SkillsGrid,
    ExperienceTable,
    AwardsGrid,
    ProjectsGrid,
    AboutMe,
    SimpleButton,
    HiWord,
  },
};
</script>

<style lang="scss" scoped>
.prim {
  color: $primary;
}
</style>
