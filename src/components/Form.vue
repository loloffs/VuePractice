<template>
    <div id="contactQuoteContainer">
      <div id="contactForm">
        <h1 class="heading" type="text">Thank you for your interest in working at {{ companyName }}</h1>
        <h3 class="subheading" type="text">Please fill in the relevant information</h3>  
        <form
          name=”ApplicationForm”
          onsubmit="return confirm('Do you really want to submit the form?');"
        >
          <div id="nameQuote">
            <input id="firstName" class="quoteInput" name="firstName" placeholder="First Name">
            <input id="lastName" class="quoteInput" name="lastName" placeholder="Last Name">
          </div>
          <div id="contactQuote">
            <input id="email" class="quoteInput" name="email" placeholder="Email">
            <input id="phone" class="quoteInput" name="phone" placeholder="Phone Number">
          </div>
          <div class="homeAddress">
            <input id="homeAddressInput" name="address" placeholder="Home Address">
            <input id="homeAddressInput" name="address" placeholder="City">
            <input id="homeAddressInput" name="address" placeholder="Postal Code">
          </div>
          <div>
            <textarea class="whyWorkHere" rows="4" cols="50" :placeholder="`Why do you want to work at ${companyName}?`"></textarea>
          </div>
          <div id="checkBoxes">
              <input class="checkboxOptions" type="checkbox" value="new"> I am a {{ citizenship }} citizen<br>
              <input class="checkboxOptions" type="checkbox" value="reno"> I require visa sponsorship<br>       
              <input class="checkboxOptions" type="checkbox" value="other"> Other<br>       
            </div>
          <div id="dropdownMenu">
            <h3 class="subheading" type="text">How did you hear about the {{ positionTitle }} position with {{ companyName }}?</h3>
            <select id="dropdown" name="choices" >
              <option value="" disabled selected hidden>Select</option>
              <option value="client">Current Employee</option>
              <option value="wom">Word of Mouth</option>
              <option value="google">Job Board</option>
              <option value="Other">Other</option>
            </select>
            <input id="submitButton" name="dropdown" type="submit" value="Submit">
          </div>
        </form>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Form',
  props: {
    companyName: String,
    positionTitle: String,
    citizenship: String
    // subheading: String,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
  /* background-color: #2c5370; */
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
#container {
  display: flex;
  justify-content: center;
  /* position: relative; */
}
#mainImg {
  /* margin-top: 4px; */
  width: 90%;
}
#contactForm {
  margin-left: 2.5em;
}
#contactQuoteContainer {
  display: flex;
  flex-direction: row;
}
</style>
