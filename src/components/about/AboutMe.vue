<template>
  <base-container title="About Me" id="about">
    <div class="about-section">
      <h3>Background</h3>
      <p>
        My journey in the world of technology began with an undergraduate degree
        in Information Management and Information Systems in China. Eager to
        dive deeper, I crossed the oceans to the United States to study computer
        science. This adventure has not only broadened my horizons but also
        honed my technical skills. The decision to explore computer science was
        driven by my fascination with its power to solve real-world problems and
        create innovative solutions.
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
            Imagine creating something from nothing, solving puzzles that make a
            tangible impact on the world, and constantly riding the wave of
            technological evolution. That's what drew me to computer science.
            It's a field where analytical skills meet creative thinking, and
            where each project presents a new challenge and an opportunity to
            innovate.
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
            <li>To become a masterful full-stack or software engineer.</li>
            <li>
              Create robust, scalable applications that truly make a difference.
            </li>
            <li>
              Embrace continuous learning and growth in the tech industry.
            </li>
            <li>
              Lead innovative projects that seamlessly blend front-end and
              back-end development.
            </li>
            <li>Craft user experiences that leave a lasting impact.</li>
          </ul>
        </div>
      </div>

      <h3>Personality and Hobbies</h3>
      <p>
        Life isn't just about coding for me. I lead an active lifestyle filled
        with vibrant hobbies. Fitness is my daily ritual; I love hitting the gym
        and staying in shape. Traveling is my way of seeking
        inspiration—exploring new places and cultures always brings fresh
        perspectives. And when I'm not traveling or at the gym, you'll find me
        in the kitchen, occasionally whipping up delicious meals. Cooking is a
        delightful mix of creativity and precision, much like coding!
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

  .about-img {
    margin-left: auto;
    margin-right: auto;
  }

  .small-img {
    height: auto;
    max-width: 100%;
  }

  .tall-img {
    height: auto;
    max-width: 100%;
  }
}
</style>
