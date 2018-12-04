<script>
import { Component, Vue } from 'nuxt-property-decorator'

@Component
export default class UserDetail extends Vue {
  render(h) {
    return (
      <div>
        <h2>
          User#
          {this.$route.params.id}
        </h2>
      </div>
    )
  }
}
</script>
