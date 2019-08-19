<template>
  <div class="offer-wrapper">
    <div class="contact-container">
      <form class="form">
        <h1>
          Masz pytania?
          <span>
            <img class="small-envelope" src="../assets/images/Envelope.svg" />
          </span>
        </h1>
        <h3>Chcesz dowiedzieć sie więcej? Pisz do nas.</h3>
        <input id="mail" class="sm-input" type="email" placeholder="Email" />
        <input id="subject" class="sm-input" type="text" placeholder="Temat" />
        <textarea id="content" class="big-input" placeholder="Treść" />
        <button class="send-btn" type="button" @click="sendMail()">Send</button>
      </form>
      <img class="big-envelope" src="../assets/images/Envelope.svg" />
    </div>
    <Footer />
  </div>
</template>

<script>
import Axios from 'axios'
import Swal from 'sweetalert2'

import Footer from '~/components/Footer'

export default {
  components: {
    Footer
  },
  methods: {
    sendMail() {
      const subject = document.querySelector('#subject').value
      const mail = document.querySelector('#mail').value
      const content = document.querySelector('#content').value
      // Local mail client version
      // const link = document.createElement('a')
      // link.setAttribute(
      //   'href',
      //   `mailto:kuba300698@gmail.com?subject=${subject}&body=${content}`
      // )
      // link.click()
      // link.remove()
      const data = {
        mail,
        subject,
        body: content
      }
      console.log(data)
      Axios.post('http://localhost:3001/mail', data).then((res) => {
        if (res) {
          Swal.fire({ type: 'success', title: 'Wiadomość wysłana!' })
          document.querySelector('Form').reset()
        } else {
          Swal.fire({ type: 'error', title: 'Ups! Coś poszło nie tak' })
        }
      })
      Swal.fire({ type: 'info', title: 'Wysyłanie' })
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
