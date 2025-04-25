<template>
    <section class="about-section">
        <h2>About Me</h2>
        <p>I'm a mid-level developer focused on backend and system integration. I work with TypeScript , Python and
            I'm constantly seeking to evolve both professionally and personally.</p>
    </section>
</template>

<script setup lang="ts">
// No additional setup needed
</script>

<style scoped>
.about-section {
    background: linear-gradient(135deg, rgba(255, 255, 255, 0.05) 0%, rgba(128, 128, 128, 0.05) 100%);
    padding: 4rem 2rem;
    width: 100%;
    border: 1px solid rgba(255, 255, 255, 0.1);
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
}

.about-section h2 {
    margin-bottom: 2rem;
    text-align: center;
}

.about-section p {
    font-size: 1.1rem;
    line-height: 1.8;
    text-align: center;
    max-width: 600px;
    margin: 0 auto;
}

@media (max-width: 768px) {
    .about-section {
        padding: 3rem 1.5rem;
        margin: 2rem 1rem;
    }
}
</style>