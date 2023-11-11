<template>
    <section class="projects" id="projects">
        <SectionTitle :title="title" :desc="desc" />
        <div class="section-content">
            <ProjectsSlider />
        </div>
    </section>
</template>

<script>
import { ref } from 'vue';
import SectionTitle from './SectionTitle.vue';
import ProjectsSlider from './ProjectsSlider.vue';

export default {
    components: {
        SectionTitle,
        ProjectsSlider
    },
    setup(){
        const title = ref('Projects')
        const desc = ref('Browse My Recent')

        return {
            title, desc
        };
    }
}
</script>

<style lang="scss">
.projects {
    min-height: 96vh;
    margin: 0 3rem;
}
</style>