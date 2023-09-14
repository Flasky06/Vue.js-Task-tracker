<template>
	<header>
		<h1>{{ "Task tracker " }}</h1>
		<AddTaskButton text="Add Task" color="green" />
	</header>
</template>

<script>
import AddTaskButton from "./Button.vue";

export default {
	name: "AppHeader",
	props: { title: { type: String, default: "Hello World" } },
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
