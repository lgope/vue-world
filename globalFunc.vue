// main file

// global function

const plugin = {
  install() {
    // global alert message
    Vue.prototype.showActionMessage = (type, msg) => {
      do something....
    };
  
  };
};

Vue.use(plugin);

Vue.config.productionTip = false;

new Vue({
  router,
  store,
  render: h => h(App)
}).$mount("#app");
