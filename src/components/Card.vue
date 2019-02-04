<template>
  <div class="card">
    <h3>{{ title }}</h3>
    <ul>
      <li v-for="photo in photos">
        <label @click="onClick"></label>
        <img width="50px" :src="photo.url" :alt="photo.title" @click="onClick"/>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'Card',
    props: {
      title: String
    },
    data() {
      return {
        photos: [
          {
            url: 'http://s2.glbimg.com/lCgKRgb9XrRUp48TMCaHiVRy0k4=/e.glbimg.com/og/ed/f/original/2017/05/30/thinkstockphotos-646108884.jpg',
            title: 'Lorem upseum'
          },
          {
            url: 'http://s2.glbimg.com/lCgKRgb9XrRUp48TMCaHiVRy0k4=/e.glbimg.com/og/ed/f/original/2017/05/30/thinkstockphotos-646108884.jpg',
            title: 'Lorem upseum'
          }
        ]
      }
    },
    methods: {
      onClick: function() {
        alert('Clicou');
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




















Lembrei que um professor no curso de desenvolvimento, sempre construia uma aplicação de gerenciamento de musicas para testar uma novo tecnologia.