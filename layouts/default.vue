<template>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4 flex justify-between items-center">
                <NuxtLink to="/" class="font-bold">NuxtBasic</NuxtLink>
                <ul class="flex gap-4">
                    <li>
                        <NuxtLink to="/">Home</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/about">About</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/products">Products</NuxtLink>
                    </li>
                </ul>
            </nav>
        </header>
    </div>
    <!-- Output the page content -->
    <div class="container mx-auto p-4">
        <slot />
    </div>
</template>

<style scoped>
@import url('../assets/tailwind.css');

.router-link-exact-active {
    color: #f15647;
}
</style>
