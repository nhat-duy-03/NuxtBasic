<template>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4 flex justify-between items-center">
                <NuxtLink to="/products">NuxtBasic</NuxtLink>
            </nav>
        </header>
    </div>
    <!-- out the page content -->
    <div class="container mx-auto p-4">
        <slot />
    </div>
    <footer class="container mx-auto p-4 flex justify-between border-t-2">
        <ul class="flex gap-4">
            <li>
                <NuxtLink to="/">
                    Home
                </NuxtLink>
            </li>
            <li>
                <NuxtLink to="/about">
                    About
                </NuxtLink>
            </li>
            <li>
                <NuxtLink to="/products">
                    Products
                </NuxtLink>
            </li>
        </ul>
    </footer>
</template>
<style scoped>
.router-link-exact-active {
    color: #f15647
}
</style>