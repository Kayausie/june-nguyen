<script setup>
import { ref } from 'vue'
import profileImage from './assets/unnamed.jpg'
import marriottLogo from './assets/marriot.png'
import careAidLogo from './assets/careaid.svg'
import yboxLogo from './assets/ybox.png'
import rmccLogo from './assets/rmcc.png'
import aiesecLogo from './assets/aiesec.jpg'
import mccormackLogo from './assets/mccormack-logo.jpeg'
import rmitLogo from './assets/rmit-university.png'

const menuOpen = ref(false)

const experiences = [
  {
    period: 'Sep 2024 — Present',
    role: 'People & Culture Coordinator',
    organisation: 'McCormack',
    type: 'People & Culture',
    logo: mccormackLogo,
    description: 'Supporting the full employee lifecycle, from attracting and selecting talent through to onboarding, development, engagement and culture-building initiatives.',
    points: ['Primary point of contact for HR-related enquiries and employee support.', 'Coordinate training and development activities to help teams grow and succeed.', 'Organise events and team experiences that bring McCormack’s values to life.'],
    featured: true,
  },
  {
    period: 'Jul 2024 — Oct 2024',
    role: 'Human Resources Intern',
    organisation: 'Marriott International',
    type: 'Human Resources',
    logo: marriottLogo,
    description: 'Partnered with the HR team to support day-to-day operations, people initiatives and the delivery of a welcoming employee experience.',
    points: ['Contributed to HR projects focused on employee wellbeing and organisational culture.', 'Supported administrative coordination, scheduling and document preparation.'],
  },
  {
    period: 'Nov 2023 — Sep 2024',
    role: 'Human Resources Administrative Officer',
    organisation: 'Care Aid Australia',
    type: 'Human Resources',
    logo: careAidLogo,
    description: 'Managed recruitment and onboarding operations for casual support workers while keeping scheduling, payroll and compliance processes organised.',
    points: ['Facilitated recruitment and onboarding for casual support workers.', 'Managed shift scheduling and weekly payroll through Xero.', 'Supported workplace health and safety training and compliance checks.'],
  },
  {
    period: 'Feb 2023 — Jul 2023',
    role: 'Talent Acquisition Intern',
    organisation: 'YBOX.VN',
    type: 'Talent Acquisition',
    logo: yboxLogo,
    description: 'Supported the talent team with candidate screening, communication and recruitment coordination across a growing organisation.',
    points: ['Screened CVs and managed candidate communications through the recruitment process.', 'Partnered with other departments to support onboarding and offboarding needs.'],
  },
]

const credentials = [
  { mark: 'RMIT', label: 'Bachelor of Business — Global Business & Human Resource Management' },
  { mark: 'UCI', label: 'Human Resources Analytics — University of California, Irvine' },
  { mark: 'IELTS', label: '7.5 IELTS — British Council' },
  { mark: 'RMIT', label: 'Developing Global Leadership — RMIT University' },
]

const volunteering = [
  { role: 'Future Edge Ambassador', organisation: 'RMIT University', period: 'Jul 2023 — Dec 2025', logo: rmitLogo },
  { role: 'oGV Team Lead', organisation: 'AIESEC', period: 'Oct 2023 — Jul 2024', logo: aiesecLogo },
  { role: 'Mentor Volunteer', organisation: 'Refugee Migrant Children Centre (RMCC)', period: 'Jul 2023 — Jan 2024', logo: rmccLogo },
]

function closeMenu() {
  menuOpen.value = false
}
</script>

