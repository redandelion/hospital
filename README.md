# hospital
医院挂号小程序

#  API 列表
#  Client 顾客创建订单 POST
    uri /hospital/client/order/create
    参数：{
        doctorId:"d002",
        clientId:"1564",
        clientOpenid:"163546548",
        clientPhone:"18485487952",
        clientAge:"15",
        clientSymptom:"感冒了"
    }
    返回值：
    {
      "code": 0,
      "msg": "成功",
      "data": {
          "orderId": "1521642795982645744"
      }
    }
#  Client 顾客查看医生列表 GET
		uri /hospital/client/client/doctors
		参数：无
		返回值：
		{
				"code": 0,
				"msg": "成功",
				"data": [
						{
								"doctorId": "d002",
								"doctorUsername": "123456",
								"doctorPassword": "123456",
								"doctorName": "张丽",
								"doctorPhone": "1564815468",
								"doctorAge": "20",
								"doctorLevel": "1",
								"doctorComment": "医生介绍栗震亚 主任医师 专长:Edgewise矫正技术、Tip—Edge矫治技术、MBT矫治技术、活动矫治技术、功能性矫治技术 陈一戎 主任医师 专长:泌尿系统肿瘤",
								"doctorImg": ""
						},
						{
								"doctorId": "d005",
								"doctorUsername": "1234567",
								"doctorPassword": "1234567",
								"doctorName": "北极熊",
								"doctorPhone": "15487988724",
								"doctorAge": "16",
								"doctorLevel": "2",
								"doctorComment": "急症医生"
						}
				]
		}
#  Client 顾客获取openid订单 GET
    uri /hospital/openid/token
    参数：{
        code:"003NeQwp1m9w3r0jUkvp1kVWwp1NeQwi"
    }
    返回值：
    {
        "code": 0,
        "msg": "成功",
        "data": {
            "openid": "on2L10GUDaFgHD6EFvRuvAkWRKSg"
        }
    }
