FROM php:8.2-apache

RUN apt-get update && apt-get install -y libonig-dev openssh-server && \
docker-php-ext-install pdo_mysql mysqli mbstring

# RUN

# RUN mkdir /var/run/sshd
# # rootのパスワードをrootpasswdに設定します。ただし、公開鍵認証でのアクセスなので使用しませんが。。
# RUN echo 'root:rootpasswd' | chpasswd
# # sshのrootでのアクセスを許可します。ただし、パスワードでのアクセスは無効
# RUN sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin prohibit-password/' /etc/ssh/sshd_config
# # sshのポートを22 => 20022に変更します
# RUN sed -i 's/#Port 22/Port 20022/' /etc/ssh/sshd_config
# # ホスト側にある公開鍵をイメージ側に登録します
# COPY ./20220405_mori_public_key_linux.pub /root/.ssh/authorized_keys
# 
# EXPOSE 20022
# CMD ["/usr/sbin/sshd", "-D"]