<template>
  <div>
    <h2>Prompt Pool</h2>
    <ul>
      <li v-for="prompt in prompts" :key="prompt.id">{{ prompt.text }}</li>
    </ul>
    <input v-model="newPrompt" placeholder="Add new prompt">
    <button @click="addPrompt">Add</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      prompts: [],
      newPrompt: ''
    };
  },
  methods: {
    addPrompt() {
      this.prompts.push({ id: this.prompts.length + 1, text: this.newPrompt });
      this.newPrompt = '';
    }
  }
};
</script>
