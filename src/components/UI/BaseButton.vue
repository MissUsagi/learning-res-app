<template>
      <button :type="type" :class="mode">
         <slot></slot>
      </button>
</template>

<script>
export default {
   props: ['type', 'mode']
}
</script>

<style scoped>
button {
  padding: 0.75rem 1.5rem;
  margin: 5px;
  background: white;
  color: #ce5c00;
  font-weight: bold;
  border: 1px solid #ce5c00;
  border-radius: 5px;
  cursor: pointer;
}

button:hover,
button:active {
   color: white;
   background-color: #ce5c00;
}

.flat {
   background-color: transparent;
   color:  #ce5c00;
   border: none;
}

.flat:hover,
.flat:active{
   background-color: #6e1130;
}
</style>