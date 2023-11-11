<template>
     <div class="logo">
        <img src="/android-chrome-512x512.png" alt="logo Timur Yessentayev">   
        Timur Yessentayev
        </div>
</template>

<style lang="scss">
.logo {
    font-size: 2rem;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 0.5rem;
    img {
        width: 100%;
        max-width: 32px;
    }
    @media screen and (max-width: 768px) {
        font-size: 1.5rem;
    }
}
</style>