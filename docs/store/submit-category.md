# 为商店添加分类

**注意：添加分类需经过审核**

## 填写 yml

要添加分类，您需要创建一个描述它的文件。该文件的名称应为 `[category].yml` 并位于 `categories` 文件夹中，`category` 可自行命名，但请不要使用中文。

从 [example/category.template.yml](https://github.com/openGiraffes/openGiraffes-store-db/blob/main/example/category.template.yml) 获取分类模板。

### name

分类的名称。

```yaml
name: games
```

### description

分类的介绍/说明。

```yaml
description: Games
```

### icon

分类的图标，值为 Font Awesome 免费版本的图标，从这里了解可选值：[https://fontawesome.com/icons?d=gallery&m=free](https://fontawesome.com/icons?d=gallery&m=free)

```yaml
icon: fa_plane
```

### locales

分类所对应的本地化字段，若无将使用默认名称。

其中`locale_code` 请根据 ISO 639-1 和我们暂时支持的语言（本地化支持情况可在此查看：https://github.com/openGiraffes/openGiraffes-store-web/tree/master/src/assets/locales）填写， `text` 为对应字段。

```yaml
locales:
 - [locale_code]: [text]
```

若需要支持更多语言：

```yaml
locales:
 - [locale_code_1]: [text_1]
   [locale_code_2]: [text_2]
```

## 提交 yml

Fork [本仓库](https://github.com/openGiraffes/openGiraffes-store-db)，将你所填写的 `[category].yml` 上传至 `categories` 文件夹。

最后在本项目发起 Pull Request，我们将对该分类进行审核，通过后将会立即添加或在第二天 6:00 （北京时间）添加（GitHub Actions 定时构建）