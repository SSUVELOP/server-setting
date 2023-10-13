# server-setting
Setting Server Configurations

Ubuntu 22.04 LTS

## ssh
    sudo apt update
    sudo apt install openssh-server

    # ssh 상태 확인
    sudo systemctl status ssh

## firewall
    sudo ufw allow ssh

    # 방화벽 해제 = 모든 포트 개방
    sudo ufw disable

## nginx
    sudo apt update
    sudo apt upgrade
    sudo apt autoremove

    sudo apt install nginx

    sudo service start nginx
    sudo service status nginx

    systemctl status nginx.service
    ## apache2 혹시 몰라
    sudo /etc/init.d/apache2 stop
    sudo service start nginx

    #nginx 버전 확인
    sudo dpkg -l nginx
    nginx -v

    #nginx 경로
    sudo find / -name nginx.conf

    sudo vim nginx.conf
    # nginx 구동 테스트
    netstat -lntp
    # 없다면?
    apt install net-tools

    # nginx 위치
    /etc/nginx/
    conf.d & nginx.conf
