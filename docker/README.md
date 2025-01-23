# How to push new image to repo

Build image
```shell
docker build -t web .
```

Login to Yandex Cloud docker regisrty
```shell
echo <OAuth>|docker login \                  
  --username oauth \
  --password-stdin \
 cr.yandex
```

Set name
```shell
docker tag web cr.yandex/crpftiduupc1q0p2dmgt/web:0.1
```

Push image to remote regisrty
```shell
docker push cr.yandex/crpftiduupc1q0p2dmgt/web:0.1
```