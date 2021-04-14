<template>
    <div>
        <nav-bar :colored-logo="true" />
        <div class="main">
            <banner />
            <promo />
            <work-process :is-gray="false" />
            <offerings :is-gray="true"/>
            <screenshots :padding-top="false" />
        </div>
    </div>
</template>

<script>
    import NavBar from "../../views/commons/NavBar.vue";
    import Banner from "../../views/index-four/Banner.vue";
    import WorkProcess from "../../views/commons/sections/WorkProcess";
    import Offerings from "../../views/about-us/Offerings.vue";
    import Promo from "../../views/index-two/Promo";
    import Screenshots from "../../views/index-one/Screenshots";

    export default {
        name: "IndexFour",
        components: {
            NavBar,
            Banner,
            Promo,
            Offerings,
            WorkProcess,
            Screenshots,
        },
    };
</script>