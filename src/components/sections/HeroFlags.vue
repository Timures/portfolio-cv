<template>
<div class="hero-flags">
    <img src="/images/flags/kz.svg" alt="Kazakhstan flag">
    <img src="/images/flags/ua.svg" alt="Ukraine flag">
    <img src="/images/flags/il.svg" alt="Israel flag">
</div> 
</template>


<style lang="scss">
.hero-flags {
    position: absolute;
    right: 1rem;
    bottom: 1rem;
    display: flex;
    gap: 1rem;
    justify-content: center;
    img {
        width: 100%;
        max-width: 32px;
        border-radius: 5px;
        box-shadow: 0px 2px 4px 2px rgba(34, 60, 80, 0.2);
    }
}
</style>