<template>
  <nav>
  <router-link exact-active-class="active" to="/home">
    <svg viewBox="0 0 100 100">
      <g transform="translate(10 5) scale(0.8 0.9)">
        <path d="M 0 30 v 70 h 100 v -70 l -50 -30 z" stroke="currentColor" stroke-width="10" fill="none"
          stroke-linejoin="round" stroke-linecap="round" />
      </g>
    </svg>
    <span>
      Home
    </span>
  </router-link>

  <router-link active-class="active" to="/search">
    <svg viewBox="0 0 100 100">
      <g transform="translate(5 5) scale(0.9 0.9)">
        <circle cx="45" cy="38" r="38" stroke="currentColor" stroke-width="10" fill="none" />
        <line x1="66" y1="65" x2="100" y2="100" stroke="currentColor" stroke-width="10" />
      </g>
    </svg>
    <span>
      Search
    </span>
  </router-link>

  <router-link active-class="active" to="/likes">
    <svg viewBox="0 0 100 100">
      <g transform="translate(5 5) scale(0.9 0.9)">
        <path d="M 50 35 a 20 20 0 0 1 50 0 q 0 25 -50 60 q -50 -35 -50 -60 a 25 25 0 0 1 50 0" stroke="currentColor"
          stroke-width="10" fill="none" stroke-linejoin="round" stroke-linecap="round" />
      </g>
    </svg>
    <span>
      Likes
    </span>
  </router-link>

  <router-link active-class="active" to="/profile">
    <svg viewBox="0 0 100 100">
      <g transform="translate(5 5) scale(0.9 0.9)">
        <circle cx="50" cy="35" r="18" stroke="currentColor" stroke-width="10" fill="none" />
        <rect x="15" y="75" width="70" height="50" rx="25" stroke="currentColor" stroke-width="10" fill="none" />
      </g>
    </svg>
    <span>
      Profile
    </span>
  </router-link>
</nav>
</template>

<script>
export default {
  data: () => ({
  }),
  mounted() {
  },
  methods:{
    handleClick(e) {
      e.target.style.setProperty('--hover-bg', '#649fff20');
      e.target.style.setProperty('--hover-c', '#649fff');
    }
  }
}
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css?family=Open+Sans:700");

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #fff;
  padding: 1rem 2rem;
  border-radius: 30px 30px 0 0; 
  box-shadow: 0 2px 15px rgba(0, 0, 0, .3);
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
}

a {
  all: unset;
  color: inherit;
  text-decoration: none;
  display: flex;
  align-items: center;
  padding: 0.75rem 1.25rem;
  border-radius: 30px;
  position: relative;
  --hover-bg: #649fff20;
  --hover-c: #649fff;
}

a svg {
  margin-right: -2.5rem;
  width: 28px;
  height: 28px;
  pointer-events: none;
  /* transition for the change in margin */
  transition: margin 0.2s ease-out;
}
/* by default hide the span element */
a span {
  opacity: 0;
  visibility: hidden;
  font-size: 0.9rem;
  margin-left: 0.9rem;
  font-family: 'Arimo', sans-serif;
}

a.active {
  content: "";
  top: 50%;
  left: 0;
  visibility: visible;
  opacity: 1;
  background: var(--hover-bg);
  color: var(--hover-c);
}
/* using the color specified by the then updated custom property show the circle of the pseudo element increasing its size and highlighting it momentarily */
a.active:before {
  background: var(--hover-c);
  opacity: 0;
  visibility: hidden;
  transform: translate(0%, -50%) scale(2);
  /* transition only when the class is applied */
  transition: all 0.4s ease-out;
}
/* remove the margin applied to the svg to make it overlay atop the anchor link */
a.active svg {
  margin-right: 0;
}
/* show the span element */
a.active span {
  visibility: visible;
  opacity: 1;
  transition: all 0.2s ease-out;
}

/* on smaller viewports show the navigation bar on the side, attached to the left of the screen */
@media (max-width: 430px) {
  nav {
    padding: 1rem 1rem;
  }
}

@media (max-width: 390px) {
  nav{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
  }
  nav a span {
    display: none;
  }
  nav a{
    padding: .75rem 2rem;
  }
  a.active{
    top: 0;
  }
}


</style>