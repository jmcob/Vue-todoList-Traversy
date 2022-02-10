<template>
        <label>
                {{ label }}
                <input type="text" />
        </label>
</template>

<script>
export default {
        name: "CustomLoginInput",
        props: {
                label: "",
        },
};
</script>
