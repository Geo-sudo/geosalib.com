<template>
  <section>
    <div class="container">
      <h1 class="display-3 section-title color">Skills & Experience</h1>
      <div class="row mt-5 ms-2">
        <div class="col-lg-8">
          <p>
            Yes, I'm a Jack of All Trades. It's empowering! From 3D Modeling to
            Cyber Security to Electronics, and even (Computational)
            Astrophysics, I've done it all!
          </p>
          <p>
            However, my main focus is Astrophysics and Cyber Security. Well,
            what will you choose, Geo? I might choose one or combine the two:
            satellite security researcher? I might delve into a completely
            different field...or a related one. Only Time will tell, and that's
            exciting!
          </p>
          <p>
            Want to collaborate? Don't hesitate to
            <router-link to="/contact">contact me</router-link>!
          </p>
        </div>
      </div>
      <div class="timeline color mt-5">
        <div class="year" data-year="2019" v-motion-slide-right>
          <div class="row g-4">
            <div class="col-lg-4">
              <div class="card w-100">
                <div class="card-img-top">
                  <div class="icon-container">
                    <svg
                      class="color"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 512 512"
                    >
                      <path
                        d="M234.5 5.7c13.9-5 29.1-5 43.1 0l192 68.6C495 83.4 512 107.5 512 134.6l0 242.9c0 27-17 51.2-42.5 60.3l-192 68.6c-13.9 5-29.1 5-43.1 0l-192-68.6C17 428.6 0 404.5 0 377.4L0 134.6c0-27 17-51.2 42.5-60.3l192-68.6zM256 66L82.3 128 256 190l173.7-62L256 66zm32 368.6l160-57.1 0-188L288 246.6l0 188z"
                      />
                    </svg>
                  </div>
                </div>
                <div class="card-body">
                  <h4 class="card-title">3D Modelling</h4>
                  <p class="card-text">
                    My journey started with 3D Modelling in Blender
                    <strong
                      ><em>{{ current_year - 2019 }} years ago</em></strong
                    >. I did all sorts of projects from abstract art to game
                    objects. This sparked the creationist inside me, and got me
                    dappling in Music Production and Game Development (and
                    consequently programming).
                  </p>
                </div>
              </div>
            </div>
            <div class="col-lg-4"></div>
          </div>
        </div>
        <div
          class="year"
          data-year="2020"
          v-motion-slide-visible-once-right
          v-motion-slide-right
        >
          <div class="row g-4">
            <div class="col-lg-4">
              <div class="card">
                <div class="card-img-top">
                  <div class="icon-container">
                    <svg
                      class="color"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 448 512"
                    >
                      <path
                        d="M439.8 200.5c-7.7-30.9-22.3-54.2-53.4-54.2h-40.1v47.4c0 36.8-31.2 67.8-66.8 67.8H172.7c-29.2 0-53.4 25-53.4 54.3v101.8c0 29 25.2 46 53.4 54.3 33.8 9.9 66.3 11.7 106.8 0 26.9-7.8 53.4-23.5 53.4-54.3v-40.7H226.2v-13.6h160.2c31.1 0 42.6-21.7 53.4-54.2 11.2-33.5 10.7-65.7 0-108.6zM286.2 404c11.1 0 20.1 9.1 20.1 20.3 0 11.3-9 20.4-20.1 20.4-11 0-20.1-9.2-20.1-20.4 .1-11.3 9.1-20.3 20.1-20.3zM167.8 248.1h106.8c29.7 0 53.4-24.5 53.4-54.3V91.9c0-29-24.4-50.7-53.4-55.6-35.8-5.9-74.7-5.6-106.8 .1-45.2 8-53.4 24.7-53.4 55.6v40.7h106.9v13.6h-147c-31.1 0-58.3 18.7-66.8 54.2-9.8 40.7-10.2 66.1 0 108.6 7.6 31.6 25.7 54.2 56.8 54.2H101v-48.8c0-35.3 30.5-66.4 66.8-66.4zm-6.7-142.6c-11.1 0-20.1-9.1-20.1-20.3 .1-11.3 9-20.4 20.1-20.4 11 0 20.1 9.2 20.1 20.4s-9 20.3-20.1 20.3z"
                      />
                    </svg>
                  </div>
                </div>
                <div class="card-body">
                  <h4 class="card-title">Python</h4>
                  <p class="card-text">
                    Used it in many projects and is my go-to language. In
                    addition to small projects, made a smart home system that
                    utilizes actuators, a Raspberry Pi, and Twillio's API; a
                    script for calculating and visualizing galaxy density
                    profiles using Numpy and Matplotlib; and a realistic
                    simulation framework for any N-body system.
                  </p>
                </div>
              </div>
            </div>
            <div class="col-lg-4">
              <div class="card">
                <div class="card-img-top">
                  <div class="icon-container">
                    <svg
                      class="color"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 512 512"
                    >
                      <path
                        d="M0 224L0 416c0 17.7 14.3 32 32 32l64 0 0-112c0-8.8 7.2-16 16-16s16 7.2 16 16l0 112 64 0 0-112c0-8.8 7.2-16 16-16s16 7.2 16 16l0 112 64 0 0-112c0-8.8 7.2-16 16-16s16 7.2 16 16l0 112 64 0 0-112c0-8.8 7.2-16 16-16s16 7.2 16 16l0 112 64 0c17.7 0 32-14.3 32-32l0-192c0-17.7-14.3-32-32-32l-32 0 0-32c0-17.7-14.3-32-32-32l-32 0 0-32c0-17.7-14.3-32-32-32L160 64c-17.7 0-32 14.3-32 32l0 32-32 0c-17.7 0-32 14.3-32 32l0 32-32 0c-17.7 0-32 14.3-32 32z"
                      />
                    </svg>
                  </div>
                </div>
                <div class="card-body">
                  <h4 class="card-title">Networking</h4>
                  <p class="card-text">
                    Studied for the Cisco Certified Network Associate (CCNA)
                    Certificate using Jeremy's IT Lab, but didn't take it due to
                    financial limitations.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="year" data-year="2021" v-motion-slide-visible-once-right>
          <div class="row g-4">
            <div class="col-lg-4">
              <div class="card">
                <div class="card-img-top">
                  <div class="icon-container">
                    <svg
                      class="color"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 448 512"
                    >
                      <path
                        d="M224 16c-6.7 0-10.8-2.8-15.5-6.1C201.9 5.4 194 0 176 0c-30.5 0-52 43.7-66 89.4C62.7 98.1 32 112.2 32 128c0 14.3 25 27.1 64.6 35.9c-.4 4-.6 8-.6 12.1c0 17 3.3 33.2 9.3 48l-59.9 0C38 224 32 230 32 237.4c0 1.7 .3 3.4 1 5l38.8 96.9C28.2 371.8 0 423.8 0 482.3C0 498.7 13.3 512 29.7 512l388.6 0c16.4 0 29.7-13.3 29.7-29.7c0-58.5-28.2-110.4-71.7-143L415 242.4c.6-1.6 1-3.3 1-5c0-7.4-6-13.4-13.4-13.4l-59.9 0c6-14.8 9.3-31 9.3-48c0-4.1-.2-8.1-.6-12.1C391 155.1 416 142.3 416 128c0-15.8-30.7-29.9-78-38.6C324 43.7 302.5 0 272 0c-18 0-25.9 5.4-32.5 9.9c-4.8 3.3-8.8 6.1-15.5 6.1zm56 208l-12.4 0c-16.5 0-31.1-10.6-36.3-26.2c-2.3-7-12.2-7-14.5 0c-5.2 15.6-19.9 26.2-36.3 26.2L168 224c-22.1 0-40-17.9-40-40l0-14.4c28.2 4.1 61 6.4 96 6.4s67.8-2.3 96-6.4l0 14.4c0 22.1-17.9 40-40 40zm-88 96l16 32L176 480 128 288l64 32zm128-32L272 480 240 352l16-32 64-32z"
                      />
                    </svg>
                  </div>
                </div>
                <div class="card-body">
                  <h4 class="card-title">Cyber Security</h4>
                  <p class="card-text">
                    Started learning it
                    <strong
                      ><em>{{ current_year - 2020 }} years</em></strong
                    >
                    ago through TryHackMe and Hack The Box. Taught 4 students in
                    an intensive 4-week boot camp and
                    <strong
                      ><em
                        >mentored 20 mentees in 13 weekly sessions</em
                      ></strong
                    >
                    in 2023/2024 as a Cyber Security Mentor at the
                    <a target="_blank" href="https://stemegypt.hackclub.com"
                      >STEM Egypt Hack Club</a
                    >.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="year" data-year="2022" v-motion-slide-visible-once-right>
          <div class="row g-4">
            <div class="col-lg-4">
              <div class="card">
                <div class="card-img-top">
                  <div class="icon-container">
                    <svg
                      class="color"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 640 512"
                    >
                      <path
                        d="M320 0c17.7 0 32 14.3 32 32l0 64 120 0c39.8 0 72 32.2 72 72l0 272c0 39.8-32.2 72-72 72l-304 0c-39.8 0-72-32.2-72-72l0-272c0-39.8 32.2-72 72-72l120 0 0-64c0-17.7 14.3-32 32-32zM208 384c-8.8 0-16 7.2-16 16s7.2 16 16 16l32 0c8.8 0 16-7.2 16-16s-7.2-16-16-16l-32 0zm96 0c-8.8 0-16 7.2-16 16s7.2 16 16 16l32 0c8.8 0 16-7.2 16-16s-7.2-16-16-16l-32 0zm96 0c-8.8 0-16 7.2-16 16s7.2 16 16 16l32 0c8.8 0 16-7.2 16-16s-7.2-16-16-16l-32 0zM264 256a40 40 0 1 0 -80 0 40 40 0 1 0 80 0zm152 40a40 40 0 1 0 0-80 40 40 0 1 0 0 80zM48 224l16 0 0 192-16 0c-26.5 0-48-21.5-48-48l0-96c0-26.5 21.5-48 48-48zm544 0c26.5 0 48 21.5 48 48l0 96c0 26.5-21.5 48-48 48l-16 0 0-192 16 0z"
                      />
                    </svg>
                  </div>
                </div>
                <div class="card-body">
                  <h4 class="card-title">Robotics & Electronics</h4>
                  <p class="card-text">
                    Tinkered with them to make school projects during each
                    semester: a smart home system written in
                    <strong><em>Python</em></strong> and controlled by a
                    <strong><em>Raspberry Pi</em></strong> that utilizes pumps,
                    motors, and warning systems to detect and put out fires, and
                    notify the authorities using
                    <strong><em>Twillio's API</em></strong
                    >; and an automatic water purification system written in
                    <strong><em>C++</em></strong> and controlled by an
                    <strong><em>Arduino UNO</em></strong> that uses pumps,
                    relays, and motors to control a water treatment plant
                    system.
                  </p>
                </div>
              </div>
            </div>
            <div class="col-lg-4">
              <div class="card">
                <div class="card-img-top">
                  <div class="icon-container">
                    <svg
                      class="cpp-logo color"
                      version="1.1"
                      id="Layer_1"
                      xmlns="http://www.w3.org/2000/svg"
                      xmlns:xlink="http://www.w3.org/1999/xlink"
                      x="0px"
                      y="0px"
                      width="306px"
                      height="344.35px"
                      viewBox="0 0 306 344.35"
                      enable-background="new 0 0 306 344.35"
                      xml:space="preserve"
                    >
                      <path
                        class="color"
                        fill="#00599C"
                        d="M302.107,258.262c2.401-4.159,3.893-8.845,3.893-13.053V99.14c0-4.208-1.49-8.893-3.892-13.052L153,172.175
	L302.107,258.262z"
                      />
                      <path
                        class="color"
                        fill="#004482"
                        d="M166.25,341.193l126.5-73.034c3.644-2.104,6.956-5.737,9.357-9.897L153,172.175L3.893,258.263
	c2.401,4.159,5.714,7.793,9.357,9.896l126.5,73.034C147.037,345.401,158.963,345.401,166.25,341.193z"
                      />
                      <path
                        class="color"
                        fill="#659AD2"
                        d="M302.108,86.087c-2.402-4.16-5.715-7.793-9.358-9.897L166.25,3.156c-7.287-4.208-19.213-4.208-26.5,0
	L13.25,76.19C5.962,80.397,0,90.725,0,99.14v146.069c0,4.208,1.491,8.894,3.893,13.053L153,172.175L302.108,86.087z"
                      />
                      <g>
                        <path
                          fill="#FFFFFF"
                          d="M153,274.175c-56.243,0-102-45.757-102-102s45.757-102,102-102c36.292,0,70.139,19.53,88.331,50.968
		l-44.143,25.544c-9.105-15.736-26.038-25.512-44.188-25.512c-28.122,0-51,22.878-51,51c0,28.121,22.878,51,51,51
		c18.152,0,35.085-9.776,44.191-25.515l44.143,25.543C223.142,254.644,189.294,274.175,153,274.175z"
                        />
                      </g>
                      <g>
                        <polygon
                          fill="#FFFFFF"
                          points="255,166.508 243.666,166.508 243.666,155.175 232.334,155.175 232.334,166.508 221,166.508 
		221,177.841 232.334,177.841 232.334,189.175 243.666,189.175 243.666,177.841 255,177.841 	"
                        />
                      </g>
                      <g>
                        <polygon
                          fill="#FFFFFF"
                          points="297.5,166.508 286.166,166.508 286.166,155.175 274.834,155.175 274.834,166.508 263.5,166.508 
		263.5,177.841 274.834,177.841 274.834,189.175 286.166,189.175 286.166,177.841 297.5,177.841 	"
                        />
                      </g>
                    </svg>
                  </div>
                </div>
                <div class="card-body">
                  <h4 class="card-title">C++</h4>
                  <p class="card-text">
                    Picked it up to improve problem-solving skills along with
                    learning algorithms and data structures. Used it for a while
                    practising on <strong>CodeForces</strong>. Passed the
                    qualification round of <strong>ECPC</strong>.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="year" data-year="2023" v-motion-slide-visible-once-right>
          <div class="row g-4">
            <div class="col-lg-4">
              <div class="card">
                <div class="card-img-top">
                  <div class="icon-container">
                    <svg
                      class="color"
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 512 512"
                    >
                      <path
                        d="M493.7 .9L299.4 75.6l2.3-29.3c1-12.8-12.8-21.5-24-15.1L101.3 133.4C38.6 169.7 0 236.6 0 309C0 421.1 90.9 512 203 512c72.4 0 139.4-38.6 175.7-101.3L480.8 234.3c6.5-11.1-2.2-25-15.1-24l-29.3 2.3L511.1 18.3c.6-1.5 .9-3.2 .9-4.8C512 6 506 0 498.5 0c-1.7 0-3.3 .3-4.8 .9zM192 192a128 128 0 1 1 0 256 128 128 0 1 1 0-256zm0 96a32 32 0 1 0 -64 0 32 32 0 1 0 64 0zm16 96a16 16 0 1 0 0-32 16 16 0 1 0 0 32z"
                      />
                    </svg>
                  </div>
                </div>
                <div class="card-body">
                  <h4 class="card-title">Astrophysics</h4>
                  <p class="card-text">
                    Participated in the International Astronomy and Astrophysics
                    Competition (IAAC) twice. Ranked
                    <strong><em>top 3% of 5040</em></strong> participants (Gold
                    Medal) in 2024 and
                    <strong><em>top 20% of 4500</em></strong> participants
                    (Silver Medal) in 2023. Made a script for calculating and
                    visualizing galaxy density profiles through a modified
                    version of Sérsic profile using Numpy and Matplotlib.
                    Created a framework for simulating N-body Lagrangian
                    Newtonian physics in Python. Check them out
                    <a
                      target="_blank"
                      href="https://github.com/Geo-sudo/Computational-Astrophysics/"
                      >Here</a
                    >!
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "SkillsView",
  props: ["themeColor"],
  data() {
    return {
      current_year:
        new Date().getMonth() < 6
          ? new Date().getFullYear()
          : new Date().getFullYear() + 1,
    };
  },
  mounted() {
    Array.from(document.getElementsByClassName("color")).forEach((element) => {
      element.classList.add(this.themeColor);
    });
  },
};
</script>

