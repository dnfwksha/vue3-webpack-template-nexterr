<template>
  <h1 @click="increase">{{ count }}</h1>
  <div v-if="count>4">4보다 큽니다!</div>
  <ul>
    <fruit v-for="fruit in fruits" :key="fruit" :name="fruit">
      {{fruit}}
    </fruit>
  </ul>
</template>

<script>
import fruit from "~/components/fruit.vue";
export default {
  components:{
    fruit
  },
  data() {
    return {
      count: 0,
      fruits: ['Apple','Banana','Cherry']
    }
  },
  methods: {
    increase() {
      this.count += 1

    }
  }
}
</script>

<!--<style lang="scss">-->
<!--h1 {-->
<!--  font-size: 5000px;-->
<!--  color: red;-->
<!--}-->
<!--</style>-->