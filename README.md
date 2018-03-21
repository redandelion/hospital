# hospital
医院挂号小程序

# API 列表
#  Client 顾客创建订单 API
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
