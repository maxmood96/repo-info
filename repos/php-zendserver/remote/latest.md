## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:f962dea98d83ac7abde3f167930c08dc6d953f06f845fdb2e5e60204ae3e3ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:daff6698050dd4f4483971271839cd768e9f3eb0b9b6224d9d466a2f1faab843
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.8 MB (395789602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa618eff4822db0f4a993879bebb98c5ff7574d0524112de16bfd5675693fd27`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Wed, 08 Mar 2023 03:22:42 GMT
ARG RELEASE
# Wed, 08 Mar 2023 03:22:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 03:22:42 GMT
LABEL org.opencontainers.image.version=18.04
# Wed, 08 Mar 2023 03:22:44 GMT
ADD file:4560926e076acae6b8396a9f1e760eee0f53e22e90ce8554dda57f1103547795 in / 
# Wed, 08 Mar 2023 03:22:44 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 04:57:37 GMT
RUN apt-get update && apt-get install -y       gnupg
# Thu, 16 Mar 2023 04:57:39 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Thu, 16 Mar 2023 04:59:46 GMT
COPY file:1e70d8fd6f9643bffb703528edddba0aa02a58e95cc53e92f58a86cde29e732a in /etc/apt/sources.list.d/zend-server.list 
# Thu, 16 Mar 2023 05:01:14 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2021.0.0+b74     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Thu, 16 Mar 2023 05:01:17 GMT
ENV ZS_INIT_VERSION=0.3
# Thu, 16 Mar 2023 05:01:17 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Thu, 16 Mar 2023 05:01:17 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Thu, 16 Mar 2023 05:01:18 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Thu, 16 Mar 2023 05:01:18 GMT
WORKDIR /usr/local/zs-init
# Thu, 16 Mar 2023 05:01:24 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Thu, 16 Mar 2023 05:01:24 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Thu, 16 Mar 2023 05:01:24 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Thu, 16 Mar 2023 05:01:25 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Thu, 16 Mar 2023 05:01:25 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Thu, 16 Mar 2023 05:01:25 GMT
EXPOSE 80
# Thu, 16 Mar 2023 05:01:25 GMT
EXPOSE 443
# Thu, 16 Mar 2023 05:01:25 GMT
EXPOSE 10081
# Thu, 16 Mar 2023 05:01:25 GMT
EXPOSE 10082
# Thu, 16 Mar 2023 05:01:26 GMT
WORKDIR /var/www/html
# Thu, 16 Mar 2023 05:01:26 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:cd150c608fee7837e3a5b28be5c7b540eaf4efa27b3b755d55326470691ce2df`  
		Last Modified: Sun, 12 Mar 2023 07:24:55 GMT  
		Size: 26.7 MB (26710746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c4e4d0dcad2ee76d70ac97a851be0f749c4753e44b907e5964f35a9d5dc0b0`  
		Last Modified: Thu, 16 Mar 2023 05:01:58 GMT  
		Size: 37.7 MB (37692669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bfa0f8bd97facb6137e75c6d7f6a108f43b78b4c88b9b8f105abef0e6dee11`  
		Last Modified: Thu, 16 Mar 2023 05:01:54 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dca7845c2652ebbf09896d0cb0827c6821970b30f7657f51683e54547ad6d5f`  
		Last Modified: Thu, 16 Mar 2023 05:02:53 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab676d9c7d34a9252ed30c9939ab089402f73263431dad1c32e2e2cf3fea93b`  
		Last Modified: Thu, 16 Mar 2023 05:03:35 GMT  
		Size: 326.0 MB (326023480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5909323d3ca866e025d57c139b36e6817de37e63c6e42fa40e5cbb8f6c4f0b`  
		Last Modified: Thu, 16 Mar 2023 05:02:53 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c800c2483943d2e907d3291829a0d0fd78a3d715bbbb632a45ff02fc855008db`  
		Last Modified: Thu, 16 Mar 2023 05:02:53 GMT  
		Size: 18.9 KB (18926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0385e78e4f03ce2c74a968b448b19e88da95973e627f23b498283b95a356866f`  
		Last Modified: Thu, 16 Mar 2023 05:02:52 GMT  
		Size: 5.3 MB (5323416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82970a74d5613db10f7f11c8719a5df90aa22a7963135a1323360e59c38d197`  
		Last Modified: Thu, 16 Mar 2023 05:02:51 GMT  
		Size: 14.3 KB (14294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea2fb542fb89090dc9469a39b0c0237c7c2623aebb0cb34978dadacc15bbc2c`  
		Last Modified: Thu, 16 Mar 2023 05:02:51 GMT  
		Size: 2.6 KB (2559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aab6406420ee54a1174bf24bbbc1495035690afc533c1788d9ca239044a8280`  
		Last Modified: Thu, 16 Mar 2023 05:02:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b2a7434e4f9fd436dd0975f72cf6fa1dfa17cfbc580c4bcac09d839243eed6`  
		Last Modified: Thu, 16 Mar 2023 05:02:51 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
