<script setup>
import ApplicationLogo from "@/Components/ApplicationLogo.vue";
</script>

<template>
    <div>
        <div>
            <div v-if="$page.props.user.permissions.includes('read articles')">
                <button type="button">Read article</button>
            </div>

            <div v-if="$page.props.user.permissions.includes('write articles')">
                <button type="button">Write article</button>
            </div>

            <div v-if="$page.props.user.permissions.includes('edit articles')">
                <button type="button">Edit article</button>
            </div>

            <div
                v-if="$page.props.user.permissions.includes('delete articles')"
            >
                <button type="button">Delete article</button>
            </div>
        </div>
    </div>
</template>
