<template>
   <div class="wrapper">
        <section id="home" class="hero container">
          <div class="row">
            <div class="col-lg-6 hero-text" data-aos="fade" data-aos-delay="300">
              <h1>Jarome Aviles</h1>
              <h2>Web Developer</h2>
              <div class="hero-btn">
                <a href="files/jaromeaviles-cv.pdf" download>Download CV</a>
              </div>
            </div>
            <div class="col-lg-6 hero-image-container">
              <img src="images/creator.jpg" class="rounded-circle" alt="banner" />
            </div>
          </div>
        </section>
      </div>
</template>

<style lang='scss'>
@import '../assets/global.scss';

.wrapper,
.project-container,
footer {
  background-image: url("../../public/images/textures.png");
}

.square-wrapper {
  background-image: url("../../public/images/square.png");
}

.hero {
  display: flex;
  align-items: center;
  justify-content: center;
  padding-bottom: 45px;

  @include breakpoint('desktop') {
    padding-left: 0;
    padding-right: 0;
    height: 100vh;
    padding-bottom: 0;
  }
  >.row {
    display: flex;
    justify-content: space-between;
    width: 100%;
  }
  img {
    display: block;
    border: 1px solid white;
    width: 100%;
    height: auto;

    @include breakpoint('desktop') {
      width: 400px;
      height: 400px;
    }
  }
  h1 {
    color: white;
    font-size: 60px;
    text-align: center;
    margin-bottom: 10px;
    @include breakpoint('desktop') {
      font-size: 65px;
      text-align: left;
    }

    @media only screen and (min-width: 1920px) {
      font-size: 90px;
    }
  }
  h2 {
    font-size: 35px;
    text-align: center;
    text-transform: inherit;
    @include breakpoint('desktop') {
      text-align: left;
      font-size: 45px;
    }
  }
}

.hero-text {
  display: flex;
  justify-content: center;
  flex-direction: column;
  margin-top: 45px;
  @include breakpoint('desktop') {
    margin-top: 0;
    padding-left: 10px;
  }

  h2 {
    color: $pewter;
    margin-bottom: 20px;
  }
}
.hero-image-container {
  display: flex;
  justify-content: center;
  padding-bottom: 0;
}
.hero-btn {
  display: flex;
  justify-content: center;
  margin-bottom: 50px;
  @include breakpoint('desktop') {
    justify-content: left;
    margin-bottom: 0;
  }

    a {
      align-items: center;
      background-color: transparent;
      color: #fff;
      cursor: pointer;
      display: flex;
      font-size: 1rem;
      font-weight: 700;
      line-height: 1.5;
      text-decoration: none;
      text-transform: uppercase;
      outline: 0;
      border: 0;
      padding: 1rem;
      border: 1px solid;

      &::before {
        background-color: #fff;
        content: "";
        display: inline-block;
        height: 1px;
        margin-right: 10px;
        transition: all .42s cubic-bezier(.25,.8,.25,1);
        width: 0;
      }

      &:hover, &:active {
        background-color: transparent;
        border: 1px solid;
      }

      &:hover:before {
        background-color: #fff;
        width: 3rem;
      }
    }
}

</style>