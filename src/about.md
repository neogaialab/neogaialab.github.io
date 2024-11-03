---
layout: page
---

<script setup>
import { VPTeamPage, VPTeamPageTitle, VPTeamMembers, VPTeamPageSection, VPLink, VPHomeContent } from 'vitepress/theme'
import PageSection from './components/PageSection.vue'

const siteSvg = '<svg role="img" xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 16 16"><path fill="currentColor" d="M0 8a8 8 0 1 1 16 0A8 8 0 0 1 0 8m7.5-6.923c-.67.204-1.335.82-1.887 1.855A8 8 0 0 0 5.145 4H7.5zM4.09 4a9.3 9.3 0 0 1 .64-1.539a7 7 0 0 1 .597-.933A7.03 7.03 0 0 0 2.255 4zm-.582 3.5c.03-.877.138-1.718.312-2.5H1.674a7 7 0 0 0-.656 2.5zM4.847 5a12.5 12.5 0 0 0-.338 2.5H7.5V5zM8.5 5v2.5h2.99a12.5 12.5 0 0 0-.337-2.5zM4.51 8.5a12.5 12.5 0 0 0 .337 2.5H7.5V8.5zm3.99 0V11h2.653c.187-.765.306-1.608.338-2.5zM5.145 12q.208.58.468 1.068c.552 1.035 1.218 1.65 1.887 1.855V12zm.182 2.472a7 7 0 0 1-.597-.933A9.3 9.3 0 0 1 4.09 12H2.255a7 7 0 0 0 3.072 2.472M3.82 11a13.7 13.7 0 0 1-.312-2.5h-2.49c.062.89.291 1.733.656 2.5zm6.853 3.472A7 7 0 0 0 13.745 12H11.91a9.3 9.3 0 0 1-.64 1.539a7 7 0 0 1-.597.933M8.5 12v2.923c.67-.204 1.335-.82 1.887-1.855q.26-.487.468-1.068zm3.68-1h2.146c.365-.767.594-1.61.656-2.5h-2.49a13.7 13.7 0 0 1-.312 2.5m2.802-3.5a7 7 0 0 0-.656-2.5H12.18c.174.782.282 1.623.312 2.5zM11.27 2.461c.247.464.462.98.64 1.539h1.835a7 7 0 0 0-3.072-2.472c.218.284.418.598.597.933M10.855 4a8 8 0 0 0-.468-1.068C9.835 1.897 9.17 1.282 8.5 1.077V4z"/></svg>'

const members = [
    {
        name: 'Luis Emidio',
        title: 'Founder | Software Developer',
        avatar: 'https://www.github.com/luisfuturist.png',
        links: [
            { icon: 'github', link: 'https://github.com/luisfuturist' },
            { icon: 'x', link: 'https://x.com/luisfuturist' },
            { icon: { svg: siteSvg }, link: 'https://luisfuturist.com' },
        ]
    },
    {
        name: 'Vinicius Emidio Bosi',
        title: 'Software Developer',
        avatar: 'https://github.com/vinicenter.png',
        links: [
            { icon: 'github', link: 'https://github.com/vinicenter' },
            { icon: 'twitter', link: 'https://x.com/vinicenter' },
            { icon: { svg: siteSvg }, link: 'https://vini.center' },
        ]
    },
    {
        name: 'Kruceo',
        title: 'Software Developer',
        avatar: 'https://github.com/kruceo.png',
        links: [
            { icon: 'github', link: 'https://github.com/kruceo' },
            { icon: { svg: siteSvg }, link: 'https://kruceo.com' },
        ]
    }
];
</script>

<VPTeamPage>
    <VPTeamPageTitle>
        <template #title>About</template>
        <template #lead>
            At NeoGaia Lab, we are a small group of developers dedicated to exploring and developing minimal, open-source projects.
        </template>
    </VPTeamPageTitle>
    <PageSection>
        <template #title>Members</template>
        <template #default>
            <p class="mb-6">
                At NeoGaia Lab, we are a small group of developers dedicated to exploring and developing minimal, open-source projects.
            </p>
            <VPTeamMembers size='small' :members='members.slice(0, 1)' />
            <div class="mb-6" />
            <VPTeamMembers size='small' :members='members.slice(1)' />
        </template>
    </PageSection>
    <PageSection>
        <template #title>Contact Us</template>
        <template #default>
            <p class="mb-2">
                We are always looking for passionate individuals to join us. If you're interested in collaborating or contributing to our projects, feel free to reach out!
            </p>
            <p>
                For inquiries, please contact Luis at <VPLink href="mailto:luisfuturist@gmail.com">luisfuturist@gmail.com</VPLink>.
            </p>
        </template>
    </PageSection>
</VPTeamPage>