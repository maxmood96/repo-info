## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:d9294dbca0fdeb29cc0cf0495ee288d92952f95a9ad0f4031fa514b2022a75b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:8fd80ca9f22806ceb29697dd12359a4b80891a9daf2c2533b0fe933765e00f88
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.1 MB (492070513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a3f9d697be1563f801ee37774ec4ac2ffe095f905b7aee362c998edc019bab`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:08 GMT
ADD file:0b40d881e3e00d68de1f1df0a565385bb838144b83814df891c994f466e9efa2 in / 
# Mon, 06 Jul 2020 21:56:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:11 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 01:36:35 GMT
RUN apt-get update && apt-get install -y       gnupg
# Tue, 07 Jul 2020 01:36:36 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Tue, 07 Jul 2020 01:36:36 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Tue, 07 Jul 2020 01:38:22 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.4+b392     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Tue, 07 Jul 2020 01:38:23 GMT
ENV ZS_INIT_VERSION=0.3
# Tue, 07 Jul 2020 01:38:23 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Tue, 07 Jul 2020 01:38:24 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Tue, 07 Jul 2020 01:38:24 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Tue, 07 Jul 2020 01:38:25 GMT
WORKDIR /usr/local/zs-init
# Tue, 07 Jul 2020 01:38:36 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Tue, 07 Jul 2020 01:38:36 GMT
COPY dir:7937a6223a1e7805720eca1fbf8c2ccd37938f8f8aa175ae003d409459d49380 in /usr/local/bin 
# Tue, 07 Jul 2020 01:38:36 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Tue, 07 Jul 2020 01:38:37 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Tue, 07 Jul 2020 01:38:37 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Tue, 07 Jul 2020 01:38:38 GMT
EXPOSE 80
# Tue, 07 Jul 2020 01:38:38 GMT
EXPOSE 443
# Tue, 07 Jul 2020 01:38:38 GMT
EXPOSE 10081
# Tue, 07 Jul 2020 01:38:38 GMT
EXPOSE 10082
# Tue, 07 Jul 2020 01:38:38 GMT
WORKDIR /var/www/html
# Tue, 07 Jul 2020 01:38:39 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:a1125296b23d78a3585a7910d649fbf0cc56284f9d2066e3243e8bc18f90b308`  
		Last Modified: Wed, 01 Jul 2020 12:21:40 GMT  
		Size: 26.7 MB (26696193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c742a4a0f38c95e690ad2dad8909c0cb232911418ac94a73da2a28becc7b734`  
		Last Modified: Mon, 06 Jul 2020 21:57:18 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5ea3b329965bf7239f4e4f484915a444ec6d78b532ae12525934d4f6f7ac9a`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4be91ead68299f53759fd80c135e0dde0eb797e91eb8fbc5a708a506e0c433`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a7132c9d77a7cd18c82b13e833b73aa5e638151300faffbb4b9eb3966a69e7`  
		Last Modified: Tue, 07 Jul 2020 01:40:59 GMT  
		Size: 28.1 MB (28081644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befa7845b54db3885d58f9968b7a27ca3f22f8f826f271ab2608451fd0bb72d7`  
		Last Modified: Tue, 07 Jul 2020 01:40:56 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0204dca8ce9ee79c5c0075bfebfa1b17282916808bc7917475b65ace22b12d02`  
		Last Modified: Tue, 07 Jul 2020 01:40:54 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c024b88fd7428da60d49c46f8188906d865dd0dee5a51ece18ec788597716`  
		Last Modified: Tue, 07 Jul 2020 01:42:01 GMT  
		Size: 417.6 MB (417550237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08cf6b5e1d6bf95cc3b5b494bddd2b75a24f308215ea4675eb018cac0812dee8`  
		Last Modified: Tue, 07 Jul 2020 01:40:54 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a654e5180bbb6a34cfff2526c4fbe5a95447e0b51deaea08717087b6881ee6ee`  
		Last Modified: Tue, 07 Jul 2020 01:40:54 GMT  
		Size: 18.9 KB (18905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08aa0c68531a5b37a7c64f94ff42e0311061b1ba6cfcc4251ee206fc2e6f25a9`  
		Last Modified: Tue, 07 Jul 2020 01:40:57 GMT  
		Size: 19.7 MB (19666855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ab80288b23784493c62b31d3163241f147dcc83d7feacb0032f43e76d0ee5`  
		Last Modified: Tue, 07 Jul 2020 01:40:53 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e0f3db3888a35d5e2b6d7ea544961059da3227b6ec2d8add89c6df64e33698`  
		Last Modified: Tue, 07 Jul 2020 01:40:53 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bca58be2b91b8da1d8b7fa402f42beae017a97a2f1c3f37ea1bb978e06f7040`  
		Last Modified: Tue, 07 Jul 2020 01:40:53 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86a60ec216890f0ca2e943ca9a2ea2b6bedf93357e491ee79ef7273c0874aa9`  
		Last Modified: Tue, 07 Jul 2020 01:40:53 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
