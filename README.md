# dpt2cld-and-poseEstimation
深度图转点云and位姿估计

流程：   
1）首先，执行dpt2cld.hdev程序；  
2）然后，执行6DPoseEstimate.hdev程序。  

说明：  
1）运行dpt2cld.hdev程序之前，box文件夹内存放剪切坐标文件，dpt文件夹内存放深度图。dpt2cld.hdev程序首先会读取dpt文件夹内的深度图和box文件夹内的剪切坐标（bbox左上角的xy坐标），然后根据原始内参与剪切坐标计算出新内参，接着根据新内参将深度图dpt转换为点云cld，最后保存点云到cld文件夹内，保存新内参在cameraPara文件夹内。  
2）运行6DPoseEstimate.hdev程序之前，model文件夹内存放工件模型点云，scene文件夹内存放场景点云、场景RGB图、剪切坐标txt。6DPoseEstimate.hdev程序首先读取model文件夹内的工件点云，读取scene文件夹内的场景点云、场景RGB图、剪切坐标txt，最后进行匹配、估计位姿。


![image](https://user-images.githubusercontent.com/29196441/192419319-440e457d-7c29-41fd-8e6d-4b9cd06753cf.png)
