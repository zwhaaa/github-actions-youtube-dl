# Github-actions-youtube-dl

使用 GitHub Actions 下载 YouTube 最高画质视频，并自动发布到 Release。


## 注意！

- **Github Release 最高可以发布 2G 大小的文件**（[官方文档说明](https://docs.github.com/cn/free-pro-team@latest/github/managing-large-files/distributing-large-binaries)），**所以视频文件超过 2G 后会进行分卷压缩，请下载全部前缀名为 downloaded 的文件并放在同目录下解压**

- **请大家下载完成后尽量删除 Release 中无用的视频文件**

- **✨善待 GitHub**

## 使用

#### 1. Fork 本仓库。

![image-20201128114406344](https://sc03.alicdn.com/kf/U1b919fe60d3c41b6907732abc04085b4C.jpg)

#### 2. 创建好自己的仓库后，在 Actions 中启用 GitHub Actions。

![image-20201128114243884](https://ae02.alicdn.com/kf/Uf0361991f56143fbb18cdcb47c151d17X.jpg)

![image-20210227151337588](https://ae03.alicdn.com/kf/U7607400616b74c6cab3f04170606ae44U.jpg)

#### 3. *按需更改 dl.conf 中的内容（非必要步骤，可以在此调整 youtube-dl 的下载参数）*。
#### 4. 将你要下载的 YouTube 视频的地址填进 *play.list* 中，每行限一个视频链接，Commit changes 提交。

![image-20210326104213586](https://ae03.alicdn.com/kf/Uafb6ab0f034c4721b4dada12a21ba8faq.jpg)

![image-20210326104324499](https://ae03.alicdn.com/kf/U7a1afda864134852835d74e6b0dbca89w.jpg)

![image-20210307231941399](https://ae03.alicdn.com/kf/U56b64cfd46af4b29ac5a158a85c41beeV.jpg)

![image-20210326104530317](https://ae03.alicdn.com/kf/Uf953e4f2a46840a0a40007b796362d6eU.jpg)

#### 5. Actions 开始下载视频，请耐心等待 Actions 的运行状态从黄色变成绿色后再去 *Release* 下载。
#### 6. Actions 运行后会将所有下载好的视频打包成 downloaded.zip .z01 .z02 发布到 *Release* 中。
#### 7. 进入 Release，下载打包好的压缩文件。

![image-20210307232152826](https://ae02.alicdn.com/kf/U2cc4b6d2e58a4e90b855b43459a3029fs.jpg)

![image-20210307234440331](https://sc04.alicdn.com/kf/U1c62e65434fb4901b2c096b728ae02efy.jpg)

## 运行失败的原因

1. 视频因为 **地区限制** 而导致 Actions 运行失败（此问题无解）

![image-failed](https://sc03.alicdn.com/kf/U9fbdca000450413ea930d0e09c128ca0Z.jpg)

2. 视频因为 **年龄限制** 而导致下载失败（在 youtube-dl 中登陆自己的账号即可，请自行更改 `dl.conf` 与 `Actions secrets` 中的内容）

![image-set0](https://ae03.alicdn.com/kf/U3e3a49159d57459688b9d7b5f32679d6O.jpg)

![image-set1](https://sc04.alicdn.com/kf/Ucf0ecdbad48f4ce8b57c08bb2735fe6eF.jpg)

3. 下载的链接中包含 `list` 导致下载时间超出 GitHub Actions 的六小时使用限制（请使用 YouTube 视频分享中的链接）

![image-failed](https://ae02.alicdn.com/kf/Ua55b6de269714409aa5ad067d75f423dr.jpg)

![image-set2](https://ae04.alicdn.com/kf/Ud2c19cc131964a328eb12584c8159346J.jpg)

## 计划中

- [x] 使用 GitHub Action 下载视频
- [x] 从列表中下载多个视频
- [x] 自定义配置
- [x] 使用分卷压缩上传多个文件以解除 Release 文件 2G 大小的限制


## License

[MIT](https://github.com/Heraldik/github-actions-youtube-dl/blob/main/LICENSE) © hw431

## 鸣谢

[justjavac](https://github.com/justjavac/github-actions-youtube-dl)

