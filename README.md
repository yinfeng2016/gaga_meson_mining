# 第一步：gaga_mining

gaga节点，美国ip挖矿奖励最高，中国ip挖矿奖励最低，如果可以，用docker之类的跑多ip

```
curl -o app-linux-amd64.tar.gz https://assets.coreservice.io/public/package/22/app/1.0.3/app-1_0_3.tar.gz && tar -zxf app-linux-amd64.tar.gz && rm -f app-linux-amd64.tar.gz && cd ./app-linux-amd64 && sudo ./app service install

sudo ./app service start

./app status

sudo ./apps/gaganode/gaganode config set --token=gusecrmbijembofvostalfqw

./app restart
```



其他命令：

```

sudo ./app service install                    # install node
sudo ./app service start                      # start node
sudo ./app service stop                       # stop node
sudo ./app service remove                     # remove node
./app status                                  # check node running status
./app restart                                 # restart node
./app upgrade                                 # upgrade node
./app log                                     # check logs
./app -h                                      # check help

```







# 第二步：meson_mining

第二行命令里https port可以修改，默认443，这个是对外端口，需要在防火墙开启

```
wget 'https://staticassets.meson.network/public/meson_cdn/v3.1.18/meson_cdn-linux-amd64.tar.gz' && tar -zxf meson_cdn-linux-amd64.tar.gz && rm -f meson_cdn-linux-amd64.tar.gz && cd ./meson_cdn-linux-amd64 && sudo ./service install meson_cdn

sudo ./meson_cdn config set --token=obzuhizjeiueeohqijsotpvs --https_port=443 --cache.size=100

sudo ./service start meson_cdn
```




服务关闭：
```
sudo ./service restart meson_cdn
```

服务重启：
```
sudo ./service restart meson_cdn
```
