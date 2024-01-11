<template>
    <article class="experience-item">
        <div class="experience-item__content">
            <h3>{{ experience.title }}</h3>
            <p>{{ experience.description }}</p>
        </div>
    </article>
</template>
  
<script>
export default {
    props: {
        experience: Object
    }
}
</script>
  
<style lang="scss">
.experience-item {
    display: flex;
    align-items: baseline;
    gap: 2rem;
    padding: 0.5rem;
    @media screen and (max-width: 540px) {
        padding: 0.1rem;
    }
    &__content {
        position: relative;
        padding-left: calc(24px + 1rem);
        @media screen and (max-width: 540px) {
            padding-left: calc(18px + 1rem);
        }
        &::before {
            content: "";
            position: absolute;
            top:4px;
            left: 0;
            width: 24px;
            height: 24px;
            display: inline-block;
            background-image: url(../../images/icons/check-success-svgrepo-com.svg);
            background-size: cover;
            @media screen and (max-width: 540px) {
                width: 18px;
                height: 18px;
            }
        }
        h3 {
            font-weight: bold;
            @media screen and (max-width: 767px) {
                font-size: 1rem;
            }
        }
        p {
            @media screen and (max-width: 767px) {
                font-size: 0.9rem;
            }
        }
    }
    img {
        width: 24px;
    }
}
</style>
  