<template>
    <div>
        <header>
            <h1>product</h1>
        </header>  
        <div>
            <slot/>
        </div>
        <footer>
            <nav>
            <ul>
                <li><NuxtLink to="/">Home</NuxtLink> </li>
                <li><NuxtLink to="/about">About</NuxtLink> </li>
            </ul>
        </nav>
        </footer>  
    </div>
</template>
