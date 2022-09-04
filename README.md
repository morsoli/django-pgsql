## 利用docker快速构建 Django 服务
### Start product service
`docker-compose -f docker-compose.prod.yaml up -d --build`
### Check for errors in the logs
`docker-compose -f docker-compose.prod.yaml logs -f`
### Stop product service
`docker-compose -f docker-compose.prod.yaml down -v`
