```shell
1. docker run -d -it --name container_name iamge_name/id
2. docker exec -it container_id /bin/bash
    1. vim /etc/ssh/sshd_config
    2. #PermitRootLogin prohibit-password 
        PermitRootLogin yes
    3. /etc/init.d/ssh restart
```

