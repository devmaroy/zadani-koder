<template>
  <div class="form-hp">
    <div class="container">
      <div class="form-hp__content">
        <div class="form-hp__header">
          <img
            src="~/images/new-design/invoice-alt-icon.svg"
            alt="Invoice icon"
          />
          <h2 class="form-hp__title">Základní údaje</h2>
        </div>

        <Form :model="resource" ref="form" class="form-hp__form">
          <div class="form-hp__wrapper">
            <div>
              <FormGroup
                prop="invoiceKind"
                :label="$t('form.invoiceForm.fields.invoiceKind.label')"
                :help="$t('form.invoiceForm.fields.invoiceKind.inputHelp')"
                floatingLabel
                hasInputValue
              >
                <Select
                  v-model="resource.invoiceKind"
                  :placeholder="
                    $t('form.invoiceForm.fields.invoiceKind.placeholder')
                  "
                  name="invoiceKind"
                >
                  <Option
                    v-for="option in invoiceKinds"
                    :key="option.value"
                    :label="option.name"
                    :value="option.value"
                  />
                </Select>
              </FormGroup>

              <FormGroup
                prop="number"
                :label="$t('form.invoiceForm.fields.number.label')"
                floatingLabel
                :hasInputValue="resource.number !== ''"
              >
                <TextInput
                  name="number"
                  type="string"
                  v-model="resource.number"
                />
              </FormGroup>

              <div class="form-hp__wrapper">
                <FormGroup
                  prop="vs"
                  :label="$t('form.invoiceForm.fields.vs.label')"
                  floatingLabel
                  :hasInputValue="resource.vs !== ''"
                >
                  <TextInput name="vs" type="string" v-model="resource.vs" />
                </FormGroup>

                <FormGroup
                  prop="vs"
                  :label="$t('form.invoiceForm.fields.ks.label')"
                  floatingLabel
                  :hasInputValue="resource.ks !== ''"
                >
                  <TextInput name="ks" type="string" v-model="resource.ks" />
                </FormGroup>
              </div>
            </div>

            <div class="form-hp__metagroup">
              <FormGroup
                input-narrow
                prop="issedOn"
                :label="$t('form.invoiceForm.fields.issedOn.label')"
                floatingLabel
                :hasInputValue="resource.issedOn !== ''"
              >
                <DatePicker
                  v-model="resource.issedOn"
                  value-format="timestamp"
                  :clearable="false"
                />
              </FormGroup>

              <FormGroup
                prop="invoiceKind"
                :label="$t('form.invoiceForm.fields.maturity.label')"
                floatingLabel
                hasInputValue
              >
                <div class="form-hp__maturity">
                  <Select
                    v-model="resource.maturityKind"
                    :placeholder="
                      $t('form.invoiceForm.fields.maturityKind.placeholder')
                    "
                    name="maturityKind"
                  >
                    <Option
                      v-for="option in maturityKinds"
                      :key="option.value"
                      :label="option.name"
                      :value="option.value"
                    />
                  </Select>

                  <span v-if="resource.issedOn !== ''">
                    {{ formatDate(getEndDate()) }}</span
                  >
                </div>
              </FormGroup>
            </div>
          </div>
        </Form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BasicForm",
  data: () => ({
    resource: {
      number: "",
      vs: "",
      ks: "",
      issedOn: "",
      invoiceKind: "vat_invoice",
      maturityKind: "7",
    },
    invoiceKinds: [
      { value: "vat_invoice", name: "Faktura - Daňový doklad (plátce DPH)" },
      { value: "invoice", name: "Faktura bez DPH" },
      { value: "proforma", name: "Proforma" },
    ],
    maturityKinds: [
      { value: "7", name: "7 dnů" },
      { value: "14", name: "14 dnů" },
      { value: "21", name: "21 dnů" },
    ],
  }),
  methods: {
    formatDate(timestamp) {
      const date = new Date(timestamp);
      const day = date.getDate().toString().padStart(2, "0");
      const month = (date.getMonth() + 1).toString().padStart(2, "0"); // JavaScript months are 0-indexed.
      const year = date.getFullYear();
      return `${day}.${month}.${year}`;
    },
    getEndDate() {
      if (!this.resource.issedOn) return null; // Check if issuedOn is set

      const issedOnDate = new Date(this.resource.issedOn); // If issuedOn is already a timestamp
      const maturityDays = parseInt(this.resource.maturityKind, 10); // Get maturity number
      issedOnDate.setDate(issedOnDate.getDate() + maturityDays);

      return issedOnDate.getTime();
    },
  },
};
</script>

<style scoped lang="scss">
.form-hp {
  margin: rem(48px);

  @media screen and (min-width: $breakpoint-lg) {
    margin-top: rem(96px);
  }
}

.form-hp__content {
  border: rem(1px) solid rgba(#bbd2e1b8, 0.7);
  border-radius: 12px;
  padding: rem(40px);
}

.form-hp__header {
  display: flex;
  align-items: center;
  margin-bottom: rem(40px);
}

.form-hp__title {
  margin: 0 0 0 rem(16px);
  font-weight: bold;
  font-size: rem(22px);
  line-height: calc(rem(22px) * 1.8);
}

.form-hp__wrapper {
  @media screen and (min-width: $breakpoint-lg) {
    display: flex;
    gap: rem(40px);

    & div {
      flex: 1;
    }
  }
}

.form-hp__metagroup {
  & div {
    flex: 1;
    width: 100%;
  }

  @media screen and (min-width: $breakpoint-lg) {
    display: flex;
    gap: rem(40px);
    display: block;
  }
}

.form-hp__maturity {
  display: flex;
  align-items: center;

  & .el-select {
    max-width: rem(200px);
  }

  & span {
    font-size: rem(16px);
    font-weight: bold;
    line-height: calc(rem(16px) * 1.5);
    margin-left: rem(16px);
  }
}
</style>
