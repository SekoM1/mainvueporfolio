<template>
  <section id="projects" class="project" style="padding-top: 30px">
    <div class="setion-title" style="margin-top: 120px">
      <h2>MY PROJECTS</h2>
    </div>

    <div class="container mx-auto mt-4">
      <div class="row" style="margin-bottom: 100px" v-if="projects">
        <ul class="cards" v-if="projects">
          <li class="cards_item">
            <div v-for="project of projects" :key="project.title" class="card">
              <div class="card_image"><img :src="project.img" /></div>
              <div class="card_content">
                <h2 class="card_title">{{ project.title }}</h2>
                <p class="card_text">{{ project.techStacks }}</p>
                <!-- <button class="btn card_btn">Read More</button> -->
                <div class="btn card_btn">
                  <!-- <button class="qhosha" target="blank"> -->
                  <a target="blank" class="" :href="project.github"
                    ><img
                      src="https://img.icons8.com/glyph-neue/20/000000/github.png"
                    />
                  </a>
                  <!-- </button> -->

                  <!-- <button class="qhosha" target="blank"> -->
                  <a target="blank" class="" :href="project.live">
                    <img
                      src="https://img.icons8.com/external-tal-revivo-tritone-tal-revivo/20/000000/external-netlify-a-cloud-computing-company-that-offers-hosting-and-serverless-backend-services-for-static-websites-logo-tritone-tal-revivo.png"
                    />
                  </a>
                  <!-- </button> -->
                </div>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projects: null,
    };
  },
  mounted() {
    fetch("https://sekos-api-project.herokuapp.com/projects")
      .then((res) => res.json())
      .then((data) => {
        console.log(data);
        this.projects = data;
      })
      .catch((e) => console.log(e));
  },
};
</script>

<style>
/* Font */
@import url("https://fonts.googleapis.com/css?family=Quicksand:400,700");

/* Design */
*,
*::before,
*::after {
  box-sizing: border-box;
}

html {
  background-color: #ecf9ff;
}

body {
  color: #272727;
  font-family: "Quicksand", serif;
  font-style: normal;
  font-weight: 400;
  letter-spacing: 0;
  padding: 1rem;
}

.main {
  max-width: 1200px;
  margin: 0 auto;
}

h1 {
  font-size: 24px;
  font-weight: 400;
  text-align: center;
}

img {
  height: auto;
  max-width: 100%;
  vertical-align: middle;
}

.btn {
  color: #ffffff;
  padding: 0.8rem;
  font-size: 14px;
  text-transform: uppercase;
  border-radius: 4px;
  font-weight: 400;
  display: block;
  width: 100%;
  cursor: pointer;
  border: 1px solid rgba(255, 255, 255, 0.2);
  background: transparent;
}

.btn:hover {
  background-color: rgba(255, 255, 255, 0.12);
}

.cards {
  display: flex;
  flex-wrap: wrap;
  list-style: none;
  margin: 0;
  padding: 0;
}

.cards_item {
  display: flex;
  padding: 1rem;
}

@media (min-width: 40rem) {
  .cards_item {
    width: 50%;
  }
}

@media (min-width: 56rem) {
  .cards_item {
    width: 33.3333%;
  }
}

.card {
  background-color: white;
  border-radius: 0.25rem;
  box-shadow: 0 20px 40px -14px rgba(0, 0, 0, 0.25);
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

.card_content {
  padding: 1rem;
  background: linear-gradient(to bottom left, #ef8d9c 40%, #ffc39e 100%);
}

.card_title {
  color: #ffffff;
  font-size: 1.1rem;
  font-weight: 700;
  letter-spacing: 1px;
  text-transform: capitalize;
  margin: 0px;
}

.card_text {
  color: #ffffff;
  font-size: 0.875rem;
  line-height: 1.5;
  margin-bottom: 1.25rem;
  font-weight: 400;
}
.made_by {
  font-weight: 400;
  font-size: 13px;
  margin-top: 35px;
  text-align: center;
}
</style>
