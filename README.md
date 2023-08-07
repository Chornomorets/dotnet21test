
### Heroku deployment steps

My Heroku app name is sample-web-api. Please change the name

```
docker build -t sample-web-api ./
heroku container:login
docker tag sample-web-api registry.heroku.com/sample-web-api/web
heroku container:push web -a sample-web-api
heroku container:release web -a sample-web-api
```