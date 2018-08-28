# tal-fe-snippets README

To have a better coding efficiency, we need a tool to help us repreat lots of code template, based on element-ui

## Requirements

Just for TAL group FE team, based on our template project and ElementUI

## Preview

![](https://raw.githubusercontent.com/dreambo8563/vscode-TAL-FE-Snippets/master/images/snippets.gif)

## Release Notes

Users appreciate release notes as you update your extension.

### 0.0.4

- tms -> tal.message.success
- tmw -> tal.message.warning
- tme -> tal.message.error

### 0.0.3

- quickfix for tal.form.watch-refresh

### 0.0.2

- add plugin icon
- rename tal-submit to tfs
- tiu -> abbr. import { } from "@/constants/URL"
- tit -> abbr. import { } from "@/constants/TEXT
- tia -> abbr. import { } from "@/constants/API
- tlp ->
  tal.list.pagination

```js
handleCurrentChange(val) {
      this.currentPage = val
     //TODO: this.refreshList(params)
}
```

- tfr -> tal.form.reset

```js
resetForm(formName) {
      this.refs[formName].resetFields()
}
```

- tfw -> tal.form.watch-refresh

```js
filterForm: {
      handler: function(v) {
        const data = {}
        this.currentPage = 1
        // TODO:this.refreshList(data);
      },
      deep: true,
      immediate: true
    }
```

- tfr -> tal.form.rules-data

```js
rules: {
        name: [
          { required: true, message: "请输入活动名称", trigger: "blur" },
          { min: 3, max: 5, message: "长度在 3 到 5 个字符", trigger: "blur" }
        ],
        region: [
          { required: true, message: "请选择活动区域", trigger: "change" }
        ],
        date1: [
          {
            type: "date",
            required: true,
            message: "请选择日期",
            trigger: "change"
          }
        ],
        type: [
          {
            type: "array",
            required: true,
            message: "请至少选择一个活动性质",
            trigger: "change"
          }
        ]
      }
```

- tfvm -> tal.form.validate-methods

```js
const validatePass = (rule, value, callback) => {
  if (value === "") {
    callback(new Error("请再次输入密码"))
  } else if (value !== this.ruleForm2.pass) {
    callback(new Error("两次输入密码不一致!"))
  } else {
    callback()
  }
}
```

### 0.0.1

- tal-submit (form submit method)

---

### For more information

- [Visual Studio Code's Markdown Support](http://code.visualstudio.com/docs/languages/markdown)
- [Markdown Syntax Reference](https://help.github.com/articles/markdown-basics/)

**Enjoy!**
