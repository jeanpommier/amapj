# Faire tourner amapj dans docker

## quick & dirty

```
docker build -t mopnaej/amapj .

docker run -it \
  -v amapj_db:/opt/amapj/amapj-db \
  -v amapj_data:/opt/amapj/data \
  --name amapj -p 8081:8080 --rm mopnaej/amapj:latest
```
## Notes
Apparemment, je n'ai pas réussi à me passer de amapj.xml et tout configurer dans le web.xml. Bizarre. Mais bon, c'est pas bien grave.
Je n'ai pas non plus ajouté les trucs rigolos comme wkhtmltopdf. Peut-être que ça vaudra le coup de s'inspirer (très librement) de https://github.com/mgodlewski/dockerfiles/blob/master/amapj/Dockerfile
