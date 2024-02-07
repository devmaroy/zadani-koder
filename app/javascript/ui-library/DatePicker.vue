<script>
import { DatePicker } from "element-ui";

export default {
  extends: DatePicker,
  props: {
    pickerOptions: {
      type: Object,
      default() {
        return {
          firstDayOfWeek: 1,
        };
      },
    },
  },
};
</script>

<style lang="scss" scoped>
:deep() {
  &.el-date-editor {
    &.el-input__inner {
      width: 100%;
    }

    .el-date-editor.el-input &.el-input--prefix {
      .el-input__inner {
        padding-right: rem(48px);
        padding-left: rem(8px);
        width: 100%;
      }

      .el-input__prefix {
        left: auto;
        right: 0;
        border-right: 0;
        border-left: $--input-border;
        background-color: $--color-primary;
        color: $--color-white;
        border-radius: 0 4px 4px 0;
      }
    }

    &.el-input--suffix {
      .el-input__suffix {
        right: rem(40px);
        border-radius: 0 4px 4px 0;
      }
    }
  }
}
</style>
