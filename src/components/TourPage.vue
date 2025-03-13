<script setup lang="ts">
import ArrowButton from './buttons/ArrowButton.vue';
</script>

<template class="tour-page">
  <div class="page3-top-imgs">

    <section class="top-img-flower-container">
      <img
        src="@/assets/page3_svg/tyler-flower-face.svg"
        class="tyler-flower-face"
        alt="Tyler the Creator is depicted as a face in the middle of a sunflower"
      />
    </section>

    <section class="top-img-lp-record-container">
        <img
          src="@/assets/page3_svg/lp-record.svg"
          class="lp-record"
          alt="Illustration of a black LP record"
        />
    </section>

    <div class="lp-text">
      <h2>LIVE TOUR</h2>
      <h3>1/26 - 3/4</h3>
      <p>CLICK DOWN BELOW TO SEE TOURPLAN AND BUY YOUR TICKETS</p>
      <div class="lp-arrow-container">
        <button class="lp-arrow">
          <ArrowButton />
        </button>
      </div>
    </div>
  </div>

    <section class="small-clouds-container">
      <img
        src="@/assets/page3_svg/page3_mobile_clouds/cloud-1.svg"
        class="cloud-1"
        alt="Illustrated image of a small cloud."
      />
      <img
        src="@/assets/page3_svg/page3_mobile_clouds/cloud-2.svg"
        class="cloud-2"
        alt="Illustrated image of a small cloud."
      />
      <img
        src="@/assets/page3_svg/page3_mobile_clouds/cloud-3.svg"
        class="cloud-3"
        alt="Illustrated image of a small cloud."
      />
      <img
        src="@/assets/page3_svg/page3_mobile_clouds/cloud-4.svg"
        class="cloud-4"
        alt="Illustrated image of a small cloud."
      />
      <img
        src="@/assets/page3_svg/page3_mobile_clouds/cloud-5.svg"
        class="cloud-5"
        alt="Illustrated image of a small cloud."
      />
      <img
        src="@/assets/page3_svg/page3_mobile_clouds/cloud-6.svg"
        class="cloud-6"
        alt="Illustrated image of a small cloud."
      />
    </section>

    <div class="tour-info-container">
      <h5 class="tour-list-text">
        <ul class="tour-date">
          <li>1/26</li>
          <li>1/27</li>
          <li>1/29</li>
          <li>1/30</li>
          <li>2/2</li>
          <li>2/3</li>
          <li>2/6</li>
          <li>2/7</li>
          <li>2/8</li>
          <li>2/10</li>
          <li>2/12</li>
          <li>2/13</li>
          <li>2/15</li>
          <li>2/17</li>
          <li>2/18</li>
          <li>2/20</li>
          <li>2/21</li>
          <li>2/23</li>
          <li>2/25</li>
          <li>2/27</li>
          <li>3/1</li>
          <li>3/2</li>
          <li>3/4</li>
        </ul>
        <ul class="tour-city">
          <li>VANCOUVER</li>
          <li>PORTLAND</li>
          <li>SF</li>
          <li>SACRAMENTO</li>
          <li>SAN DIEGO</li>
          <li>TEMPE</li>
          <li>DENVER</li>
          <li>KANSAS CITY</li>
          <li>DALLAS</li>
          <li>ATLANTA</li>
          <li>MIAMI</li>
          <li>ORLANDO</li>
          <li>PHILLY</li>
          <li>TORONTO</li>
          <li>MONTREAL</li>
          <li>PITTSBURGH</li>
          <li>ROCHESTER</li>
          <li>NYC</li>
          <li>DC</li>
          <li>DETROIT</li>
          <li>MADISON</li>
          <li>CHICAGO</li>
          <li>MILWAUKEE</li>
        </ul>
        <ul class="tour-venue">
          <li>PNE FORUM</li>
          <li>MEMORIAL COLISEUM</li>
          <li>THE ARMORY</li>
          <li>MEMORIAL AUDITORIUM</li>
          <li>VALLEY VIEW CASINO CENTER</li>
          <li>MARQUEE THEATRE</li>
          <li>1STBANK CENTER</li>
          <li>ARVEST BANK THEATRE</li>
          <li>BOMB FACTORY</li>
          <li>WORLD CONGRESS CENTER</li>
          <li>JAMES L. KNIGHT CENTER</li>
          <li>ORLANDO AMPHITHEATRE</li>
          <li>LIACOURAS CENTER</li>
          <li>RICOH COLISEUM</li>
          <li>MTELUS</li>
          <li>STAGE AE</li>
          <li>MAIN STREET ARMORY</li>
          <li>THE THEATER AT MSG</li>
          <li>THE ANTHEM</li>
          <li>TEMPLE THEATRE</li>
          <li>ALLIANT ENERGY CENTER</li>
          <li>ARAGON BALLROOM</li>
          <li>EAGLES BALLROOM</li>
        </ul>
      </h5>
      <section class="big-cloud-container">
      <img
        src="@/assets/page3_svg/cloud-with-bee.svg"
        class="bee-image"
        alt="Illustrated image of a big cloud."
      />
      </section>
      <button class="ticket-button">
        Get your tickets here
      </button>
    </div>
