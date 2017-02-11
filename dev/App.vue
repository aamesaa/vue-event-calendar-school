<template>
  <div id="app">
    <h1>vue-event-calendar-dev</h1>
    <h2 class="t-center">Defalut template</h2>
    <vue-event-calendar :events="demoEvents"></vue-event-calendar>
    <h2 class="t-center">Custom template</h2>
    <vue-event-calendar :events="demoEvents">
      <template scope="props">
        <div v-for="(event, index) in props.showEvents" class="event-item">
          <!-- In here do whatever you want, make you owner event template -->
          {{event}}
        </div>
      </template>
    </vue-event-calendar>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      demoEvents: [{
        date: '2017/02/10',
        title: '今天也放假',
        desc: 'longlonglong description'
      },{
        date: '2017/02/11',
        title: '今天也放假',
        desc: 'longlonglong description'
      },{
        date: '2017/02/12',
        title: '端午节放假',
        desc: 'longlonglong description'
      },{
        date: '2017/02/13',
        title: '国庆节放假',
        desc: 'longlonglong description'
      },{
        date: '2017/02/14',
        title: '中秋节放假',
        desc: 'longlonglong description'
      },{
        date: '2017/02/15',
        title: '清明节放假',
        desc: 'longlonglong description'
      },{
        date: '2017/02/16',
        title: '端午节放假',
        desc: 'longlonglong description'
      },{
        date: '2017/02/17',
        title: '国庆节放假',
        desc: 'longlonglong description'
      },{
        date: '2017/02/18',
        title: '中秋节放假',
        desc: 'longlonglong description'
      },{
        date: '2017/02/19',
        title: '今天也放假'
      }]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 30px;
}

h1, h2, h3 {
  font-weight: normal;
  margin: 0;
  padding: 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
.t-center{
  text-align: center;
  margin: 20px;
}
</style>
