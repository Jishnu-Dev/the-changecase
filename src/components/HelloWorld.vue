<template>
  <div class="container">
    <div class="page-content">
      <div class="row">
        <div class="col">
          <div class="mb-3">
            <h1 id="title" class="mb-0">{{ welcomeMessage }}</h1>
            <small>Convert text between different cases</small>
          </div>
          <div class="d-flex flex-column align-items-center">
            <div class="input-group input-box mb-3">
              <input
                id="user-input"
                type="text"
                v-model="userInput"
                class="form-control"
                placeholder="Enter text to convert"
                aria-label="Recipient's username"
                aria-describedby="button-addon2">
              <button
                class="btn btn-dark"
                type="button"
                onclick="document.getElementById('user-input').value = ''; document.getElementById('user-output').value = ''; ">Clear</button>
            </div>
            <div class="input-group input-box mb-3">
              <input
                id="user-output"
                type="text"
                class="form-control"
                placeholder="Converted text appears here"
                aria-label="Recipient's username"
                aria-describedby="button-addon3">
              <button
                id="copy-btn"
                class="btn btn-primary"
                type="button"
                @click="copyText(); showAlert();">
                Copy
                </button>
            </div>
          </div>
          <div>
          </div>
          <div class="button-block">
            <button type="button" class="btn btn-outline-dark buttons" @click="upperCase()"> UPPER CASE </button>
            <button type="button" class="btn btn-outline-dark buttons" @click="lowerCase()"> lower case </button>
            <button type="button" class="btn btn-outline-dark buttons" @click="titleCase()"> Title Case </button>
            <button type="button" class="btn btn-outline-dark buttons" @click="capitalize()"> Capitalize </button>
            <button type="button" class="btn btn-outline-dark buttons" @click="snakeCase()"> snake_case </button>
            <button type="button" class="btn btn-outline-dark buttons" @click="kebabCase()"> kebab-case </button>
          </div>
          <div id="footer">
          <p>
            <small>
              This tool is a sidehustle project of Jishnu Raj, so it may have its pitfalls of drawbacks.
              I hope this tool will help you do some basic stuff. Thank you for using my website.
            </small>
          </p>
          <p>
            <small>
              Intro illustration from <a href="https://storyset.com" target="_blank">StorySet ❤️</a>  by <a href="https://github.com/Jishnu-Dev" target="_blank">Jishnu Raj ✔️</a>
            </small>
          </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
var v = require('voca');

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
    components: {
    },
  data() {
    return {
      welcomeMessage: 'ChangeCase',
      userInput: ''
    }
  },
  methods: {
    upperCase() {
      var userOutput = this.userInput.toUpperCase()
      document.getElementById('user-output').value = userOutput
    },
    lowerCase() {
      var userOutput = this.userInput.toLowerCase()
      document.getElementById('user-output').value = userOutput
    },
    titleCase() {
      var userOutput = v.titleCase(this.userInput)
      document.getElementById('user-output').value = userOutput
    },
    capitalize() {
      var userOutput = v.capitalize(this.userInput)
      document.getElementById('user-output').value = userOutput
    },
    snakeCase(){
      var userOutput = v.snakeCase(this.userInput)
      document.getElementById('user-output').value = userOutput
    },
    kebabCase(){
      var userOutput = v.kebabCase(this.userInput)
      document.getElementById('user-output').value = userOutput
    },
    copyText () {
      if (document.getElementById('user-output').value !== '') {
        var copyText = document.getElementById('user-output')
        copyText.select()
        copyText.setSelectionRange(0, 99999)
        document.execCommand('copy')
        document.getElementById('copy-btn').innerHTML = 'Copied 👍🏻'
        setTimeout(() => document.getElementById('copy-btn').innerHTML = 'Copy', 1500)
      }
    }
  }
}
</script>

<style scoped>
.page-content {
  margin-right: 14vw !important;
  margin-left: 14vw !important;
}
@media (max-width: 992px) { 
  .page-content {
    margin-right: 2vw !important;
    margin-left: 2vw !important;
  }
}
.button-block > button {
  width: 130.65px !important;
  margin-right: 1rem;
  margin-bottom: 1rem;
}
/* @media (max-width: 768px) {
  .button-block > button {
    margin-bottom: 1rem;
  }
} */
#footer {
  margin-top: 60px;
}
</style>