<style lang="scss">
@import "../assets/scss/_variables.scss";

.container {
  padding-top: 4rem;
  padding-bottom: 1rem;
  .section-title {
    font-weight: bold;
    @include generateColors("box-shadow", "inset 0 0 0 0");
    //  box-shadow: inset 0 0 0 0 nth($list: $colors, $n: $i);
    @include generateColorsLighten("color", 5);
    // color: lighten($color: $my-red-color, $amount: 5);
    transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
    width: fit-content;
    &:hover {
      @include generateColors("box-shadow", "inset 15ch 0 0 0");
      // box-shadow: inset 15ch 0 0 0 $my-red-color;
      color: white;
    }
  }
  a {
    @include generateColorsLighten("color", 15);
    // color: lighten($color: $my-red-color, $amount: 15);
    text-decoration: none;
    transition: 0.2s;
    &:hover {
      @include generateColorsLighten("color", 7);
      // color: lighten($color: $my-red-color, $amount: 7);
    }
  }
}

.timeline {
  margin-left: 3rem;
  position: relative;
  @include generateColors("color");
  &::before {
    content: "";
    height: 102%;
    width: 5px;
    // color: white;
    background-color: currentColor;
    // background-color: $my-red-color;
    position: absolute;
    top: -10px;
    left: 0;
    border-radius: 2px;
  }
  .year {
    position: relative;
    padding-left: 2.5rem;
    margin-bottom: 2.5rem;
    color: white;
    &::before {
      content: attr(data-year);
      position: absolute;
      top: 40px;
      left: -55px;
      font-weight: bold;
      font-style: italic;
      letter-spacing: 1.2px;
    }
    &::after {
      content: "";
      position: absolute;
      top: 43px;
      left: -5px;
      width: 15px;
      height: 15px;
      border-radius: 50%;
      border: 2px solid darken($color: $main-bg-color, $amount: 5);
      background-color: #ffffff;
    }
    .card {
      background: lighten($color: $main-bg-color, $amount: 5);
      border: 3px solid darken($color: $main-bg-color, $amount: 5);
      padding: 1rem;
      width: 100%;
      height: max-content;
      .card-img-top {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        height: 100px;
        .icon-container {
          width: fit-content;
          background-color: white;
          padding: 0.75rem;
          border-radius: 50%;
          box-shadow: 5px 5px 3px 0px darken($color: $main-bg-color, $amount: 5);
          transition: 0.2s;
          &:hover {
            box-shadow: 7px 7px 3px 0px
              darken($color: $main-bg-color, $amount: 5);
            transform: scale(1.05);
          }
          svg {
            padding: 2px;
            @include generateColors("fill");
            // fill: $my-red-color;
            width: 50px;
            height: 50px;
            path {
              @include generateColors("fill");
              // fill: $my-red-color;
            }
            rect {
              @include generateColors("fill");
              // fill: $my-red-color;
            }
            &.vue-logo {
              g g:nth-child(2) path {
                @include generateColorsLighten("fill", 20);
                // fill: lighten($color: $my-red-color, $amount: 20);
              }
            }
            &.cpp-logo {
              path:nth-child(1) {
                @include generateColorsLighten("fill", 7);
              }
              path:nth-child(2) {
                @include generateColors("fill");
              }
              path:nth-child(3) {
                @include generateColorsLighten("fill", 15);
              }
            }
          }
        }
      }
      .card-body {
        text-align: center;
        flex-direction: column;
        justify-content: space-evenly;
        .card-text {
          font-size: 0.9rem;
          color: rgba(255, 255, 255, 0.7);
        }
      }
    }
  }
}

@media (max-width: 991.98px) {
  .timeline {
    margin-left: 4rem;
    margin-right: 1rem;
  }
}
</style>
