<template>
  <li :class="relevant == true?'relevant':''"><b>{{title}}</b> {{description}}</li>
</template>

<script>
export default {
    name:'cronoItem',
    props: ['title', 'description', "relevant"]
}
</script>

<style>
  .relevant{    
    text-decoration: underline;
    color: var(--color4);
  }
</style>