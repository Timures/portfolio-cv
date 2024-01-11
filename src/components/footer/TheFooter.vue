<template>
    <footer class="footer">
        <TheNavbar />
        
        <div class="footer_content">
            <p>&copy; {{ currentYear }} All Rights Reserved.</p>
            <p>Timur Yessentayev</p>
        </div>
    </footer>
</template>

<script>
import TheNavbar from '../header/TheNavbar.vue';

export default {
    components: {
        TheNavbar
    },
    data() {
    return {
      currentYear: new Date().getFullYear(),
    };
  },
}
</script>

<style lang="scss">
    .footer {
        display: flex;
        flex-direction: column;
        gap: 3rem;

        justify-content: center;
        align-items: center;

        margin: 3rem auto;

        &_content {
            text-align: center;
        }
        
    }
</style>