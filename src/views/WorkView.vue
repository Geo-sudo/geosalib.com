<template>
  <section>
    <div class="container">
      <h1 class="display-3 section-title color">Projects</h1>
      <div class="projects-container row g-0" v-motion-slide-right>
        <div
          class="project col-lg-3 col-md-4 col-sm-6"
          @click="showProjectViewer('NBodySim')"
        >
          <!-- NBodySim -->
          <div class="project-thumb">
            <img
              src="https://i.ibb.co/ksHNRN16/image-2026-01-01-222945407.png"
            />
          </div>
          <div class="view-project color">View<br />Project</div>
        </div>
        <div
          class="project col-lg-3 col-md-4 col-sm-6"
          @click="showProjectViewer('YSJ')"
        >
          <!-- YSJ -->
          <div class="project-thumb">
            <!-- <img src="https://picsum.photos/600/600" /> -->
            <img src="https://i.ibb.co/LvKK4yD/ysj-logo.png" />
          </div>
          <div class="view-project color">View<br />Project</div>
        </div>

        <div
          class="project col-lg-3 col-md-4 col-sm-6"
          @click="showProjectViewer('HackClub')"
        >
          <!-- Hack Club -->
          <div class="project-thumb">
            <img src="https://i.ibb.co/y8CKCSP/hc-logo.png" />
          </div>
          <div class="view-project color">View<br />Project</div>
        </div>
        <div
          class="project col-lg-3 col-md-4 col-sm-6"
          @click="showProjectViewer('Scrapyard')"
        >
          <!-- Scrapyard -->
          <div class="project-thumb">
            <img src="https://i.ibb.co/mC1xnTmX/scrapyard-big.webp" />
          </div>
          <div class="view-project color">View<br />Project</div>
        </div>
        <div
          class="project col-lg-3 col-md-4 col-sm-6"
          @click="showProjectViewer('Counterspell')"
        >
          <!-- Counterspell -->
          <div class="project-thumb">
            <img src="https://i.ibb.co/FqWRDjyp/counterspell.png" />
          </div>
          <div class="view-project color">View<br />Project</div>
        </div>
        <!--
        <div
          class="project col-lg-3 col-md-4 col-sm-6"
          @click="showProjectViewer('ACTTrainer')"
        >
          
          <div class="project-thumb">
            <img src="https://i.ibb.co/qNXfpCV/actt-logo.png" />
          </div>
          <div class="view-project color">View<br />Project</div>
        </div>
        <div
          class="project col-lg-3 col-md-4 col-sm-6"
          @click="showProjectViewer('EnRevisions')"
        >
          
          <div class="project-thumb">
            <img src="https://i.ibb.co/xL3qy28/enrevisions-logo.png" />
          </div>
          <div class="view-project color">View<br />Project</div>
        </div>
        <div
          class="project col-lg-3 col-md-4 col-sm-6"
          @click="showProjectViewer('MUNMaadi')"
        >
          
          <div class="project-thumb">
            <img src="https://i.ibb.co/G7S9jhQ/munmaadi-logo.png" />
          </div>
          <div class="view-project color">View<br />Project</div>
        </div> -->
      </div>
      <div class="other-projects">
        <p class="background-title">&</p>
        <h1 class="display-5 section-title color">Other Works</h1>
        <div
          class="row g-5"
          v-motion-slide-visible-once-right
          v-motion-slide-right
        >
          <div class="col-lg-4 col-sm-6">
            <div class="card color" @click="showProjectViewer('IAAC24')">
              <img
                src="https://i.ibb.co/yvXfJCB/image-2026-01-18-024608669.png"
                class="card-img-top"
              />
              <div class="card-body">
                <h5 class="card-title">
                  International Astronomy and Astrophysics Competition
                </h5>
                <p class="card-text">
                  Top 3% of ∼5040 competitors, Gold Honor
                  <span class="time">24</span>
                </p>
              </div>
            </div>
          </div>
          <div class="col-lg-4 col-sm-6">
            <div class="card color" @click="showProjectViewer('IAAC23')">
              <img
                src="https://i.ibb.co/yvXfJCB/image-2026-01-18-024608669.png"
                class="card-img-top"
              />
              <div class="card-body">
                <h5 class="card-title">
                  International Astronomy and Astrophysics Competition
                </h5>
                <p class="card-text">
                  Top 20% of 4500+ competitors, Silver Honor
                  <span class="time">23</span>
                </p>
              </div>
            </div>
          </div>
          <div class="col-lg-4 col-sm-6">
            <div class="card color" @click="showProjectViewer('Poems')">
              <img
                src="https://i.ibb.co/bR2Z7fKm/image-2026-01-18-032323205.png"
                class="card-img-top"
              />
              <div class="card-body">
                <h5 class="card-title">Poems</h5>
                <p class="card-text">
                  A selection of poems I wrote :)
                  <span class="time">Inf</span>
                </p>
              </div>
            </div>
          </div>
          <div class="col-lg-4 col-sm-6">
            <div class="card color" @click="showProjectViewer('Immerse')">
              <img
                src="https://i.ibb.co/ksBK3vps/image-2026-01-18-033850371.png"
                class="card-img-top"
              />
              <div class="card-body">
                <h5 class="card-title">Immerse Education Essay Competition</h5>
                <p class="card-text">
                  Top 7–8% of ∼6000 entrants
                  <span class="time">23</span>
                </p>
              </div>
            </div>
          </div>

          <div class="col-lg-4 col-sm-6">
            <div class="card color fst-italic text-muted future">
              <!-- <img src="https://picsum.photos/600/600" class="card-img-top" /> -->
              <div class="card-body">
                <h5 class="card-title">
                  "Never Count On Beginnings, The Game Hasn't Started Yet!"
                </h5>
                <p class="card-text">
                  <!-- <span class="DCollege"> -->
                  @My Dream College
                  <!-- </span> -->
                  <span class="time text-muted">Very Near Future</span>
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <p class="visit-github">
        Interested? Dive into my
        <a href="https://github.com/Geo-sudo" target="_blank" class="color">
          GitHub
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 496 512">
            <!--! Font Awesome Pro 6.2.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
            <path
              d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"
            />
          </svg>
        </a>
        for more.
      </p>
    </div>
    <!-- Project Viewer -->
    <div class="modal fade project-viewer" id="project-viewer" tabindex="-1">
      <div class="modal-dialog modal-dialog-centered modal-dialog-scrollable">
        <div class="modal-content">
          <button
            type="button"
            class="btn-close btn-close-white"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button>
          <div class="modal-body">
            <!-- <div class="loader" id="loader"><span class="color"></span></div> -->
            <!-- <iframe id="project-viewer-frame"></iframe> -->
            <div class="project-details" v-show="projectToView == 'YSJ'">
              <img
                src="https://media.springernature.com/full/springer-static/image/art%3A10.1038%2Fs42254-019-0127-2/MediaObjects/42254_2019_127_Fig1_HTML.png"
                alt="YSJ"
                class="project-bg"
              />
              <div class="row">
                <div class="col-lg-9">
                  <div class="overview">
                    <div class="logo">
                      <img
                        src="https://i.ibb.co/LvKK4yD/ysj-logo.png"
                        alt="YSJ"
                        class="color"
                      />
                      <p>
                        A comparison: galactic formation & evolution through
                        semi-analytic and numerical hydrodynamic frameworks in
                        the context of extragalactic astronomy<br /><span
                          class="time"
                          >23/24</span
                        >
                      </p>
                    </div>
                    <p class="fst-italic px-5">
                      "A review paper on the computational astrophysics
                      simulation paradigms. Ranked 2nd best out of 48
                      submissions to the Youth Science Journal (YSJ). Published
                      in YSJ's tenth issue"
                    </p>
                    <p class="text-center">
                      <a
                        href="https://issues.ys-journal.org/index.php/ysciencejournal/en/article/view/73"
                        target="_blank"
                        class="color"
                        >Read on YSJ
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                      &nbsp;&nbsp;&nbsp;
                      <a
                        href="https://www.researchgate.net/publication/398367184_A_comparison_galactic_formation_evolution_through_semi-analytic_and_numerical_hydrodynamic_frameworks_in_the_context_of_extragalactic_astronomy"
                        target="_blank"
                        class="color"
                        >Read on ResearchGate
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                    </p>
                  </div>
                </div>
                <div class="col-lg-3">
                  <div class="used-techs">
                    <p>Used Techs / Services</p>
                    <ol>
                      <li>IEEE Citation Style</li>
                      <li>
                        <a
                          href="https://www.zotero.org/"
                          target="_blank"
                          class="color"
                          >Zotero</a
                        >
                      </li>
                    </ol>
                  </div>
                </div>
              </div>
            </div>
            <div class="project-details" v-show="projectToView == 'HackClub'">
              <img
                src="https://i.ibb.co/HT15D1f8/Cyberquest.jpg"
                alt="IYNA"
                class="project-bg"
              />
              <div class="row">
                <div class="col-lg-9">
                  <div class="overview">
                    <div class="logo">
                      <img
                        src="https://i.ibb.co/cK6GWt8Q/hackclub-logo.jpg"
                        alt="Hack Club"
                        class="color"
                      />
                      <p>
                        STEM Egypt Hack Club<br /><span class="time"
                          >22/25</span
                        >
                      </p>
                    </div>
                    <p class="fst-italic px-5 text-center">
                      "A dynamic community of teen hackers from around the world
                      who code together, building cool tech projects. We annualy
                      provide free sessions for everyone to participate and
                      learn something new. Together, we utilize our expertise to
                      build each other up to become better makers and hackers as
                      a whole!"<br />Oversaw 9 mentors, 90+ sessions, and 70+
                      members; organized a 4-week boot camp, consisting of 5 CS
                      tracks and 125+ mentees, and handpicked its mentors;
                      supervised a CP competition with 225+ contestants from 20
                      countries; taught CyberSec to 20 students in 14+ weekly
                      sessions (2024); Mentored 4 students in an intensive
                      four-week CyberSec boot camp (2023); prepared curriculum
                      and tasks, and evaluated submissions during both.
                    </p>
                    <p class="text-center">
                      <a
                        href="https://stemegypt.hackclub.com/"
                        target="_blank"
                        class="color"
                        >Visit Website
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                    </p>
                  </div>
                </div>
                <div class="col-lg-3">
                  <div class="used-techs">
                    <p>Positions</p>
                    <ol>
                      <li>Legacy Advisor (25-Present)</li>
                      <li>
                        <a
                          href="https://stemegypt.hackclub.com/Meet-Us"
                          target="_blank"
                          class="color"
                          >Vice President (24/25)</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://stemegypt.hackclub.com/Meet-Us"
                          target="_blank"
                          class="color"
                          >CyberSecurity Mentor (23/24)</a
                        >
                      </li>
                      <li>Memeber (22/23)</li>
                    </ol>
                  </div>
                </div>
              </div>
            </div>
            <div class="project-details" v-show="projectToView == 'NBodySim'">
              <img
                src="https://news.yale.edu/sites/default/files/styles/horizontal_topper_image/public/2025-05/YNews-Twin-Star-System.jpg"
                alt="Binary Star"
                class="project-bg"
              />
              <div class="row">
                <div class="col-lg-9">
                  <div class="overview">
                    <div class="logo">
                      <img
                        src="https://i.ibb.co/ksHNRN16/image-2026-01-01-222945407.png"
                        alt="Binary Star"
                        class="color"
                      />
                      <p>
                        N-Body System Simulation Framework<br /><span
                          class="time"
                          >2024</span
                        >
                      </p>
                    </div>
                    <p class="fst-italic px-5 text-center">
                      "A Lagrangian framework to simulate Newtonian binary and
                      multi-star systems, validated with real data & produced
                      accurate results."
                    </p>
                    <p class="text-center">
                      <a
                        href="https://github.com/Geo-sudo/Projects/tree/main/Computational-Astrophysics/3D_N-Body_Simulation#binary-star-system-simualtion"
                        target="_blank"
                        class="color"
                        >See on Github
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                      &nbsp;&nbsp;&nbsp;
                      <a
                        href="https://blog.geosalib.com/posts/2024/binary-star-system-simulation/"
                        target="_blank"
                        class="color"
                        >See on My Blog
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                      <!-- &nbsp;&nbsp;&nbsp;
                      <a
                        href="https://github.com/Welly0007/IYNA_WEB"
                        target="_blank"
                        class="color"
                        >GitHub Repository
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a> -->
                    </p>
                  </div>
                </div>
                <div class="col-lg-3">
                  <div class="used-techs">
                    <p>Used Techs / Services</p>
                    <ol>
                      <li>
                        <a
                          href="https://www.python.org"
                          target="_blank"
                          class="color"
                          >Python</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://matplotlib.org/3.5.3/api/pyplot_summary.html"
                          target="_blank"
                          class="color"
                          >matplotlib.pyplot</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://matplotlib.org/3.5.3/api/animation_api.html"
                          target="_blank"
                          class="color"
                          >matplotlib.animation</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://numpy.org"
                          target="_blank"
                          class="color"
                          >numpy</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://docs.python.org/3/library/argparse.html"
                          target="_blank"
                          class="color"
                          >argparse</a
                        >
                      </li>
                    </ol>
                  </div>
                </div>
              </div>
            </div>
            <div class="project-details" v-show="projectToView == 'ACTTrainer'">
              <img
                src="https://i.ibb.co/rcpbn01/actt-bg.png"
                alt="ACT Trainer"
                class="project-bg"
              />
              <div class="row">
                <div class="col-lg-9">
                  <div class="overview">
                    <div class="logo">
                      <img
                        src="https://i.ibb.co/qNXfpCV/actt-logo.png"
                        alt="ACT Trainer"
                        class="color"
                      />
                      <p>
                        ACT Trainer Platform<br /><span class="time">22</span>
                      </p>
                    </div>
                    <p class="fst-italic px-5 text-center">
                      "ACT Trainer is an initiative to help students, especially
                      the ones with low financial capabilities, get their
                      perfect ACT score from the first trial.<br />So far, only
                      the essential part of the platform is finished - The ACT
                      Online Testing Platform - built to mimic the experience of
                      the official platform.<br />(Other parts of the platform
                      are still under development)."
                    </p>
                    <p class="text-center">
                      <a
                        href="https://mikhaelmounay.github.io/ACT-Trainer/#/"
                        target="_blank"
                        class="color"
                        >Visit Website
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                      &nbsp;&nbsp;&nbsp;
                      <a
                        href="https://github.com/MikhaelMounay/ACT-Trainer"
                        target="_blank"
                        class="color"
                        >GitHub Repository
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                    </p>
                  </div>
                </div>
                <div class="col-lg-3">
                  <div class="used-techs">
                    <p>Used Techs / Services</p>
                    <ol>
                      <li>HTML/CSS/JS</li>
                      <li>
                        <a
                          href="https://vuejs.org/"
                          target="_blank"
                          class="color"
                          >Vue JS 3</a
                        >
                        &
                        <a
                          href="https://cli.vuejs.org/"
                          target="_blank"
                          class="color"
                          >Vue CLI 5</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://sass-lang.com/"
                          target="_blank"
                          class="color"
                          >Sass</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://getbootstrap.com/"
                          target="_blank"
                          class="color"
                          >Bootstrap 5</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://www.mathjax.org/"
                          target="_blank"
                          class="color"
                          >MathJax 3</a
                        >
                        &
                        <a
                          href="https://github.com/hansonGong/mathjax-vue"
                          target="_blank"
                          class="color"
                          >MathJax-Vue</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://github.com/jesperorb/json-server-heroku"
                          target="_blank"
                          class="color"
                          >JSON Server</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://github.com/florian/cookie.js"
                          target="_blank"
                          class="color"
                          >cookie.js</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://glitch.com/"
                          target="_blank"
                          class="color"
                          >Glitch</a
                        >
                        <span class="small">
                          (used to serve tests data files for the
                          platform)</span
                        >
                      </li>
                      <li>
                        <a
                          href="https://imgbb.com/"
                          target="_blank"
                          class="color"
                          >ImgBB</a
                        >
                        <span class="small">
                          (used to serve images files for the platform)</span
                        >
                      </li>
                      <li>
                        <a
                          href="https://developers.google.com/apps-script"
                          target="_blank"
                          class="color"
                          >Google Apps Script</a
                        >
                        +
                        <a
                          href="https://www.google.com/forms/"
                          target="_blank"
                          class="color"
                          >Google Forms</a
                        >
                        <span class="small">
                          (used externally for tests addition)</span
                        >
                      </li>
                    </ol>
                  </div>
                </div>
              </div>
            </div>
            <div class="project-details" v-show="projectToView == 'MUNMaadi'">
              <img
                src="https://i.ibb.co/Xx534F7/munmaadi-bg.png"
                alt="MUN Maadi"
                class="project-bg"
              />
              <div class="row">
                <div class="col-lg-9">
                  <div class="overview">
                    <div class="logo">
                      <img
                        src="https://i.ibb.co/G7S9jhQ/munmaadi-logo.png"
                        alt="MUN Maadi"
                        class="color"
                      />
                      <p>
                        Maadi STEM Model United Nations<br /><span class="time"
                          >21/22</span
                        >
                      </p>
                    </div>
                    <p class="fst-italic px-5 text-center">
                      "Maadi STEM Model United Nations is a way for young
                      students to enter the MUN platform where students play the
                      role of delegates from different countries and attempt to
                      solve real world issues with the policies and perspectives
                      of their assigned country."
                    </p>
                    <p class="text-center">
                      <a
                        href="https://mikhaelmounay.github.io/Maadi_STEM_MUN/"
                        target="_blank"
                        class="color"
                        >Visit Website
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                      &nbsp;&nbsp;&nbsp;
                      <a
                        href="https://github.com/MikhaelMounay/Maadi_STEM_MUN"
                        target="_blank"
                        class="color"
                        >GitHub Repository
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                    </p>
                  </div>
                </div>
                <div class="col-lg-3">
                  <div class="used-techs">
                    <p>Used Techs / Services</p>
                    <ol>
                      <li>HTML/CSS/JS</li>
                      <li>
                        <a
                          href="https://jquery.com/"
                          target="_blank"
                          class="color"
                          >jQuery</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://getbootstrap.com/"
                          target="_blank"
                          class="color"
                          >Bootstrap 5</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://animejs.com/"
                          target="_blank"
                          class="color"
                          >anime.js</a
                        >
                      </li>
                    </ol>
                  </div>
                </div>
              </div>
            </div>
            <div class="project-details" v-show="projectToView == 'Scrapyard'">
              <img
                src="https://i.ibb.co/B5Y4v80D/sora.jpg"
                alt="Scrapyard Giza"
                class="project-bg"
              />
              <div class="row">
                <div class="col-lg-9">
                  <div class="overview">
                    <div class="logo">
                      <img
                        src="https://i.ibb.co/JWCR9ZW5/scrapyard-profile.jpg"
                        alt="Scrapyard Giza"
                        class="color"
                      />
                      <p>Scrapyard Giza<br /><span class="time">2025</span></p>
                    </div>
                    <p class="fst-italic px-5 text-center">
                      "Organized through the
                      <a
                        href="https://hackclub.com"
                        target="_blank"
                        class="color"
                        >Hack Club organization</a
                      >, Scrapyard Giza was a 12-hour beginner-friendly
                      hackathon that ranked #1 among 60+ global cities. Held
                      during Ramadan at Masters Language School, the event saw
                      160 high schoolers build unconventional "scrappy" tech and
                      attend technical workshops in Arduino and web/game
                      development, fostering a unique culture of youth-led
                      creativity in Egypt." <br />Managed part of the day-of
                      operation budgeting, logistics, and financials.
                    </p>
                    <p class="text-center">
                      <a
                        href="https://stemegypt.hackclub.com/Hackathons/scrapyard"
                        target="_blank"
                        class="color"
                        >See More
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                      <!-- &nbsp;&nbsp;&nbsp;
                      <a
                        href="https://github.com/MikhaelMounay/Maadi_STEM_MUN"
                        target="_blank"
                        class="color"
                        >GitHub Repository
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a> -->
                    </p>
                  </div>
                </div>
                <div class="col-lg-3">
                  <div class="used-techs">
                    <p>Statistics</p>
                    <ol>
                      <li>The largest high school hackathon in Egypt</li>
                      <li>Fundraised $2000+ (& Prizes)</li>
                      <li>48+ Projects</li>
                      <li>475+ Sign-ups</li>
                      <li>4+ Workshops</li>
                      <li>Ranked #1 out of 100+ cities globally</li>
                      <li>
                        Sponsored by
                        <a
                          href="https://the.hackfoundation.org"
                          target="_blank"
                          class="color"
                          >The Hack Foundation</a
                        >
                      </li>
                    </ol>
                  </div>
                </div>
              </div>
            </div>
            <div
              class="project-details"
              v-show="projectToView == 'Counterspell'"
            >
              <img
                src="https://i.ibb.co/HD6TXzGH/Home-page.webp"
                alt="Counterspell Giza"
                class="project-bg"
              />
              <div class="row">
                <div class="col-lg-9">
                  <div class="overview">
                    <div class="logo">
                      <img
                        src="https://i.ibb.co/FqWRDjyp/counterspell.png"
                        alt="Counterspell Giza"
                        class="color"
                      />
                      <p>
                        Counterspell Giza<br /><span class="time">2024</span>
                      </p>
                    </div>
                    <p class="fst-italic px-5 text-center">
                      "A 12-hour beginner friendly game jam organized through
                      the
                      <a
                        href="https://hackclub.com"
                        target="_blank"
                        class="color"
                        >Hack Club organization</a
                      >
                      in 100+ cities globally." <br />Managed day-of operation
                      budgeting, logistics, and financials including venue,
                      t-shirts, and catering; negotiated a 5% discount with food
                      supplier and negotiated budget increases with partners &
                      sponsers.
                    </p>
                    <p class="text-center">
                      <a
                        href="https://stemegypt.hackclub.com/Hackathons/counterspell"
                        target="_blank"
                        class="color"
                        >See More
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                      <!-- &nbsp;&nbsp;&nbsp;
                      <a
                        href="https://github.com/MikhaelMounay/Maadi_STEM_MUN"
                        target="_blank"
                        class="color"
                        >GitHub Repository
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a> -->
                    </p>
                  </div>
                </div>
                <div class="col-lg-3">
                  <div class="used-techs">
                    <p>Statistics</p>
                    <ol>
                      <li>
                        Previously the largest high school hackathon in Egypt
                      </li>
                      <li>Fundraised $1500+ (& Prizes)</li>
                      <li>30+ Projects</li>
                      <li>281+ Sign-ups</li>
                      <li>3+ Workshops</li>
                      <li>Ranked #1 out of 100+ cities globally</li>
                      <li>
                        Sponsored by
                        <a
                          href="https://chucklefish.org/"
                          target="_blank"
                          class="color"
                          >ChuckleFish</a
                        >
                      </li>
                      <li>
                        Sponsored by
                        <a
                          href="https://www.swish-swoosh.com/"
                          target="_blank"
                          class="color"
                          >Swish Swoosh</a
                        >
                      </li>
                    </ol>
                  </div>
                </div>
              </div>
            </div>
            <div class="project-details" v-show="projectToView == 'IAAC24'">
              <img
                src="https://i.ibb.co/Vc6r4vCf/bg.jpg"
                alt="IAAC_bg"
                class="project-bg"
              />
              <div class="row">
                <div class="col-lg-9">
                  <div class="overview">
                    <div class="logo">
                      <img
                        src="https://i.ibb.co/yvXfJCB/image-2026-01-18-024608669.png"
                        alt="IAAC_logo"
                        class="color"
                      />
                      <p>
                        International Astronomy and Astrophysics Competition<br /><span
                          class="time"
                          >24</span
                        >
                      </p>
                    </div>

                    <p class="fst-italic px-5 text-center">
                      Top 3% of ∼5040 competitors, Gold Honor

                      <br />
                      "The International Astronomy and Astrophysics Competition
                      is an educational science competition that enables
                      students from all countries to test their skills in
                      astronomy and astrophysics. Participants can receive
                      certificates, awards, cash prizes, and global
                      recognition."
                    </p>
                    <p class="text-center">
                      <a
                        href="https://iaac.space/en/"
                        target="_blank"
                        class="color"
                        >Visit Website
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                    </p>
                  </div>
                </div>
                <div class="col-lg-3">
                  <div class="used-techs">
                    <p>Certificate</p>
                    <ol>
                      <li>
                        <a
                          href="https://drive.google.com/file/d/15FMymL_fuX4hrpRh7xltwA1l37h_NQK_/view?usp=sharing"
                          target="_blank"
                          class="color"
                          >View My Certificate</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://iaac.space/en/verify"
                          target="_blank"
                          class="color"
                          >Verify My Certificate</a
                        >
                      </li>
                    </ol>
                  </div>
                </div>
              </div>
            </div>
            <div
              class="project-details"
              v-show="projectToView == 'EnRevisions'"
            >
              <img
                src="https://i.ibb.co/pXv2b43/enrevisions-bg.png"
                alt="English Revisions"
                class="project-bg"
              />
              <div class="row">
                <div class="col-lg-9">
                  <div class="overview">
                    <div class="logo">
                      <img
                        src="https://i.ibb.co/xL3qy28/enrevisions-logo.png"
                        alt="English Class Revisions"
                        class="color"
                      />
                      <p>
                        English Class Revisions (Handouts / Website)<br /><span
                          class="time"
                          >20/22</span
                        >
                      </p>
                    </div>
                    <p class="px-5">
                      The "English Revisions" project is an idea I have been
                      working on since my 10<sup>th</sup> grade to help my high
                      school class prepare for their English exams using the
                      handouts and exercises included in this website.
                    </p>
                    <p class="text-center">
                      <a
                        href="https://mikhaelmounay.github.io/English_Revisions/"
                        target="_blank"
                        class="color"
                        >Visit Website
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                      &nbsp;&nbsp;&nbsp;
                      <a
                        href="https://github.com/MikhaelMounay/English_Revisions"
                        target="_blank"
                        class="color"
                        >GitHub Repository
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                    </p>
                  </div>
                </div>
                <div class="col-lg-3">
                  <div class="used-techs">
                    <p>Used Techs / Services</p>
                    <ol>
                      <li>HTML/CSS/JS</li>
                      <li>
                        <a
                          href="https://mikhaelmounay.github.io/English_Revisions/"
                          target="_blank"
                          class="color"
                          >Notion</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://www.python.org/"
                          target="_blank"
                          class="color"
                          >Python</a
                        >
                        +
                        <a
                          href="https://pyautogui.readthedocs.io/en/latest/"
                          target="_blank"
                          class="color"
                          >PyAutoGUI</a
                        >
                        +
                        <a
                          href="https://pypi.org/project/beautifulsoup4/"
                          target="_blank"
                          class="color"
                          >beautifulsoup4</a
                        >
                        <br />
                        <span class="small"
                          >(used intensively for automating and webscraping
                          purposes to get the needed data for the
                          handouts)</span
                        >
                      </li>
                    </ol>
                  </div>
                </div>
              </div>
            </div>
            <div class="project-details" v-show="projectToView == 'Poems'">
              <img
                src="https://i.ibb.co/d4mxbG0Z/jeremy-thomas.jpg"
                alt="Poems_bg"
                class="project-bg"
              />
              <div class="row">
                <div class="col-lg-9">
                  <div class="overview">
                    <div class="logo">
                      <img
                        src="https://i.ibb.co/bR2Z7fKm/image-2026-01-18-032323205.png"
                        alt="Poems"
                        class="color"
                      />
                      <p>My Poems<br /><span class="time">Inf</span></p>
                    </div>
                    <p class="fst-italic px-5 text-center">
                      Some poems I wrote in moments of reflection and/or awe.
                    </p>
                    <p class="text-center">
                      <a
                        href="https://drive.google.com/drive/folders/15zgJ7bTrv5ZuVWbbptG5ENMW5Eirorze?usp=sharing"
                        target="_blank"
                        class="color"
                        >Read Poems
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                    </p>
                  </div>
                </div>
                <div class="col-lg-3">
                  <div class="used-techs">
                    <p>Poems</p>
                    <ol>
                      <li>
                        <a
                          href="https://drive.google.com/file/d/1YIL0K1vpJGN7jI3jYikDpd9vdRS_ciYL/view?usp=drive_link"
                          target="_blank"
                          class="color"
                          >On A Cold Night</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://drive.google.com/file/d/1qudWVv7XCQKD9A9tWXvbkuYq34gIUEV4/view?usp=drive_link"
                          target="_blank"
                          class="color"
                          >Gazing at the Heights</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://drive.google.com/file/d/1cYbFFbKig1XAhZlYW3b9r0AljGeRvcGt/view?usp=drive_link"
                          target="_blank"
                          class="color"
                          >A Stunning View</a
                        >
                      </li>
                    </ol>
                  </div>
                </div>
              </div>
            </div>
            <div class="project-details" v-show="projectToView == 'IAAC23'">
              <img
                src="https://i.ibb.co/Vc6r4vCf/bg.jpg"
                alt="IAAC_bg"
                class="project-bg"
              />
              <div class="row">
                <div class="col-lg-9">
                  <div class="overview">
                    <div class="logo">
                      <img
                        src="https://i.ibb.co/yvXfJCB/image-2026-01-18-024608669.png"
                        alt="IAAC_logo"
                        class="color"
                      />
                      <p>
                        International Astronomy and Astrophysics Competition<br /><span
                          class="time"
                          >23</span
                        >
                      </p>
                    </div>
                    <p class="fst-italic px-5 text-center">
                      Top 20% of 4500+ competitors, Silver Honor

                      <br />
                      "The International Astronomy and Astrophysics Competition
                      is an educational science competition that enables
                      students from all countries to test their skills in
                      astronomy and astrophysics. Participants can receive
                      certificates, awards, cash prizes, and global
                      recognition."
                    </p>
                    <p class="text-center">
                      <a
                        href="https://iaac.space/en/"
                        target="_blank"
                        class="color"
                        >Visit Website
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                    </p>
                  </div>
                </div>
                <div class="col-lg-3">
                  <div class="used-techs">
                    <p>Certificate</p>
                    <ol>
                      <li>
                        <a
                          href="https://drive.google.com/file/d/1y6psthRpFgKasSa7U5vU7Eq3wLRM0rll/view?usp=sharing"
                          target="_blank"
                          class="color"
                          >View My Certificate</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://iaac.space/en/verify"
                          target="_blank"
                          class="color"
                          >Verify My Certificate</a
                        >
                      </li>
                    </ol>
                  </div>
                </div>
              </div>
            </div>
            <div class="project-details" v-show="projectToView == 'Immerse'">
              <img
                src="https://i.ibb.co/d4mxbG0Z/jeremy-thomas.jpg"
                alt="Immerse"
                class="project-bg"
              />
              <div class="row">
                <div class="col-lg-9">
                  <div class="overview">
                    <div class="logo">
                      <img
                        src="https://i.ibb.co/ksBK3vps/image-2026-01-18-033850371.png"
                        alt="Kilecy"
                        class="color"
                      />
                      <p>
                        Immerse Education Essay Competition<br /><span
                          class="time"
                          >23</span
                        >
                      </p>
                    </div>

                    <p class="fst-italic px-5 text-center">
                      Top 7–8% of ∼6000 entrants, awarded ∼$1000 scholarship for
                      a 550-word research essay on stellar evolution
                    </p>
                    <p class="text-center">
                      <a
                        href="https://drive.google.com/file/d/12v8ObUgS-Cc4APyo6RBcTk9jmqJHL9_S/view?usp=drive_link"
                        target="_blank"
                        class="color"
                        >Read Essay
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                    </p>
                  </div>
                </div>
                <div class="col-lg-3">
                  <div class="used-techs">
                    <p>Links</p>
                    <ol>
                      <li>
                        <a
                          href="https://www.immerse.education/essay-competition/"
                          target="_blank"
                          class="color"
                          >Immerse Education</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://drive.google.com/file/d/1C4hOFdYkIHWVq86pUrniG5rfohJEqD-Q/view?usp=sharing"
                          target="_blank"
                          class="color"
                          >Proof of Rank</a
                        >
                      </li>
                    </ol>
                  </div>
                </div>
              </div>
            </div>
            <div class="project-details" v-show="projectToView == 'SaltyMed'">
              <img
                src="https://i.ibb.co/5MJ3Z7L/saltymed-bg.png"
                alt="Green-Hesive"
                class="project-bg"
              />
              <div class="row">
                <div class="col-lg-9">
                  <div class="overview">
                    <div class="logo">
                      <img
                        src="https://i.ibb.co/0BQfHTv/saltymed-logo.png"
                        alt="Kilecy"
                        class="color"
                      />
                      <p>
                        Salty Mediterranean Project<br /><span class="time"
                          >22/23</span
                        >
                      </p>
                    </div>
                    <p class="px-5">
                      Salty Mediterranean was my team's 12<sup>th</sup>-grade
                      Capstone project. It was about developing an
                      <em>IoT System</em> that focuses on improving the use of
                      technology to solve problems related to
                      <em>Climate Change</em>.
                    </p>
                    <p class="fst-italic px-5">
                      From reducing shorelines to unprecedented levels of heat,
                      the negative consequences of climate change and water
                      pollution continually affect Egypt, while there is a lack
                      of adequate industrial base, and hence the science and
                      technology to solve this arising issue. The purpose of the
                      study is to gather data and make a prediction regarding
                      future salinity levels in the Mediterranean Sea and try to
                      mitigate the negative consequences. ...
                    </p>
                    <p class="text-center">
                      <a
                        href="https://drive.google.com/drive/folders/1Sovq3OB_-J1gDgjgbsQqczefiaZ3ZM5N?usp=share_link"
                        target="_blank"
                        class="color"
                        >View Project Files
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                      &nbsp;&nbsp;&nbsp;
                      <a
                        href="https://github.com/MikhaelMounay/salty-med"
                        target="_blank"
                        class="color"
                        >GitHub Repository
                        <svg
                          xmlns="http://www.w3.org/2000/svg"
                          viewBox="0 0 448 512"
                        >
                          <!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                          <path
                            d="M280 80C266.7 80 256 69.25 256 56C256 42.75 266.7 32 280 32H424C437.3 32 448 42.75 448 56V200C448 213.3 437.3 224 424 224C410.7 224 400 213.3 400 200V113.9L200.1 312.1C191.6 322.3 176.4 322.3 167 312.1C157.7 303.6 157.7 288.4 167 279L366.1 80H280zM0 120C0 89.07 25.07 64 56 64H168C181.3 64 192 74.75 192 88C192 101.3 181.3 112 168 112H56C51.58 112 48 115.6 48 120V424C48 428.4 51.58 432 56 432H360C364.4 432 368 428.4 368 424V312C368 298.7 378.7 288 392 288C405.3 288 416 298.7 416 312V424C416 454.9 390.9 480 360 480H56C25.07 480 0 454.9 0 424V120z"
                          /></svg
                      ></a>
                    </p>
                  </div>
                </div>
                <div class="col-lg-3">
                  <div class="used-techs">
                    <p>Used Techs / Services</p>
                    <ol>
                      <li>HTML/CSS/JS</li>
                      <li>
                        <a
                          href="https://vuejs.org/"
                          target="_blank"
                          class="color"
                          >Vue JS 3</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://jquery.com/"
                          target="_blank"
                          class="color"
                          >jQuery</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://sass-lang.com/"
                          target="_blank"
                          class="color"
                          >Sass</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://getbootstrap.com/"
                          target="_blank"
                          class="color"
                          >Bootstrap 5</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://firebase.google.com/"
                          target="_blank"
                          class="color"
                          >Firebase Realtime DB</a
                        >
                      </li>
                      <br />
                      <li>
                        <a
                          href="https://www.python.org/"
                          target="_blank"
                          class="color"
                          >Python</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://www.heroku.com/"
                          target="_blank"
                          class="color"
                          >Heroku</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://numpy.org/"
                          target="_blank"
                          class="color"
                          >NumPy</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://pandas.pydata.org/"
                          target="_blank"
                          class="color"
                          >pandas</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://scikit-learn.org/stable/"
                          target="_blank"
                          class="color"
                          >scikitlearn</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://plotly.com/"
                          target="_blank"
                          class="color"
                          >Plotly</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://flask.palletsprojects.com/"
                          target="_blank"
                          class="color"
                          >Flask</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://gunicorn.org/"
                          target="_blank"
                          class="color"
                          >Gunicorn</a
                        >
                      </li>
                      <br />
                      <li>
                        <a
                          href="https://cplusplus.com/"
                          target="_blank"
                          class="color"
                          >C/C++</a
                        >
                      </li>
                      <li>
                        <a
                          href="https://www.arduino.cc/"
                          target="_blank"
                          class="color"
                          >Arduino IDE</a
                        >
                      </li>
                    </ol>
                  </div>
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
