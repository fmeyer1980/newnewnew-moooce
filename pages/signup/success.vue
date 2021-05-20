<template>
    <div>
        <Signup :success="true" />
    </div>
</template>

<script>
import Signup from "~/components/Signup";
export default {
    name: "signup",
    components: {Signup},
    meta: {
        pageClasses: ['no-top-padding'],
    },
};
</script>

<style lang="scss" scoped>

</style>

