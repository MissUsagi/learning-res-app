<template>
<li>
   <base-card>
      <header>
      <h2>{{title}}</h2>
      <base-button @click="deleteResource">Delete</base-button>
        <!-- <base-button mode="flat">Delete</base-button> -->
      </header>
      <p>{{description}}</p>
      <nav>
      <a :href="siteUrl" target="_blank">Go to Resource</a>
      </nav>
   </base-card>
</li>
</template>

<script>

export default {
   props: [
      'title', 'description', 'siteUrl'
   ],
   inject: ['deleteResource']
}
</script>

<style scoped>
li {
  margin: auto;
  max-width: 40rem;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h3 {
  font-size: 1.25rem;
  margin: 0.5rem 0;
}

p {
  margin: 0.5rem 0;
}

a {
  text-decoration: none;
  color: #ce5c00;
}

a:hover,
a:active {
  color: #c89300;
}
</style>