<template>
    <div class="project-card">
        <div class="project-card_img">
            <img :src="`images/projects/${project.pic}`" :alt="`screenshot from ${project.title}`">
        </div>
        <div class="project-card_info">
            <div class="project-card_title">{{ project.desc }}</div>
            <div class="project-card_link">
                <a :href="project.url" class="project-card_link-btn" target="_blank" rel="nofollow">{{
                project.title }}</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProjectCard',
    props: {
        project: Object
    }
}
</script>

<style lang="scss">
.project-card {
    display: flex;
    flex-direction: column;
    border: 1px solid #111;
        border-radius: 2rem;
        padding: 1rem;
    gap: 1rem;
    padding: 1rem;
    &_img {
        img {
            width: 100%;
            max-height: 320px;
            border-radius: 1rem;
        }
    }

    &_info { 
        display: flex;
        justify-content: center;
        gap: 1rem;
        padding: 1rem;
        min-height: 57px;
        @media screen and (max-width: 767px) {
            flex-direction: column;
        }
    }

    &_link-btn {       
        font-size: 1rem;
        line-height: 1;
        font-weight: bold;
        transition: 0.35s ease-in-out all;
        padding: 1rem;
        width: 10rem;
        border-radius: 2rem;
        border: 1px solid #111;
        cursor: pointer;
        color: #111;
        text-decoration: none;
        transition: 0.25s ease-in-out all;

        &:hover {
            border-color: rgba(17,17,17, 0.6);
        }
    }
}


</style>