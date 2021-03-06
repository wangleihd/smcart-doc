# 数据库设计 集合说明

## 汽车信息说明

### carinfo

| 中文名称 | 英文 | 类型 | 说明 | 备注 |
|---------|------|------|------|-----|
| 编号     | \_id | MD5  | 系统自动创建 |   |
| 工单号 | id |  String | 170708153028 | 年月日时分秒各取2位 |
| 车牌号 | carnum | String |  |  |
| 车主姓名 | name | String |   |   |
| 车主电话 | phone| String  | |  | 
| 车主公司 | company | String |  |  |
| 车主地址 | address | String |  |  |
| 保险公司 | baoxian | String |  |  |
| 车名     | carname | String |  |  |
| 车类型   | cartype | String |  |  |
| 车着色   | carcolor | String|  |  |
| sa姓名   | saname | String |   |  |
| 输入时间 | nowtime | String | 登记时间 |  |
| 交车时间 | ftime  |  Date | 预计交车时间 |  |
| 实交车时间 | realtime | date | 实际的交车时间 |  |
| 钣金工序 | bjgx | string | 钣金工序 | 是否完成工序 |
| 钣金工序时间 | bjgx-start | string | 钣金工序开始时间 |  |
| 钣金工序时间 | bjgx-end | string | 钣金工序结束时间 |  |
| 钣金工序时间 | bjgx-about | string | 钣金工序预计花费的时间 | 这个工序大约需要2小时间 |
| 钣金工序时间 | bjgx-will | string | 钣金工序预计时间 |  |
| 钣金工序时间 | bjgx-about | string | 钣金工序预计花费的时间 | 这个工序大约需要2小时间 |





## 工人信息

### userinfo

| 中文名称 | 英文 | 类型 | 说明 | 备注 |
|---------|------|------|------|-----|
| 帐号    | user  | string | 工人登录名  | 英文  |
| 姓名    | name  | string | 工人姓名  | 中文 |
| 密码    | passwd | string | MD5加密 |  |
| 职位    | worktype | string | 职位 |  "work">工人师傅, "sa">前台服务人员,"master">车间管理员,"root">系统管 |
| 头像    | pic     | string | 头像设置 | 暂时设置成图片 |
| 分组    | group   | string | 分组 | 默认值为 null |
| 电话    | phone | number | 电话号码 | 默认值为 0 |
| 部门    | department    | string | 部分名称 | 默认值为 null |
| 权限    | permission | Number|        |  默认值为 0 |
| 工位    |  station  | Number |  修理车位号 | 默认值为 0 |
| 状态    | status    |  Number |   | 默认值为 0 |
| 性别    |  sex      | Number | 性别 | 默认为 0 , 0表示男性, 1表示女生 |
| 工种    | workkind | arry | 技术工人能做的工作 | 钣金, 喷漆, 底处理, 抛光, 中涂, 装配, 检验 |




### 打卡记录



```js
let userShema = Schema({
    user: { type: String },  //账号
    name: { type: String }, //真实姓名
    pic: { type: String, default: ""}, //头像
    passwd: { type: String }, //密码
    worktype: { type: Array }, //职能
    group: { type: String, default: "" }, //分组
    phone: { type: Number, default: 0 }, //电话
    department: { type: String, default: "" }, //部门
    permission: { type: Number, default: 0 }, //权限
    station: { type: Number, default: 0 }, //工位
    status: { type: Number, default: 0 },
    sex: { type: Number, default: 0 }  //性别
});
```
