<script>
import Home from './home/Home';
import MeetLoutus from './meetLoutus/MeetLoutus';
import Work from './work/Work';

export default {
  name: "MainContent",
  data () { return {
    currentRoute: window.location.pathname,
    routes: {
      '/': Home,
      '/meet-loutus': MeetLoutus,
      '/work': Work
    }
  }},
  beforeMount () {
    window.addEventListener('popstate', () => {
      this.currentRoute = window.location.pathname;
    })
  },
  computed: {
    ViewComponent () {
      return this.routes[this.currentRoute] || Home;
    }
  },
  render (h) {
    return h(this.ViewComponent);
  }
}
</script>