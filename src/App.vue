<template>
  <div id="app">
    <TextTag :data="tagArr" />
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
    TextTag: () => import('./components/TextTag.vue')

  },
  data()  {
    return {
      tagArr: [
        {
          title: '"Город сыра и мира"',
          details: [
            {
              icon: 'fa-regular fa-star icon-tag',
              iconTitle: '5'
            },
            {
              iconTitle: 'Историческая'
            },
            {
              icon: 'fa-solid fa-bus icon-tag',
              iconTitle: 'На автобусе'
            },
            {
              iconTitle:'28 марта'
            },
            {
              icon: 'fa-regular fa-clock icon-tag last-tag',
              iconTitle: '9 часов'
            }
          ]
        },
        {
          title: 'Экскурсия в национальный парк "Куршская коса"',
          details: [
            {
              icon: 'fa-regular fa-star icon-tag',
              iconTitle: '5'
            },
            {
              iconTitle: 'Обзорная'
            },
            {
              icon: 'fa-solid fa-bus icon-tag',
              iconTitle: 'На автобусе'
            },
            {
              iconTitle:'25 марта'
            },
            {
              icon: 'fa-regular fa-clock icon-tag last-tag',
              iconTitle: '6 часов'
            }
          ]
        },
        {
          title: '"О кирхах, рыцарях и замках"',
          details: [
            {
              icon: 'fa-regular fa-star icon-tag',
              iconTitle: '5'
            },
            {
              iconTitle: 'Историческая'
            },
            {
              icon: 'fa-solid fa-bus icon-tag',
              iconTitle: 'На автобусе'
            },
            {
              iconTitle:'29 марта'
            },
            {
              icon: 'fa-regular fa-clock icon-tag last-tag',
              iconTitle: '6 часов'
            }
          ]
        },
        {
          title: 'Экскурсия в Янтарный',
          details: [
            {
              iconTitle: 'Историческая'
            },
            {
              icon: 'fa-solid fa-bus icon-tag',
              iconTitle: 'На автобусе'
            },
            {
              iconTitle:'29 марта'
            },
            {
              icon: 'fa-regular fa-clock icon-tag',
              iconTitle: '6 часов'
            },
            {
              icon: 'fa-solid fa-user icon-tag last-tag',
              iconTitle: 'до 49'
            }
          ]
        },
      ]
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;500&display=swap');

*{
  font-family: 'Roboto', sans-serif;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
