<!--2017-12-26 20:35:30-->
<template>
    <div class="app1226">
        {{message}}
        <store-test></store-test>
         <store-test1></store-test1>
    </div>
    
</template>
<script>
import storeTest from "./store-test";
import Vue from "vue";
import Vuex from "vuex";
Vue.use(Vuex);

const store = new Vuex.Store({
  state: {
    count: 0
  },
  mutations: {
    increment(state) {
      state.count++;
    }
  }
});

export default {
  name: "app1226",
  store,
  components: {
    storeTest,
    "store-test1": {
      name: "store-test1",
      template: "<div>{{count}}</div>",
      computed: {
        count() {
          return store.state.count;
        }
      }
    }
  },
  data() {
    return {
      message: "hello world"
    };
  }
};
</script>