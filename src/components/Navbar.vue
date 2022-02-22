<template>
<!--     
      <MDBNavbar expand="lg" light bg="light">

        <MDBNavbarToggler
          target="#navbarRightAlignExample"
          @click="collapse5 = !collapse5"
        ></MDBNavbarToggler>
        <MDBNavbarBrand href="#home">
          <img
            class="logo"
            src="../assets/logo.png"
            height="100"
            alt=""
            loading="lazy"
          />
        </MDBNavbarBrand>

        <MDBCollapse v-model="collapse5" id="navbarRightAlignExample">
          <MDBNavbarNav right class="mb-2 mb-lg-0">

            <MDBNavbarItem href="#home" active> Home </MDBNavbarItem>
            <MDBNavbarItem href="#about" active> About </MDBNavbarItem>
            <MDBNavbarItem href="#resume" active> Resume </MDBNavbarItem>
            <MDBNavbarItem href="#projects" active> Projects </MDBNavbarItem>
            <MDBNavbarItem href="#contact" active> Contact </MDBNavbarItem>
          </MDBNavbarNav>
        </MDBCollapse>
      </MDBNavbar> -->


<nav class="navbar navbar-dark navbar-expand-sm bg-dark fixed-top">
        <div class="container">
        <a href="#home" class="navbar-brand">
        <img
            class="logo"
            src="../assets/logo.png"
            height="100"
            alt=""
            loading="lazy">
       &nbsp;
       
        </a>

        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarCollapse">
            <span class="navbar-toggler-icon"></span>
        </button>


        <div id="navbarCollapse" class="collapse navbar-collapse">
        <ul class="navbar-nav ml-auto">
            <li class="nav-item">
                <a href="#home" class="nav-link active">
                    Home
                </a>
            </li>
            <li class="nav-item">
                <a href="#about" class="nav-link active">
                    About
                </a>
            </li>
            <li class="nav-item">
                <a href="#resume" class="nav-link active">
                    Resume
                </a>
            </li>
            <li class="nav-item">
                <a href="#projects" class="nav-link active">
                    Projects
                </a>
            </li>
            <li class="nav-item">
                <a href="#contact" class="nav-link active">
                    Contact
                </a>
            </li>
        </ul>
        </div>
        </div>
        </nav>
</template>



<style scoped>
.navbar {
  box-shadow: rebeccapurple;
  background: rgb(250, 255, 221) !important;
  box-shadow: 0 0 25px 0 rgba(7, 7, 7, 0.37);
  position: fixed !important;
/* 
  left: 0 !important;
  top: 0 !important;
  width: 100% !important;
  z-index: 3; */

}
.logo {
  height: 90px;
  width: 90px;
  border-radius: 50%;
  border: 4px solid #8686e098;
}
.navbar-dark .nav-link.active:hover {
  /* color: #080808; */
  border-bottom: 2px solid rgba(101, 20, 114, 0.548);
}
a.nav-link.active{
  color: black !important;
}
.navbar-toggler-icon {
 
  background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' width='30' height='30' viewBox='0 0 30 30'%3e%3cpath stroke='rgba%28255, 255, 255, 0.5%29' stroke-linecap='round' stroke-miterlimit='10' stroke-width='2' d='M4 7h22M4 15h22M4 23h22'/%3e%3c/svg%3e");
  backface-visibility: visible;
  background-color: #afaca375;
}
/* @media screen and (max-width: 400px) {
  .logo {
    height: 70px;
    width: 70px;
    border-radius: 50%;
  }
}
@media screen and (min-width: 990px) {
  .navbar-brand {
    padding-left: 5%;
  }
  .navbar-expand-lg .navbar-collapse {
    padding-right: 5%;
  }

} */
</style>
