<template>
  <section class="blog-posts">
    <div class="container">
      <ul class="blog-posts__list">
        <li>
          <div class="blog-posts__img">
            <img src="~/images/new-design/post.jpg" alt="Blog post image" />
          </div>

          <h3 class="blog-posts__title">
            Nevíte, zda podnikat jako fyzická či právnická osoba?
          </h3>
          <div class="blog-posts__meta">
            <span>23.9.2023</span>
            <ul class="blog-posts__categories">
              <li><a href="/kategorie/dane">Daně</a></li>
              <li><a href="/kategorie/dalsi">Další kategorie</a></li>
            </ul>
          </div>
          <p class="blog-posts__text">
            V začátcích podnikání většinou lidé stojí před otázkou, zda v
            podnikání vystupovat jako fyzická osoba, tedy OSVČ, nebo zda zvolit
            formu osoby právnické, tedy s.r.o. Obecně lze říci, že OSVČ, tedy
            osoby samostatně výdělečně činné ...
          </p>
        </li>

        <li>
          <div class="blog-posts__img">
            <img src="~/images/new-design/post.jpg" alt="Blog post image" />
          </div>

          <h3 class="blog-posts__title">
            Podnikání: Založení živnosti - podmínky a druhy
          </h3>
          <div class="blog-posts__meta">
            <span>23.9.2023</span>
            <ul class="blog-posts__categories">
              <li><a href="/kategorie/dane">Daně</a></li>
              <li><a href="/kategorie/dalsi">Další kategorie</a></li>
            </ul>
          </div>
          <p class="blog-posts__text">
            Zjednodušte si podnikání s FakturaOnline.cz! V našem seriálu tipů
            pro podnikatele se v prvním dílu dozvíte vše o založení živnosti,
            jejích druzích a podmínkách. Začněte svou podnikatelskou cestu s
            jistotou!
          </p>
        </li>

        <li>
          <div class="blog-posts__img">
            <img src="~/images/new-design/post.jpg" alt="Blog post image" />
          </div>

          <h3 class="blog-posts__title">
            FakturaOnline spustila funkci zobrazení stavu faktur
          </h3>
          <div class="blog-posts__meta">
            <span>23.9.2023</span>
            <ul class="blog-posts__categories">
              <li><a href="/kategorie/dane">Daně</a></li>
              <li><a href="/kategorie/dalsi">Další kategorie</a></li>
            </ul>
          </div>
          <p class="blog-posts__text">
            FakturaOnline.cz přichází s novou funkcí, která pomůže všem
            uživatelům udělat si trochu pořádek a odhalit případné neplatiče.
            Nově nyní můžete využívat označení stavu faktur. Tedy pokud patříte
            mezi předplatitele tarifu PREMIUM.
          </p>
        </li>

        <li>
          <div class="blog-posts__img">
            <img src="~/images/new-design/post.jpg" alt="Blog post image" />
          </div>

          <h3 class="blog-posts__title">
            Daňový kalendář 2022 pro Google a ke stažení
          </h3>
          <div class="blog-posts__meta">
            <span>23.9.2023</span>
            <ul class="blog-posts__categories">
              <li><a href="/kategorie/dane">Daně</a></li>
              <li><a href="/kategorie/dalsi">Další kategorie</a></li>
            </ul>
          </div>
          <p class="blog-posts__text">
            Pro daňové poplatníky platí také v roce 2022 určité povinnosti.
            Přinášíme přehled jednotlivých daní, který si můžete přidat jako
            kalendář do svého Google kalendáře, nebo si ho můžete stáhnout a
            importovat do kalendáře v počítači.
          </p>
        </li>

        <li>
          <div class="blog-posts__img">
            <img src="~/images/new-design/post.jpg" alt="Blog post image" />
          </div>

          <h3 class="blog-posts__title">Podpora v nezaměstanosti pro OSVČ</h3>
          <div class="blog-posts__meta">
            <span>23.9.2023</span>
            <ul class="blog-posts__categories">
              <li><a href="/kategorie/dane">Daně</a></li>
              <li><a href="/kategorie/dalsi">Další kategorie</a></li>
            </ul>
          </div>
          <p class="blog-posts__text">
            Mají OSVČ nárok na podporu v nezaměstnanosti? A pokud ano, tak v
            jaké výši? Všechny informace na jednom místě přinášíme v tomto
            článku.
          </p>
        </li>

        <li>
          <div class="blog-posts__img">
            <img src="~/images/new-design/post.jpg" alt="Blog post image" />
          </div>

          <h3 class="blog-posts__title">Pravidla fakturace</h3>
          <div class="blog-posts__meta">
            <span>23.9.2023</span>
            <ul class="blog-posts__categories">
              <li><a href="/kategorie/dane">Daně</a></li>
              <li><a href="/kategorie/dalsi">Další kategorie</a></li>
            </ul>
          </div>
          <p class="blog-posts__text">
            Tento článek věnujeme základním informacím o fakturaci, všech
            náležitostech faktur pro plátce i neplátce DPH a možnostech online
            fakturace.
          </p>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "BlogPosts",
};
</script>

<style lang="scss" scoped>
.blog-posts {
  margin-top: rem(40px);

  @media screen and (min-width: $breakpoint-lg) {
    margin-top: rem(48px);
  }
}
.blog-posts__list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  grid-gap: rem(24px);
  list-style: none;
  padding: 0;
  margin: 0;

  @media screen and (min-width: $breakpoint-lg) {
    grid-gap: rem(56px);
  }
}

.blog-posts__img {
  margin-bottom: rem(12px);
}

.blog-posts__title {
  font-size: rem(24px);
  line-height: calc(rem(24px) * 1.5);
  font-weight: bold;
  color: $blue;
  text-decoration: underline;
  margin: 0;
}

.blog-posts__meta {
  display: flex;
  margin-top: rem(12px);
  font-size: rem(16px);
  line-height: calc(rem(16px) * 1.2);
  margin-bottom: rem(12px);
}

.blog-posts__categories {
  display: flex;
  gap: rem(12px);
  list-style: none;
  font-weight: bold;
}

.blog-posts__text {
  font-size: rem(16px);
  line-height: calc(rem(16px) * 1.5);
}
</style>
