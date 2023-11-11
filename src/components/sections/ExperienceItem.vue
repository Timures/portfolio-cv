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
    &__content {
        position: relative;
        padding-left: calc(24px + 1rem);
        &::before {
            content: "";
            position: absolute;
            top:4px;
            left: 0;
            width: 24px;
            height: 24px;
            display: inline-block;
            background-image: url(../../assets/icons/check-success-svgrepo-com.svg);
            background-size: cover;
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
  