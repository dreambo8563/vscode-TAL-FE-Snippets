# README

To have a better coding efficiency, we need a tool to help us repreat lots of code template, based on element-ui

## Requirements

Just for TAL group FE team, based on our template project and ElementUI

## Preview

![](https://raw.githubusercontent.com/dreambo8563/vscode-TAL-FE-Snippets/master/images/snippets.gif)
![](https://raw.githubusercontent.com/dreambo8563/vscode-TAL-FE-Snippets/master/images/form_tpl.gif)

## Release Notes

Users appreciate release notes as you update your extension.

### 0.0.5

vue-html Form Code Template

- tfc -> tal.form.container

```html
<el-form :model="ruleForm" :rules="rules" ref="ruleForm" label-width="100px" class="demo-ruleForm">
  <el-form-item>
    <el-button type="primary" @click="submitForm('ruleForm')">立即创建</el-button>
    <el-button @click="resetForm('ruleForm')">重置</el-button>
  </el-form-item>
</el-form>
```

- tfi -> tal.form.input

```html
<el-form-item label="活动名称" prop="name">
  <el-input v-model="ruleForm.name"></el-input>
</el-form-item>
```

- tfs -> tal.form.select

```html
<el-form-item label="活动区域" prop="region">
  <el-select v-model="ruleForm.region" placeholder="请选择活动区域">
    <el-option label="区域一" value="shanghai"></el-option>
  </el-select>
</el-form-item>
```

- tfdp -> tal.form.datepicker

```html
<el-form-item label="活动时间" prop="date1">
  <el-date-picker type="date" placeholder="选择日期" v-model="ruleForm.date1" style="width: 100%;"></el-date-picker>
</el-form-item>
```

- tftp -> tal.form.timepicker

```html
<el-form-item label="活动时间" prop="date2">
  <el-time-picker type="fixed-time" placeholder="选择时间" v-model="ruleForm.date2" style="width: 100%;"></el-time-picker>
</el-form-item>
```

- tfs -> tal.form.switch

```html
<el-form-item label="即时配送" prop="delivery">
  <el-switch v-model="ruleForm.delivery"></el-switch>
</el-form-item>
```

- tfcg -> tal.form.checkboxgroup

```html
<el-form-item label="活动性质" prop="type">
  <el-checkbox-group v-model="ruleForm.type">
    <el-checkbox label="美食/餐厅线上活动" name="type"></el-checkbox>
    <el-checkbox label="地推活动" name="type"></el-checkbox>
  </el-checkbox-group>
</el-form-item>
```

- tfrg -> tal.form.radiogroup

```html
<el-form-item label="特殊资源" prop="resource">
  <el-radio-group v-model="ruleForm.resource">
    <el-radio label="线上品牌商赞助"></el-radio>
  </el-radio-group>
</el-form-item>
```

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
