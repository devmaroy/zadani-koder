<template>
  <section class="steps">
    <div class="container">
      <ul class="steps__list">
        <li>
          <div class="steps__icon">
            <img
              src="~/images/new-design/step01.svg"
              alt="Step decoration icon"
            />
          </div>
          <div>
            <h3>Vyplnit formulář a stáhnout PDF fakturu</h3>
            <p>
              Vystavení PDF faktury je jednoduché. Stačí vyplnit své
              identifikační údaje, které si můžete uložit pro další použití,
              údaje o odběrateli, přidat fakturované položky a kliknout na
              Vystavit fakturu. Hotovo.
              <a href="/vystavit-fakturu">Vystaví se vám PDF faktura</a>, kterou
              můžete poslat e-mailem, nebo vytisknout.
            </p>
          </div>
        </li>

        <li>
          <div class="steps__icon">
            <img
              src="~/images/new-design/step01.svg"
              alt="Step decoration icon"
            />
          </div>
          <div>
            <h3>Elektronická evidence tržeb integrována</h3>
            <p>
              V případě přijatých plateb je plně v provozu možnost
              <strong
                >napojení systému FakturaOnline.cz na elektronickou evidenci
                tržeb.</strong
              >
              Pro aktivaci vyplňte při vystavování faktury vaše údaje pro EET,
              otestujte spojení a pak využívejte evidenci tržeb u faktur, které
              si vyberete.
            </p>
          </div>
        </li>

        <li>
          <div class="steps__icon">
            <img
              src="~/images/new-design/step01.svg"
              alt="Step decoration icon"
            />
          </div>
          <div>
            <h3>Žádný elektronický podpis na faktuře nepotřebujete!</h3>
            <p>
              Pro zasílání elektronické faktury e-mailem ji nemusíte opatřit
              elektronickým podpisem. PDF faktura je platný doklad, stejně jako
              papírová faktura. Elektronickým podpisem by se musela faktura
              opatřit pouze v případě, že ji chcete pro účely účetnictví
              uchovávat v elektronické podobě - bez nutnosti tisku do papírové
              podoby.
            </p>
          </div>
        </li>

        <li>
          <div class="steps__icon">
            <img
              src="~/images/new-design/step01.svg"
              alt="Step decoration icon"
            />
          </div>
          <div>
            <h3>
              Je libo daňový doklad nebo zálohovou proforma fakturu včetně vzorů
              v PDF?
            </h3>
            <p>
              Systém FakturaOnline.cz umožňuje vystavení nejen běžných faktur -
              daňového dokladu, faktury pro neplátce DPH, zálohových faktur, či
              tzv. <strong>proforma faktury</strong>. Než vystavíte jakýkoliv
              druh faktury, podívejte se na jejich vzor v sekci
              <a href="/vzory-faktur">Vzory faktur</a>.
            </p>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "Steps",
};
</script>

<style lang="scss" scoped>
.steps {
  margin-top: rem(40px);

  @media screen and (min-width: $breakpoint-lg) {
    margin-top: rem(48px);
  }
}

.steps__list {
  list-style: none;
  padding: 0;

  @media screen and (min-width: $breakpoint-lg) {
    display: grid;
    grid-template-columns: repeat(2, minmax(260px, 1fr));
    gap: rem(32px) rem(56px);
  }
}

.steps__list li {
  &:not(:last-child) {
    margin-bottom: rem(40px);
  }

  @media screen and (min-width: $breakpoint-lg) {
    display: flex;
    gap: rem(24px);
    margin-bottom: 0;
  }
}

.steps__icon {
  flex-shrink: 0;
}

.steps__list h3 {
  font-size: rem(24px);
  line-height: calc(rem(24px) * 1.2);
  font-weight: bold;
  margin: 0 0 rem(12px) 0;
}

.steps__list p {
  font-size: rem(16px);
  line-height: calc(rem(16px) * 1.5);
}

.steps__list a {
  font-weight: bold;
}
</style>
