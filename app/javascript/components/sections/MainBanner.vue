<template>
  <section class="main-banner">
    <div class="container">
      <div class="main-banner__content">
        <div class="main-banner__wrapper">
          <h2 class="main-banner__title">Začněte fakturovat ZDARMA</h2>
          <span class="main-banner__subtitle"
            >První fakturu vystavíte do 5 minut</span
          >
          <div class="main-banner__action">
            <Button type="link" variant="orange" size="lg">
              <img
                src="~/images/new-design/invoice-icon.svg"
                alt="Invoice icon"
              />
              Vystavit fakturu
            </Button>
          </div>
        </div>

        <div class="main-banner__img">
          <img src="~/images/new-design/invoice.png" alt="Invoice image" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Button from "~/components/common/Button";

export default {
  name: "MainBanner",
  components: { Button },
};
</script>

<style lang="scss" scoped>
.main-banner {
  margin-top: rem(40px);
}

.main-banner__title {
  font-size: rem(36px);
  line-height: calc(rem(36px) * 1.2);
  color: $blue;
  font-weight: bold;

  @media screen and (min-width: $breakpoint-lg) {
    font-size: rem(48px);
    line-height: calc(rem(48px) * 1.2);
  }
}

.main-banner__subtitle {
  font-size: rem(22px);
  line-height: calc(rem(22px) * 1.2);
  color: $blue;
  font-weight: bold;

  @media screen and (min-width: $breakpoint-lg) {
    font-size: rem(32px);
    line-height: calc(rem(32px) * 1.2);
  }
}

.main-banner__content {
  position: relative;
  background: $blue-sky;
  background-image: url("pattern-secondary.svg");
  border-radius: rem(24px);
  padding: rem(32px);

  @media screen and (min-width: $breakpoint-lg) {
    display: flex;
    justify-content: space-between;
    gap: rem(40px);
    padding: rem(64px) rem(96px);
  }
}

.main-banner__wrapper {
  max-width: 70%;
}

.main-banner__action {
  margin-top: rem(24px);
}

.main-banner__img {
  display: none;

  @media screen and (min-width: $breakpoint-lg) {
    display: block;
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    width: 35%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
}
</style>
