<template>
    <section class="experience" id="experience">
        <SectionTitle :title="title" :desc="desc" />
        <div class="section-content">
            <div class="experience-content">
                <div class="experience-details">
                    <h2>Frontend Development</h2>
                    <div class="experiences-container">
                        <experience-item v-for="experience in experiences" :key="experience.id" :experience="experience" />
                    </div>
                </div>

                <div class="experience-details">
                    <h2>Frontend Development - Additionally</h2>
                    <div class="experiences-container">
                        <experience-item v-for="additional in additionally" :key="additional.id" :experience="additional" />
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import { ref } from 'vue';
import ExperienceItem from './ExperienceItem.vue';
import SectionTitle from './SectionTitle.vue';
export default {
    components: {
        SectionTitle,
        ExperienceItem
    },
    setup() {
        // Список опыта
        const experiences = ref([
            { id: 1, title: 'Vue', description: 'Experienced' },
            { id: 2, title: 'React', description: 'Intermediate' },
            { id: 3, title: 'JavaScript', description: 'Intermediate' },
            { id: 4, title: 'TypeScript', description: 'Intermediate' },
            { id: 5, title: 'SASS', description: 'Advanced' },
            
            // Добавь больше опыта, если необходимо
        ]);
        const additionally = ref([
            { id: 1, title: 'Git', description: 'Intermediate' },
            { id: 2, title: 'Figma', description: 'Basic' },
            { id: 5, title: 'BEM', description: 'Advanced' },
            // Добавь больше опыта, если необходимо
        ]);

        const title = ref('Experience')
        const desc = ref('Explore My')

        return {
            title, desc, experiences, additionally
        };
    }
}
</script>

<style lang="scss">

.experience {
    min-height: 96vh;
    width: 90%;
    max-width: 1024px;
    margin: 0 auto;
    @media screen and (max-width: 1023px) {
        width: 90%;
    }
    @media screen and (max-width: 767px) {
        width: 100%;
        padding: 0 1rem 5rem;
    }

    &-content {
        display: flex;
        gap: 2rem;
        @media screen and (max-width: 1023px) {
            flex-direction: column;
        }
    }

    &-details {
        border: 1px solid #111;
        border-radius: 2rem;
        padding: 1rem;
        width: 100%;
        h2 {
            text-align: center;
            color: rgba(#111, 0.8);
            font-weight: bold;
        }
    }
}

.experiences-container {
    margin-top: 1rem;
    display: grid;
    grid-template-columns: repeat(2, auto);
    grid-template-rows: auto;
    gap: 2rem;
}
</style>