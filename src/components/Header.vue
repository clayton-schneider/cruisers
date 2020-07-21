<template>
  <nav v-if="home" class="nav nav--home">
    <div class="nav__logo">
      <g-link to="/">
        <g-image src="~/assets/imgs/cruisers-logo.png" alt="Cruiser's Logo" />
      </g-link>
    </div>

    <div class="nav__links">
      <g-link class="nav__link" to="/about">About Us</g-link>
      <g-link class="nav__link" to="/are-we-a-good-fit"
        >Are We A Good Fit?</g-link
      >
      <g-link class="nav__link btn btn--outline" to="/schedule"
        >Schedule A Free Consultation</g-link
      >
    </div>
  </nav>

  <nav v-else-if="!home" class="nav nav--secondary">
    <div class="nav__logo">
      <g-link to="/">
        <g-image src="~/assets/imgs/cruisers-logo.png" alt="Cruiser's Logo" />
      </g-link>
    </div>

    <div class="nav__links">
      <g-link class="nav__link" to="/about">About Us</g-link>
      <g-link class="nav__link" to="/faqs">Are We A Good Fit?</g-link>
      <g-link class="nav__link btn btn--outline" to="/schedule"
        >Schedule A Free Consultation</g-link
      >
    </div>
  </nav>
</template>

<script>
export default {
  props: {
    home: {
      type: Boolean,
      default: true,
    },
  },
};
</script>
