<template>
  <section class="secondary-banner">
    <div class="container">
      <div class="secondary-banner__content">
        <div>
          <h2 class="secondary-banner__title">
            S námi zvládne <span> fakturovat úplně každý</span>
          </h2>

          <div class="secondary-banner__action">
            <Button type="link" variant="orange" size="lg">
              <img
                src="~/images/new-design/invoice-icon.svg"
                alt="Invoice icon"
              />Vystavit fakturu</Button
            >
          </div>
        </div>

        <div class="secondary-banner__img">
          <img
            src="~/images/new-design/man.png"
            alt="Man driving a car, smilling, happy"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Button from "~/components/common/Button";

export default {
  name: "SecondaryBanner",
  components: { Button },
};
</script>

<style lang="scss" scoped>
.secondary-banner {
  margin-top: rem(40px);

  @media screen and (min-width: $breakpoint-lg) {
    margin-top: rem(48px);
  }
}

.secondary-banner__content {
  position: relative;
  background: $blue;
  background-image: url("pattern.svg");
  border-radius: rem(24px);
  padding: rem(32px);

  @media screen and (min-width: $breakpoint-lg) {
    padding: rem(40px) rem(96px);
  }
}

.secondary-banner__title {
  font-size: rem(32px);
  line-height: calc(rem(32px) * 1.2);
  font-weight: bold;
  color: $white;
  margin: 0;

  @media screen and (min-width: $breakpoint-lg) {
    & span {
      display: block;
    }

    font-size: rem(40px);
    line-height: calc(rem(40px) * 1.2);
  }
}

.secondary-banner__action {
  margin-top: rem(24px);
}

.secondary-banner__img {
  display: none;
  overflow: hidden;

  @media screen and (min-width: $breakpoint-lg) {
    display: block;
    position: absolute;
    top: -50%;
    right: 0;
    bottom: 0;
    display: flex;
    justify-content: flex-end;
  }

  @media screen and (min-width: $breakpoint-xl) {
    align-items: center;
    justify-content: center;

    & img {
      width: 55%;
    }
  }
}
</style>
