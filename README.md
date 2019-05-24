
定制redis镜像，修改默认配置文件

### docker-compose

```yaml
version: "3"
services:
    redis5:
        image: "snkso/redis:5-alpine"
        #build:
        #    context: .
        #    dockerfile: Dockerfile
        stdin_open: true
        restart: always
        tty: true
        working_dir: '/data'
        volumes:
            - "./data:/data"
        ports:
          - 16379:6379
```
