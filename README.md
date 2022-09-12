## 利用docker快速构建 Django 服务
### Start product service
```shell
docker-compose -f docker-compose.prod.yaml up -d --build
docker-compose -f docker-compose.prod.yaml exec web python manage.py migrate --noinput
docker-compose -f docker-compose.prod.yaml exec web python manage.py collectstatic --no-input --clear
```
### Check for errors in the logs
`docker-compose -f docker-compose.prod.yaml logs -f`
### Stop product service
`docker-compose -f docker-compose.prod.yaml down -v`

## 利用 GitHub Action， 接入CI/CD

