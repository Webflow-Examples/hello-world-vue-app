<script setup lang="ts">
import WebflowLogo from './components/WebflowLogo.vue';
import DocCard from './components/DocCard.vue';

const FRAMEWORK = 'Vue 3 + Vite';

const DOC_LINKS = [
  {
    title: 'Webflow Cloud overview',
    description: 'What Webflow Cloud is and what you can build on it.',
    href: 'https://developers.webflow.com/webflow-cloud',
  },
  {
    title: 'Storing data',
    description: 'Add SQLite, Key Value, and Object Storage bindings.',
    href: 'https://developers.webflow.com/webflow-cloud/storing-data/overview',
  },
  {
    title: `${FRAMEWORK} on Webflow Cloud`,
    description: 'Build and deploy your first Webflow Cloud app.',
    href: 'https://developers.webflow.com/webflow-cloud/getting-started',
  },
  {
    title: 'Environments & deployments',
    description: 'Manage previews, production, and deployment history.',
    href: 'https://developers.webflow.com/webflow-cloud/environments',
  },
];
</script>

<template>
  <div class="wf-page">
    <div class="wf-glow" aria-hidden />

    <header class="wf-header">
      <div class="wf-brand">
        <WebflowLogo />
        <span class="wf-brand-text">Webflow Cloud</span>
      </div>
      <nav class="wf-nav">
        <a href="https://developers.webflow.com/webflow-cloud" target="_blank" rel="noreferrer">Docs</a>
        <a href="https://github.com/Webflow-Examples" target="_blank" rel="noreferrer" class="wf-nav-ghost">GitHub</a>
      </nav>
    </header>

    <main class="wf-main">
      <section class="wf-hero">
        <p class="wf-eyebrow">Hello, world · {{ FRAMEWORK }}</p>
        <h1 class="wf-title">
          Your <span class="wf-gradient">{{ FRAMEWORK }}</span> app
          <br />is live on Webflow Cloud.
        </h1>
        <p class="wf-subtitle">
          This is a minimal starter. Customize <code>src/App.vue</code> and push to deploy.
        </p>
        <div class="wf-cta">
          <a class="wf-btn wf-btn-primary" href="https://developers.webflow.com/webflow-cloud/quickstart" target="_blank" rel="noreferrer">
            Read the quickstart
          </a>
          <a class="wf-btn wf-btn-ghost" href="https://github.com/Webflow-Examples/hello-world-vue-app" target="_blank" rel="noreferrer">
            View on GitHub
          </a>
        </div>
      </section>

      <section class="wf-cards" aria-label="Documentation">
        <DocCard v-for="l in DOC_LINKS" :key="l.href" v-bind="l" />
      </section>
    </main>

    <footer class="wf-footer">
      <span>
        Built with {{ FRAMEWORK }} · Deployed on
        <a href="https://webflow.com/cloud" target="_blank" rel="noreferrer">Webflow Cloud</a>
      </span>
    </footer>
  </div>
</template>
