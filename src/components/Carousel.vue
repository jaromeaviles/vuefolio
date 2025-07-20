<template>
  <div class="splide" ref="splide" aria-label="projects" data-aos="fade-up" data-aos-delay="500">
    <div class="splide__track">
      <ul class="splide__list">
        <li class="splide__slide">
          <div class="project-description">
            <a href="https://kdsfun.000webhostapp.com/" target="_blank">
              <img src="../assets/img/for-upload/kidoos.png" alt="kidoos" />
            </a>
            <div>
              <h3>Kidoos</h3>
              <p>
                Kidoos is a visionary project aimed at revolutionizing the
                management of student information, communication, and engagement
                within educational institutions.
              </p>

              <a href="https://kdsfun.000webhostapp.com/" target="_blank"
                >View</a
              >
              |
              <a href="https://github.com/jaromeaviles/kidoos" target="_blank"
                >Github</a
              >
            </div>
          </div>
        </li>

        <li class="splide__slide">
          <div class="project-description">
            <a
              href="https://jaromeaviles.github.io/Portfolio-Design-Project/"
              target="_blank"
            >
              <img
                src="../assets/img/for-upload/portfolio.png"
                alt="portfolio project"
              />
            </a>
            <div>
              <h3>Specter</h3>
              <p>
                Step into Specter portfolio, a sleek and static showcase
                highlighting my journey, skills, and achievements. With an
                emphasis on clean design and intuitive navigation, this platform
                offers a glimpse into specter's professional&nbsp;endeavors.
              </p>

              <a
                href="https://jaromeaviles.github.io/Portfolio-Design-Project/"
                target="_blank"
                >View</a
              >
              |
              <a
                href="https://github.com/jaromeaviles/Portfolio-Design-Project"
                target="_blank"
                >Github</a
              >
            </div>
          </div>
        </li>

        <li class="splide__slide">
          <div class="project-description">
            <a
              href="https://jaromeaviles.github.io/todolist-with-vue/"
              target="_blank"
            >
              <img src="../assets/img/for-upload/todos.png" alt="todos" />
            </a>
            <div>
              <h3>Todo with Vue</h3>
              <p>
                Explore my static To-Do app in Vue.js, embodying simplicity and
                functionality in task management. With a clean interface and
                responsive design, this project reflects my adept use of Vue.js
                to enhance user&nbsp;experience.
              </p>

              <a
                href="https://jaromeaviles.github.io/todolist-with-vue/"
                target="_blank"
                >View</a
              >
              |
              <a
                href="https://github.com/jaromeaviles/todolist-with-vue"
                target="_blank"
                >Github</a
              >
            </div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import Splide from "@splidejs/splide";

export default {
  mounted() {
    new Splide(this.$refs.splide, {
      type: 'slide',
      perPage: 1,
      rewind: true,
      pagination: false
    }).mount();
  }
};
</script>

<style lang="scss" scoped>
@import "../assets/global.scss";

.project-description {
  display: flex;
  justify-content: center;
  flex-direction: column;
  padding: 0 80px 0 80px;
  color: white;
  @include breakpoint("desktop") {
    align-items: center;
    flex-direction: row;
    padding: 0 80px 0 120px;
  }

  img {
    width: 100%;
    height: auto;
    @include breakpoint("desktop") {
      width: 500px;
    }
  }

  div {
    padding: 0;
    margin-top: 20px;
    text-align: center;
    @include breakpoint("desktop") {
      padding: 0 60px;
      margin-top: 0;
      text-align: left;
    }

    h3 {
      font-size: 20px;
      text-transform: capitalize;
      @include breakpoint("desktop") {
        font-size: 22px;
        margin-bottom: 10px;
      }
    }
    h3,
    p,
    a {
      color: white;
    }
    p {
      @include breakpoint("mobile") {
        display: none;
      }
    }
    a {
      text-decoration: none;
      margin-top: 10px;
      display: inline-block;
      font-size: 14px;
    }
  }
}
</style>
