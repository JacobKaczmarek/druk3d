<template>
  <div class="offer-wrapper">
    <div class="contact-container">
      <form class="form" action>
        <h1>Masz pytania?</h1>
        <h3>Chcesz dowiedzieć sie więcej? Pisz do nas.</h3>
        <input id="subject" class="sm-input" type="text" placeholder="Temat" />
        <textarea id="content" class="big-input" placeholder="Treść" />
        <button class="send-btn" @click="sendMail()">Send</button>
      </form>
      <img src="../assets/images/Envelope.svg" />
    </div>
    <img class="wave" src="../assets/images/Wave.svg" alt />
  </div>
</template>

<script>
export default {
  methods: {
    sendMail() {
      const subject = document.querySelector('#subject').value
      console.log(subject)
      const content = document.querySelector('#content').value
      const link = document.createElement('a')
      link.setAttribute(
        'href',
        `mailto:kuba300698@gmail.com?subject=${subject}&body=${content}`
      )
      link.click()
    }
  }
}
</script>

<style scoped>
.offer-wrapperr {
  width: 100%;
}
.contact-container {
  display: flex;
  justify-content: space-between;
  width: 80%;
  height: 60vh;
  margin: 10px auto;
}

.form {
  display: flex;
  flex-direction: column;
}

.sm-input,
.big-input {
  border: #707070;
  box-shadow: none;
  width: 400px;
  margin-top: 25px;
  padding: 5px;
  border-bottom: 2px solid #707070;
}

.big-input {
  width: 700px;
  height: 500px;
  border: 2px solid #707070;
  text-align: top;
}

.wave {
  position: absolute;
  bottom: -90px;
  left: 0;
  width: 100vw;
}

.send-btn {
  font-size: 23px;
  color: white;
  background: #51c4f5;
  width: 100px;
  margin-top: 30px;
  padding: 10px 20px;
  border: none;
  text-decoration: none;
}

input:focus,
select:focus,
textarea:focus,
button:focus {
  outline: none;
}
</style>
