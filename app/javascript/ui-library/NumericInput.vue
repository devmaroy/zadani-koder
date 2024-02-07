<script>
import { Input } from "element-ui";

export default {
  extends: Input,
  props: {
    autocomplete: {
      type: String,
      default: "",
    },
  },
};
</script>

<style lang="scss">
.el-input {
  &.is-disabled {
    .el-input__inner:disabled {
      font-weight: 700;
      color: $--color-text-regular;
      -webkit-text-fill-color: $--color-text-regular;
      cursor: default;
    }
  }
}

.el-input__inner {
  height: rem(56px);
}

.el-input--large {
  .el-input__inner {
    height: $--input-large-height;
  }

  .el-input__prefix {
    width: rem(40px);
  }

  .el-input__icon {
    line-height: $--input-large-height;
  }
}

.el-input--prefix {
  .el-input__inner {
    padding-left: rem(16px);
    &:focus {
      border-color: $--input-border-color;
    }
  }
}

.el-input__inner,
.el-textarea__inner {
  padding: rem(12px) rem(16px);
  font-size: rem(16px);
  line-height: calc(rem(16px) * 1.5);
  font-weight: bold;
}

.el-input__prefix {
  left: auto;
  right: 0;
  width: rem(40px);
  height: 100%;
  font-size: rem(24px);
  pointer-events: none;
  .el-input__icon {
    width: 100%;
    pointer-events: none;
    cursor: default;
    color: $--color-blue-new;
  }
}
</style>
