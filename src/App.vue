<template>
  <div class="container">
      <nav>
      <div class="mobileNav">
        <div class="btn-icon btn-menu hamburgerClosed" @click="toggleMenu"></div>

        <div class="mobileHeading">
          <h1>Merchant Profile</h1>
        </div>

        <div class="menuRightMobile">
          <a href="#" class="btn-icon btn-search searchMobile"></a>

          <!--<router-link href="#" class="btn-icon btn-profile profileMobile"></router-link>-->

          <a href="#" class="btn-icon btn-profile profileMobile" @click.native="showProfileModal">
          </a>
        </div>
      </div>

      <div class="menu" :class="{'active': isActive, 'close-menu': !isActive}">
        <div class="menuLeft">
          <a href="#" class="logo">
          <!--<img src="../assets/images/yqlogo.png">-->
          </a>

          <div class="btn-icon btn-x hamburgerOpen" @click="toggleMenu"></div>

          <li class="menuItemContainer">
            <a href="#" class="menuItem dashboardItem">
              Home
            </a>
          </li>

          <li class="menuItemContainer">
            <a href="#" class="menuItem">
              About
            </a>

            <ul class="dropdownMenu">
              <a href="#" class="subMenuItem">
                Sub menu 1
              </a>
              <a href="#" class="subMenuItem">
                Sub menu 2
              </a>
              <a href="#" class="subMenuItem">
                Sub menu 3
              </a>
            </ul>
          </li>

          <li class="menuItemContainer">
            <a href="#" class="menuItem">
              Portfolio
            </a>

            <ul class="dropdownMenu">
              <a href="#" class="subMenuItem">
                Sub menu 1
              </a>
              <a href="#" class="subMenuItem">
                Sub menu 2
              </a>
            </ul>
          </li>

          <li class="menuItemContainer">
            <a href="#" class="menuItem">
              Skills
            </a>

            <ul class="dropdownMenu">
              <a href="#" class="subMenuItem">
                Sub menu 1
              </a>
            </ul>
          </li>

          <li class="menuItemContainer">
            <a href="#" class="menuItem">
              Contact
            </a>
          </li>
        </div>
      </div>
    </nav>

    <div class="overlay" @click="toggleMenu" :class="{'active': isActive, 'close-menu': !isActive}"></div>



    <div class="aboveTheFold">
      <div class="homeTitle">
        <h1>JE<span>SS</span>ICA <span>Y</span>EOH</h1>
      </div>

      <div>
        <h2>Front End Developer</h2>
        <h2>Front End Designer</h2>
        <h2>Support Officer</h2>
      </div>
    </div>

    <div class="about">
      <div>
        <h1 class="arrow">A little <span>about</span> me</h1>
          
        <p>I am currently a Front End Developer at Jadon Solutions Pte Ltd. My role is focused on projects that develop responsive websites, emails and administration portal pages. My passion and strong work ethic has helped me develop my programming skills quickly. My development stack consists of HTML, CSS, SASS, JS, jQuery, VueJS, PHP and MySQL.</p>
        
        <p>I also have over four years experience as an Executive Assistant and have worked in the hospitality/retail industry for over five years.</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" src="./assets/main.scss"></style>


<script>
export default {
  name: 'app',
  data () {
    return {
      isActive: false
    }
  },
  methods: {
    toggleMenu () {
      this.isActive = !this.isActive
    },
  },
}
</script>

