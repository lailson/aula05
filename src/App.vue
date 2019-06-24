<template>
  <div id="app">
    <h1>Tarefas</h1>
    <TaskGrid :tasks="tasks"/>
  </div>
</template>

<script>
import TaskGrid from './components/TaskGrid.vue'
export default {
  components: {TaskGrid},
  name: 'app',
  data(){
    return {
      tasks: [
        { name: 'tarefa1', pending: false},
        { name: 'tarefa2', pending: true},
      ]
    }
  }
}
</script>

<style>
body {
		font-family: 'Lato', sans-serif;
		background: #304352;  /* fallback for old browsers */
    background: -webkit-linear-gradient(to right, #d7d2cc, #304352);  /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(to right, #d7d2cc, #304352); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

		color: #FFF;
	}

	#app {
		display: flex;
		flex: 1;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}

	#app h1 {
		margin-bottom: 5px;
		font-weight: 300;
		font-size: 3rem;
	}
</style>
