<script setup lang="ts">
const allianceName = '2271 United'
const allianceTag = '271U'
const gameName = 'Last War'
const serverNumber = '2271'

const discordInviteUrl = 'https://discord.gg/VUAU7U3NBf'
</script>

<template>
  <main class="site-shell">
    <section class="hero-card" aria-labelledby="page-title">
      <div class="logo-wrap">
        <img
          src="/alliance-logo.png"
          :alt="`${allianceName} alliance logo`"
          class="alliance-logo"
        />
      </div>

      <p class="eyebrow">{{ gameName }} · Server {{ serverNumber }}</p>

      <h1 id="page-title">
        {{ allianceName }}
      </h1>

      <p class="tag">
        {{ allianceTag }}
      </p>

      <p class="tagline">
        Active, social, supportive — and possibly dangerous for your screen time.
      </p>

      <div class="actions">
        <a
          class="discord-button"
          :href="discordInviteUrl"
          target="_blank"
          rel="noopener noreferrer"
        >
          Join our Discord
        </a>
      </div>

      <div class="coming-soon">
        <span>Full website coming soon</span>
      </div>
    </section>
  </main>
</template>

<style scoped>
:global(*) {
  box-sizing: border-box;
}

:global(html) {
  min-width: 320px;
  min-height: 100%;
  background: #080a12;
}

:global(body) {
  min-width: 320px;
  min-height: 100vh;
  margin: 0;
  font-family:
    Inter,
    ui-sans-serif,
    system-ui,
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    sans-serif;
  background:
    radial-gradient(circle at top left, rgba(255, 196, 87, 0.22), transparent 34rem),
    radial-gradient(circle at bottom right, rgba(116, 84, 255, 0.22), transparent 32rem),
    linear-gradient(135deg, #080a12 0%, #101827 50%, #15101f 100%);
  color: #f8fafc;
}

:global(#app) {
  min-height: 100vh;
}

.site-shell {
  display: grid;
  min-height: 100vh;
  place-items: center;
  padding: clamp(1rem, 4vw, 4rem);
}

.hero-card {
  width: min(100%, 920px);
  border: 1px solid rgba(255, 255, 255, 0.14);
  border-radius: clamp(1.25rem, 3vw, 2rem);
  padding: clamp(2rem, 6vw, 5rem);
  text-align: center;
  background: linear-gradient(145deg, rgba(255, 255, 255, 0.12), rgba(255, 255, 255, 0.055));
  box-shadow: 0 24px 90px rgba(0, 0, 0, 0.45);
  backdrop-filter: blur(18px);
}

.logo-wrap {
  display: grid;
  place-items: center;
  width: clamp(8rem, 18vw, 12rem);
  height: clamp(8rem, 18vw, 12rem);
  margin: 0 auto 1.5rem;
  border-radius: 2rem;
  background: linear-gradient(135deg, rgba(255, 211, 122, 0.25), rgba(255, 255, 255, 0.08));
  box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.16);
}

.alliance-logo {
  width: 72%;
  height: 72%;
  object-fit: contain;
}

.eyebrow {
  margin: 0 0 0.75rem;
  color: #ffd37a;
  font-size: clamp(0.8rem, 1.8vw, 0.95rem);
  font-weight: 800;
  letter-spacing: 0.16em;
  text-transform: uppercase;
}

h1 {
  margin: 0;
  font-size: clamp(3.25rem, 10vw, 7.5rem);
  line-height: 0.9;
  letter-spacing: -0.08em;
}

.tag {
  width: fit-content;
  margin: 1.25rem auto 0;
  border: 1px solid rgba(255, 211, 122, 0.5);
  border-radius: 999px;
  padding: 0.45rem 0.9rem;
  color: #ffd37a;
  background: rgba(255, 211, 122, 0.1);
  font-size: 0.95rem;
  font-weight: 900;
  letter-spacing: 0.12em;
}

.tagline {
  max-width: 46rem;
  margin: 1.75rem auto 0;
  color: #d4daea;
  font-size: clamp(1.15rem, 2.4vw, 1.65rem);
  line-height: 1.55;
  font-weight: 650;
}

.actions {
  margin-top: 2rem;
}

.discord-button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-height: 3.25rem;
  border-radius: 999px;
  padding: 0.9rem 1.35rem;
  color: #101827;
  background: #ffd37a;
  font-weight: 950;
  text-decoration: none;
  transition:
    transform 180ms ease,
    box-shadow 180ms ease,
    background-color 180ms ease;
}

.discord-button:hover {
  transform: translateY(-2px);
  background: #ffe09c;
  box-shadow: 0 12px 28px rgba(255, 211, 122, 0.24);
}

.discord-button:focus-visible {
  outline: 3px solid #ffffff;
  outline-offset: 4px;
}

.coming-soon {
  margin-top: 2rem;
  color: #aeb8d0;
  font-size: 0.95rem;
  font-weight: 750;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

@media (max-width: 520px) {
  .hero-card {
    padding: 1.5rem;
  }

  .discord-button {
    width: 100%;
  }
}

@media (prefers-reduced-motion: reduce) {
  .discord-button {
    transition: none;
  }

  .discord-button:hover {
    transform: none;
  }
}
</style>
