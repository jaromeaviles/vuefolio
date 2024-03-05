<template>
  <Header />
  <main>
    <HeroBanner />

    <!-- About -->
    <section id="about" class="about-container container-fluid">
      <div class="row about container">
        <div class="col-lg-6 about-image-container">
          <img src="./assets/img/coding.svg" alt="coding" class="coding" />
        </div>
        <div class="col-lg-6">
          <h2>About</h2>
          <p>
            I am a passionate and highly skilled professional dedicated to
            creating impactful and innovative solutions with a proven track
            record in Wed Development. I thrive on pushing the boundaries of
            what is possible and delivering outstanding results here you will
            discover the essence of my journey expertise and commitment
            to&nbsp;excellence.
          </p>
        </div>
      </div>
    </section>

    <!-- projects -->
    <section id="projects" class="project-container container-fluid p-0">
      <svg
        class="separator"
        width="100%"
        height="120"
        viewBox="0.1 0.1 180 40"
        preserveAspectRatio="none"
      >
        <g transform="translate(-18.298844,-77.973964)">
          <path
            style="fill: #ffffff"
            d="M 31.615583,86.351641 H 192.16499 v 26.901969 c 0,0 -32.03411,-14.237983 -59.62682,-12.72484 -22.34188,1.2252 -54.779359,9.72634 -54.779359,9.72634 0,0 -22.029534,3.62882 -34.471238,-1.88988 -12.441702,-5.51871 -11.67199,-22.013589 -11.67199,-22.013589 z"
          />
          <path
            style="fill: #ffffff"
            d="M 18.441597,78.106256 H 198.58126 v 39.288614 c 0,0 -43.10672,-27.825245 -73.47599,-19.687823 -30.369264,8.137423 -46.832208,12.548653 -46.832208,12.548653 0,0 -32.775418,8.05972 -46.735258,0 C 17.577964,102.19598 18.441597,78.106256 18.441597,78.106256 Z"
          />
        </g>
      </svg>

      <div class="container project">
        <div class="row">
          <div class="col-12">
            <h2>Projects</h2>
            <Carousel />
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import Header from "./components/Header.vue"
import HeroBanner from "./components/HeroBanner.vue"
import Carousel from "./components/Carousel.vue"

export default {
  name: "App",
  components: { Header, HeroBanner, Carousel },
  mounted() {

    // Set active link when scrolling to sections
    const sections = document.querySelectorAll("section");
    const navLi = document.querySelectorAll(".navbar .navbar-nav li");

    window.addEventListener("scroll", () => {
      let current = "";
      sections.forEach((section) => {
        const sectionTop = section.offsetTop;
        const sectionHeight = section.clientHeight;

        if (scrollY >= sectionTop - sectionHeight / 3) {
          current = section.getAttribute("id");
        }
      });

      navLi.forEach((li) => {
        li.classList.remove("active");
        if (li.classList.contains(current)) {
          li.classList.add("active");
        }
      });
    });
  },
};
</script>

<style lang="scss" scoped>
@import "./assets/global.scss";

// About
.about-container {
  .about {
    padding-top: 90px;
    padding-bottom: 60px;
    margin: 0 auto;
    text-align: center;
    @include breakpoint("desktop") {
      text-align: left;
      padding-left: 0;
      padding-right: 0;
    }
    div {
      &:last-child {
        display: flex;
        justify-content: center;
        flex-direction: column;
      }
    }
    h2 {
      color: $black;
      font-size: 50px;
      line-height: 50px;
      margin-bottom: 16px;
      font-weight: bold;
      @include breakpoint("mobile") {
        margin-top: 25px;
      }
    }
    p {
      color: $black;
    }
    .about-image-container {
      display: flex;
      align-items: center;
      .coding {
        height: auto;
        width: 100%;
        @include breakpoint("desktop") {
          width: 400px;
        }
      }
    }

    .column {
      &:last-child {
        display: flex;
        justify-content: center;
        flex-direction: column;
      }
    }
  }
}

.project-container {
  padding-top: 0;
  padding-bottom: 60px;
  .separator {
    margin-top: -1px;
  }
  .project {
    padding-top: 60px;
    padding-bottom: 90px;
    @include breakpoint("desktop") {
      padding-left: 0;
      padding-right: 0;
    }
  }
  h2 {
    text-align: center;
    font-size: 50px;
    color: white;
    margin-bottom: 60px;
  }

  .project-content {
    padding: 20px;

    h3 {
      font-size: 16px;
      margin-bottom: 5px;
      text-align: center;
      color: white;
    }
    p {
      font-size: 14px;
      margin-bottom: 20px;
    }
  }
}

// Contact
.contact-container {
  padding-top: 100px;
  padding-bottom: 50px;

  h2 {
    font-size: 50px;
    color: $black;
    text-align: center;
    line-height: 50px;
    margin-bottom: 16px;
    @include breakpoint("desktop") {
      text-align: left;
    }
  }

  p {
    margin-bottom: 20px;
    text-align: center;
    @include breakpoint("desktop") {
      text-align: left;
    }
  }
}
</style>
