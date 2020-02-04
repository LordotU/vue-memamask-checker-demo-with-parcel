<template>
  <MetamaskChecker>
    <template slot="errored" slot-scope="{ error }">
      <Err :error="error" />
    </template>

    <template slot="checked" slot-scope="props">
      <Content v-bind="{ ...props }" />
    </template>

    <Loader />
  </MetamaskChecker>
</template>

<script>
  import MetamaskChecker from '@metamask-checker/vue'

  import Err from '../components/Err'
  import Content from '../components/Content'
  import Loader from '../components/Loader'

  export default {
    components: {
      MetamaskChecker,

      Err,
      Content,
      Loader,
    },
  }
</script>
