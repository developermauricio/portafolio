<script setup>
let isOpen = ref(false)

function toggleMenu() {
  isOpen = !isOpen
}
</script>

<template>
  <aside class="sidebar" :class="{ active: isOpen }">
    <div class="sidebar-info">
      <figure class="avatar-box">
        <img src="/images/photo-mauricio-gutierrez.webp" alt="Mauricio Gutierrez" width="80">
      </figure>

      <div class="info-content">
        <h1 class="name" title="Mauricio Gutierrez">
          Mauricio Gutierrez
        </h1>

        <p class="title text-center xl:block flex items-center justify-center gap-1">
          <span class="xl:after:content-[''] after:content-[',']">Ingeniero Informático</span>
<!--          <span>Desarrollador Web</span>-->
        </p>
      </div>

      <button class="info_more-btn" @click="isOpen = !isOpen">
        <span>Información de Contacto</span>

        <ion-icon name="chevron-down" />
      </button>
    </div>

    <div class="sidebar-info_more">
      <div class="separator" />

      <ul class="contacts-list">
        <li class="contact-item">
          <div class="icon-box">
            <ion-icon name="mail-outline" />
          </div>

          <div class="contact-info">
            <p class="contact-title">
              {{ $t('email') }}
            </p>

            <a href="mailto:info@afsakar.com" class="contact-link">info@afsakar.com</a>
          </div>
        </li>

        <li class="contact-item">
          <div class="icon-box">
            <ion-icon name="logo-github" />
          </div>

          <div class="contact-info">
            <p class="contact-title">
              Github
            </p>

            <a href="https://github.com/afsakar" class="contact-link" target="_blank">mauroaicode</a>
          </div>
        </li>

        <li class="contact-item">
          <div class="icon-box">
            <ion-icon name="logo-linkedin" />
          </div>

          <div class="contact-info">
            <p class="contact-title">
              Linkedin
            </p>

            <a href="https://tr.linkedin.com/in/afsakar" class="contact-link" target="_blank">Mauricio Gutierrez</a>
          </div>
        </li>

        <li class="contact-item">
          <div class="icon-box">
            <ion-icon name="location-outline" />
          </div>

          <div class="contact-info">
            <p class="contact-title">
              {{ $t('location') }}
            </p>

            <address>Colombia - Ecuador</address>
          </div>
        </li>
      </ul>

      <div class="separator" />

      <ul class="social-list">
        <li class="social-item">
          <NuxtLink to="https://www.twitter.com/afsakar" class="social-link" target="_blank">
            <ion-icon name="logo-twitter" />
          </NuxtLink>
        </li>

        <li class="social-item">
          <NuxtLink to="https://www.instagram.com/afsakar" class="social-link" target="_blank">
            <ion-icon name="logo-instagram" />
          </NuxtLink>
        </li>
        <LangSwitcher2 />
<!--        <DarkToggle />-->
      </ul>
    </div>
  </aside>
</template>
