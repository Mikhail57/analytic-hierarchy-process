<template>
  <div class="home">
    <h1>Главная</h1>
    <h2>Критерии</h2>
    <CriteriaInput />
  </div>
</template>

<script>
// @ is an alias to /src
import CriteriaInput from '../components/CriteriaInput'

export default {
  name: 'home',
  components: {
    CriteriaInput
  }
}
</script>
