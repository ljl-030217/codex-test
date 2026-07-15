<script setup lang="ts">
const features = [
  {
    title: 'Fast Vue setup',
    description: 'Vite, TypeScript, Router, and Pinia are already wired for the next feature.',
  },
  {
    title: 'Clean structure',
    description: 'A focused starter surface with room for real content, states, and workflows.',
  },
  {
    title: 'Ready to iterate',
    description: 'Simple styling, responsive spacing, and clear sections make changes easy.',
  },
]
</script>

<template>
  <main class="page-shell">
    <nav class="topbar" aria-label="Primary navigation">
      <a class="brand" href="/">
        <span class="brand-mark" aria-hidden="true">C</span>
        <span>Codex Test</span>
      </a>

      <div class="nav-links" aria-label="Page sections">
        <a href="#features">Features</a>
        <a href="#status">Status</a>
        <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue Docs</a>
      </div>
    </nav>

    <section class="hero" aria-labelledby="hero-title">
      <div class="hero-copy">
        <p class="eyebrow">Vue 3 starter project</p>
        <h1 id="hero-title">王秋雨1</h1>
        <p class="hero-text">
          This project now has a polished first screen with clear hierarchy, useful sections, and a
          calm visual system you can extend without fighting the template.
        </p>

        <div class="actions" aria-label="Primary actions">
          <a class="button button-primary" href="#features">View features</a>
          <a class="button button-secondary" href="https://vite.dev/" target="_blank" rel="noopener">
            Vite guide
          </a>
        </div>
      </div>

      <aside id="status" class="status-panel" aria-label="Project status">
        <div class="panel-header">
          <span class="status-dot" aria-hidden="true"></span>
          <span>Development status</span>
        </div>

        <dl class="status-list">
          <div>
            <dt>Framework</dt>
            <dd>Vue 3</dd>
          </div>
          <div>
            <dt>Build tool</dt>
            <dd>Vite</dd>
          </div>
          <div>
            <dt>State</dt>
            <dd>Pinia ready</dd>
          </div>
        </dl>
      </aside>
    </section>

    <section id="features" class="features" aria-label="Project features">
      <article v-for="feature in features" :key="feature.title" class="feature-card">
        <h2>{{ feature.title }}</h2>
        <p>{{ feature.description }}</p>
      </article>
    </section>
  </main>
</template>

<style scoped>
:global(*) {
  box-sizing: border-box;
}

:global(body) {
  margin: 0;
  min-width: 320px;
  min-height: 100vh;
  color: #17211f;
  background:
    radial-gradient(circle at top left, rgba(41, 121, 101, 0.16), transparent 34rem),
    linear-gradient(135deg, #f6f7f2 0%, #f4f0e8 48%, #eaf2ef 100%);
  font-family:
    Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
}

:global(a) {
  color: inherit;
  text-decoration: none;
}

.page-shell {
  width: min(1120px, calc(100% - 32px));
  margin: 0 auto;
  padding: 28px 0 56px;
}

.topbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 24px;
  padding: 14px 0;
}

.brand {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  color: #17211f;
  font-size: 15px;
  font-weight: 750;
}

.brand-mark {
  display: grid;
  width: 34px;
  height: 34px;
  place-items: center;
  border-radius: 8px;
  color: #ffffff;
  background: #1f6f5a;
  font-size: 16px;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 22px;
  color: #56615e;
  font-size: 14px;
  font-weight: 600;
}

.nav-links a {
  transition: color 160ms ease;
}

.nav-links a:hover {
  color: #1f6f5a;
}

.hero {
  display: grid;
  grid-template-columns: minmax(0, 1fr) 360px;
  gap: 56px;
  align-items: center;
  min-height: 560px;
  padding: 54px 0 42px;
}

.hero-copy {
  max-width: 680px;
}

