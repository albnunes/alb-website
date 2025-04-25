<template>
    <section class="projects-section">
        <h2>Portfolio</h2>
        <div class="cards-grid">
            <Card title="Marko Adapter Figma"
                description="A Vite adapter that automatically bundles and inlines all assets (JS, CSS, images) into Figma plugin pages, simplifying the development process with Marko."
                color="#4CAF50" websiteUrl="https://github.com/albnunes/marko-run-adapter-figma">
                <template #icon>
                    <img src="../assets/marko.svg" alt="Marko Logo" class="custom-icon">
                </template>
            </Card>

            <Card title="CVA: Component Variants Automator"
                description="CVA automates variant generation, freeing you from tedious tasks and boosting your productivity."
                color="rgba(193, 41, 6, 0.9)" websiteUrl="https://cva.design">
                <template #icon>
                    <img src="../assets/c_do_cva.png" alt="CVA Logo" class="custom-icon">
                </template>
            </Card>
        </div>
    </section>
</template>

<script setup lang="ts">
import Card from './Card.vue';
</script>

<style scoped>
.projects-section {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.cards-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 350px));
    gap: 2rem;
    width: 100%;
    padding: 2rem;
    margin-top: 2rem;
    justify-content: center;
}

.custom-icon {
    width: 24px;
    height: 24px;
    object-fit: contain;
    filter: brightness(1.1);
}

@media (max-width: 768px) {
    .cards-grid {
        grid-template-columns: minmax(280px, 350px);
        padding: 1rem;
    }
}
</style>