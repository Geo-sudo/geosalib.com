<template>
  <section class="under-construction">
    <img
      src="@/assets/UnderConstruction.jpg"
      alt="Under Construction"
      class="under-construction-image"
    />
  </section>
</template>

<script>
import bootstrap from "bootstrap/dist/js/bootstrap.min.js";

export default {
  name: "ProjectsView",
  props: ["themeColor"],
  data() {
    return {
      projectViewer: null,
      projectToView: null,
    };
  },
  methods: {
    showProjectViewer(projectToView) {
      // document.getElementById("project-viewer-frame").src = url;
      // document.getElementById("go-to-project").href = url;
      this.projectToView = projectToView;
      this.projectViewer.show();
    },
    hideProjectViewer() {
      this.projectViewer.hide();
    },
    // hideLoader() {
    //   console.log("loaded");
    //   if (document.getElementById("loader")) {
    //     document.getElementById("loader").style.display = "none";
    //   }
    // },
    // showLoader() {
    //   if (document.getElementById("loader")) {
    //     document.getElementById("loader").style.display = "block";
    //   }
    // },
  },
  mounted() {
    Array.from(document.getElementsByClassName("color")).forEach((element) => {
      element.classList.add(this.themeColor);
    });
    this.projectViewer = new bootstrap.Modal(
      document.getElementById("project-viewer")
    );

    document
      .getElementById("project-viewer")
      .addEventListener("hidden.bs.modal", () => {
        // document.getElementById("project-viewer-frame").src = "";
        this.projectToView = null;
      });

    window.addEventListener("popstate", (event) => {
      event.preventDefault();
      event.stopPropagation();
      if (this.projectToView != null) {
        this.projectViewer.hide();
        history.go(1);
      }
    });
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_variables.scss";

.under-construction {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 80vh;

  .under-construction-image {
    max-width: 100%;
    height: auto;
  }
}

p.visit-github {
  margin-top: 3rem;
  letter-spacing: 1px;
  text-align: center;
  color: rgba(255, 255, 255, 0.75);
  a {
    @include generateColors("color");
    svg {
      width: 22px;
      height: 22px;
      fill: currentColor;
    }
    &:hover {
      @include generateColorsDarken("color", 5);
    }
  }
}

.projects-container {
  margin-top: 4rem;
  .project {
    aspect-ratio: 1.5;
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    cursor: pointer;
    transition: 0.2s;
    div {
      transition: 0.3s;
      overflow: hidden;
    }
    .project-thumb {
      width: 100%;
      height: 100%;
      img {
        width: 100%;
        transition: 0.3s;
        margin-top: -15%;
      }
    }
    .view-project {
      @include generateColorsLighten("background-color", 10);
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 50%;
      width: 90px;
      height: 90px;
      color: black;
      font-weight: 300;
      font-size: 0.8rem;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translatex(-50%) translateY(-50%);
      opacity: 0;
    }
    &:hover {
      div {
        filter: grayscale(75%);
        img {
          transform: scale(1.1);
        }
      }
      .view-project {
        opacity: 1;
        filter: grayscale(0%);
      }
    }
  }
}

.other-projects {
  margin-top: 7rem;
  position: relative;
  p.background-title {
    color: rgba(255, 255, 255, 0.2);
    font-weight: bold;
    font-size: 25rem;
    line-height: 1;
    position: absolute;
    top: -130px;
    right: 0;
    // right: 70px;
    pointer-events: none;
  }
  .row {
    margin-top: -0.5rem;
    .card {
      cursor: pointer;
      border: 2px solid;
      // border-color: $my-red-color;
      @include generateColorsDarken("border-color", 5);
      background-color: darken($color: $main-bg-color, $amount: 3);
      text-align: center;
      color: whitesmoke;
      transition: 0.2s;
      height: 100%;
      .card-img-top {
        height: 250px;
        width: auto;
        object-fit: cover;
        transition: 0.2s;
      }
      &:hover {
        color: white;
        .card-img-top {
          filter: contrast(120%);
        }
      }
      .card-body {
        display: flex;
        align-items: center;
        justify-content: space-evenly;
        flex-direction: column;
        .card-text {
          font-size: 0.9em;
          .time {
            display: block;
            color: rgb(200, 200, 200);
            font-size: 0.85em;
            margin-top: 0.5rem;
          }
          .DCollege {
            position: relative;
            &:hover {
              text-decoration: line-through;
            }
            &:hover::after {
              content: "Davidson College";
              height: fit-content;
              width: fit-content;
              min-width: 100%;
              white-space: pre;
              // background-color: red;
              position: absolute;
              top: -110%;
              right: -5px;
              padding-bottom: 2px;
              text-align: center;
              color: rgb(178, 178, 178);
              font-weight: bold;
            }
          }
        }
      }
    }
    .future {
      cursor: auto;
    }
  }
}

.project-viewer {
  .modal-dialog {
    --bs-modal-width: 80vw;
    .modal-content {
      background-color: $main-bg-color;
      position: relative;
      // a {
      //   position: absolute;
      //   right: 40px;
      //   top: -40px;
      //   svg {
      //     width: 20px;
      //     height: 20px;
      //     fill: #878889;
      //   }
      //   &:hover {
      //     svg {
      //       fill: #c3c3c4;
      //     }
      //   }
      // }
      button {
        position: absolute;
        right: 0;
        top: -40px;
      }
      .modal-body {
        padding: 0;
        height: fit-content;
        max-height: 80vh;
        overflow-x: hidden;
        // .loader {
        //   span {
        //     display: block;
        //     width: 10%;
        //     height: 4px;
        //     @include generateColors("background-color");
        //     border-radius: 1px;
        //     animation: loading 4s ease-in-out infinite;
        //   }
        // }
        // iframe {
        //   width: 100%;
        //   height: 80vh;
        //   border-radius: 5px;
        // }
        .project-details {
          // padding: 2rem;
          a {
            @include generateColorsLighten("color", 15);
            text-decoration: none;
            transition: 0.2s;
            &:hover {
              @include generateColorsLighten("color", 7);
            }
          }
          .project-bg {
            height: 300px;
            width: 100%;
            object-fit: cover;
            object-position: center;
            // margin: -2rem -2rem 0;
            & ~ .row {
              padding: 2rem;
            }
          }
          .overview {
            .logo {
              display: flex;
              align-items: center;
              margin-top: -4.5rem;
              margin-bottom: 2rem;
              img {
                border-radius: 50%;
                border: 2px solid;
                @include generateColorsDarken("border-color", 5);
                width: 150px;
                margin-left: 1.5rem;
              }
              p {
                margin-top: 3rem;
                margin-left: 2rem;
                font-size: 1.5rem;
                font-weight: bold;
                .time {
                  color: rgb(170, 170, 170);
                  font-size: 0.85rem;
                  font-style: italic;
                  margin-top: 0.5rem;
                  display: block;
                  // text-align: center;
                }
              }
            }
            a {
              svg {
                width: 20px;
                height: 20px;
                fill: #878889;
                transition: 0.2s;
              }
              &:hover {
                svg {
                  fill: #5c5c5c;
                }
              }
            }
          }
          .used-techs {
            border-left: 2px solid #eee;
            padding-left: 1rem;
            padding-bottom: 0.5rem;
            p {
              font-weight: bold;
              font-size: 1.25rem;
            }
            ol {
              margin-bottom: 0;
              li {
                margin-bottom: 0.3rem;
                letter-spacing: 0.7px;
                .small {
                  font-size: 0.7rem;
                  color: #ccc;
                }
              }
            }
          }
        }
      }
    }
  }
}

@media (max-width: 991.98px) {
  .projects-container {
    padding-left: 2rem;
    padding-right: 2rem;
    margin-top: 2rem;
  }
  .other-projects {
    & > .row {
      padding-left: 1rem;
      padding-right: 1rem;
    }
    p.background-title {
      right: -60px;
    }
  }
  .project-viewer {
    .modal-dialog {
      .modal-content {
        .modal-body {
          .project-details {
            .project-bg ~ .row {
              padding: 0.5rem;
            }
            .overview {
              margin-top: 2rem;
            }
            .used-techs {
              margin-top: 2.5rem;
              margin-bottom: 2rem;
              margin-left: 1rem;
            }
          }
        }
      }
    }
  }
}

// @keyframes loading {
//   0% {
//     width: 10%;
//   }
//   25% {
//     width: 100%;
//   }
//   50% {
//     width: 10%;
//     margin-left: auto;
//   }
//   75% {
//     width: 100%;
//     margin-left: auto;
//   }
//   76% {
//     margin-left: 0;
//   }
//   100% {
//     width: 10%;
//   }
// }
</style>
