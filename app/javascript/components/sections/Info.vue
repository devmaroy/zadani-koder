<template>
  <section class="info">
    <div class="container">
      <div class="info__content">
        <ul class="info__list">
          <li>
            <h2>10 let</h2>
            <span>působíme na trhu</span>
          </li>

          <li>
            <h2>67 714 faktur</h2>
            <span>vystavili naši uživatelé za srpen</span>
          </li>

          <li>
            <h2>23 999 100 Kč</h2>
            <span>bylo vyfakturováno za srpen</span>
          </li>

          <li>
            <h2>24 541 uživatelů</h2>
            <span>nám zachovává přízeň</span>
          </li>

          <li>
            <h2>5 trhů</h2>
            <span>na kterých působíme</span>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Info",
};
</script>

<style lang="scss" scoped>
.info {
  margin-top: rem(40px);
}

.info__content {
  background: $blue-sky;
  border-radius: rem(24px);
  padding: rem(40px) rem(48px);
}
.info__list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: rem(32px);

  list-style: none;
  padding: 0;
  margin: 0;
  text-align: center;

  @media screen and (min-width: $breakpoint-lg) {
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  }
}

.info__list h2 {
  font-size: rem(26px);
  line-height: calc(rem(24px) * 1.2);
  font-weight: bold;
  margin: 0 0 rem(12px) 0;

  @media screen and (min-width: $breakpoint-lg) {
    font-size: rem(28px);
    line-height: calc(rem(28px) * 1.2);
  }
}

.info__list span {
  font-size: rem(16px);
  line-height: calc(rem(16px) * 1.2);
  font-weight: normal;
  color: $blue-off;
}
</style>
