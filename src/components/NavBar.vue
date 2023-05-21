<template>
    <h1> {{ title }}</h1>
    <div v-for="article in articles" :key="article.id">
      <h3> {{ article.title }} </h3>
      <h4> {{ article.description }} </h4>
      <p> {{ article.content }} </p>
    </div>
  
  </template>
  
  <script>
  export default {
      name: 'NavBar',
      props: {
          title: {
              type: String
          }
      },
      data() {
          return {
              articles: [
                  {
                  id: 1,
                  title: 'Title one',
                  description: 'Description article one',
                  content: 'This is the content for article one'
                  },
                  {
                  id: 2,
                  title: 'Title two',
                  description: 'Description article two',
                  content: 'This is the content for article two'
                  },
                  {
                  id: 3,
                  title: 'Title three',
                  description: 'Description article three',
                  content: 'This is the content for article three'
                  }
              ]
          }
      }
  }
  </script>
  
  <style scoped>
  
  </style>
  