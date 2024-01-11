<template>
    <section class="hero">
        <div class="hero-pic">
            <img src="/images/timures_photo.jpeg" alt="hero pic">
            
        </div>
        <div class="hero-text">
            <p>
                Hello, I'm
            </p>
            <h1 class="title">Timur Yessentayev</h1>
            <p class="desc">
                Frontend Developer
            </p>
            <div class="hero-actions">
                <a href="#contacts" class="btn hero-action--contact">Contact Info</a>
            </div>
            <div class="hero-socials">
                <a href="https://github.com/Timures/" target="_blank" rel="nofollow">
                    <img class="icon" src="/images/icons/github-142-svgrepo-com.svg" alt="Github Profile">
                </a>
                <a href="https://www.linkedin.com/in/timures" target="_blank" rel="nofollow">
                    <img class="icon" src="/images/icons/linkedin-round-svgrepo-com.svg" alt="LinkedIn Profile">
                </a>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
.hero {
    min-height: 96vh;
    margin: 0 10rem;
    display: flex;
    align-items: center;
    justify-content: center;
    column-gap: 10%;

    @media screen and (max-width: 1023px) {
        margin: 0 2rem;
        min-height: calc(100svh - 67px);
    }

    @media screen and (max-width: 767px) {
        margin: 0 1rem;
    }
}

.hero-pic {
    position: relative;
    img {
        width: 100%;
        max-width: 400px;
        border-radius: 100%;
    }
    @media screen and (max-width: 767px) {
        display: none;
    }
}



.hero-text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    p {
        font-size: 1.75rem;
    }

    h1 {
        font-size: 3rem;
        @media (max-width: 767px) { 
            text-align: center;
            font-size: 2.5rem;
         }
    }

    .desc {
        font-size: 2rem;
        color: rgba(#111, 0.6);
        font-weight: bold;
        @media screen and (max-width: 767px) {
        font-size: 1.5rem;
    }
    }

}

.hero-actions {
    padding: 1rem 0;
    display: flex;
    justify-content: center;

    gap: 1rem;

    @media screen and (max-width: 767px) {
        flex-direction: column;
        width: 90%;
        margin: 2rem auto;
    }
}

.btn {
    font-size: 1rem;
    line-height: 1;
    font-weight: bold;
    transition: 0.35s ease-in-out all;
    padding: 1rem;
    width: 10rem;
    border-radius: 2rem;
    border: 1px solid #111;
    cursor: pointer;

    @media screen and (max-width: 767px) {
        width: 100%;
    }
}

.hero-action {
    &--download {   
        &:hover {
            background-color: rgba(#111, 0.6);
            color:#fff;
        }
    }
    &--contact {
        background-color: rgba(#111, 0.8);
        color: #fff;
        text-align: center;
        text-decoration: none;
        &:hover {
            background-color: #000;
        }
    }
}



.hero-socials {
    display: flex;
    justify-content: center;
    gap: 1rem;
    .icon {
        width: 100%;
        max-width: 2rem;
    }
}</style>