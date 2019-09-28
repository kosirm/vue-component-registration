<template>
  <div>
    <h1>Using dynamic import</h1>
    <component :is="componentInstance" />
  </div>
</template>

<script>
export default {
  props: {
    isCompany: { type: Boolean, default: false },
  },
  computed: {
    componentInstance () {
      const name = this.isCompany ? 'CompanyInfo' : 'UserInfo'
      return () => import(`./components/${name}`)
    }
  }
}
</script>