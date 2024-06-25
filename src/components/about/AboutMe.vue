<template>
  <base-container title="About Me" id="about">
    <div class="about-section">
      <h3>Background</h3>
      <p>
        I completed my undergraduate degree in Information Management and
        Information Systems in China. After graduation, I decided to pursue my
        passion for technology and moved to the United States to study computer
        science. This journey from China to the U.S. has been transformative,
        broadening my horizons and deepening my technical expertise. The
        decision to study computer science stemmed from my fascination with how
        technology can solve real-world problems and create innovative
        solutions.
      </p>
      <div class="img-row">
        <img
          src="@/assets/images/background1.jpg"
          alt="Background"
          class="about-img small-img"
        />
        <img
          src="@/assets/images/location.png"
          alt="Background"
          class="about-img small-img"
        />
        <img
          src="@/assets/images/background2.jpg"
          alt="Background"
          class="about-img small-img"
        />
      </div>

      <div class="split-section">
        <div class="split-left">
          <h3>Why Computer Science</h3>
          <p>
            My interest in computer science was sparked by the endless
            possibilities it offers. The ability to create something from
            nothing and the constant evolution of the field keep me motivated. I
            am particularly drawn to the problem-solving aspect and the
            opportunity to work on projects that have real-world applications.
            Studying computer science allows me to merge my analytical skills
            with my creative thinking, and I am excited to see where this path
            will take me.
          </p>
        </div>
        <img
          src="@/assets/images/computer-science.jpg"
          alt="Computer Science"
          class="about-img split-img"
        />
      </div>

      <div class="split-section">
        <img
          src="@/assets/images/career.png"
          alt="Career"
          class="about-img split-img"
        />
        <div class="split-right career-aspirations-section">
          <h3>Career Aspirations</h3>
          <ul>
            <li>Become a proficient full-stack or software engineer.</li>
            <li>
              Build robust and scalable applications that make a difference.
            </li>
            <li>Continuously learn and grow within the tech industry.</li>
            <li>
              Lead projects that blend front-end and back-end development.
            </li>
            <li>Create seamless and impactful user experiences.</li>
          </ul>
        </div>
      </div>

      <h3>Personality and Hobbies</h3>
      <p>
        Outside of coding, I have a vibrant and active lifestyle. Fitness is a
        big part of my daily routine—I love hitting the gym and staying active.
        Traveling is another passion of mine; exploring new places and
        experiencing different cultures gives me fresh perspectives and
        inspiration. When I'm not traveling or at the gym, you can find me in
        the kitchen experimenting with baking recipes. I find baking to be a
        perfect mix of creativity and precision, much like coding.
      </p>
      <div class="img-row">
        <img
          src="@/assets/images/fitness.jpg"
          alt="Fitness"
          class="about-img small-img"
        />
        <img
          src="@/assets/images/fitness1.jpg"
          alt="Fitness"
          class="about-img small-img"
        />
        <img
          src="@/assets/images/fitness2.jpg"
          alt="Fitness"
          class="about-img small-img"
        />
      </div>
      <div class="img-row">
        <img
          src="@/assets/images/fitness3.jpg"
          alt="Fitness"
          class="about-img small-img"
        />
        <img
          src="@/assets/images/hobby1.jpg"
          alt="Hobby"
          class="about-img small-img"
        />
        <img
          src="@/assets/images/hobby2.jpg"
          alt="Hobby"
          class="about-img small-img"
        />
      </div>
    </div>
  </base-container>
</template>

<script>
import BaseContainer from "../reusable/BaseContainer.vue";

export default {
  name: "AboutMe",
  components: {
    BaseContainer,
  },
};
</script>

<style scoped>
.about-section {
  padding: 2em;
}

.about-section h3,
.about-section h4 {
  color: #34495e;
}

.about-section p {
  margin-bottom: 1.5em;
  line-height: 1.6;
}

.about-img {
  width: 100%;
  max-width: 400px;
  margin: 1em 0;
  display: block;
  border-radius: 8px;
}

.img-row {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

.img-row .about-img {
  width: 32%;
}

.small-img {
  height: 340px;
  object-fit: cover;
}

.tall-img {
  height: 370px;
  object-fit: cover;
}

.split-section {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 2.7em 0;
  flex-wrap: wrap;
}

.split-left,
.split-right {
  flex: 1;
  padding: 1em;
}

.split-img {
  flex-shrink: 0;
  width: 100%;
  max-width: 300px;
  margin-left: 1em;
  border-radius: 8px;
}

.split-left {
  padding-right: 3em;
}

.split-right {
  padding-left: 2em;
}

.career-aspirations-section ul {
  padding-left: 2rem;
  margin-top: 1em;
}

.career-aspirations-section li {
  margin-bottom: 1.2rem;
  font-size: 1.1em;
}

@media (max-width: 768px) {
  .split-section {
    flex-direction: column;
  }

  .split-img {
    margin-left: 0;
    margin-bottom: 1em;
  }

  .split-left {
    padding-right: 0;
  }

  .split-right {
    padding-left: 0;
  }

  .img-row .about-img {
    width: 100%;
  }

  .small-img {
    height: auto;
  }

  .tall-img {
    height: auto;
  }
}
</style>
