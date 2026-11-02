# bmp.dudubox.pro

新版页面通过 `User_Data/data.json` 管理车辆信息。每条记录的 `uuid` 必须唯一，二维码链接使用对应的参数：

```text
https://你的域名/index.html?uuid=10013500
```

要增加或修改车辆，编辑 `User_Data/data.json` 中的 `plate`、`name` 和 `join_time`。例如：

```json
{
  "uuid": 10013520,
  "plate": "赣ARJV960",
  "name": "孙**",
  "join_time": "2026-11-02 15:30:00"
}
```

每个 `uuid` 生成一个独立二维码。部署时必须上传整个项目目录，不能只上传 `index.html`；页面需要通过 HTTPS 网站访问，直接双击 HTML 文件会因浏览器禁止读取 JSON 而无法加载数据。

请只在获得授权的场景使用页面内容。
