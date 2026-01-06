<script setup></script>

<template>
  <div class="page">
    <header class="top-bar">
      <div class="logo">
        <span class="mark"></span>
        <span class="word">stori</span>
      </div>
      <nav class="nav">
        <a href="#">Productos <img src="./assets/down.svg" alt="" /></a>
        <a href="#">Beneficios <img src="./assets/down.svg" alt="" /></a>
        <a href="#">Sobre Stori <img src="./assets/down.svg" alt="" /></a>
        <a href="#">Preguntas frecuentes <img src="./assets/down.svg" alt="" /></a>
        <a href="#">Blog <img src="./assets/down.svg" alt="" /></a>
      </nav>
      <div class="actions">
        <div class="lang">
          <span class="flag">🇲🇽</span>
          <span class="flag">🇨🇴</span>
          <span class="flag">🇺🇸</span>
        </div>
        <button class="primary ghost">Quiero mi Stori</button>
      </div>
    </header>

    <main class="hero">
      <div class="hero__copy">
        <h1>Elige ganar<br />con stori</h1>
        <div class="pill">10 millones ya descargaron nuestra app</div>
        <ul class="benefits">
          <li>
            <span class="check">✓</span>
            Cashback en todas tus compras con Stori Black
          </li>
          <li>
            <span class="check">✓</span>
            Hasta 15.00% de ganancia anual total en plazo fijo con Stori Inversión+
          </li>
          <li>
            <span class="check">✓</span>
            99% de aprobación, sin anualidad
          </li>
        </ul>
        <div class="cta-row">
          <button class="primary">Quiero mi Stori</button>
          <span class="hint">Proceso 100% digital y seguro</span>
        </div>
      </div>

      <div class="hero__visual">
        <img src="@/assets/stori_card_hero.avif" alt="" />
      </div>
    </main>

    <section class="social">
      <h2>Ellos también comparten nuestra Stori</h2>
      <div class="avatars">
        <span class="avatar" aria-hidden="true"></span>
        <span class="avatar" aria-hidden="true"></span>
        <span class="avatar" aria-hidden="true"></span>
        <span class="avatar" aria-hidden="true"></span>
        <span class="avatar" aria-hidden="true"></span>
      </div>
    </section>
  </div>
</template>

<style scoped>
.page {
  max-width: 1200px;
  margin: 0 auto;
  padding: 28px 32px 80px;
}

.top-bar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 8px 12px;
  position: sticky;
  top: 0;
  background: rgba(255, 255, 255, 0.9);
  backdrop-filter: blur(10px);
  z-index: 10;
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-soft);
}

.logo {
  display: flex;
  align-items: center;
  gap: 10px;
  font-weight: 800;
  font-size: 22px;
  color: var(--teal-800);
}

.mark {
  width: 34px;
  height: 24px;
  border-radius: 8px;
  background: linear-gradient(135deg, var(--emerald-500), #009f63);
  position: relative;
  box-shadow: var(--shadow-soft);
}

.mark::after {
  content: '';
  position: absolute;
  inset: 4px;
  border-radius: 6px;
  background: #ffffff;
  clip-path: polygon(0 40%, 60% 40%, 60% 0, 100% 0, 100% 100%, 40% 100%, 40% 60%, 0 60%);
}

.nav {
  display: flex;
  gap: 24px;
  color: var(--gray-700);
  font-weight: 600;
}

.nav a {
  display: flex;
  position: relative;
  padding-bottom: 6px;

  img {
    margin-left: 4px;
    width: 16px;
    position: relative;
    top: 2px;
  }
}

.nav a::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  width: 0;
  height: 2px;
  background: var(--emerald-500);
  transition: width 0.2s ease;
}

.nav a:hover::after {
  width: 100%;
}

.actions {
  display: flex;
  align-items: center;
  gap: 16px;
}

.lang {
  display: flex;
  gap: 8px;
  font-size: 15px;
}

