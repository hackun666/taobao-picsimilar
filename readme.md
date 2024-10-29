# 淘宝图片搜同款 API 文档

## 概述

本 API 提供了一个简单的方式，通过图片链接来搜索淘宝上的同款商品。用户可以通过调用此 API，获取与您的图片相似的商品列表。

## 演示demo

[演示demo](https://open.one-api.club/demo.html)

## 接口地址

```
https://open.one-api.club/taobao/app/taobao/query
```

## 请求方式

- **POST**

## 请求参数

| 参数名   | 类型   | 是否必填 | 描述                 |
| -------- | ------ | -------- | -------------------- |
| `api_key`  | string   | 是       | 请求密钥       |
| `img_src`  | string   | 是       | 图片链接       |
| `page`   | int    | 否       | 分页参数，默认为1    |

## 请求示例

```bash
curl -X POST "https://open.one-api.club/taobao/app/taobao/query" \
-F "img_src=https://img.ithome.com/newsuploadfiles/thumbnail/2024/10/806000_240.jpg" \
-F "page=1"
```

## 响应参数

| 参数名       | 类型   | 描述                 |
| ------------ | ------ | -------------------- |
| `errcode`       | int    | 响应状态码           |
| `errmsg`    | string | 响应信息             |
| `results`       | array  | 商品列表             |

## 响应示例

```json
{
  "errcode": 0,
  "errmsg": "Success",
  "results": [
      {
      "RankScore": "0.8553",
      "Result": {
          "CategoryName": "无线/蓝牙音箱",
          "CommissionRate": "45",
          "CouponAmount": 0,
          "CouponEndTime": "",
          "CouponInfo": "",
          "CouponRemainCount": 0,
          "CouponStartFee": "",
          "CouponStartTime": "",
          "CouponTotalCount": "",
          "ItemId": "pvkb27vI3f6xVWXrMZhgy3tptm-vVbNx0sB7pMo7grIOo",
          "LevelOneCategoryName": "影音电器",
          "MaxCommission": [

          ],
          "Nick": "",
          "PicUrl": "https://img.alicdn.com/i1/2586909304/O1CN01eNA59K2IbHyFtimbS_!!2586909304.jpg",
          "PriceAfterCoupon": "2199.00",
          "Provcity": "江苏 南京",
          "ReservePrice": "2999.00",
          "SellerId": "2586909304",
          "ShopTitle": "千冠数码",
          "ShortTitle": "哈曼卡顿琉璃4礼物家用氛围灯",
          "SubTitle": "",
          "Title": "哈曼卡顿音响琉璃4四代无线蓝牙音箱礼物家用透明音响小型琉璃3代",
          "UserType": 0,
          "Volume": 1,
          "ZkFinalPrice": "2199"
          }
      },
  ]
}
```

## 错误码

| 错误码 | 描述                 |
| ------ | -------------------- |
| 400    | 请求参数错误         |
| 404    | 未找到相似商品       |
| 500    | 服务器内部错误       |

## 注意事项

1. 图片链接格式支持 `jpg`, `jpeg`, `png`。
2. 每次请求最多返回10条结果，可以通过 `page` 参数调整。
3. 如果未找到相似商品，`results` 字段将为空数组。


## 购买 API-KEY 说明

为了使用本 API 服务，您需要购买一个有效的 API-KEY。API-KEY 是访问本 API 的唯一凭证，确保您的请求能够被正确识别和处理。

### 购买流程

1. **访问购买页面**：点击以下链接跳转到购买页面。
2. **选择套餐**：根据您的需求选择合适的套餐。
3. **支付**：完成支付流程。
4. **获取 API-KEY**：支付成功后，您将收到一封包含 API-KEY 的电子邮件。

### 购买链接

[点击这里购买 200次卡](https://shop.51fkba.com/details/AECE8C94)

[点击这里购买 1000次卡](http://shop.51fkba.com/details/794263E5)

### 注意事项

1. 请妥善保管您的 API-KEY，避免泄露给他人。
2. 每个 API-KEY 都有使用限制，请根据您的套餐合理使用。
3. 如果您需要更高的使用限额或特殊需求，请联系我们的客服团队。
