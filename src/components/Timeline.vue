<template>
    <h2>Timeline</h2>
    <div class="timeline">
        <div v-for="(item, index) in timelineItems" :key="index" class="timeline-item">
            <div class="timeline-content" :class="{ 'timeline-right': index % 2 === 0 }">
                <div class="timeline-card">
                    <h3>{{ item.title }}</h3>
                    <p>{{ item.description }}</p>
                    <span class="timeline-date">{{ item.date }}</span>
                </div>
            </div>
            <div class="timeline-dot">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="timeline-icon">
                    <path :d="item.icon" />
                </svg>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Timeline',
    data() {
        return {
            timelineItems: [
                {
                    title: 'Independent Developer & Job Seeker',
                    description: 'Currently working on side projects like a game and looking for a job',
                    date: '2025 - Present',
                    icon: 'M21.731 2.269a2.625 2.625 0 00-3.712 0l-1.157 1.157 3.712 3.712 1.157-1.157a2.625 2.625 0 000-3.712zM19.513 8.199l-3.712-3.712-12.15 12.15a5.25 5.25 0 00-1.32 2.214l-.8 2.685a.75.75 0 00.933.933l2.685-.8a5.25 5.25 0 002.214-1.32L19.513 8.2z'
                },
                {
                    title: 'Full Stack Developer',
                    description: 'At Toki, I learned to learn. All knowledge that came from this was driven by knowing how to study alone and efficiently. The knowledge acquired was countless, but here I can name a few: Most used design patterns and how to use them, DDD and ES, and best of all, I am now self-taught',
                    date: '2021 - 2025',
                    icon: 'M11.42 15.17L17.25 21A2.652 2.652 0 0021 17.25l-5.877-5.877M11.42 15.17l2.496-3.03c.317-.384.74-.626 1.208-.766M11.42 15.17l-4.655 5.653a2.548 2.548 0 11-3.586-3.586l6.837-5.63m5.108-.233c.55-.164 1.163-.188 1.743-.14a4.5 4.5 0 004.486-6.336l-3.276 3.277a3.004 3.004 0 01-2.25-2.25l3.276-3.276a4.5 4.5 0 00-6.336 4.486c.091 1.076-.071 2.264-.904 2.95l-.102.085m-1.745 1.437L5.909 7.5H4.5L2.25 3.75l1.5-1.5L7.5 4.5v1.409l4.26 4.26m-1.745 1.437l1.745-1.437m6.615 8.206L15.75 15.75M4.867 19.125h.008v.008h-.008v-.008z'
                },
                {
                    title: 'Freelancer',
                    description: 'Learning web development fundamentals. Working with HTML, CSS and JavaScript. Participation in real projects.',
                    date: '2020 - 2021',
                    icon: 'M4.26 10.147a60.436 60.436 0 00-.491 6.347A48.627 48.627 0 0112 20.904a48.627 48.627 0 018.232-4.41 60.46 60.46 0 00-.491-6.347m-15.482 0a50.57 50.57 0 00-2.658-.813A59.905 59.905 0 0112 3.493a59.902 59.902 0 0110.399 5.84c-.896.248-1.783.52-2.658.814m-15.482 0A50.697 50.697 0 0112 13.489a50.702 50.702 0 017.74-3.342M6.75 15a.75.75 0 100-1.5.75.75 0 000 1.5zm0 0v-3.675A55.378 55.378 0 0112 8.443m-7.007 11.55A5.981 5.981 0 006.75 15.75v-1.5'
                }
            ]
        }
    }
}
</script>

<style scoped>
.timeline {
    position: relative;
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
}

h2 {
    margin-bottom: 1rem;
    text-align: center;
}

.timeline::after {
    content: '';
    position: absolute;
    width: 4px;
    background-color: #e5e7eb;
    top: 0;
    bottom: 0;
    left: 50%;
    margin-left: -2px;
}

.timeline-item {
    padding: 10px 40px;
    position: relative;
    width: 50%;
}

.timeline-item:nth-child(odd) {
    left: 0;
}

.timeline-item:nth-child(even) {
    left: 50%;
}

.timeline-dot {
    position: absolute;
    width: 40px;
    height: 40px;
    background-color: #3b82f6;
    border-radius: 50%;
    top: 50%;
    transform: translateY(-50%);
    z-index: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
}

.timeline-item:nth-child(odd) .timeline-dot {
    right: -20px;
}

.timeline-item:nth-child(even) .timeline-dot {
    left: -20px;
}

.timeline-icon {
    width: 24px;
    height: 24px;
}

.timeline-right {
    left: 50%;
}

.timeline-content {
    padding: 20px;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1);
}

.timeline-card h3 {
    margin: 0 0 10px 0;
    color: #1f2937;
    font-size: 1.25rem;
}

.timeline-card p {
    margin: 0 0 10px 0;
    color: #4b5563;
}

.timeline-date {
    color: #6b7280;
    font-size: 0.875rem;
}

@media screen and (max-width: 768px) {
    .timeline::after {
        left: 31px;
    }

    .timeline-item {
        width: 100%;
        padding-left: 70px;
        padding-right: 25px;
        left: 0 !important;
    }

    .timeline-dot {
        left: 11px !important;
    }

    .timeline-right {
        left: 0;
    }
}
</style>