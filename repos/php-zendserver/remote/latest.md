## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:755e956bdcc675148cb4c388e7f0a95ce239bd39f2ef01bdbe219a7ce07875db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:974bdf3034a2fd5869b77cd6b48e063817fb1ca3c8bca79edfd3f337867371e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.5 MB (394519548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a421bc426d59a090e00d6b2a558b7fe5b12a1b753dffc6ab6e0cc7f38dc9f1`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:04 GMT
ADD file:ed601c56cf74241eeb1971b24ed969fb855cd2b9330276d3c5779ecdb0b28364 in / 
# Tue, 04 Oct 2022 23:35:04 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:49:31 GMT
RUN apt-get update && apt-get install -y       gnupg
# Wed, 05 Oct 2022 18:49:32 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Wed, 05 Oct 2022 18:51:54 GMT
COPY file:1e70d8fd6f9643bffb703528edddba0aa02a58e95cc53e92f58a86cde29e732a in /etc/apt/sources.list.d/zend-server.list 
# Wed, 05 Oct 2022 18:53:25 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2021.0.0+b74     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Wed, 05 Oct 2022 18:53:28 GMT
ENV ZS_INIT_VERSION=0.3
# Wed, 05 Oct 2022 18:53:28 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Wed, 05 Oct 2022 18:53:28 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Wed, 05 Oct 2022 18:53:29 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Wed, 05 Oct 2022 18:53:29 GMT
WORKDIR /usr/local/zs-init
# Wed, 05 Oct 2022 18:53:34 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Wed, 05 Oct 2022 18:53:34 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Wed, 05 Oct 2022 18:53:35 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Wed, 05 Oct 2022 18:53:35 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Wed, 05 Oct 2022 18:53:35 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Wed, 05 Oct 2022 18:53:35 GMT
EXPOSE 80
# Wed, 05 Oct 2022 18:53:35 GMT
EXPOSE 443
# Wed, 05 Oct 2022 18:53:36 GMT
EXPOSE 10081
# Wed, 05 Oct 2022 18:53:36 GMT
EXPOSE 10082
# Wed, 05 Oct 2022 18:53:36 GMT
WORKDIR /var/www/html
# Wed, 05 Oct 2022 18:53:36 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:e706e0a9f42365312b366bf4caa22f3cdd8fc7fd8f6f49b4dd3782711f66aca7`  
		Last Modified: Tue, 04 Oct 2022 11:37:26 GMT  
		Size: 26.7 MB (26711852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd252b7f9a96265764ed8af0d73eb7bb85429f89ae24bfb5f4e8ae740357491`  
		Last Modified: Wed, 05 Oct 2022 18:54:08 GMT  
		Size: 36.5 MB (36454415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa46b0b60dda0538593ec6a74c85088a924468c3778d768ec4328a981b6ff79f`  
		Last Modified: Wed, 05 Oct 2022 18:54:04 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0e671b46dd8124d5084c46e029e319ae962b68dd53c6b498668685e49d821b`  
		Last Modified: Wed, 05 Oct 2022 18:55:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b659a07f5f21c5870eac7087870bb60025f73293cc48318f8007dc1819754e6`  
		Last Modified: Wed, 05 Oct 2022 18:55:51 GMT  
		Size: 326.0 MB (326002496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554019f1e81c3c7aada774ef899ab8c3090c3ead02c7dc7ec0384409c7c5f211`  
		Last Modified: Wed, 05 Oct 2022 18:55:06 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479d60473bdb7eec64cf2157078f55dce32e4057d6b0ef29423cbf6d9870f6f7`  
		Last Modified: Wed, 05 Oct 2022 18:55:06 GMT  
		Size: 18.9 KB (18932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6216390c1c286bca6e03472a24fbc093e7fe8c266cdba2999cbe506aa6b392`  
		Last Modified: Wed, 05 Oct 2022 18:55:05 GMT  
		Size: 5.3 MB (5311487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770d02e632ad276ae62a3e725ffc376390e8d0448a688f94341dbdd33b1d3778`  
		Last Modified: Wed, 05 Oct 2022 18:55:04 GMT  
		Size: 14.3 KB (14293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87fbc691f87ed1d3170000259efd427dfa800f003f916126ca34d01f2cc0597`  
		Last Modified: Wed, 05 Oct 2022 18:55:04 GMT  
		Size: 2.6 KB (2557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b0a29776ee0ee899c58b9b41ecef37f3f4afc386fdf60c9cfe0bac09517398`  
		Last Modified: Wed, 05 Oct 2022 18:55:04 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8724f832559dfcb14a05a6a0168c8021fe8690f5845caf43e573930546bdc872`  
		Last Modified: Wed, 05 Oct 2022 18:55:04 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
