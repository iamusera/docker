# docker

1. 登录

   ```shell
   $ docker login --username=anykey0911 registry.cn-hangzhou.aliyuncs.com
   ```

2. pull, python仓库名称，下载对应版本3.8.10

   ```shell
   $ docker pull registry.cn-hangzhou.aliyuncs.com/image-anykey/python:3.8.10
   ```

3. push

   ```
   $ docker tag [ImageId] registry.cn-hangzhou.aliyuncs.com/image-anykey/python:3.8.10
   $ docker push registry.cn-hangzhou.aliyuncs.com/image-anykey/python:3.8.10
   ```