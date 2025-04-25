<template>
    <div class="social-icons">
        <a href="https://github.com/albnunes" target="_blank" rel="noopener noreferrer" class="social-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
                stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path
                    d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22">
                </path>
            </svg>
            <span class="tooltip">GitHub</span>
        </a>
        <a href="https://www.linkedin.com/in/alberto-nunes-macana/" target="_blank" rel="noopener noreferrer" class="social-icon">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
                stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path>
                <rect x="2" y="9" width="4" height="12"></rect>
                <circle cx="4" cy="4" r="2"></circle>
            </svg>
            <span class="tooltip">LinkedIn</span>
        </a>
    </div>
</template>

<script setup lang="ts">
// No additional setup needed
</script>

<style scoped>
.social-icons {
    display: flex;
    justify-content: center;
    gap: 1.5rem;
    margin-top: 2rem;
}

.social-icon {
    position: relative;
    color: var(--text-color);
    transition: var(--transition);
}

.social-icon:hover {
    color: var(--accent);
    transform: translateY(-3px);
}

.tooltip {
    position: absolute;
    bottom: -30px;
    left: 50%;
    transform: translateX(-50%);
    background: var(--accent);
    color: var(--bg-color);
    padding: 0.5rem 1rem;
    border-radius: 4px;
    font-size: 0.875rem;
    opacity: 0;
    visibility: hidden;
    transition: var(--transition);
    white-space: nowrap;
}

.tooltip::before {
    content: '';
    position: absolute;
    top: -5px;
    left: 50%;
    transform: translateX(-50%);
    border-width: 0 5px 5px 5px;
    border-style: solid;
    border-color: transparent transparent var(--accent) transparent;
}

.social-icon:hover .tooltip {
    opacity: 1;
    visibility: visible;
    bottom: -35px;
}
</style>