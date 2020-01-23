<template>
    <div class="header">
        <div class="logo">
            <h1>Header</h1>
        </div>
        <div class="links">
            <nav class="nav">
                <g-link
                    v-for="(menu, key) in menuOptions"
                    class="nav__link"
                    :key="key"
                    :to="menu.route">
                    {{ menu.label }}
                </g-link>
            </nav>
        </div>
        <div class="login">
            <button> Login </button>
        </div>
    </div>
        <!-- <header class="header">
      <strong>
        <g-link to="/">{{ $static.metadata.siteName }}</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Home</g-link>
        <g-link class="nav__link" to="/about/">About</g-link>
      </nav>
    </header> -->
</template>

<script>
    export default {
        name: "CoreHeader",
        props: {
            headerName: {
                type: String,
                default: "Good Monday",
                required: false
            }
        },
        computed: {
            menuOptions () {
            return [
                ...this.edges.map(edge => {
                return {
                    label: edge.node.name,
                    route: edge.node.full_slug
                }
                })
            ]
            },
            edges () {
            return this.$static.allStoryblokEntry.edges || []
            }
        }
    }
</script>

<static-query>
query {
  metadata {
    siteName
  }

  allStoryblokEntry {
    edges {
      node {
        id
        full_slug
        name
      }
    }
  }
}
</static-query>

<style scoped lang="scss">
.header {
    padding: 20px;
    background-color: cadetblue;
}

</style>