<template>
  <div>
    <h1>{{ $t('contact.title') }}</h1>
    <p class="lead">
      {{ $t('contact.introduction') }}<br>
      <a href="mailto:hi@simonwuyts.com">{{ $t('contact.cta') }}</a>
    </p>
    <p>
      Simon Wuyts<br>
      <a href="mailto:hi@simonwuyts.com">
        hi@simonwuyts.com
      </a>
      <br>
      <a href="tel:0032485071617">
        +32 (0)485 07 16 17
      </a>
    </p>

    <p>BE0557975573</p>
  </div>
</template>

<script>
import PreviewImage from '~/components/PreviewImage.vue';

export default {
  fetch({ store }) {
    store.commit('SET_PAGE', 'contact');
    store.commit('SET_LOGO_COLOR', '#FFF');
    store.commit('SET_PREVIEW_COLOR', '#0076FF');
    store.commit('SET_PREVIEW_IMAGE', {
      src: '/images/contact.png',
      srcRetina: '/images/contact@2x.png',
      width: 666,
      widthRetina: 1332,
      alt: 'Send me a letter',
      align: 'right',
      verticalOffset: 0
    });
  },
  head() {
    return {
      title: this.$t('contact.title')
    }
  },
  components: {
    PreviewImage
  }
}
</script>
