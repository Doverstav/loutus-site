<script>
import Home from './home/Home';
import MeetLoutus from './meetLoutus/MeetLoutus';
import Contact from './contact/Contact';
import Work from './work/Work';

export default {
  name: "MainContent",
  data () { return {
    currentRoute: window.location.pathname,
    routes: {
      '/': Home,
      '/meet-loutus': MeetLoutus,
      '/work': Work,
      '/contact': Contact
    }
  }},
  beforeMount () {
    window.addEventListener('popstate', () => {
      console.log("new state!");
      console.log(window.location.pathname)
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