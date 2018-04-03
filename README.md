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
#  Client 顾客查看医生详情 GET
	uri /hospital/client/client/doctor
    参数： {
      doctorId:"d002"
    }
    返回值：   
    {
        "code": 0,
        "msg": "成功",
        "data": {
            "doctorId": "d002",
            "doctorUsername": "123456",
            "doctorPassword": "123456",
            "doctorName": "张丽",
            "doctorPhone": "1564815468",
            "doctorAge": "20",
            "doctorLevel": "1",
            "doctorComment": "医生介绍栗震亚 主任医师 专长:Edgewise矫正技术、Tip—Edge矫治技术、MBT矫治技术、活动矫治技术、功能性矫治技术 陈一戎 主任医师 专长:泌尿系统肿瘤",
            "doctorImg": ""
        }
    }  
#  Client 顾客查看序号详情 GET
	uri hospital/client/order/number
	参数： {
			openid:15444
      doctorId:"d002",
    }	
	返回值:
	{
    "code": 0,
    "msg": "成功",
    "data": {
        "number": 2
    }
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
#  Doctor医生登录 POST
	uri /hospital/doctor/login
	 参数：{
	 		username:"123456",
			password:"123456"
	 }
	返回值：
	{
    "code": 0,
    "msg": "成功",
    "data": {
        "role": "123456",
        "name": "张丽"
    }
}
#  Doctor获取患者列表 GET
	uri /hospital/doctor/clientList
	 参数：{
	  doctorId:"d002"
	 }
	返回值：
	{
			"code": 0,
			"msg": "成功",
			"data": [
					{
							"orderId": "1521880105005733727",
							"doctorId": "d002",
							"clientId": "1565",
							"clientOpenid": "1544",
							"clientPhone": "15445272",
							"clientStatus": 0,
							"clientAge": "20",
							"clientSymptom": "喉咙发炎",
							"createTime": 1521880099000,
							"updateTime": 1522751237000
					},
					{
							"orderId": "1521881349495887991",
							"doctorId": "d002",
							"clientId": "15655",
							"clientOpenid": "15444",
							"clientPhone": "154452721",
							"clientStatus": 0,
							"clientAge": "5",
							"clientSymptom": "发热",
							"createTime": 1521881343000,
							"updateTime": 1522751242000
					},
					{
							"orderId": "1521978041562668323",
							"doctorId": "d002",
							"clientId": "156556",
							"clientOpenid": "154442",
							"clientPhone": "154452721",
							"clientStatus": 0,
							"clientAge": "5",
							"clientSymptom": "发热了",
							"createTime": 1521978035000,
							"updateTime": 1521978035000
					},
					{
							"orderId": "1522738533068750113",
							"doctorId": "d002",
							"clientId": "156556",
							"clientOpenid": "154442",
							"clientPhone": "154452721",
							"clientStatus": 0,
							"clientAge": "5",
							"clientSymptom": "发热了lj ",
							"createTime": 1522738530000,
							"updateTime": 1522738530000
					}
			]
	}	
#  Doctor删除患者列表 POST
    uri /hospital/doctor/deleteClient
    参数：{
	    openid:"1544"
	 }
	  返回值：
    {
    "code": 0,
    "msg": "成功",
    "data": {
        "status": 1
    }
    }
#  Admin 管理员开放系统 POST
	 uri /hospital/admin/open
    参数：无
	  返回值：
    {
    "code": 0,
    "msg": "成功",
    "data": {
        "systemStatus": "1"
    }
    }
#  Admin 管理员关闭系统 POST	
	 uri /hospital/admin/close
    参数：无
	  返回值：
	{
    "code": 0,
    "msg": "成功",
    "data": {
        "systemStatus": "0"
    }
    }
	
	
