# IDEA创建gradle项目犹如乌龟爬行（缓慢）解决方案

下载镜像慢。解决办法：在gradle中创建init.gradle文件【C:\gradle】，使用阿里镜像，每次创建项目皆会使用阿里源

内容如下：

~~~
allprojects {
    repositories {
        mavenLocal()
        maven { url 'http://maven.aliyun.com/nexus/content/repositories/central/' }
    }
}
~~~

