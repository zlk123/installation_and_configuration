
| question| solver | append|
|--------|--------| --------|
|     deb文件无法安装，缺少 wps 文件（很奇怪）   |     使用run文件安装   | 可以探究为什么deb文件不行
|run 文件出错 |gpu驱动版本不对，卸载安装相应版本| 细节参考相关代码
|安装完无法进入图形界面|再次运行gpu驱动安装程序|
|安装完成窗口边框消失|安装compizconfig | 配置信息： 使用unity存档，Gsetting 后端，启用unityshell|
|安装完cudann 无法找到路径|LD_LIBRARY_PATH="$LD_LIBRARY_PATH:" CUDA_HOME=/usr/local/cuda|在.bash_rc,zsh中需要修改./zshrc


- 卸载nvidia 驱动，
- 安装对应驱动
- 安装cuda
- 安装对应驱动
- compizconfig（解决窗口边框消失）
- 将使用unity存档， Gsetting 后端， unityshell 启用

- 使用anaconda 安装 tensorflow 确实方便


```bash
conda create -n tensorflow python=2.7 #创建tensorflow环境
activate conda tensorflow  #激活tensorflow环境
conda install ipython  #安装notebook
conda install jupyter  #安装jupyter
jupyter notebook #启动jupyter
```
gpu模式明明路径都已经设置好了在 bash_p
里面，为什么还是说找不到

相关代码
``` bash
# Hit CTRL+ALT+F1 and login using your credentials.
sudo service lightdm stop # kill your current X server session by typing 
sudo lightdm stop
sudo init 3# Enter runlevel 3 by typing ,and install your
 ./*.run # run initfile.
You might be required to reboot when the installation finishes. If not, run `sudo service lightdm start` or sudo start lightdm to start your X server again.
```