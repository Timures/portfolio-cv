<template>
    <section id="contacts" class="contact">
        <SectionTitle :title="title" :desc="desc" />
        <div class="contact-content">
            <a :href="`mailto:${mail}`" class="contact_link">
                <img src="/images/icons/email-circle-fill-svgrepo-com.svg" alt="mail icon">
                <span>Write Me</span>
            </a>
            <a :href="linkedin" target="_blank" rel="nofollow" class="contact_link">
                <img src="/images/icons/linkedin-round-svgrepo-com.svg" alt="linkedIn icon">
                <span>LinkedIn</span>
            </a>
        </div>
    </section>
</template>

<script>
import { ref } from 'vue';
import SectionTitle from './SectionTitle.vue';

export default {
    components: {
        SectionTitle
    },
    setup() {
        const title = ref('Contact Me')
        const desc = ref('Get In Touch')
        const mail = ref('bisemsk@gmail.com')
        const linkedin = ref('https://www.linkedin.com/in/timures/')
        return {
            title, desc, mail, linkedin
        };
    }
}
</script>

<style lang="scss">
.contact {
    height: 50vh;
    margin: 0 10rem;
    @media screen and (max-width: 767px) {
        margin: 0 1rem;
    }

    &-content {
        margin: 2rem auto;
        border: 1px solid #111;
        border-radius: 2rem;
        padding: 1rem;
        display: flex;
        justify-content: space-around;
        gap: 5rem;
        width: fit-content;
        @media screen and (max-width: 767px) {
            flex-direction: column;
            gap: 2rem;
            width: 90%;
        }
    }

    &_link {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 1rem;
        text-decoration: none;
        color: #111;
        font-size: 1.2rem;
        padding: 0.5rem;

        img {
            width: 100%;
            max-width: 40px;
        }
    }
}</style>