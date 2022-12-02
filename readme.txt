一，修改配饰文件
1. 打开config.cfg文件，依次进行如下配置
2. 复制4个相机的图片和内参文件路径。
3. 修改 ref_points，按照标定数据的日期选择对应的技研 SVC 点位文件
4. 修改车辆信息文件：在 /vehicle_info 下根据不同的项目选择不同文件
5.根据不同的项目修改 data_type 和 veh_platform

举例：
1. 对于 NT2.0 数采、工厂 ET7：
    "vehicle_info_file" 为 /vehicle_info/nt2/et7_vehicle_info.json
    “data_type” 为 online
    "veh_platform" 为 NT2.0
2. 对于 NT2.0 数采 ES8 （CN, EU）：
    "vehicle_info_file" 为 /vehicle_info/nt2/es8_vehicle_info.json
    “data_type” 为 offline
    "veh_platform" 为 NT2.0
3. 对于 NT1.2 数采 ES6，ES8：
    "vehicle_info_file" 为 /vehicle_info/nt12/vehicle_info_es8.json 或 /vehicle_info/nt12/vehicle_info_es6.json 或 /vehicle_info/nt12/vehicle_info_ec6.json
    “data_type” 为 online
    "veh_platform" 为 NT1.2

运行程序：
1. 如果是 NT1.2： 
      ./bin/nt12_calib/ config.cfg
1. 如果是 NT2.0： 
      ./bin/nt2_calib/ config.cfg

标定结果：
拼接图和标定json文件在 /result 文件夹下
注意 NT2.0 数采 ES8 （CN, EU）的运行结果也是 ET7 量产 json 格式
