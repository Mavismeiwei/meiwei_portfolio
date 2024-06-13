<template>
  <div class="col-sm-12 col-md-4 mb-3">
    <div class="text-center">
      <img
        class="mb-3"
        :src="require(`@/assets/images/${skill.image}`)"
        data-aos="fade-up"
        :data-aos-delay="delay"
        data-aos-anchor-placement="top-bottom"
      />
      <h4
        class="mb-3"
        data-aos="fade-up"
        :data-aos-delay="delay + 100"
        data-aos-anchor-placement="top-bottom"
      >
        {{ skill.title }}
      </h4>
      <div
        class="tags mb-3 has-text-weight-semibold"
        data-aos="fade-up"
        :data-aos-delay="delay + 200"
        data-aos-anchor-placement="top-bottom"
      >
        <span
          v-for="language in skill.languages"
          :key="language.id"
          class="tag"
          :class="language.css"
        >
          {{ language.title }}
        </span>
      </div>
      <div>
        {{ skill.description }}
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "SingleSkill",
  props: ["skill"],
  data: () => {
    return {
      delay: 500,
    };
  },
};
</script>
<style scoped>
img {
  width: 128px;
  height: 128px;
}

.tags .tag:not(:last-child) {
  margin-right: 0.5rem;
  margin-bottom: 0.5rem;
}

.tag:not(body) {
  align-items: center;
  background-color: #f5f5f5;
  color: #4a4a4a;
  display: inline-flex;
  font-size: 0.75rem;
  height: 2em;
  justify-content: center;
  line-height: 1.5;
  padding-left: 0.75em;
  padding-right: 0.75em;
  white-space: nowrap;
}

span {
  -webkit-transition: 0.1s ease-in;
  -o-transition: 0.1s ease-in;
  transition: 0.1s ease-in;
}

span:hover {
  -webkit-transform: translate3d(0px, -5px, 0px);
  transform: translate3d(0px, -5px, 0px);
}

.java:hover {
  color: #fff;
  background-color: #007396;
}

.python:hover {
  color: #fff;
  background-color: #0faed6;
}

.nodejs:hover {
  color: #fff;
  background-color: #4ab93b;
}

.spring:hover {
  color: #fff;
  background-color: #6db33f;
}

.django:hover {
  color: #fff;
  background-color: #3f79b3;
}

.expressjs:hover {
  color: #fff;
  background-color: #4fc08d;
}

.mysql:hover {
  color: #fff;
  background-color: #ff6f00;
}

.mongodb:hover {
  color: #fff;
  background-color: #ffd900;
}

.js:hover {
  color: #fff;
  background-color: #eb8602;
}

.reactjs:hover {
  color: #fff;
  background-color: #00d1b2;
}

.vuejs:hover {
  color: #fff;
  background-color: #4fc08d;
}

.angular:hover {
  color: #fff;
  background-color: #00d1b2;
}

.typescript:hover {
  color: #fff;
  background-color: #3178c6;
}

.bootstrap:hover {
  color: #fff;
  background-color: #7952b3;
}

.jira:hover {
  color: #fff;
  background-color: #d9411e;
}

.confluence:hover {
  color: #fff;
  background-color: #d9411e;
}

.docker:hover {
  color: #fff;
  background-color: #2496ed;
}

.cicd:hover {
  color: #fff;
  background-color: #ff6f00;
}

.jenkins:hover {
  color: #fff;
  background-color: #a21386;
}
</style>
