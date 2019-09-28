<template>
  <div>
    <h1>Good ol' way</h1>
    <company-info v-if="isCompany" />
    <user-info v-else />
  </div>
</template>

<script>
import UserInfo from './components/UserInfo'
import CompanyInfo from './components/CompanyInfo'

export default {
  name: 'GoodOldWay',
  components: {
    UserInfo,
    CompanyInfo,
  },
  props: {
    isCompany: { type: Boolean, default: false },
  },
}
</script>