.flag {
  filter: saturate(1.1);
}

.primary {
  background: linear-gradient(135deg, var(--emerald-500), var(--emerald-400));
  color: var(--white);
  border: none;
  padding: 12px 20px;
  border-radius: 999px;
  font-weight: 700;
  cursor: pointer;
  box-shadow: var(--shadow-soft);
  transition: transform 0.15s ease, box-shadow 0.15s ease;
}

.primary:hover {
  transform: translateY(-1px);
  box-shadow: var(--shadow-strong);
}

.primary.ghost {
  background: #e9fff3;
  color: var(--emerald-500);
  box-shadow: none;
  border: 1px solid var(--emerald-400);
}

.hero {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 32px;
  align-items: center;
  margin-top: 48px;
}

.hero__copy h1 {
  font-size: clamp(36px, 4vw, 54px);
  line-height: 1.05;
  margin: 14px 0 24px;
  color: var(--teal-900);
}

.pill {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  background: var(--emerald-50);
  padding: 10px 16px;
  border-radius: 999px;
  color: var(--teal-800);
  font-weight: 600;
  box-shadow: var(--shadow-soft);
}

.benefits {
  margin-top: 24px;
  list-style: none;
  display: grid;
  gap: 12px;
  color: var(--gray-700);
  font-weight: 600;
}

.benefits li {
  display: grid;
  grid-template-columns: auto 1fr;
  align-items: center;
  gap: 10px;
  background: #ffffff;
  padding: 12px 14px;
  border-radius: 14px;
  box-shadow: var(--shadow-soft);
}

.check {
  width: 26px;
  height: 26px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  background: var(--emerald-500);
  color: #fff;
  font-weight: 800;
}

.cta-row {
  display: flex;
  align-items: center;
  gap: 16px;
  margin-top: 18px;
}

.hint {
  color: var(--gray-500);
  font-weight: 600;
}

.hero__visual {
  position: relative;
  min-height: 520px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 24px;
}

.coins {
  position: absolute;
  inset: 0;
  pointer-events: none;
}

