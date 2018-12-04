<script>
import { Component, Vue } from 'nuxt-property-decorator'

@Component
export default class UserDetail extends Vue {
  data() {
    return {
      props: {
        id: this.$route.params.id
      }
    }
  }
  head() {
    return {
      title: `User#${this.props.id} Detail`
    }
  }

  render(h) {
    return (
      <div>
        <h2>{`User#${this.props.id}`}</h2>
        <no-ssr>
          <span>This is not SSR element.</span>
        </no-ssr>
      </div>
    )
  }
}
</script>
