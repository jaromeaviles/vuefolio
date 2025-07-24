<template>
  <div class="splide" ref="splide" aria-label="projects" data-aos="fade-up" data-aos-delay="500">
    <div class="splide__track">
      <ul class="splide__list">

        <!-- Dayvigo -->

        <li class="splide__slide">
          <div class="project-description">
            <a href="https://www.dayvigo.com/" target="_blank">
              <img src="images/projects/dayvigo.png" alt="dayvigo" />
            </a>
            <div>
              <h3>Dayvigo</h3>
              <p>
                I was part of the development team for the Dayvigo website, 
                a branded pharmaceutical site focused on insomnia treatment. My work involved front-end development using HTML, CSS, and JavaScript, 
                along with content integration in Sitecore CMS—all while adhering to strict accessibility and regulatory standards.
              </p>

              <a href="https://www.dayvigo.com/" target="_blank"
                >View</a>
            </div>
          </div>
        </li>

        <!-- Dayvigo HK -->
        
         <li class="splide__slide">
          <div class="project-description">
            <a href="https://www.dayvigo.hk/" target="_blank">
              <img src="images/projects/dayvigo-hk.png" alt="dayvigo hk" />
            </a>
            <div>
              <h3>Dayvigo HK</h3>
              <p>
                I also contributed to the development of the Dayvigo Hong Kong website, 
                adapting global content and structure to meet local market needs. 
                My role focused on front-end implementation using HTML, CSS, and JavaScript, and integrating content through 
                Sitecore CMS while ensuring alignment with brand guidelines, accessibility standards, and regional compliance requirements.
              </p>

              <a href="https://www.dayvigo.hk/" target="_blank"
                >View</a>
            </div>
          </div>
        </li>

        <!-- Fycompa -->

        <li class="splide__slide">
          <div class="project-description">
            <a href="https://www.fycompa.com/hcp/" target="_blank">
              <img src="images/projects/fycompa.png" alt="fycompa" />
            </a>
            <div>
              <h3>Fycompa</h3>
              <p>
                I worked on the Fycompa HCP (Healthcare Professional) website, a medical resource platform for healthcare providers. 
                My responsibilities included implementing responsive front-end components using HTML, CSS, and JavaScript, 
                and managing content updates through Sitecore CMS. 
                I ensured that all updates followed accessibility guidelines and regulatory standards specific to pharmaceutical industry requirements.
              </p>

              <a href="https://www.fycompa.com/hcp/" target="_blank"
                >View</a>
            </div>
          </div>
        </li>

        <!-- Pizzarox -->

        <li class="splide__slide">
          <div class="project-description">
            <a href="https://pizzarox.com/" target="_blank">
              <img src="images/projects/pizzarox.png" alt="pizzarox" />
            </a>
            <div>
              <h3>Pizzarox</h3>
              <p>
                I built the Pizza Rox website using WordPress with the Beaver Builder theme, 
                customizing layouts and components to create a responsive, user-friendly experience. The site showcases the brand’s menu, 
                locations, and promotions, with a focus on fast performance, mobile optimization, 
                and ease of content management for the client.
              </p>

              <a href="https://pizzarox.com/" target="_blank"
                >View</a>
            </div>
          </div>
        </li>

        <!-- Specter -->

        <li class="splide__slide">
          <div class="project-description">
            <a
              href="https://jaromeaviles.github.io/Portfolio-Design-Project/"
              target="_blank"
            >
              <img
                src="images/projects/specter.png"
                alt="specter"
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

        <!-- Todo with Vue -->

        <li class="splide__slide">
          <div class="project-description">
            <a
              href="https://jaromeaviles.github.io/todolist-with-vue/"
              target="_blank"
            >
              <img src="images/projects/todos-with-vue.png" alt="todos" />
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
                >View</a>
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

.project {
  .splide__arrow {
    background-color: white;
    opacity: 1;
  }
}

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
    border-radius: 10px;
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
