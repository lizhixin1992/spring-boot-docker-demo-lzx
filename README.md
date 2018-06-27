# springboot 整合 docker 测试
# 本地启动需要开启docker服务，并打开相应的端口连接
# 因为使用了docker的插件，所以不需要在配置文件中写docker的配置
# 操作顺序：
    1.项目先打包
    2.使用docker第三方插件创建镜像
        docker-maven-plugin的docker:build
        这个会在target下创建docker文件夹，并生成相关配置
    3.启动镜像
        在cmd里面运行 docker run -p 8090:8090 -d springio/spring-boot-demo
        端口号和镜像的名称自己配置，这样创建的容器名称是docker自己命名的，如要自定义容器名称这需要设置--name *****
        
# 本地的docker镜像推到dockerhub上，请到 https://blog.csdn.net/qq_22985751/article/details/80826586
