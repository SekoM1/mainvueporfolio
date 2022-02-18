<template>
    
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
      </MDBNavbar>
</template>

<script>
import {
  MDBNavbar,
  MDBNavbarToggler,
  MDBNavbarBrand,
  MDBNavbarNav,
  MDBNavbarItem,
  MDBCollapse,
  MDBDropdown,
  MDBDropdownToggle,
  MDBDropdownMenu,
  MDBDropdownItem,
} from "mdb-vue-ui-kit";
import { ref } from "vue";
export default {
  components: {
    MDBNavbar,
    MDBNavbarToggler,
    MDBNavbarBrand,
    MDBNavbarNav,
    MDBNavbarItem,
    MDBCollapse,
    MDBDropdown,
    MDBDropdownToggle,
    MDBDropdownMenu,
    MDBDropdownItem,
  },
  setup() {
    const collapse5 = ref(false);
    const dropdown8 = ref(false);
    return {
      collapse5,
      dropdown8,
    };
  },
};
</script>

<style>
.navbar {
  box-shadow: rebeccapurple;
  background: rgb(250, 255, 221) !important;
  box-shadow: 0 0 25px 0 rgba(7, 7, 7, 0.37);
  position: fixed !important;

  left: 0 !important;
  top: 0 !important;
  width: 100% !important;
  z-index: 3;

}
.logo {
  height: 90px;
  width: 90px;
  border-radius: 50%;
  border: 4px solid #8686e098;
}
.navbar-light .navbar-nav .nav-link.active:hover {
  /* color: #080808; */
  border-bottom: 2px solid rgba(101, 20, 114, 0.548);
}

.navbar-toggler {
  padding-right: 175px;
  background-color: transparent !important;
}
@media screen and (max-width: 400px) {
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

}
</style>
