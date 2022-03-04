<template>
  <section id="projects" class="project" style="padding-top: 30px">
    <div class="setion-title" style="margin-top: 120px">
      <h2>MY PROJECTS</h2>
    </div>
    <div class="container mx-auto mt-4">
      <div class="row" style="margin-bottom: 100px" v-if="projects">
        <div
          v-for="project of projects"
          :key="project.title"
          class="col-md-4 mb-5"
        >
          <div class="card">
            <img
              :src="project.img"
              class="card-img-top"
              alt="A picture of my work"
            />

            <div class="card-body">
              <h5 class="card-title">{{ project.title }}</h5>
              <ul class="list-group SEKO list-group-flush">
                <p>{{ project.techStacks }}</p>
                <div class="maqhosha">
                  <!-- <button class="qhosha" target="blank"> -->
                  <a target="blank" class="qhosha fa fa-github" :href="project.github"></a>
                  <!-- </button> -->

                  <!-- <button class="qhosha" target="blank"> -->
                  <a target="blank" class="qhosha" :href="project.live"
                    ><span class="iconify" data-icon="bx:bxl-netlify"></span
                  ></a>
                  <!-- </button> -->
                </div>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <div v-else>Loading...</div>
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

<style scoped>
.maqhosa {
  display: inline-flex;
}

:root {
  --gradient: linear-gradient(to left top, #dd2476 10%, #ff512f 90%) !important;
}
.card-body {
  flex: 1 1 auto;
  padding: 1rem 1rem;
  
  background: linear-gradient(to bottom left, #EF8D9C 40%, #FFC39E 100%);
}
.project {
  background-color: beige;
  padding-bottom: 1px;
}
.qhosha {
  border: none;
  display: inline-flex;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  margin: 14px 2px;
  cursor: pointer;
  color: black;
}
.qhosha a {
  text-decoration: none;
  color: rgb(3, 3, 3);
}

.qhosha:hover {
  color: rgba(97, 36, 116, 0.623);
}

.card img {
  height: 300px;
  object-fit: cover;
}
.mt-4 {
  margin-top: 4.5rem !important;
}
.card-img-top {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.list-group-flush {
  border-radius: 0;
  display: inline-flex;
}
.card-body{
  height: 250px;
}
.card {
  /* position: relative; */
  /* display: flex; */
  /* flex-direction: column; */
  /* min-width: 0; */
  word-wrap: break-word;
  background-color: rgb(248, 248, 210);
  background-clip: border-box;
  border-radius: 0.5rem;
}
@media only screen and (min-width: 1000px) {
  /* .qhosha {
    margin: 4px 4px;
    cursor: pointer;
    border-radius: 50px;
    width: 150px;
    height: 50px;
    display: inline-block;
  } */
  .card-body {
    height: 265px;
  }
}
@media only screen and (min-width: 1200px) {
  /* .qhosha {
    margin: 4px 4px;
    cursor: pointer;
    border-radius: 50px;
    width: 150px;
    height: 50px;
    display: inline-block;
  } */
  .card-body {
    height: 365px;
  }
}
</style>
