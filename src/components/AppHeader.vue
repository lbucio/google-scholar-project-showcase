<template>
  
  <header class="header">
    <nav class="header__nav">
      <div class="nav-item nav-brand">Project Showcase</div>
  
      <div class="nav-item nav-toggle" :class="{ 'is-open' : isOpen }" @click="toggleNav">
          <div class="nav-toggle-item">
              <span class="nav-toggle-bar"></span>
              <span class="nav-toggle-bar"></span>
              <span class="nav-toggle-bar"></span>
          </div>
      </div>

    </nav>
  </header>

</template>

<script>
export default {

  data() {
    return {
      isOpen: false,
    };
  },

  methods: {

    toggleNav() {
      this.isOpen = !this.isOpen;
    },

  },

};
</script>

<style lang="scss">
.header {
  margin: 0;
  height: 57px;
  min-height: 0;
  min-width: 0;
  padding: 0;
  background-color: #FFFFFF;
  position: relative;
  z-index: 3;

  color: #222222;

  display: flex;
  flex-flow: column nowrap;
  flex-basis: auto;
  flex-shrink: 0;
  align-items: stretch;
}

.header__nav {
  display: flex;
  height: 100%;
}

.nav-item {
  flex: 1 1 0%;
}

.nav-brand {
  padding: 5px 10px;
  display: flex;
  justify-content: flex-start;
  align-items: center;

  font-weight: 900;
  font-size: 1rem;
  line-height: 1;
  letter-spacing: -.25px;
  text-transform: uppercase;
  flex-grow: 2;
}

/* Nav Toggle */
.nav-toggle {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    padding: 10px;
}

.nav-toggle-bar {
  height: 2px;
  width: 20px;
  background: hsl(0, 0%, 96%);
  background: hsl(0, 0%, 4%);
  display: block;
  margin-top: 2px;
  margin-bottom: 2px;

  transition: transform .25s ease-out;
    
  &:first-child {
    transform-origin: top left;
  }
    
  &:nth-child(2) {
    transition: opacity .1s .25s ease-out;
  }

  &:last-child {
    transform-origin: bottom left;
  }
}

.is-open.nav-toggle {
    .nav-toggle-bar:first-child {
        transform: translateX(3px) rotate(45deg);
    }

    .nav-toggle-bar:nth-child(2) {
        transition: opacity .2s ease-out;
        opacity: 0;
    }

    .nav-toggle-bar:last-child {
        transform: translate(3px, 5px) rotate(-45deg);
    }
}


</style>
