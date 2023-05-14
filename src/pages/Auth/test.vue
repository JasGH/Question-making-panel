<template>
  <question-field ref="tiptapChoice"
                  :key="key" />
</template>

<script>
import API_ADDRESS from 'src/api/Addresses.js'
import QuestionField from 'src/components/Question/QuestionPage/QuestionField.vue'

export default {
  name: 'Test',
  components: { QuestionField },
  mixins: [],
  beforeRouteEnter () {
    // console.log('debug beforeRouteEnter')
  },
  beforeRouteLeave () {
    // console.log('debug beforeRouteLeave')
  },
  beforeRouteUpdate () {
    // console.log('debug beforeRouteUpdate')
  },
  props: {
    testProp: {
      type: Boolean,
      default () {
        return false
      }
    }
  },
  data () {
    return {
      testValue: '',
      testValue1: '',
      key: 0
    }
  },
  computed: {
    test1 () {
      return API_ADDRESS.question.uploadImage('dfbdgbdgbgfnhfn')
    },
    test2 () {
      return 'Bearer ' + this.$store.getters['Auth/accessToken']
    }
  },
  watch: {
    testValue: {
      handler () {},
      deep: true
    },
    testValue1 (oldVal, newVal) {}
  },
  activated () {
    // console.log('debug activated')
  },
  updated () {
    // console.log('debug updated')
  },
  created () {
    // console.log('debug created')
    const that = this
    setTimeout(() => {
      that.key = 'Date.now()'
    }, 100)
  },
  mounted () {
    // console.log('debug mounted')
  },
  methods: {}
}
</script>

<style scoped lang="scss">
.video-player-container{
  width: 700px;
  height: auto;
  border-radius: 20px;
}
</style>
