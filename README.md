# hospital
医院挂号小程序

# API 列表
#  Client 顾客创建订单 API 
    请求类型：POST
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
#  Client 顾客查看医生列表 API
     uri /hospital/client/order/doctors
     参数：无
     返回值：
     
     
#  Client 顾客获取openid API    
     请求类型：GET
     uri /hospital/openid/token
     参数： {
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
