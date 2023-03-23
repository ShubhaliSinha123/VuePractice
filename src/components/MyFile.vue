<template>
  <!-- <h1>{{ getName('Sinha') }}</h1> -->
  <!-- <h1>{{ email }}</h1>
<h1>{{ date }}</h1>
<h1>{{ (mobile = 5455) }}</h1>
<h1>{{ mobile }}</h1>
<h1>{{ getMyName('Anaya') }}</h1>
<h1 v-on:mousemove="getConsole()">{{ getAllData().email }}</h1>
<button v-on:click="getData('Button 1 is clicked')">Click me!</button>
<button v-on:dblclick="getData('Button 2 is double clicked')">
    Click me!
</button>
<h1>Total Hover: {{count}}</h1> -->
  <!-- <input type="text" v-model="name" />
<h1>{{ name }}</h1>
<input type="text" v-model="text" placeholder="enter text" />
<br />
<br />
<input type="password" v-model="password" placeholder="enter password" />
<br />
<br />
<button v-on:click="getProfile()">Get Profile</button>
<h3>Technologies</h3>
<label for="java" class="cursor-p">Java</label>
<input type="checkbox" value="Java" id="java" v-model="technologies" /> <br />
<label for="react" class="cursor-p">React</label>
<input type="checkbox" value="React" id="react" v-model="technologies" />
<br />
<label for="node" class="cursor-p">Node</label>
<input type="checkbox" value="Node" id="node" v-model="technologies" /> <br />
<h1 v-if="technologies?.length">
    Technologies: {{ technologies?.length ? technologies : '' }}
</h1>
<h1 v-else>No selected technology yet</h1>
<h1 v-if="show">Hi, I am here!</h1>
<button v-on:click="show=!show">Click me please to {{show ? "hide" : "show"}} the text</button>
<br />
<h1>Who I am?</h1>
<h2>= {{ post }}</h2>
<label for="student">Student</label>
<input type="radio" value="Student" id="student" v-model="post" name="post" /><br />
<label for="developer">Developer</label>
<input type="radio" value="Developer" id="developer" v-model="post" name="post" /><br /><br /> -->
  <!-- <ul>
    <li v-for="item in technology" :key="item">
        {{ item }}
    </li>
</ul>
<br />
<br />
<ul>
    <li v-for="item in user" :key="item?.category">
        Name:{{ item?.name }} and Category:{{ item?.category }}
    </li>
</ul> -->
  <ul>
    <li v-for="items in user" :key="items.name">
      <ChildComponent :user="items" :getAllData="getData" :colors="colors" />
    </li>
  </ul>
</template>

<script>
import ChildComponent from './Child.vue';

export default {
  name: 'MyFile',
  components: {
    ChildComponent,
  },
  data() {
    return {
      // getName: function (lastName) {
      //     return `Shubhali ${lastName}`;
      // },
      // // email: 'shubh@gmail.com',
      // // date: '12/4/2001',
      // // mobile: 8585,
      // //   count: 0,
      // name: '',
      // text: '',
      // password: '',
      // technologies: [],
      // post: '',
      // show: true,
      // technology: ['Java', 'React', 'Node', 'Vue'],
      user: [
        {
          name: 'Orange',
          category: 'color',
        },
        {
          name: 'Hen',
          category: 'animal',
        },
        {
          name: 'Red',
          category: 'color',
        },
        {
          name: 'Cow',
          category: 'animal',
        },
      ],
      colors: { name: 'Grey', shade: '#ccc' },
    };
  },
  methods: {
    // getMyName(name) {
    //     return name;
    // },
    // getAllData() {
    //     return {
    //         name: 'Shubhali',
    //         email: this.email,
    //     };
    // },
    getData(data) {
      alert(data);
    },
    // getConsole() {
    //     console.warn("Function is clicked!")
    //     this.count = this.count + 1
    // }
    // getProfile() {
    //     alert(`text: ${this.text}, password: ${this.password}`);
    // },
  },
};
</script>

<style scoped>
h1 {
  color: red;
}

.cursor-p {
  cursor: pointer;
}
</style>
