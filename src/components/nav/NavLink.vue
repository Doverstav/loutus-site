<template>
  <span
    class="nav-link"
    v-bind:class="{active: isActive}"
    v-on:click="go"
  >{{text}}</span>
</template>

<script>
export default {
  name: "NavLink",
  props: {
    text: String,
    href: String,
  },
  data () { return {
    isActive: false,
  }},
  beforeMount () {
    this.isActive = this.href === window.location.pathname;
    window.addEventListener('popstate', () => {
      this.isActive = this.href === window.location.pathname;
    })
  },
  methods: {
    go() {
      window.history.pushState(
        null,
        "",
        this.href
      );
      // Make sure that things update
      dispatchEvent(new PopStateEvent('popstate'));
    }
  }
}
</script>

<style scoped>
.nav-link {
  align-self: center;
  justify-self: center;

  border-bottom: 4px solid rgba(0, 0, 0, 0);

  font-family: "Maven Pro", sans-serif;
}

.nav-link:hover {
  border-bottom: 4px solid #86c7c4;
  cursor: pointer;
}

.active {
  border-bottom: 4px solid #86c7c4 !important;
}
</style>