<template>
  <div class="site-shell">
    <header class="site-header">
      <a class="brand" href="#top" aria-label="June Nguyen home" @click="closeMenu">
        <span class="brand-mark">JN</span><span class="brand-name">June Nguyen</span>
      </a>
      <button class="menu-toggle" type="button" aria-label="Toggle navigation" :aria-expanded="menuOpen" @click="menuOpen = !menuOpen"><span></span><span></span></button>
      <nav class="site-nav" :class="{ 'is-open': menuOpen }" aria-label="Primary navigation">
        <a href="#about" @click="closeMenu">About</a><a href="#experience" @click="closeMenu">Experience</a><a href="#impact" @click="closeMenu">Impact</a><a href="#contact" class="nav-cta" @click="closeMenu">Let’s connect <span>↗</span></a>
      </nav>
    </header>

    <main id="top">
      <section class="hero section-wrap">
        <div class="hero-copy">
          <p class="eyebrow"><span class="eyebrow-dot"></span> People, culture & meaningful work</p>
          <h1>Creating workplaces where <em>people can thrive.</em></h1>
          <p class="hero-lede">Hi, I’m June — a People & Culture Coordinator who brings care, structure and energy to the employee experience.</p>
          <div class="hero-actions"><a class="button button-dark" href="#experience">Explore my experience <span>↘</span></a><a class="text-link button" href="#contact">Get in touch <span>↗</span></a></div>
          <div class="hero-meta" aria-label="Current role details"><span>Based in Melbourne, Australia</span><span class="meta-divider"></span><span>Currently at McCormack</span></div>
        </div>
        <div class="hero-visual">
          <div class="portrait-frame"><img :src="profileImage" alt="June Nguyen smiling" /><span class="portrait-sticker">People<br />first</span></div>
          <div class="hero-note"><span class="note-line"></span><span>Thoughtful<br />by nature</span></div>
        </div>
      </section>

      <section class="award-banner section-wrap" aria-label="Award recognition">
        <div class="award-icon" aria-hidden="true">✦</div>
        <div class="award-copy"><p class="eyebrow">A proud moment</p><h2>Employee of the Year <span>at McCormack</span></h2></div>
        <p class="award-detail">Recognised for bringing care, collaboration and a people-first mindset to the workplace.</p><span class="award-seal" aria-hidden="true">NEW<br /><small>HONOUR</small></span>
      </section>

      <section id="about" class="about section-wrap section-grid">
        <div class="section-label"><span>01</span><span class="label-rule"></span><span>About</span></div>
        <div class="about-content"><div><p class="eyebrow">A little about me</p><h2>People are at the heart of every <em>good organisation.</em></h2></div><div class="about-body"><p>I’m passionate about building workplaces where people feel supported, connected and able to do their best work. My experience spans people operations, employee engagement, talent acquisition and HR administration.</p><p>I’m at my best where thoughtful coordination meets genuine human connection — helping teams grow, creating memorable employee experiences and turning culture into something people feel every day.</p><div class="focus-list" aria-label="Areas of focus"><span>Employee experience</span><span>People operations</span><span>Talent & culture</span></div></div></div>
      </section>

      <section id="experience" class="experience-section section-wrap">
        <div class="section-heading"><div class="section-label"><span>02</span><span class="label-rule"></span><span>Experience</span></div><div><p class="eyebrow">A career built around people</p><h2>Turning the everyday into an <em>experience.</em></h2></div></div>
        <div class="timeline">
          <article v-for="experience in experiences" :key="experience.role" class="timeline-item" :class="{ featured: experience.featured }">
            <div class="timeline-date">{{ experience.period }}</div>
            <div class="timeline-card"><div class="timeline-card-top"><div class="company-logo" :class="{ 'logo-placeholder': !experience.logo }"><img v-if="experience.logo" :src="experience.logo" :alt="`${experience.organisation} logo`" /><span v-else>MC</span></div><div><p class="card-kicker">{{ experience.type }}</p><h3>{{ experience.role }}</h3><p class="company-name">{{ experience.organisation }}</p></div><span v-if="experience.featured" class="current-badge">Current role</span></div><p class="timeline-description">{{ experience.description }}</p><ul><li v-for="point in experience.points" :key="point">{{ point }}</li></ul></div>
          </article>
        </div>
      </section>

      <section id="impact" class="impact section-wrap">
        <div class="impact-intro"><div class="section-label"><span>03</span><span class="label-rule"></span><span>Beyond the role</span></div><p class="eyebrow">Contribution in action</p><h2>Curious, collaborative & <em>community-minded.</em></h2><p>I enjoy creating momentum with people — on the team, in the wider community and wherever a new idea can make a difference.</p></div>
        <div class="impact-cards"><article class="impact-card impact-card-primary"><div class="impact-number">01</div><p class="eyebrow">Leadership</p><h3>Building connection across teams</h3><p>From employee events to cross-functional initiatives, I bring an organised and inclusive approach to shared experiences.</p><div class="impact-chips"><span>Events</span><span>Engagement</span><span>Culture</span></div></article><article class="impact-card impact-card-secondary"><div class="impact-number">02</div><p class="eyebrow">Community</p><h3>Making space for people to grow</h3><p>Volunteering and student leadership have shaped how I listen, support and help people feel they belong.</p><div class="impact-chips"><span>Mentoring</span><span>Inclusion</span></div></article></div>
      </section>

      <section class="credentials section-wrap section-grid">
        <div class="section-label"><span>04</span><span class="label-rule"></span><span>Credentials</span></div>
        <div class="credentials-content"><div><p class="eyebrow">Learning is ongoing</p><h2>Grounded in curiosity, <em>growing with intention.</em></h2></div><div class="credential-list"><div v-for="credential in credentials" :key="credential.label" class="credential-row"><div class="credential-logo" aria-hidden="true"><span>{{ credential.mark }}</span></div><p>{{ credential.label }}</p><span class="row-arrow">↗</span></div></div><div class="volunteer-strip"><p class="eyebrow">Selected volunteering</p><div class="volunteer-list"><div v-for="item in volunteering" :key="item.role" class="volunteer-item"><div class="volunteer-logo" :class="{ 'logo-placeholder': !item.logo }"><img v-if="item.logo" :src="item.logo" :alt="`${item.organisation} logo`" /><span v-else>FE</span></div><div><strong>{{ item.role }}</strong><span>{{ item.organisation }} · {{ item.period }}</span></div></div></div></div></div>
      </section>

      <section id="contact" class="contact section-wrap"><div class="contact-inner"><p class="eyebrow">Let’s make good work happen</p><h2>Have a people-first idea?<br /><em>I’d love to hear it.</em></h2><a class="button button-light" href="https://www.linkedin.com/in/june-nguyen-0ab059253/" target="_blank" rel="noreferrer">Connect on LinkedIn <span>↗</span></a></div><div class="contact-orbit orbit-one"></div><div class="contact-orbit orbit-two"></div></section>
    </main>

    <footer class="site-footer section-wrap"><span>© 2026 June Nguyen</span><span>People & Culture · Melbourne</span><a href="#top">Back to top ↑</a></footer>
  </div>
</template>
