<template>
<!-- <router-link @click="scrollToTop"  id="myBtn" title="Go to top">Top</router-link> -->
  <footer id="footer">
    <div class="container">
      <div class="social-links" style="margin-bottom: 30px;">
        <a href="https://www.instagram.com/melachild_blvck/" target="_blank" class="fa fa-instagram"></a>
        <a href="https://www.linkedin.com/in/nomvuyiseko-mpofu-0a782b117/" target="_blank" class="fa fa-linkedin"></a>
        <a href="https://github.com/SekoM1/PORTFOLIO" target="_blank" class="fa fa-github"></a>
      </div>

      <div class="copyright">
        © Copyright <strong><span>Nomvuyiseko</span></strong>. All Rights Reserved
      </div>

    </div>
  </footer>
 
</template>


<style scoped>
#footer {
  background: beige;
  padding: 30px 0;
  color: #8685E0;
  font-size: 14px;
  text-align: center;
  box-shadow: rgb(34, 19, 9);
}
/* social media btns */
.fa-instagram {
  background-color: #8686e0;

  color: beige;
  border-radius: 50%;
}
.fa-github {
  background-color: #8686e0;

  color: beige;
  border-radius: 50%;
}
.fa-linkedin {
  background-color: #8686e0;
  color: beige;
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



</style>