<template>
    <div class="card" :style="{ '--card-color': color }">
        <div class="card-icon">
            <slot name="icon"></slot>
        </div>
        <h3 class="card-title">{{ title }}</h3>
        <p class="card-description">{{ description }}</p>
        <a v-if="websiteUrl" :href="websiteUrl" target="_blank" rel="noopener noreferrer" class="website-link">
            Visit Website
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none"
                stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"></path>
                <polyline points="15 3 21 3 21 9"></polyline>
                <line x1="10" y1="14" x2="21" y2="3"></line>
            </svg>
        </a>
    </div>
</template>

<script setup lang="ts">
defineProps<{
    title: string;
    description: string;
    color: string;
    websiteUrl?: string;
}>();
</script>

<style scoped>
.card {
    background: linear-gradient(145deg, rgba(30, 20, 15, 0.8), rgba(20, 15, 10, 0.95));
    border: 1px solid rgba(193, 41, 6, 0.1);
    border-radius: 12px;
    padding: 2rem;
    width: 100%;
    max-width: 350px;
    min-height: 250px;
    display: flex;
    flex-direction: column;
    align-items: center;
    transition: var(--transition);
    position: relative;
    overflow: hidden;
    backdrop-filter: blur(10px);
}

.card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: var(--card-color);
    box-shadow: 0 0 20px var(--card-color);
}

.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 30px rgba(193, 41, 6, 0.15);
    background: linear-gradient(145deg, rgba(35, 25, 20, 0.85), rgba(25, 20, 15, 0.98));
}

.card-icon {
    width: 60px;
    height: 60px;
    border-radius: 50%;
    background: var(--card-color);
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 1.5rem;
    font-size: 1.5rem;
    color: var(--bg-color);
    box-shadow: 0 0 15px var(--card-color);
}

.card-title {
    font-size: 1.5rem;
    margin-bottom: 1rem;
    color: var(--text-color);
    font-weight: 500;
}

.card-description {
    text-align: center;
    line-height: 1.6;
    color: var(--text-color);
    opacity: 0.9;
    margin-bottom: 1.5rem;
}

.website-link {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.5rem 1rem;
    background: var(--card-color);
    color: var(--bg-color);
    border-radius: 6px;
    font-weight: 500;
    transition: var(--transition);
    margin-top: auto;
}

.website-link:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 15px var(--card-color);
}

.website-link svg {
    transition: transform 0.3s ease;
}

.website-link:hover svg {
    transform: translate(2px, -2px);
}
</style>