.eyebrow {
  margin: 0 0 14px;
  color: #9b5d21;
  font-size: 13px;
  font-weight: 800;
  letter-spacing: 0;
  text-transform: uppercase;
}

h1 {
  margin: 0;
  max-width: 760px;
  color: #111817;
  font-size: clamp(42px, 7vw, 78px);
  line-height: 0.98;
  letter-spacing: 0;
}

.hero-text {
  max-width: 620px;
  margin: 24px 0 0;
  color: #4f5d58;
  font-size: 18px;
  line-height: 1.65;
}

.actions {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-top: 34px;
}

.button {
  display: inline-flex;
  min-height: 46px;
  align-items: center;
  justify-content: center;
  border-radius: 8px;
  padding: 0 18px;
  font-size: 15px;
  font-weight: 750;
  transition:
    transform 160ms ease,
    border-color 160ms ease,
    background 160ms ease;
}

.button:hover {
  transform: translateY(-1px);
}

.button-primary {
  color: #ffffff;
  background: #1f6f5a;
}

.button-primary:hover {
  background: #195f4d;
}

.button-secondary {
  border: 1px solid rgba(23, 33, 31, 0.18);
  color: #24312e;
  background: rgba(255, 255, 255, 0.52);
}

.button-secondary:hover {
  border-color: rgba(31, 111, 90, 0.5);
}

.status-panel {
  border: 1px solid rgba(23, 33, 31, 0.14);
  border-radius: 8px;
  padding: 24px;
  background: rgba(255, 255, 255, 0.68);
  box-shadow: 0 24px 70px rgba(43, 61, 56, 0.12);
  backdrop-filter: blur(18px);
}

.panel-header {
  display: flex;
  align-items: center;
  gap: 10px;
  color: #24312e;
  font-size: 14px;
  font-weight: 800;
}

.status-dot {
  width: 10px;
  height: 10px;
  border-radius: 999px;
  background: #2f9e6d;
  box-shadow: 0 0 0 6px rgba(47, 158, 109, 0.12);
}

.status-list {
  display: grid;
  gap: 18px;
  margin: 28px 0 0;
}

.status-list div {
  display: flex;
  align-items: baseline;
  justify-content: space-between;
  gap: 16px;
  border-bottom: 1px solid rgba(23, 33, 31, 0.1);
  padding-bottom: 16px;
}

.status-list div:last-child {
  border-bottom: 0;
  padding-bottom: 0;
}

.status-list dt {
  color: #68736f;
  font-size: 13px;
  font-weight: 700;
}

.status-list dd {
  margin: 0;
  color: #17211f;
  font-size: 16px;
  font-weight: 800;
}

.features {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 16px;
  padding-top: 18px;
}

.feature-card {
  min-height: 164px;
  border: 1px solid rgba(23, 33, 31, 0.12);
  border-radius: 8px;
  padding: 24px;
  background: rgba(255, 255, 255, 0.55);
}

.feature-card h2 {
  margin: 0;
  color: #17211f;
  font-size: 18px;
  line-height: 1.25;
}

.feature-card p {
  margin: 14px 0 0;
  color: #5b6864;
  font-size: 15px;
  line-height: 1.6;
}

@media (max-width: 820px) {
  .page-shell {
    width: min(100% - 24px, 680px);
    padding-top: 16px;
  }

  .topbar,
  .nav-links {
    align-items: flex-start;
  }

  .topbar {
    flex-direction: column;
  }

  .nav-links {
    flex-wrap: wrap;
    gap: 14px;
  }

  .hero {
    grid-template-columns: 1fr;
    gap: 28px;
    min-height: auto;
    padding: 44px 0 28px;
  }

  h1 {
    font-size: 46px;
    line-height: 1.02;
  }

  .hero-text {
    font-size: 16px;
  }

  .status-panel {
    padding: 20px;
  }

  .features {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 460px) {
  h1 {
    font-size: 38px;
  }

  .actions,
  .button {
    width: 100%;
  }
}
</style>