</template>

<style scoped lang="scss">

body {
  background-color: $bg-light-blue;
}

/* ----------------------*/
/* ----`*~ MOBILE ~*´----*/
/* ----------------------*/
.small-clouds-container {
  position: relative;
  
  z-index: -1;
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: repeat(12, 1fr);
  transition: all 0.3s ease-in-out; 
  top: 200px; 
  img {
    object-fit: cover;
    width: 50vw;
  }
  .cloud-1 {
    grid-column: 1 / span 3;
    grid-row: 1;
    width: 40vw;
  }
  .cloud-2 {
    grid-column: 9 / span 3;
    grid-row: 2; 
  }
  .cloud-3 {
    grid-column: 1 / span 3;
    grid-row: 4;
  }
  .cloud-4 {
    grid-column: 9 / span 3;
    grid-row: 8;
  }
  .cloud-5 {
    grid-column: 1 / span 3;
    grid-row: 9;
  }
  .cloud-6 {
    grid-column: 9 / span 3;
    grid-row: 10 / span 2;
    width: 50vw;
  }
}
.big-cloud-container {
  display: none;
  visibility: hidden;
  opacity: 0; 
  transition: all 0.3s ease-in-out;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  img {
    grid-column: 1 / span 3;
    justify-self: center;
    max-width: 96vw;
    min-width: 500px;
  }
}
.tour-list-text {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  top: 0;

  .tour-date {
    grid-column: 2;

    text-align: right;
    margin-right: 40px;
  }
  .tour-city {
    grid-column: 3;

    text-align: left;
    margin-right: 20px;
  }
  .tour-venue {
    grid-column: 4;

    text-align: left;
    visibility: hidden;
    display: none;
  }
}

