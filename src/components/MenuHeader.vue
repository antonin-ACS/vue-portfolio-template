<template>
    <nav>
        <ul>
            <li v-for="menuElem in menuElements">
                <router-link :to="menuElem.url">{{menuElem.name}}</router-link>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
  name: 'Menu',
  data () {
    return {
        menuElements : [
            {
                url: '/',
                name: 'Home'
            },
            {
                url: '/experiences',
                name: 'Experiences'
            },
            {
                url: '/projets',
                name: 'Projets'
            },
        ]
    }
  }
}
</script>

<style lang="scss" scoped>
    ul {
        display: flex;
        justify-content: space-between;
        list-style-type: none;
        max-width:1300px;
        margin: 0 auto;
    }

    @media screen and (max-width: 640px) {
        ul {
            display: block;
        }
    }
</style>
