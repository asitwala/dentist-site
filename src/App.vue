<template>
  <div id="app">
    <div id="ds-pre-nav">
      <div class="ds-pre-nav-left">
        <p>Bell, CA</p>
        <div class="ds-divider"></div>
        <p>(323) 221-8836</p>
      </div>
      <div class="ds-pre-nav-right">
        <p>Cypress, CA</p>
        <div class="ds-divider"></div>
        <p>(714) 506-5375</p>
      </div>
    </div>
    <div id="ds-nav">
      <div class="ds-nav-left">
        <p class="ds-primary-name">SITWALA</p>
        <p class="ds-secondary-name">FAMILY DENTISTRY</p>
      </div>

      <div class="ds-nav-right">
          <router-link to="/">HOME</router-link>
          <router-link to="/about">ABOUT</router-link>
          <router-link to="/about">SERVICES</router-link>
          <router-link to="/about">PATIENT INFORMATION</router-link>
          <router-link to="/about">TECHNOLOGY</router-link>
          <router-link to="/about">CONTACT</router-link>
      </div>

    </div>
    <router-view/>

  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
  @import "./styles/app";

  body {
    width: 100%;
    margin: 0;
    padding: 0;
  }

  #app {
    width: 100%;
  }

  .ds-divider {
    height: 15px;
    width: 2px;
    background-size: 1px 2px;
    background-image: linear-gradient(to bottom, white 50%, transparent 50%);
    background-repeat: repeat-y;
    margin: 0 12px;
    display: inline-block;
  }

  #ds-pre-nav {
    background-color: #010e35;
    display: flex;
    padding: 0 40px;
    min-height: 35px;
    font-weight: 300;
    align-items: center;
    justify-content: space-between;
  }

  .ds-pre-nav-left {
    color: $offWhite;
    display: flex;
    align-items: center;
    flex-wrap: wrap;
  }

  .ds-pre-nav-right {
    color: $offWhite;
    display: flex;
    align-items: center;
    flex-wrap: wrap;
  }

  #ds-nav {
    background-color: $darkBlue;
    min-height: 70px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  p {
    margin: 0;
    padding: 0;
  }

  .ds-nav-left {
    width: 150px;
    margin: 0 12px;
    display: block;
  }

  .ds-nav-right {
    margin: 12px;
    display: flex;
    flex-wrap: wrap;
  }

  .ds-primary-name {
    color: $offWhite;
    font-size: 18px;
    font-weight: 700;
    text-align: center;
  }

  .ds-secondary-name {
    color: $offWhite;
    font-weight: 300;
    text-align: center;
    margin-top: -2px;
    line-height: 14px;
  }

  a {
    color: $offWhite;
    margin: 0 20px;
    text-decoration: none;
    letter-spacing: 1px;
    font-size: 14px;
  }
</style>
