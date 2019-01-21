# madsiberian_infra
madsiberian Infra repository

# Домашнее задание №3
Подключение в одну строку:
**ssh -A appuser@35.240.42.130 -t ssh appuser@10.132.0.3**

Для подключения через алиас (**ssh someinternalhost**), следует дописать в .ssh/config следующее:
Host someinternalhost
        Hostname 35.240.42.130
        User appuser
        ForwardAgent yes
        RequestTTY force
        RemoteCommand ssh appuser@10.132.0.3

bastion_IP = 35.240.42.130
someinternalhost_IP = 10.132.0.3
