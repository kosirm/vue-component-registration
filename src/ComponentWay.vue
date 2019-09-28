<template>
  <div>
    <h1>Using built-in component</h1>
    <component :is="componentName" />
  </div>
</template>

<script>
import UserInfo from './components/UserInfo'
import CompanyInfo from './components/CompanyInfo'

export default {
  components: {
    UserInfo,
    CompanyInfo,
  },
  props: {
    isCompany: { type: Boolean, default: false },
  },
  computed: {
    componentName () {
      return this.isCompany ? 'company-info' : 'user-info'
    },
  },
}
</script>