.tour-info-container {
  position: absolute;
  top: 1500px;
  left: 50vw;

  .tour-list-text {
    position: relative;
    top: 42%;
    //left: 50%;
    transform: translate(-50%, -50%);
  }
  .ticket-button {
    position: absolute;
    top: 300px;

    margin-top: 10vh;
    margin-bottom: 10vh;
    transform: translate(-50%, -50%);
  }
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.lp-text {
  color: #fff;
}
.lp-arrow {
  background: transparent;
  margin: 0;
  border: 0;
}

.ticket-button {
  color: $font-primary;
  font-size: 1.25rem;
  font-weight: 900;
  text-transform: uppercase;
  text-align: center;

  width: 225px;
  height: 60px;
  border: 0;
  border-radius: 15px;
  background-color: #111111;
  box-shadow: 0 6px #000;

  cursor: pointer;
}
.ticket-button:hover {
  background-color: #1d1d1d;
}
.ticket-button:active {
  background-color: #111111;
  box-shadow: 0 1px #000;
  transform: translateY(4px);
}
.page3-top-imgs {
    margin-top: 50px;
    margin-bottom: 20vh;
    position: relative;
    margin-left: 28vw;

    img {
      max-width: 250px;
      max-height: 500px;
    }
    .top-img-lp-record-container {
      position: relative;      
    }
    .top-img-flower-container {
      z-index: 1;
      position: absolute;
      top: 200px;
    }
    .lp-text {
      text-align: center;
      position: absolute;
      top: 40px;
      bottom: 0;
      left: 0;
      h2, h3 {
        max-width: 250px;
        max-height: 400px;
      }
      h3 {
        margin-top: 70px;
      }
      p {      
        color: #000;
        margin-top: 35vh;
      }
      .lp-arrow {
        margin-top: 40px;
      }
      p, .lp-arrow {
        
        max-width: 250px;
        max-height: 500px;
      }
    }
  }

/* ----------------------*/
/* ----`*~ TABLET ~*´----*/
/* ----------------------*/
@media screen and (min-width: 744px) {

    .small-clouds-container {

    img {
      object-fit: cover;
      width: 50vw;
    }
    .cloud-1 {
      grid-column: 1 / span 3;
      grid-row: 1;
      width: 40vw;
    }
    .cloud-2 {
      grid-column: 9 / span 3;
      grid-row: 2; 
    }
    .cloud-3 {
      grid-column: 1 / span 3;
      grid-row: 4;
    }
    .cloud-4 {
      grid-column: 9 / span 3;
      grid-row: 8;
    }
    .cloud-5 {
      grid-column: 1 / span 3;
      grid-row: 9;
    }
    .cloud-6 {
      grid-column: 9 / span 3;
      grid-row: 10 / span 2;
      width: 50vw;
    }
  }
  .page3-top-imgs {
    margin-top: 50px;
    margin-bottom: 20vh;
    position: relative;
    margin-left: 34vw;

    img {
      max-width: 400px;
      max-height: 500px;
    }
    .top-img-lp-record-container {
      //position: relative;      
    }
    .top-img-flower-container {
      z-index: 1;
      //position: absolute;
      top: 300px;
    }
    .lp-text {
      text-align: center;
      position: absolute;
      top: 40px;
      bottom: 0;
      left: 50px;
      h2, h3 {
        font-size: 2rem;
        max-width: 300px;
        max-height: 500px;
      }
      h3 {
        margin-top: 140px;
      }
      p {
        margin-top: 50vh;
      }
      .lp-arrow {
        margin-top: 40px;
      }
      p, .lp-arrow {
        max-width: 300px;
        max-height: 500px;
      }
    }
  } 
}

/* -----------------------*/
/* ----`*~ DESKTOP ~*´----*/
/* -----------------------*/

@media screen and (min-width: 1366px) {
  .small-clouds-container {
    visibility: hidden;
    display: none;
    opacity: 0;
    transition: all 0.3s ease-in-out;  
  }
  .big-cloud-container {
    position: relative;
    visibility: visible;
    opacity: 1;
    transition: all 0.3s ease-in-out;  
      img {
        max-width: 96vw;
        min-width: 300px;
      }
  }

  .tour-list-text {
    
    display: flex;
    justify-content: center;

    .tour-date {
      grid-column: 2;

      text-align: right;
      margin-right: 40px;
    }
    .tour-city {
      grid-column: 3;

      margin-right: 30px;
      text-align: right;
    }
    .tour-venue {
      grid-column: 4;

      text-align: left;
      visibility: visible;
      display: initial;
    }
  }
  .ticket-button {
    width: 323px;
    height: 92px;
    font-size: 1.25rem;
    font-weight: 700;
    top: 0;
    
  }
  .tour-info-container {
    position: static;

    .tour-list-text {
      //position: static;
      transform: none;
      z-index: 2;
    }
    .ticket-button {
      position: static;
      transform: none;
      margin-left: 35vw;
    }
  }

  .page3-top-imgs {
    margin-top: 50px;
    margin-bottom: 20vh;
    position: relative;
    margin-left: 20vw;
    img {
      max-width: 600px;
      max-height: 650px;
    }
    .top-img-lp-record-container {
      position: relative;
      left: 500px;
    }
    .top-img-flower-container {
      position: absolute;
      z-index: 1;
      top: 0;
    }
    .lp-text {
      max-width: 500px;
      max-height: 500px;
      text-align: center;
      position: absolute;
      top: 10%;
      left: 650px;
      h2, h3 {
        max-width: 500px;
        max-height: 500px;
      }
      h3 {
        margin-top: 0;
      }
      p {
        color: #fff;
        margin-top: 170px;
      }
      .lp-arrow {
        margin-top: 40px;
      }
    }
  }
    
}
</style>