.coin {
  position: absolute;
  width: 96px;
  height: 96px;
  border-radius: 50%;
  background: radial-gradient(circle at 30% 30%, #fff6c4, #e7b300 60%, #b47a00);
  box-shadow: 0 10px 28px rgba(180, 122, 0, 0.26);
  opacity: 0.9;
  animation: float 5s ease-in-out infinite;
}

.coin--lg {
  top: 10%;
  left: 60%;
  animation-delay: 0.1s;
}

.coin--md {
  bottom: 12%;
  left: 52%;
  width: 78px;
  height: 78px;
  animation-delay: 0.5s;
}

.coin--sm {
  top: 20%;
  right: 14%;
  width: 64px;
  height: 64px;
  animation-delay: 0.9s;
}

.device {
  width: min(420px, 100%);
  background: linear-gradient(160deg, #0f3f44, #0b2c2e 60%, #0f3f44);
  border-radius: 36px;
  padding: 22px 20px;
  box-shadow: var(--shadow-strong);
  color: #e8f8f4;
  position: relative;
  overflow: hidden;
}

.status {
  display: flex;
  gap: 6px;
  margin-bottom: 14px;
}

.status .dot {
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.5);
}

.balance {
  background: linear-gradient(135deg, #103c3f, #0f554f);
  padding: 16px;
  border-radius: 18px;
  box-shadow: var(--shadow-soft);
}

.label {
  font-size: 13px;
  letter-spacing: 0.3px;
  color: #a6dad3;
}

.amount {
  font-size: 28px;
  font-weight: 800;
  margin: 6px 0;
}

.sub {
  color: #a6dad3;
  font-size: 13px;
}

.actions-bar {
  display: flex;
  gap: 10px;
  margin: 16px 0 12px;
}

.chip {
  padding: 9px 14px;
  background: #e9fff3;
  color: var(--teal-800);
  border-radius: 12px;
  font-weight: 700;
}

.chip.alt {
  background: rgba(255, 255, 255, 0.12);
  color: #d2fff0;
  border: 1px solid rgba(255, 255, 255, 0.14);
}

.limits {
  display: grid;
  grid-template-columns: 1fr auto;
  align-items: center;
  gap: 14px;
  padding: 12px 0 6px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.08);
}

.limits p {
  font-weight: 700;
  margin-bottom: 4px;
}

.limits small {
  color: #9cd8d0;
}

.bars {
  display: grid;
  gap: 6px;
}

.bar {
  width: 120px;
  height: 7px;
  border-radius: 999px;
  background: linear-gradient(90deg, var(--emerald-400), rgba(255, 255, 255, 0.15));
}

.bar.short {
  width: 90px;
  opacity: 0.7;
}

.cards-stack {
  position: absolute;
  right: -32px;
  bottom: -40px;
  display: grid;
  gap: 12px;
}

.card {
  width: 240px;
  height: 140px;
  border-radius: 18px;
  padding: 16px;
  color: #ffffff;
  position: relative;
  box-shadow: var(--shadow-strong);
  transform: rotate(-6deg);
}

.card.black {
  background: radial-gradient(circle at 30% 30%, #243436, #0f191a 80%);
  transform: rotate(-2deg);
}

.card.teal {
  background: radial-gradient(circle at 30% 30%, #0f9b89, #02645c 80%);
}

.card .chip {
  position: absolute;
  top: 16px;
  left: 18px;
  width: 28px;
  height: 22px;
  background: linear-gradient(135deg, #f5e4a6, #d3b34f);
  border-radius: 6px;
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.25);
}

.card .wave {
  position: absolute;
  top: 20px;
  right: 22px;
  width: 26px;
  height: 18px;
  background: radial-gradient(circle at 0 50%, rgba(255, 255, 255, 0.85) 0 40%, transparent 42% 100%),
    radial-gradient(circle at 50% 50%, rgba(255, 255, 255, 0.65) 0 40%, transparent 42% 100%),
    radial-gradient(circle at 100% 50%, rgba(255, 255, 255, 0.5) 0 40%, transparent 42% 100%);
  border-radius: 6px;
  opacity: 0.9;
}

.card .brand {
  position: absolute;
  bottom: 16px;
  right: 18px;
  font-size: 20px;
  font-weight: 800;
  letter-spacing: 0.6px;
}

.social {
  margin-top: 80px;
  background: #e9fff3;
  padding: 32px;
  border-radius: var(--radius-lg);
  text-align: center;
  color: var(--teal-800);
  box-shadow: var(--shadow-soft);
}

.social h2 {
  margin-bottom: 20px;
  font-size: 26px;
}

.avatars {
  display: flex;
  justify-content: center;
  gap: 12px;
}

.avatar {
  width: 46px;
  height: 46px;
  border-radius: 50%;
  background: linear-gradient(135deg, #0f9b89, #00c768);
  box-shadow: var(--shadow-soft);
  position: relative;
}

.avatar::after {
  content: '';
  position: absolute;
  inset: 6px;
  border-radius: 50%;
  background: #ffffff;
  opacity: 0.4;
}

@keyframes float {
  0% {
    transform: translateY(0) rotate(0deg);
  }
  50% {
    transform: translateY(-10px) rotate(2deg);
  }
  100% {
    transform: translateY(0) rotate(0deg);
  }
}

@media (max-width: 900px) {
  .top-bar {
    position: static;
    flex-wrap: wrap;
    gap: 12px;
  }

  .nav {
    flex-wrap: wrap;
  }

  .cards-stack {
    position: static;
    display: flex;
    justify-content: center;
  }

  .device {
    padding-bottom: 180px;
  }

  .hero__visual {
    min-height: 480px;
  }
}
</style>
