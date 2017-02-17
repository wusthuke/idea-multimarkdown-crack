注意编译环境需要jdk8

使用`update-alternatives`配置多jdk环境，设置jdk8
```
sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/jdk1.8.0_91/bin/java 300
sudo update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/jdk1.8.0_91/bin/javac 300
sudo update-alternatives --install /usr/bin/jar jar /usr/lib/jvm/jdk1.8.0_91/bin/jar 300
```

使用jar命令将修改后的`LicenseAgent.java`和`LicenseAgent.class`打包到`idea-multimarkdown.jar`中

```
jar uvf idea-multimarkdown.jar com/vladsch/idea/multimarkdown/license/LicenseAgent.java
jar uvf idea-multimarkdown.jar com/vladsch/idea/multimarkdown/license/LicenseAgent.class
```
