<template>
        <div>
                <div v-for="task in tasks" :key="task._id">
                        <Task
                                @toggle-reminder="
                                        $emit('toggle-reminder', task._id)
                                "
                                @delete-task="$emit('delete-task', task._id)"
                                :task="task"
                        />
                </div>
        </div>
</template>

<script>
import Task from "./Task";
export default {
        name: "Tasks",
        props: {
                tasks: Array,
        },
        components: { Task },
        emits: ["delete-task", "toggle-reminder"],
};
</script>
