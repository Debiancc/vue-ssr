<script>
import Logo from '../components/Logo.vue'
import { Component, Vue } from 'nuxt-property-decorator'

@Component({
  components: { Logo }
})
export default class Landing extends Vue {
  title = 'Landing#Index'

  head() {
    return {
      title: this.title,
      meta: [
        { hid: 'keyword', name: 'keyword', content: `${this.title} keywords` },
        {
          hid: 'description',
          name: 'description',
          content: `${this.title} description`
        }
      ]
    }
  }
  asyncData() {
    // mock async data like backend template variable
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        return resolve({
          users: [
            { id: 0, name: 'user-0' },
            { id: 1, name: 'user-1' },
            { id: 2, name: 'user-2' },
            { id: 3, name: 'user-3' }
          ]
        })
      }, 1000 * 2)
    })
  }

  render(h) {
    return (
      <div>
        <h1>Landing#Index</h1>
        <ul>
          <li>
            <nuxt-link to="/user/1">User 1</nuxt-link>
          </li>
        </ul>
      </div>
    )
  }
}
</script>
