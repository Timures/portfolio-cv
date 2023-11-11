<template>
    <nav>
        <ul class="nav-links">
            <li class="nav-link"><a href="#about">About</a></li>
            <li class="nav-link"><a href="#experience">Experience</a></li>
            <li class="nav-link"><a href="#projects">Projects</a></li>
            <li class="nav-link"><a href="#contacts">Contacts</a></li>
        </ul>


    </nav>
</template>

<style lang="scss">
.nav-links {
    list-style-type: none;
    display: flex;
    margin: 0;
    padding: 0;
    column-gap: 20px;

    @media screen and (max-width: 768px) {
        display: none;
    }
}

.nav-link {
    font-size: 1.5rem;

    a {
        text-decoration: none;
        color: #111111;
        transition: 0.35 ease-in-out color;

        &:hover {
            color: rgba(#111111, 0.6)
        }
    }
}

.nav-link {
    display: flex;
}</style>