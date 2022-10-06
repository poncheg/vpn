# Настроить VPN/Proxy c российским IP


Для начала нужно
- Купить самый дешевый виртуальные сервер VPS, например [здесь](https://ruvds.com/ru-rub)
- добавить ваш публичный SSH ключ по root в ~/.ssh/authorized_keys, [инструкция](https://www.digitalocean.com/community/tutorials/how-to-configure-ssh-key-based-authentication-on-a-linux-server)


## Sock5 Proxy
Для настройки нужно
- добавить в bashrc или zshrc alias, для удобства
> alias vpn-up="ssh -D 9090 -N -f  root@YOUR_INTERNET_IP_HOST"
- выполнить **vpn-up** в теминале, чтобы подключить ssh tunnel. Они иногда отваливаеться, поэтому нужно перезапускать :yum:
- настройить в Wifi подключении Socks Proxy, например для Mac, чтобы браузеры "ходили" через proxy 
![image info](https://github.com/poncheg/vpn/blob/main/Mac_network_settings.png)


## Другой VPN (не работает вместе с Cisco AnyConnect)
воспользоваться [инструкцией](https://github.com/hwdsl2/setup-ipsec-vpn) и скриптом другого чела
