<template>
  <div id="contact" class="contact" style="padding-top: 30px">
    <div class="container-xl">
      <div class="setion-title" style="margin-top: 120px">
        <h2>CONTACT</h2>
      </div>
      <div class="row" style="pandding-top: 50px">
        <div class="col-md-8 mx-auto">
          <div class="contact-form" style="padding-top: 30px">
            <h1>GET IN TOUCH WITH ME</h1>
            <p class="hint-text">
              I'd love to hear from you, please drop me a line if you've any
              query.
            </p>

            <form @submit.prevent="submitForm">
              <div class="row">
                <div class="col-sm-6">
                  <div class="form-group">
                    <label for="inputFirstName">First Name</label>
                    <input
                      type="text"
                      name="name"
                      v-model="name"
                      class=""
                      id="inputFirstName"
                      required
                    />
                  </div>
                </div>
                <div class="col-sm-6">
                  <div class="form-group">
                    <label for="inputLastName">Last Name</label>
                    <input
                      type="text"
                      name="lastName"
                      v-model="lastName"
                      class=""
                      id="inputLastName"
                      required
                    />
                  </div>
                </div>
              </div>
              <div class="form-group">
                <label for="inputEmail">Email Address</label>
                <input
                  type="email"
                  name="email"
                  v-model="email"
                  class=""
                  id="inputEmail"
                  required
                />
              </div>
              <div class="form-group">
                <label for="inputMessage">Message</label>
                <textarea
                  class="form-control"
                  name="message"
                  v-model="message"
                  id="inputMessage"
                  rows="5"
                  required
                ></textarea>
              </div>
              <input type="submit" class="butt" value="Submit" />
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: null,
      lastName: null,
      email: null,
      message: null,
    };
  },
  methods: {
    submitForm() {
      console.log(this.name, this.lastName, this.email, this.message)
       fetch("https://sekos-api-project.herokuapp.com/contact", {
        method: "POST",
        headers: { "Content-type": "application/json; charset=UTF-8" },

        body: JSON.stringify({
          name: this.name,
          lastName: this.lastName,
          email: this.email,
          message: this.message,
        }),
      })
        .then((response) => response.json())
        .then((json) => {
          console.log(json);
        
        })
        .catch((err) => console.log(err));
    },
  },
};
</script>

<style scoped>
.contact {
  background: #dcc2ec7a;
  border-radius: none;
  outline: none;
}
form {
  max-width: 720px;
  margin-left: 90px;
  background: transparent;
  text-align: left;
  padding: 40px;
  outline: none;
}
/* .mb-4 {
  display: inline-block;
  margin: 25px 0 15px;
  font-size: 0.6em;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
} */
input {
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid rgb(140, 90, 153);
  background: none;
  outline: none;
}
.form-control .textarea .form-group {
  outline: none;
}

/* input:focus,
form:focus,
.contact:focus {
  border-bottom: 2px solid #341f97;
  width: 300px;
  transition: 0.5s;
} */

.butt {
  background: #8686e098;
  color: rgb(247, 244, 244);
  border-radius: 20px;
  box-shadow: 2px 4px rgba(124, 104, 177, 0.589);
  padding: 10px 20px;
  margin-top: 30px;
  font-weight: bold;
  text-align: center !important;
  border-bottom: none;
}
.form-control {
  border-radius: none;
  border: 1px solid rgb(140, 90, 153);
  background: beige;
}
.form-group {
  padding-bottom: 40px;
}
</style>
