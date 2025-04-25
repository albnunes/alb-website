<template>
    <footer class="footer">
        <div class="contact-section">
            <h2>Contact</h2>
            <ul>
                <li><a href="mailto:bisneto.alberto@gmail.com">Email</a></li>
                <li><a href="https://www.linkedin.com/in/alberto-nunes-macana/" target="_blank">LinkedIn</a></li>
                <li><a href="https://github.com/albnunes" target="_blank">GitHub</a></li>
            </ul>
        </div>
        <div class="copyright">
            © 2020-2025 Alberto Nunes
        </div>
    </footer>
</template>

<style scoped>
.footer {
    width: 100%;
    padding: 2rem 0;
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.contact-section {
    margin-bottom: 2rem;
    text-align: center;
    max-width: 600px;
    width: 100%;
    padding: 0 1rem;
}

.contact-section ul {
    display: inline-block;
    text-align: center;
}

.contact-section li {
    text-align: left;
    display: inline-block;
    margin: 0 1rem;
}

.copyright {
    font-size: 0.75rem;
    color: var(--text-color);
    opacity: 0.7;
    text-align: center;
    padding: 1rem 0;
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
}
</style>