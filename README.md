# mixins
HTML

<div id="yeahyeet">
  <Mix1></Mix1>
  <Mix2></Mix2>
</div>

JavaScript/Vue

const myMixin = {
	template: `<input v-model="name">`
};

const Mix1 = Vue.extend({
  mixins: [myMixin],
  data() {
  	return { name: 'Pre' }
  }
})

const Mix2 = Vue.extend({
  mixins: [myMixin],
  data() {
  	return { name: 'Workout' }
  }
})

new Vue({
    el: '#yeahyeet',
    components: { Mix1, Mix2 }
});
