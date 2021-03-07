# Github-actions-youtube-dl ![do](https://github.com/Heraldik/github-actions-youtube-dl/workflows/do/badge.svg)

使用 GitHub Actions 下载 YouTube 最高画质视频，并自动发布到 Release。


## 注意！

- **Github Release 最高可以发布 2G 大小的文件**（[官方文档说明](https://docs.github.com/cn/free-pro-team@latest/github/managing-large-files/distributing-large-binaries)），**所以视频文件超过 2G 后会进行分卷压缩，请下载全部前缀名为 downloaded 的文件并放在同目录下解压**

- **请大家下载完成后尽量删除 Release 中无用的视频文件**

- **✨善待 GitHub**

## 使用

1. Fork 本仓库。

![image-20201128114406344](README.assets/image-20201128114406345.png)

2. 创建好自己的仓库后，在 Actions 中启用 GitHub Actions。

![image-20201128114243884](README.assets/image-20201128114243884.png)

![image-20210227151337588](README.assets/image-20210227151337588.png)

3. *按需更改 dl.conf 中的内容（非必要步骤，可以在此调整 youtube-dl 的下载参数）*。
4. 将你要下载的 YouTube 视频的地址填进 **play.list** 中，每行限一个视频链接，commit push 提交。

![image-20210307231941399](README.assets/image-20210307231941399.png)

5. Actions 自动运行后会将所有下载好的视频打包成 downloaded.zip .z01 .z02 发布到 **Release** 中。
6. 进入 Release，下载打包好的压缩文件。

![image-20210307232152826](README.assets/image-20210307232152826.png)

![image-20210307234440331](README.assets/image-20210307234440331.png)


## 计划中

- [x] 使用 GitHub Action 下载视频
- [x] 从列表中下载多个视频
- [x] 自定义配置
- [x] 使用分卷压缩上传多个文件以解除 Release 文件 2G 大小的限制


## License

[MIT](https://github.com/Heraldik/github-actions-youtube-dl/blob/main/LICENSE) © hw431

## 鸣谢

[justjavac](https://github.com/justjavac/github-actions-youtube-dl)

