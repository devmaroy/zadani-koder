<template>
  <section class="hero">
    <div class="container">
      <div class="hero__banner">
        <div class="hero__wrapper">
          <h1 class="hero__title">
            S námi zvládne <span> fakturovat každý</span>
          </h1>
          <h2 class="hero__subtitle">
            bezpečně a zdarma
            <span class="hero__shape"> za méně než 30 vteřin</span>
          </h2>

          <div class="hero__action">
            <Button type="link" variant="orange" size="lg">
              <img
                src="~/images/new-design/invoice-icon.svg"
                alt="Invoice icon"
              />
              Vystavit fakturu
            </Button>
          </div>
        </div>

        <div class="hero__img">
          <img
            src="~/images/new-design/girl.png"
            alt="Woman in orange t-shirt, smilling, happy."
          />
        </div>
      </div>

      <ul class="hero__info">
        <li><a href="/doklady">Doklady ihned připraveny ve formátu PDF</a></li>
        <li>
          <a href="/faktura">
            Zálohová a proforma faktura, daňový doklad pro plátce i neplátce DPH
            a další</a
          >
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import Button from "~/components/common/Button";

export default {
  name: "Hero",
  components: {
    Button,
  },
};
</script>

<style lang="scss" scoped>
.hero {
  margin-top: rem(40px);
}

.hero__banner {
  background: $blue;
  background-image: url("pattern.svg");

  border-radius: rem(24px);

  @media screen and (min-width: $breakpoint-lg) {
    display: flex;
  }
}

.hero__wrapper {
  padding: rem(32px);

  @media screen and (min-width: $breakpoint-lg) {
    padding: rem(96px);
  }
}

.hero__title {
  font-size: rem(40px);
  line-height: calc(rem(40px) * 1.2);
  font-weight: bold;
  color: $white;
  margin-bottom: rem(16px);

  & span {
    font-weight: bold;
  }

  @media screen and (min-width: $breakpoint-lg) {
    font-size: rem(56px);
    line-height: calc(rem(56px) * 1.2);
  }

  @media screen and (min-width: $breakpoint-xl) {
    & span {
      font-weight: bold;
    }
  }
}

.hero__subtitle {
  position: relative;
  display: inline-block;
  font-size: rem(24px);
  line-height: calc(rem(24px) * 1.2);
  font-weight: bold;
  color: $white;

  @media screen and (min-width: $breakpoint-lg) {
    font-size: rem(36px);
    line-height: calc(rem(36px) * 1.2);
  }
}
.hero__shape {
  &::after {
    @media screen and (min-width: $breakpoint-lg) {
      content: url("line.svg");
      position: absolute;
      right: 0;
      bottom: rem(-35px);
    }
  }

  @media screen and (min-width: $breakpoint-lg) {
    display: block;
  }
}

.hero__action {
  margin-top: rem(24px);

  @media screen and (min-width: $breakpoint-lg) {
    margin-top: rem(40px);
  }
}

.hero__info {
  gap: rem(10px);
  text-align: center;
  list-style: none;
  margin-top: rem(32px);

  @media screen and (min-width: $breakpoint-lg) {
    display: flex;
    justify-content: space-around;
  }
}

.hero__info li:not(:last-child) {
  margin-bottom: rem(12px);
}

.hero__info a {
  color: $blue;
  font-weight: bold;
  text-decoration: none;
}

.hero__img {
  display: none;

  @media screen and (min-width: $breakpoint-xl) {
    display: block;
    align-self: flex-end;
    width: 75%;

    & img {
      width: 75%;
    }
  }
}
</style>
