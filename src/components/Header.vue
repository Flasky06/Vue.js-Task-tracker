<template>
	<header>
		<h1>{{ title }}</h1>
		<AddTaskButton
			@btn-click="$emit('toggle-add-task')"
			:text="showAddTask ? 'Close' : 'Add Task'"
			:color="showAddTask ? 'red' : 'green'"
		/>
	</header>
</template>

<script>
import AddTaskButton from "./Button.vue";

export default {
	name: "AppHeader",
	props: { title: { type: String }, showAddTask: Boolean },
	components: { AddTaskButton },
};
</script>

<style scoped>
header {
	display: flex;
	justify-content: space-between;
	align-items: center;
	margin-bottom: 20px;
}
</style>
