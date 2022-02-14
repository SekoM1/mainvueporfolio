<a href="#about" class="btn btn button rounded-pill margin-right"
      >EXPLORE</a
    >
    <a class="btn btn button rounded-pill" href="#contact">LET'S CONNECT</a>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.landing {
  height: 200px;
  width: 200px;
  border-radius: 50%;
  margin-top: 230px;
  border: 8px double #8686e098;
}

.logo {
  height: 90px;
  width: 90px;
  border-radius: 50%;
  border: 2px solid #8686e098;
}
#home {
  min-height: 100vh;
  /* min-width: 100vw; */
  background: linear-gradient(
      0deg,
      rgba(243, 247, 193, 0.294),
      rgba(44, 44, 44, 0.6)
    ),
    url(https://media.istockphoto.com/photos/lavender-flowers-picture-id1251251421?k=20&m=1251251421&s=612x612&w=0&h=y0X4rOePrGzf8VdMvGO6EuZuqSZAjEvNb1lhHbP6t3g=);
  background-size: cover;
  background-repeat: no-repeat;
}

#home h1 {
  font-size: 35px;
  color: transparent !important;
  -webkit-text-stroke: 1px rgb(250, 246, 246);
  background: url(../assets/back.png);
  -webkit-background-clip: text;
  background-position: 0 0;
  animation: back 20s linear infinite;
}
@keyframes back {
  100% {
    background-position: 2000px 0;
  }
}

/* social media btns */
.fa-instagram {
  background-color: #8686e0;

  color: rgb(248, 244, 244);
  border-radius: 50%;
}
.fa-github {
  background-color: #8686e0;

  color: rgb(253, 251, 251);
  border-radius: 50%;
}
.fa-linkedin {
  background-color: #8686e0;
  color: rgb(218, 219, 207);
  border-radius: 50%;
}
.header-social-links .fa {
  display: inline-block;
  justify-content: space-around;
  list-style: none;
  margin: 15px 25px;
  padding: 10px;
  justify-content: end !important;
}
.social-links .fa {
  display: inline-block;
  justify-content: space-around;
  list-style: none;
  margin: 0 15px;
  padding: 10px;
  justify-content: end !important;
}
.fa:hover {
  color: rgba(66, 22, 77, 0.699);
}
/* home buttons */
.button {
  border: none;
  color: rgb(8, 8, 8);
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  margin: 4px 4px;
  cursor: pointer;
  width: 240px;
  font-size: small;
  margin-bottom: 10px;
}
.button:hover {
  background-color: #8686e098;
  color: #000;
}
.margin-right {
  margin-right: 40px;
}

@media only screen and (max-width: 480px) {
  .margin-right {
    margin-right: 0px;
  }
}
@media only screen and (min-width: 480px) {
  .button {
    margin-bottom: 30px;
  }
}
</style>
