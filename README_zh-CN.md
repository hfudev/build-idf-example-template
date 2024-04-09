# 在 GitHub Actions 中手动触发 ESP-IDF 示例的构建

这是一个 GitHub 操作模板项目，用于触发 GitHub Actions 中 ESP-IDF 示例项目的构建。

## 用法

访问 https://github.com/hfudev/build-idf-example-template，单击`Use this template`按钮，基于此模板创建一个新的存储库。

访问刚刚创建的存储库，单击`Actions`选项卡，然后单击`build-idf-example-ad-hoc-yml`操作。

![action](./docs/assets/action.png)

单击`Run workflow`按钮，填写变量，然后单击`Run workflow`按钮。（变量应该是不言自明的。）

![variables](./docs/assets/variables.png)

片刻之后，构建将被触发，并且新的构建将显示在同一页面中。

![after](./docs/assets/after.png)

构建完成后，您可以手动下载工件。

![done](./docs/assets/done.png)

## 提示

### 使用本地 `sdkconfig` 文件

由于[`on.workflow_dispatch.inputs.<input_id>.type`](https://docs.github.com/en/enterprise-cloud@latest/actions/using-workflows/workflow-syntax-for-github-actions#onworkflow_dispatchinputsinput_idtype)不支持`file`类型输入，您可以使用以下命令打印`sdkconfig`文件的内容，然后将内容复制并粘贴到`override_sdkconfig_items`输入中。

```bash
grep -v '^#' [PATH_TO_YOUR_SDKCONFIG_FILE] | tr '\n' ',' | sed 's/,$//'
```
