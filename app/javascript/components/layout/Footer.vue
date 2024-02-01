<template>
  <footer class="footer">
    <div class="container">
      <div class="footer__content">
        <div>
          <ul class="footer__mainmenu">
            <li><a href="/vzory-faktur">Vzory faktur</a></li>
            <li><a href="/cenik">Ceník</a></li>
            <li><a href="/novinky">Novinky</a></li>
            <li><a href="/navody">Návody</a></li>
            <li><a href="/mam-problem">Mám problém</a></li>
            <li>
              <a href="/podnikatelsky-zpravodaj">Podnikatelský zpravodaj</a>
            </li>
          </ul>
        </div>

        <div class="footer__menu">
          <div>
            <span>Návody</span>
            <ul>
              <li><a href="/vzory-word-excel">Vzory Word a Excel</a></li>
              <li><a href="/reporty">Reporty</a></li>
              <li><a href="/faktury">Faktury</a></li>
              <li><a href="/casto-kladene-otazky">Často kladené otázky</a></li>
              <li><a href="/navody">Nápověda</a></li>
            </ul>
          </div>

          <div>
            <span>Další informace</span>
            <ul>
              <li><a href="/neziskove-organizace">Neziskové organizace</a></li>
              <li><a href="/o-nas">O nás</a></li>
              <li><a href="/kontakt">Kontaktujte nás</a></li>
              <li>
                <a href="/zacinajici-podnikatele">Začínající podnikatelé</a>
              </li>
              <li><a href="/navody">Nápověda</a></li>
            </ul>
          </div>

          <div>
            <!-- Nice joke 💩 -->
            <!-- But because we are professionals, I will remove it and keep it here
      just for a reference, haha. -->
            <span>Dokumenty</span>
            <ul>
              <li><a href="/smluvni-podminky">Smluvní podmínky</a></li>
              <li><a href="/o-nas">O nás</a></li>
              <li>
                <a href="/ochrana-osobnich-udaju">Ochrana osobních údajů</a>
              </li>
              <li><a href="/cookie-policy">Cookie Policy</a></li>
              <li><a href="/navody">Nápověda</a></li>
            </ul>
          </div>

          <div>
            <div>
              <span>Pro vývojaře</span>
              <ul>
                <li><a href="/api">API</a></li>
              </ul>
            </div>

            <div>
              <span>Migrace faktur z</span>
              <ul>
                <li><a href="/migrace-billapp">BillApp</a></li>
              </ul>
            </div>
          </div>

          <div>
            <div>
              <span>Sledujte nás na</span>
              <ul>
                <li>
                  <a href="https://facebook.com/fakturaonline">Facebooku</a>
                </li>
                <li>
                  <a href="https://linkedin.com/in/fakturaonline">Linkedinu</a>
                </li>
              </ul>
            </div>

            <div>
              <ul>
                <li>
                  <a href="/cs"><img src="lang" alt="" /></a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>

      <div class="footer__copyright">
        <div class="footer__img">
          <img
            src="~/images/new-design/logo-alt.svg"
            alt="Fakturaonline.cz logo"
          />
        </div>

        <div>&copy; 2023 FakturaOnline s.r.o</div>

        <div class="footer__contact">
          <a href="mailto:podpora@fakturaonline.cz">podpora@fakturaonline.cz</a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style lang="scss" scoped>
.footer {
  margin-top: rem(40px);
  border: none;
}

.footer__content {
  border-top: 1px solid $blue-light;
}

.footer__mainmenu {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  list-style: none;
  margin: 0;
  padding: 0;
  gap: rem(16px);
  margin-top: rem(48px);
}

.footer__mainmenu a {
  color: $blue;
  font-weight: bold;
  font-size: rem(16px);
}

.footer__menu {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: rem(24px);
  margin-top: rem(48px);
}

.footer__menu ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

.footer__menu span {
  display: inline-block;
  font-size: rem(14px);
  line-height: calc(rem(14px) * 1.5);
  font-weight: bold;
  margin-bottom: rem(12px);
}

.footer__menu a {
  font-size: rem(14px);
  line-height: calc(rem(14px) * 1.5);
  font-weight: bold;
  color: $blue-off;
  text-decoration: none;
}

.footer__menu li {
  margin-bottom: rem(12px);
}

.footer__copyright {
  margin-top: rem(32px);
  text-align: center;

  @media screen and (min-width: $breakpoint-lg) {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}

.footer__img {
  margin-bottom: rem(16px);

  @media screen and (min-width: $breakpoint-lg) {
    margin-bottom: 0;
  }
}

.footer__contact {
  margin-top: rem(16px);

  @media screen and (min-width: $breakpoint-lg) {
    margin-top: 0;
  }
}

.footer__contact a {
  font-size: rem(18px);
  line-height: calc(rem(18px) * 1.5);
  color: $gray-800;
  text-decoration: none;
  font-weight: bold;
}
</style>
