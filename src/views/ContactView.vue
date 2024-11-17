<template>
  <section>
    <div class="container">
      <div class="page-container">
        <div class="content-wrap">
          <h1 class="display-3 section-title color">Contact me</h1>
          <div class="main-container">
            <p class="smspecial">
              “Alone we can do so little; together we can do so much.” — Helen
              Keller
            </p>
            <!-- <p>
              If you have a request or question, don’t hesitate to use the form.
            </p> -->
            <div class="form-container">
              <form @submit.prevent="submitForm">
                <div class="row g-0 gy-lg-0 gy-3">
                  <div class="col-lg-6 h-100 pe-lg-2">
                    <input
                      type="text"
                      name="name"
                      v-model="name"
                      required
                      placeholder="Name"
                      maxlength="50"
                      class="color"
                    />
                    <textarea
                      name="message"
                      v-model="message"
                      required
                      placeholder="Message"
                      class="color"
                    ></textarea>
                  </div>
                  <div class="col-lg-6 ps-lg-2 pb-0">
                    <input
                      type="email"
                      name="email"
                      v-model="email"
                      required
                      placeholder="Email"
                      maxlength="50"
                      class="color"
                    />
                    <input type="submit" name="submit" class="color" />
                  </div>
                </div>
              </form>
              <div class="sentMessage" v-if="sentMessage" v-motion-slide-right>
                <p>
                  Thank you for your interest. I will reply as soon as possible.
                  <br />
                  <strong><em>Live Life!</em></strong>
                </p>
              </div>
            </div>
          </div>
        </div>
        <footer>
          <div>
            <a href="https://linkedin.com/in/geo-sudo/" target="_blank"
              ><svg
                class="color"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 448 512"
              >
                <!--! Font Awesome Pro 6.2.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                <path
                  d="M416 32H31.9C14.3 32 0 46.5 0 64.3v383.4C0 465.5 14.3 480 31.9 480H416c17.6 0 32-14.5 32-32.3V64.3c0-17.8-14.4-32.3-32-32.3zM135.4 416H69V202.2h66.5V416zm-33.2-243c-21.3 0-38.5-17.3-38.5-38.5S80.9 96 102.2 96c21.2 0 38.5 17.3 38.5 38.5 0 21.3-17.2 38.5-38.5 38.5zm282.1 243h-66.4V312c0-24.8-.5-56.7-34.5-56.7-34.6 0-39.9 27-39.9 54.9V416h-66.4V202.2h63.7v29.2h.9c8.9-16.8 30.6-34.5 62.9-34.5 67.2 0 79.7 44.3 79.7 101.9V416z"
                /></svg
            ></a>
            <a href="https://x.com/Geo_sudo" target="_blank"
              ><svg
                class="color"
                mlns="http://www.w3.org/2000/svg"
                viewBox="0 0 512 512"
              >
                <path
                  d="M389.2 48h70.6L305.6 224.2 487 464H345L233.7 318.6 106.5 464H35.8L200.7 275.5 26.8 48H172.4L272.9 180.9 389.2 48zM364.4 421.8h39.1L151.1 88h-42L364.4 421.8z"
                /></svg
            ></a>
            <a href="https://github.com/Geo-sudo/" target="_blank"
              ><svg
                class="color"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 496 512"
              >
                <!--! Font Awesome Pro 6.2.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                <path
                  d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"
                /></svg
            ></a>

            <a href="javascript:void(0)" @click="copyEmail">
              <svg
                class="color"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 512 512"
              >
                <path
                  d="M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48L48 64zM0 176L0 384c0 35.3 28.7 64 64 64l384 0c35.3 0 64-28.7 64-64l0-208L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z"
                />
              </svg>
            </a>
            <div
              v-if="showConfirmation"
              :class="{ 'confirmation-message': true, 'fade-out': isFadingOut }"
            >
              Email copied to clipboard!
            </div>
          </div>
        </footer>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ContactView",
  props: ["themeColor"],
  data() {
    return {
      sentMessage: false,
      showConfirmation: false,
      isFadingOut: false,
      name: "",
      email: "",
      subject: "",
      message: "",
    };
  },
  methods: {
    showSentMessage() {
      this.sentMessage = true;
      setTimeout(() => {
        this.sentMessage = false;
      }, 5000);
    },
    async submitForm() {
      // Validation: Check if fields are empty
      if (!this.name || !this.email || !this.message) {
        return alert("Please fill in all fields");
      }

      const WEB3FORMS_ACCESS_KEY = "837bf8f1-5b44-4405-9f54-fc8f03a60d0a";

      const response = await fetch("https://api.web3forms.com/submit", {
        method: "POST",
        headers: {
          "Content-Type": "application/json",
          Accept: "application/json",
        },
        body: JSON.stringify({
          access_key: WEB3FORMS_ACCESS_KEY,
          name: this.name,
          email: this.email,
          message: this.message,
        }),
      });

      const result = await response.json();

      if (result.success) {
        this.showSentMessage();
        // Reset form fields
        this.name = "";
        this.email = "";
        this.message = "";
      } else {
        alert("An error occurred. Please try again later.");
      }
    },
    copyEmail() {
      const email = "george.nady.contact@gmail.com";
      navigator.clipboard
        .writeText(email)
        .then(() => {
          this.showConfirmation = true;
          this.isFadingOut = false;

          setTimeout(() => {
            this.isFadingOut = true;
          }, 2000);

          // Completely hide after fade-out
          setTimeout(() => {
            this.showConfirmation = false;
          }, 3000); // 1000ms for fade-out duration
        })
        .catch((err) => {
          console.error("Failed to copy email: ", err);
        });
    },
  },
  mounted() {
    Array.from(document.getElementsByClassName("color")).forEach((element) => {
      element.classList.add(this.themeColor);
    });
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";

.page-container {
  position: relative;
  min-height: 88vh;
  .content-wrap {
    padding-bottom: 100px;
    width: fit-content;
    margin-left: auto;
    margin-right: auto;
    text-align: center;
    h1 {
      margin-left: auto;
      margin-right: auto;
    }
  }
  footer {
    position: absolute;
    bottom: 0;
    margin-left: auto;
    margin-right: auto;
    height: fit-content;
    width: 100%;
    div {
      display: flex;
      align-items: center;
      justify-content: center;
      a {
        text-decoration: none;
        transition: 0.3s;
        margin-left: 0.75rem;
        margin-right: 0.75rem;
        svg {
          @include generateColorsDarken("fill", 7);
          width: 25px;
          transition: 0.3s;
          &:hover {
            @include generateColors("fill");
          }
        }
      }
    }
  }
}

.main-container {
  margin-top: 1.5rem;
  // padding-left: 1.5rem;
  & > p.smspecial {
    font-size: 1.1rem;
    font-style: italic;
  }
  & > p:not(.smspecial) {
    font-size: 0.9rem;
  }
  .form-container {
    margin-top: 3rem;
    width: 100%;
    max-width: 900px;
    form {
      .row {
        width: 100%;
      }
      input,
      textarea {
        width: 100%;
        background-color: darken($color: $main-bg-color, $amount: 2);
        border: 1px solid;
        @include generateColorsDarken("border-color", 20);
        color: white;
        margin-bottom: 1rem;
        padding: 0.5rem 0.75rem;
        transition: 0.2s;
        &:last-child {
          margin-bottom: 0;
        }
        &:focus,
        &:focus-visible {
          @include generateColors("border-color");
          outline: none;
        }
      }
      input {
        height: 50px;
      }
      textarea {
        height: 100%;
        min-height: 175px;
        max-height: 250px;
        resize: vertical;
        margin: 0;
      }
      input[type="submit"] {
        &:hover {
          border: 3px solid;
          border-color: $main-bg-color;
          @include generateColorsDarken("background-color", 10);
        }
      }
    }
  }
  .sentMessage {
    margin-top: 2rem;
    font-size: 1rem;
    width: 100%;
    text-align: center;
  }
}

@media (max-width: 991.98px) {
  .page-container {
    min-height: unset !important;
  }
  .main-container {
    .form-container {
      form {
        textarea {
          height: 100px;
          min-height: 100px;
        }
      }
    }
  }
}

.confirmation-message {
  position: fixed;
  bottom: 20px;
  background-color: #4caf50;
  color: white;
  padding: 10px 20px;
  border-radius: 15px;
  font-size: 14px;
  text-align: center;
  opacity: 1;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: opacity 1s ease-in-out;
  z-index: 1000;
}

.confirmation-message.fade-out {
  opacity: 0;
}
</style>
