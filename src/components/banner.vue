<template>
    <div class="container">
        <div class="banner_container">
            <div class="image">
                <img class="mobile img_mob" src="@/assets/mobile-banner.png" alt="banner mobile">
            </div>
            <div class="image">
                <img class="desktop" src="@/assets/desktop-.jpg" alt="banner desktop">
            </div>
            <div class="points">
                <div class="point active"></div>
                <div class="point"></div>
                <div class="point"></div>
            </div>
        </div>

    </div>
</template>
<script>
export default {
    name: 'bannerComponent',
    data() {
        return {

        }
    },
    methods: {

    }
}
</script>
<style>
.desktop {
    width: 100%;
    display: none;
}

.mobile {
    width: 100%;
    display: block;
}

.image img{
    width: 100%;
    height: auto;
}
.banner_container {
    position: relative;
    overflow: hidden;
}

.points {
    margin-top: 10px;
    text-align: center;
    position: absolute;
    bottom: 10px;
    left: 40%;
}

.point {
    display: inline-block;
    width: 14px;
    height: 14px;
    background-color: #E6E6E6;
    border-radius: 50%;
    margin: 0 5px;
    cursor: pointer;
}

.point.active {
    background-color: #1C69D4;
}

@media(min-width: 769px) {
    .mobile {
        display: none;
    }

    .desktop {
        display: block;
    }
    .points{
        left: 50%;
    }
}</style>