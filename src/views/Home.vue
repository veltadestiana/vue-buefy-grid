<template>
  <section class="home">
    <div class="hero is-primary">
      <div class="hero-body">
        <div class="container has-text-centered">
          <h1 class="title">
            Suche Coupons
          </h1>
          <div class="search-box is-fullwidth">
            <input class="input" type="text" placeholder="Suchen">
          </div>
        </div>
      </div>
    </div>

    <div class="container">
      <div class="columns is-multiline">
        <div class="column is-one-third">
          <div class="card">
            <div class="card-image">
              <figure class="image">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/59/Amazon.de-Logo.svg/2000px-Amazon.de-Logo.svg.png" alt="Placeholder image">
              </figure>
              <div class="ribbon ribbon-top-right"><span>Bis Zu 5%</span></div>
            </div>
          <div class="card-content">
            <div class="content">
              <p class="title is-size-4 has-text-centered" style="margin: 10px 0 10px 0">Amazon Gesusche</p>
                <div class="field is-grouped">
                  <p class="control">
                    <span class="button is-rounded is-static">Bücher</span>
                  </p>
                  <p class="control">
                    <span class="button is-rounded is-static">Elektronik</span>
                  </p>
                  <p class="control">
                    <span class="button is-rounded is-static">Haushalt</span>
                  </p>
                </div>
            </div>
          </div>
          <a class="button is-link is-fullwidth" style="margin-top: 0; border-radius: 0; letter-spacing: 2px"><strong>See Details →</strong></a>
        </div>
        </div>

        <div class="column is-one-third">
          <div class="card">
            <div class="card-image">
              <figure class="image">
                <img src="data:image/png;base64,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" alt="Placeholder image">
              </figure>
              <div class="ribbon ribbon-top-right"><span>Bis Zu 5%</span></div>
            </div>
          <div class="card-content">
            <div class="content">
              <p class="title is-size-4 has-text-centered" style="margin: 10px 0 10px 0">Zalando Gutschein</p>
                <div class="field is-grouped" style="display: flex; justify-content: center;">
                  <p class="control">
                    <span class="button is-rounded is-static">Mode</span>
                  </p>
                  <p class="control">
                    <span class="button is-rounded is-static">Schuhe</span>
                  </p>
                  <p class="control">
                    <span class="button is-rounded is-static">Sport</span>
                  </p>
                </div>
            </div>
          </div>
          <a class="button is-link is-fullwidth" style="margin-top: 0; border-radius: 0; letter-spacing: 2px"><strong>See Details →</strong></a>
        </div>
        </div>

        <div class="column is-one-third">
          <div class="card">
            <div class="card-image">
              <figure class="image">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e1/Notebooksbilliger.de_logo.svg/2000px-Notebooksbilliger.de_logo.svg.png">
              </figure>
              <div class="ribbon ribbon-top-right"><span>Bis Zu 5%</span></div>
            </div>
          <div class="card-content">
            <div class="content">
              <p class="title is-size-4 has-text-centered" style="margin: 10px 0 10px 0">Notebooksbiliger Gutschein</p>
                <div class="field is-grouped" style="display: flex; justify-content: center;">
                  <p class="control">
                    <span class="button is-rounded is-static">Notebooks</span>
                  </p>
                  <p class="control">
                    <span class="button is-rounded is-static">Smartphones</span>
                  </p>
                  <p class="control">
                    <span class="button is-rounded is-static">TV</span>
                  </p>
                </div>
            </div>
          </div>
          <a class="button is-link is-fullwidth" style="margin-top: 0; border-radius: 0; letter-spacing: 2px"><strong>See Details →</strong></a>
        </div>
      </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      msg: 'Vue.js starter with full-featured Webpack and Buefy'
    }
  }
}
</script>

<style lang="scss" scoped>
.title {
  margin: 20px;
}

.container {
  margin-top: -30px;
}

.image {
  height:100px;
  width:100%;
}

.card {
  margin: 0 20px 15px 20px;
}

.card:hover {
  top: -2px;
  box-shadow: 0 4px 5px rgba(0,0,0,0.2);
}

.is-grouped {
  margin-left: 0 30px 0 30px;
  display: flex;
  justify-content: center;
}

.search-box input {
  border-radius: 20px;
}

figure {
  position: relative;
  padding: 50px;
  margin-bottom: 20px;
}

.top-right {
  position: absolute;
  top: 0;
  right: 0;
  background: hsl(141, 71%, 48%);
  color: white;
  padding: 10px;
  text-align: right;
  opacity: 0.7;
}

.ribbon {
  width: 150px;
  height: 150px;
  overflow: hidden;
  position: absolute;
  opacity: 0.95;
}
.ribbon::before,
.ribbon::after {
  position: absolute;
  z-index: -1;
  content: '';
  display: block;
  border: 5px solid #2980b9;
}
.ribbon span {
  position: absolute;
  display: block;
  width: 225px;
  padding: 15px 0;
  background-color: #3498db;
  box-shadow: 0 5px 10px rgba(0,0,0,.1);
  color: #fff;
  font: 700 18px/1 'Open Sans', sans-serif;
  text-transform: uppercase;
  text-align: center;
}


/* top right*/
.ribbon-top-right {
  top: -10px;
  right: -10px;
}
.ribbon-top-right::before,
.ribbon-top-right::after {
  border-top-color: transparent;
  border-right-color: transparent;
}
.ribbon-top-right::before {
  top: 0;
  left: 0;
}
.ribbon-top-right::after {
  bottom: 0;
  right: 0;
}
.ribbon-top-right span {
  left: -25px;
  top: 30px;
  transform: rotate(45deg);
}


</style>
