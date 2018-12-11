------------------------------------
#2018-06-26
1、在前期的基础上增加Welcome.Activity模块，存在无法绑定人脸的问题

2、增加访问后台获取摄像头IP的接口
```
public final static String url_cameras = "http://192.168.1.6:8080/door-api/enterprise/cameras";

params.put("enterpriseId", s);
```
3、增加人脸识别成功后上传比对信息到后台

```
public final static String url_clockUpload = "http://192.168.1.8:8080/door-api/clockUpload";

params.put("enterpriseId", SPUtil.getInstance(MainPhoneActivity.this).getString(enterpriseid));
params.put("image", imagedata);
params.put("employeeName", name);
params.put("confidence", confidence);
params.put("clockTime", CaptureTime);
params.put("employeeId", employeeId);
```
#2018-06-27
1、同时接收两个摄像头的比对信息---------------待测试
2、增加中华万年历天气接口

#2018-07-02
1、替换HomeRecyAdapter中图片加载方式，使用Glide框架，加载图片不出现OOM问题
#2018-07-03
1、实现从后台获取摄像头ip，获取数据上传数据与后台打通。后台服务器地址写入全局变量中

2、整合功能、将上传人脸库功能加入logo单击响应中
#2018-07-04
1、解决打卡弹窗被遮挡问题，目前只是修改了空白卡的高度，将空白卡高度缩小，暂时可用，后期需优化

2、修改项目包名为com.emwit.face、添加图标，设置名字

3、打卡弹窗可同时显示多人

4、在timer定时器中30秒清一次上传人员的id_flag,打卡成功3秒后清除打卡flag

#2018-07-05

1、为添加人脸库添加访客人脸库上传，添加回调接口，更新成功后弹出toast

2、对上传打卡图片进行压缩，压缩到5Kb左右

#2018-07-06
1、屏幕+人脸识别相机+云平台的整套产品, 名字我们叫facejoy，域名就是facejoy.com




















``Change
