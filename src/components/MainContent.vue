<script>
import DoubleGradient from './DoubleGradientContainer';
import MeetLoutus from './MeetLoutus';
import Contact from './Contact';
import Work from './Work';

export default {
  name: "MainContent",
  data () { return {
    currentRoute: window.location.pathname,
    routes: {
      '/': DoubleGradient,
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
      return this.routes[this.currentRoute] || DoubleGradient;
    }
  },
  render (h) {
    return h(this.ViewComponent);
  }
}
</script>