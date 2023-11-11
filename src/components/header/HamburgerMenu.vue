<template>
    <div class="hamburger-nav" @click="toggleHamburgerLinks">
        <button class="hamburger-icon" :class="{ 'open': isHamburgerActive }">
            <span class="top"></span>
            <span class="middle"></span>
            <span class="bottom"></span>
        </button>
        <div class="hamburger-links" :class="{ 'open': isHamburgerActive }">
            <ul>
                <li class="nav-link"><a href="#about">About</a></li>
                <li class="nav-link"><a href="#experience">Experience</a></li>
                <li class="nav-link"><a href="#projects">Projects</a></li>
                <li class="nav-link"><a href="#contacts">Contacts</a></li>
            </ul>
        </div>
    </div>
</template>
  
<script>
import { ref } from 'vue';

export default {
    setup() {
        const isHamburgerActive = ref(false);

        const toggleHamburgerLinks = () => {
            isHamburgerActive.value = !isHamburgerActive.value;
        };

        return {
            isHamburgerActive,
            toggleHamburgerLinks
        };
    }
};
</script>
  
<style lang="scss">
.hamburger-nav {
    display: none;

    @media screen and (max-width: 768px) {
        display: flex;
    }
}

.hamburger-links {
    position: absolute;
    top: 3.5rem;
    left: 100%;
    background-color: #cecece;
    width: 0;
    height: calc(100svh - 3.5rem);
    overflow: hidden;
    transition: all 0.35s ease-in-out;
    
    &.open {
        left: 0;
        padding: 1rem;
        width: 100%;
    }

    ul {
        margin: 2rem auto;
        padding: 0;
        display: flex;
        flex-direction: column;
        gap: 2rem;
        align-items: center;

        li {
            a {
                font-size: 1.5rem;
            }
            &:not(:first-child){
                position: relative;
                
                &::before {
                    content: "";
                    position: absolute;
                    top: -25px;
                    left: calc(50% - 12px);
                    background-image: url(/wolf-192.png);
                    background-repeat: no-repeat;
                    background-position: 0 0;
                    background-size: contain;
                    width: 24px;
                    height: 24px;
                }
            }
        }
    }
}

.hamburger-icon {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 24px;
    width: 30px;
    cursor: pointer;
    position: relative;
    background-color: none;
    border: none;
    background: transparent;
    span {
        display: block;
        width: 20px;
        height: 2px;
        margin: auto;
        background: #111;
        position: absolute;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        transition: all .4s ease;

        &.top {
            transform: translateY(-8px);
        }

        &.bottom {
            transform: translateY(8px);
        }
    }

    &.open {
        .top {
            transform: rotate(-45deg);
        }

        .middle {
            transform: translateX(20px) rotate(-360deg);
            opacity: 0;
        }

        .bottom {
            transform: rotate(45deg);
        }
    }
}</style>
  