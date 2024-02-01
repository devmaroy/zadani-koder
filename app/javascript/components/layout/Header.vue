<template>
  <header class="header">
    <div class="container">
      <div class="header__info">
        <div>
          <img
            src="~/images/new-design/logo.svg"
            alt="Fakturaonline.cz logo"
            class="header__img"
          />
        </div>

        <p class="header__subtitle">
          Vystavujte faktury zdarma za méně než 30 vteřin.
        </p>

        <!-- Does your project use bootstrap, or are you moving away from it to custom css? -->
        <ul class="header__action">
          <!-- vue router would be better, but I didn't find any reference 
          in your code so I don't know if it's requirement or not.
          so i will keep the a href instead -> full page refresh :( -->
          <li>
            <Button type="link" variant="orange"
              ><img
                src="~/images/new-design/invoice-icon.svg"
                alt="invoice icon"
              />Vystavit fakturu</Button
            >

            <!-- <a href="/vystavit-fakturu" class="button button--orange"
              >Vystavit fakturu</a
            > -->
          </li>
          <li>
            <Button type="link" variant="blue-outline"
              ><img
                src="~/images/new-design/account-icon.svg"
                alt="invoice icon"
              />
              Přihlásit se</Button
            >
          </li>
        </ul>
      </div>

      <nav>
        <ul class="header__menu">
          <li><a href="/novinky">Novinky</a></li>
          <li><a href="/navody">Návody</a></li>
          <li><a href="/mam-problem">Mám problém</a></li>
          <li>
            <a href="/podnikatelsky-zpravodaj">Podnikatelský zpravodaj</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
import Button from "~/components/common/Button";

export default {
  name: "Header",
  components: {
    Button,
  },
};
</script>

<style lang="scss" scoped>
.header {
  margin-top: rem(20px);
}

.header__img {
  width: rem(343px);
  height: rem(32px);
}

.header__info {
  text-align: center;

  @media screen and (min-width: $breakpoint-lg) {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
}
.header__subtitle {
  font-size: rem(14px);
  font-weight: bold;

  @media screen and (min-width: $breakpoint-lg) {
    margin: 0;
    margin-right: rem(16px);
    flex-basis: 20%;
  }

  @media screen and (min-width: $breakpoint-xl) {
    flex-basis: auto;
  }
}

.header__action {
  list-style: none;
  padding: 0;
  margin: 0;
  margin-top: rem(32px);

  @media screen and (min-width: $breakpoint-lg) {
    margin-top: 0;
    display: flex;
  }
}

.header__action li:not(:last-child) {
  margin-bottom: rem(16px);

  @media screen and (min-width: $breakpoint-lg) {
    margin-bottom: 0;
    margin-right: rem(12px);
  }
}

.header__menu {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  list-style: none;
  padding: 0;
  margin: 0;
  gap: rem(16px);
  margin-top: rem(32px);
}

.header__menu a {
  color: $blue;
  font-weight: bold;
}
</style>
