<template>
  <div class="offer-wrapper">
    <div class="contact-container">
      <form class="form" @submit="sendMail()">
        <h1>
          Masz pytania?
          <span>
            <img class="small-envelope" src="../assets/images/Envelope.svg" />
          </span>
        </h1>
        <h3>Chcesz dowiedzieć sie więcej? Pisz do nas.</h3>
        <input id="subject" class="sm-input" type="text" placeholder="Temat" />
        <textarea id="content" class="big-input" placeholder="Treść" />
        <button class="send-btn" type="submit">Send</button>
      </form>
      <img class="big-envelope" src="../assets/images/Envelope.svg" />
    </div>
    <Footer />
  </div>
</template>

<script>
import Footer from '~/components/Footer'

export default {
  components: {
    Footer
  },
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
      link.remove()
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
  align-items: center;
  width: 80%;
  margin: 10px auto;
}

.form {
  display: flex;
  flex-direction: column;
  height: 500px;
}

.big-envelope {
  margin-left: 30px;
}

.small-envelope {
  display: none;
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
  height: 400px;
  border: 2px solid #707070;
  text-align: top;
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
  z-index: 1;
  cursor: pointer;
}

input:focus,
select:focus,
textarea:focus,
button:focus {
  outline: none;
}

@media screen and (max-width: 765px) {
  .small-envelope {
    display: inline-block;
    max-width: 40px;
    transform: translateY(10px);
  }

  .form {
    width: 90%;
  }

  .big-envelope {
    display: none;
  }

  .sm-input,
  .big-input {
    width: 100%;
  }

  .big-input {
    height: 200px;
  }
}
</style>
