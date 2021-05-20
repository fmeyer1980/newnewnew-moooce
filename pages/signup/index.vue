<template>
    <section class="signup">
        <Test headline="Ansøg om at komme med fra start" summary="- Vær blandt de første der kan sælge varer via Moooce" />
        <Signup />
        <img src="/images/moooce-live-mobile-video-commerce.jpg" alt="Signup for Moooce" />
    </section>
</template>

<script>
import Test from '@/components/Test'
import Signup from "~/components/Signup";
export default {
    name: "signup",
    components: {Signup,Test},
    meta: {
        pageClasses: ['no-top-padding'],
    }
};
</script>

<style lang="scss" scoped>
.signup{
    position: relative;

    img{
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top center;
        opacity: .2;
        z-index: -1;
    }
}
</style>
