<template>
  <div class="container">
    <Container>
      <template #header>
        <Test />
      </template>
      <template #header2>
        <Test2 />
      </template>
      <template>
        <Test1 />
      </template>
    </Container>
  </div>
</template>

<script>
import Test2 from '../components/Test2'
const Test = () => import('../components/Test')
const Test1 = () => import('../components/Test1')
const Container = () => import('../components/Container')
export default {
  components: {
    Test,
    Test1,
    Test2,
    Container
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
