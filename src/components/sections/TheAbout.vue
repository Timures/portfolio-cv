

<template>
    <section class="about" id="about">

        <SectionTitle :title="title" :desc="desc" />
        <div class="about-content">
            <div class="about-pic">
                <img src="/images/t-shirt.png" alt="Vue logo">
            </div>
            <div class="about-details">
                <div class="about-main">
                    <div class="about-experience">
                        <img src="/images/icons/user-success.svg" alt="experience">
                        <h3>Experience</h3>
                        <p>6+ years <br />Frontend Development</p>
                    </div>

                    <div class="about-experience">
                        <img src="/images/icons/user-success.svg" alt="experience">
                        <h3>Experience</h3>
                        <p>3+ years <br />Business Analyst</p>
                    </div>
                </div>

                <div class="about-text">
                    <h3>About Me</h3>
                    <p>
                        Hey there! 👋 I'm Timur, a passionate frontend developer with over five years of hands-on
                        experience in creating immersive and user-friendly web experiences.
                    </p>

                    <h3>Professional Background:</h3>
                    <p>
                        I've dedicated the past few years to honing my skills in frontend development, working on a variety
                        of projects that span from dynamic websites to responsive web applications. My commitment to staying
                        current with the latest technologies allows me to bring innovative and efficient solutions to every
                        project.
                    </p>

                    <h3>Work experience</h3>
                    <p>
                        I have worked for more than 5 years in several top web agencies with various projects (from landing to CRM), startup, and for more than 2 years as a freelancer (frontend for services, integration with backend). I prefer remote work and flexible schedule.
                    </p>
                    <h3>Hobbies:</h3>
                    <p>
                        Beyond the world of coding, you'll often find me cruising around on my scooter, soaking in the
                        freedom of the open road. Writing is another one of my passions—I maintain a <a
                            href="https://timures.com/" target="_blank">blog</a> specifically geared towards
                        aspiring entrepreneurs, sharing insights, tips, and lessons learned from my own journey.
                    </p>
                </div>
            </div>
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
        const title = ref('About Me')
        const desc = ref('Get To Know More')
        return {
            title, desc
        };
    }
}
</script>

<style lang="scss">
.about {
    min-height: 100vh;
    margin: 0 10rem;

    position: relative;
    max-width: 1280px;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 0 auto;

    &-content {
        margin: 4rem 2rem 0;
        display: grid;
        grid-template-columns: 2fr 3fr;
        grid-template-rows: auto;

        @media screen and (max-width: 1023px) {
            grid-template-columns: auto;
            padding: 1rem;
        }

        @media screen and (max-width: 767px) {
            grid-template-columns: auto;
            padding: 1rem 1rem 5rem;
        }
    }

    &-pic {
        display: flex;
        align-items: center;
        justify-content: center;

        img {
            width: 100%;
            max-width: 250px;
        }

        @media screen and (max-width: 1023px) {
            margin-bottom: 1rem;

            img {
                max-width: 125px;
            }
        }

        @media screen and (max-width: 767px) {
            margin-bottom: 2rem;

            img {
                max-width: 125px;
            }
        }
    }

    &-main {
        display: flex;
        gap: 2rem;
    }

    &-experience {
        width: 100%;
        padding: 1rem;
        border: 1px solid #111;
        border-radius: 12px;

        img {
            width: 100%;
            max-width: 24px;
        }
    }

    &-text {
        margin-top: 2rem;

        h3 {
            margin: 1rem 0;
        }
    }
}


.experience {}

.arrow-down {
    border: none;
    position: absolute;
    bottom: 0;
    right: 0;

    img {
        width: 100%;
        max-width: 24px;
    }
}</style>