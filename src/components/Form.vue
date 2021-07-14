<template>
  <div id="contactQuoteContainer">
    <div id="contactForm">
      <h1 class="heading" type="text">Thank you for your interest in working at {{ companyName }}</h1>
      <h3 class="subheading" type="text">Please fill in the relevant information</h3>  
      <form
        id="applicationSubmit"
        name=”ApplicationForm”
        onsubmit="submitAlert"
        v-on:submit="submit"
      >
        <div id="nameQuote">
          <input type="firstName" v-model="firstName" id="firstName" class="quoteInput" name="firstName" placeholder="First Name" />
          <input type="lastName" v-model="lastName" id="lastName" class="quoteInput" name="lastName" placeholder="Last Name">
        </div>
        <div id="contactQuote">
          <input type="email" v-model="email" id="email" class="quoteInput" name="email" placeholder="Email">
          <input type="phone" v-model="phone" id="phone" class="quoteInput" name="phone" placeholder="Phone Number">
        </div>
        <div class="homeAddress">
          <input type="homeAddress" v-model="homeAddress" id="homeAddressInput" name="address" placeholder="Home Address">
          <input type="city" v-model="city" id="homeAddressInput" name="address" placeholder="City">
          <input type="postalCode" v-model="postalCode" id="homeAddressInput" name="address" placeholder="Postal Code">
        </div>
        <div>
          <textarea type="whyWorkHere" v-model="whyWorkHere" class="whyWorkHere" rows="4" cols="50" :placeholder="`Why do you want to work at ${companyName}?`"></textarea>
        </div>
        <div id="teams">
          <h3 class="subheading" type="text">Which teams would interst you the most?</h3>
            <div class="teamChoice">
            <input type="checkbox" value="Team 1" v-model="teams">
            <label>Front End</label>
          </div>
          <div class="teamChoice">
            <input type="checkbox" value="Team 2" v-model="teams">
            <label>Back End</label>
          </div>
          <div class="teamChoice">
            <input type="checkbox" value="Team 3" v-model="teams">
            <label>Team 3</label>
          </div>
          <div class="teamChoice">
            <input type="checkbox" value="Team 4" v-model="teams">
            <label>Team 4</label>
          </div>
        </div>
        <div id="dropdownMenu">
          <h3 class="subheading" type="text">How did you hear about the {{ positionTitle }} position with {{ companyName }}?</h3>
          <select v-model="dropdown" id="dropdown" name="choices" >
            <option value="" disabled selected hidden>Select</option>
            <option value="Current Employee">Current Employee</option>
            <option value="Word of Mouth">Word of Mouth</option>
            <option value="Job Board">Job Board</option>
            <option value="Other">Other</option>
          </select>
          <br>
          <div id="terms">
            <input v-model="termsConditions" class="checkboxOptions" type="checkbox" value="citizen">
            <label>Agree to terms and conditions</label>
          </div>
          <input id="submitButton" name="dropdown" type="submit" value="Submit">
        </div>
      </form>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        firstName: "",
        lastName: "",
        email: "",
        phone: "",
        homeAddress: "",
        city: "",
        postalCode: "",
        whyWorkHere: "",
        dropdown: "",
        termsConditions: false,
        teams: []
      }
    },
    props: [
      "citizenship",
      "companyName",
      "positionTitle",
    ],
    name: "Form",
    methods: {
      submit: function() {
        alert(
          `First Name: ${this.firstName}\nLast Name: ${this.lastName}\nEmail: ${this.email}\nPhone: ${this.phone}\nLast Home Address: ${this.homeAddress}\nCity: ${this.city}\nPostal Code: ${this.postalCode}\nDescription: ${this.whyWorkHere}\nDropdown: ${this.dropdown}\nTerms and Conditions: ${this.termsConditions}\nTeams: ${this.teams}`
        );
      },
    },
    updated: function () {
      console.log(this.$data)
    }
  }
</script>

<style scoped>
  * {
  scroll-behavior: smooth;
}

.heading {
  display: flex;
  justify-content: left;
  color: grey;
  font-family: 'Helvetica neue';
  font-weight: 200;
  margin-left: .8em;
  margin-top: 2em;
}

.subheading {
  color: grey;
  display: flex;
  opacity: .7;
  font-family: 'Helvetica neue';
  font-weight: 300;
  margin-left: 1.6em;
  margin-bottom: 2em;
  font-weight: 400;
}

#nameQuote {
  margin-left: 1.8em;
  width: 40em;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: stretch;
  margin-top: 1em;
  font-family: 'Helvetica neue';
}

#contactQuote {
  margin-left: 1.8em;
  width: 40em;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: stretch;
  margin-top: 1em;
}

.homeAddress {
  margin-left: 1.8em;
  width: 40em;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: stretch;
  margin-top: 1em;
}

#homeAddressInput {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 2.5em;
  margin-right: 1em;
}

.quoteInput {
  display: flex;
  flex-direction: column;
  width: 70%;
  height: 2.5em;
  margin-right: 1em;
}

#checkBoxes {
  display: block;
  font-family: 'Helvetica neue';
  opacity: .7;
  position: relative;
  margin-left: 1.8em;
  margin-top: 1em;
  cursor: pointer;
  font-size: 1em;
}

#teams {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.teamChoice {
  margin-left: 2em;
}

#terms {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  margin-left: 2em;
}

.whyWorkHere {
  display: flex;
  flex-direction: column;
  font-family: 'Helvetica neue';
  font-size: .9em;
  font-weight: 400;
  width: 43.2em;
  height: 9.5em;
  margin-left: 2em;
  margin-top: 1em;
  resize: none;
  margin-bottom: .5em;
}

#dropdownMenu {
  display: flex;
  flex-direction: column;
  width: 40em;
}

#dropdown {
  margin-left: 2.1em;
  width: 47%;
}

#submitButton {
  margin-left: 1.8em;
  margin-top: 2em;
  width: 10em;
  background-color: #303030;
  border: none;
  color: white;
  padding: .7em 1.4em;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 1.1em;
  font-family: 'Helvetica neue';
  cursor: pointer;
}
#submitButton:hover {
  opacity: .95;
}
#contactForm {
  margin-left: 2.5em;
}
#contactQuoteContainer {
  display: flex;
  flex-direction: row;
}
</style>
