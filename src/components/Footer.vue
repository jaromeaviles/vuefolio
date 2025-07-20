<template>
  <footer>
      <section class="container">
        <div class="row">
          <div class="col-lg-6">
            <p>&copy; Jarome Aviles 2025</p>
          </div>
          <div class="col-lg-6">
            <!-- Linkedin -->
            <span class="icon">
              <a href="https://www.linkedin.com/in/jarome-carlo-aviles-b7a88315a/" target="_blank">
              <img src="../assets/img/linkedin.png" alt="Linkedin" /></a>
            </span>

            <!-- Github -->
            <span class="icon">
              <a href="https://github.com/jaromeaviles" target="_blank">
               <img src="../assets/img/github.png" alt="Github" /></a>
            </span>
          </div>
        </div>
      </section>
    </footer>
</template>

<style lang="scss" scoped>
@import "../assets/global.scss";

footer {
  background-color: $brown;
  color: $pewter;
  text-align: center;
  padding: 10px;
  display: flex;
  justify-content: center;

  .row {
    div:last-child {
      display: flex;
      justify-content: center;
      @include breakpoint('desktop') {
        justify-content: flex-end;
      }
    }
  }

  p {
    text-align: center;
    margin-bottom: 10px;
    @include breakpoint('desktop') {
      text-align: left;
      margin-bottom: 0;
      font-size: 14px;
    }
  }

  .icon i {
    font-size: 20px;

    &:first-child {
      margin-right: 10px;
    }
  }

  a {
    color: $pewter;
    line-height: 16px;
    display: inline-block;
    padding: 0 2px;

    &:hover {
      color: $pewter;
    }
  }

  img {
    width: 25px;
    height: auto;
  }
}

</style>