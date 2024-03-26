<template>
    <nav class="navbar">
        <div class="container flex justify-evenly">
            <ul class="navbar-nav flex">
                <li class="nav-item">
                    <a href="#about">Services</a>
                </li>
                <li class="nav-item">
                    <a href="#services">Packs</a>
                </li>
            </ul>
            <a class="navbar-brand" href="#"> <img src="/Felek.svg" class="logo" alt="Felek logo" /></a>
            <ul class="navbar-nav flex">
                <li class="nav-item">
                    <a href="#about">Events</a>
                </li>
                <li class="nav-item">
                    <a href="#services">About</a>
                </li>
            </ul>
        </div>
    </nav>
</template>

<style scoped>

.logo {
    fill: white;
    height: 200px;
    margin-top: 40px;
}

.navbar {
    font-family: 'Lemon Milk';
    height: 100px;
    top: 0;
    left: 0;
    width: 100%;
    padding: 10px 0;
    z-index: 1000;
    /* Ensure it's above other content */
}

.container {
    display: flex;
    justify-content: space-between;
    height: 100px;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
}

.navbar-nav {
    gap: 40px;
    padding: 0px 30px;
}

.navbar-brand,
.nav-item {
    color: #fff;
    text-decoration: none;
    padding: 0 10px;
}

.nav-item a {
    text-decoration: none;
    color: #fff;
}

.nav-item a:hover {
    color: #ccc;
}
</style>