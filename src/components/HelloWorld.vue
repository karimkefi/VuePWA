<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li v-for="({ name, link }, index) in plugins" :key='index'>
        <a :href="link">{{name}}</a>
      </li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
       <li v-for="({ name, link }, index) in websites" :key='index'>
        <a :href="link">{{name}}</a>
      </li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li v-for="({ name, link }, index) in ecosystems" :key='index'>
        <a :href="link">{{name}}</a>
      </li>
    </ul>
  </div>

</template>



<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },

  data() {
    return {
      ecosystems: [
      {
        link: 'https://router.vuejs.org',
        name: 'vue-router'
      },
      {
        link: 'https://vuex.vuejs.org',
        name: 'vuex'
      },
      {
        link: 'https://github.com/vuejs/vue-devtools#vue-devtools',
        name: 'vue-devtools'
      },
      {
        link: 'https://vue-loader.vuejs.org',
        name: 'vue-loader'
      },
      {
        link: 'https://github.com/vuejs/awesome-vue',
        name: 'awesome-vue'
      }],

      websites: [
      {
        link: 'https://vuejs.org',
        name: 'Vue Docs'
      },
      {
        link: 'https://forum.vuejs.org',
        name: 'Forum'
      },
      {
        link: 'https://news.vuejs.org',
        name: 'News'
      }
    ],

    plugins: [
      {
        link: 'https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel',
        name: 'babel'
      },
      {
        link: 'https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-pwa',
        name: 'pwa'
      },
      {
        link: 'https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint',
        name: 'eslint'
      }
    ]

    }
  }


}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
</style>
