<template>
    <div class="try">
        <p v-if="true">Try This!</p>
        <p v-if="false">Don't Try This!</p>
        <p>Users</p>
        <ul>
            <li v-for="name in usernames" v-bind:key="name">{{name}}</li>
        </ul>
        <button :disabled="disabled">Button!</button>
        <p>Seconds: {{seconds}}</p>
    </div>
</template>

<script>
export default {
    name: 'Try',
    data() {
        return {
            seconds: 0,
            disabled: true,
            usernames: [
                "Brian",
                "Tia",
                "Pepper",
                "Ivy"
            ]
        }
    },
    created() {
        setInterval(() => this.seconds++, 1000); 
    }
}
</script>