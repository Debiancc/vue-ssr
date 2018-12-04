<script>
import Logo from '../components/Logo.vue'
import { Component, Vue } from 'nuxt-property-decorator'

@Component({
  components: { Logo }
})
export default class Landing extends Vue {
  render(h) {
    return <h1>Landing#Index</h1>
  }
}
</script>

<style>
</style>
