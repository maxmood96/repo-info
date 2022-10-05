<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `php-zendserver`

-	[`php-zendserver:2019.0`](#php-zendserver20190)
-	[`php-zendserver:2021.0`](#php-zendserver20210)
-	[`php-zendserver:5.6`](#php-zendserver56)
-	[`php-zendserver:8.5`](#php-zendserver85)
-	[`php-zendserver:8.5-php5.6`](#php-zendserver85-php56)
-	[`php-zendserver:9.1`](#php-zendserver91)
-	[`php-zendserver:latest`](#php-zendserverlatest)

## `php-zendserver:2019.0`

```console
$ docker pull php-zendserver@sha256:6a2b9e38ce5c571519749ff8aef24711434be745d8b2caf61bdb2fd4af972405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:2019.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:d1e21ddf10b3fdb84f12dc3b7689d0343596aaacc717abeade351010553b7ac3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.7 MB (486657822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ce3875b35a2c5e9789b07644aed9eb9d4a1963e11327e22bb6ed1903ee9608`
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
# Wed, 05 Oct 2022 18:49:32 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Wed, 05 Oct 2022 18:51:30 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.7+b403     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Wed, 05 Oct 2022 18:51:34 GMT
ENV ZS_INIT_VERSION=0.3
# Wed, 05 Oct 2022 18:51:34 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Wed, 05 Oct 2022 18:51:34 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Wed, 05 Oct 2022 18:51:35 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Wed, 05 Oct 2022 18:51:35 GMT
WORKDIR /usr/local/zs-init
# Wed, 05 Oct 2022 18:51:40 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Wed, 05 Oct 2022 18:51:40 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Wed, 05 Oct 2022 18:51:40 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Wed, 05 Oct 2022 18:51:41 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Wed, 05 Oct 2022 18:51:41 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Wed, 05 Oct 2022 18:51:41 GMT
EXPOSE 80
# Wed, 05 Oct 2022 18:51:41 GMT
EXPOSE 443
# Wed, 05 Oct 2022 18:51:41 GMT
EXPOSE 10081
# Wed, 05 Oct 2022 18:51:42 GMT
EXPOSE 10082
# Wed, 05 Oct 2022 18:51:42 GMT
WORKDIR /var/www/html
# Wed, 05 Oct 2022 18:51:42 GMT
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
	-	`sha256:16bf7e98edb272e094085a4cc9741a24836a13372ffaf09609d8a42c7187b14c`  
		Last Modified: Wed, 05 Oct 2022 18:54:03 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a256b25757efa67354e84f6cd81ebf5c2e0326e1c030cbea356e771fdbe62d7`  
		Last Modified: Wed, 05 Oct 2022 18:54:57 GMT  
		Size: 418.1 MB (418140661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de204ebe7f3215c7b27a46b02951b3e9e5e8703a2feb86fb9a14972a558a92f3`  
		Last Modified: Wed, 05 Oct 2022 18:54:03 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464377bd36e4e2392e667cf5b487aba2400b123536c2763c7e6654924cc2317f`  
		Last Modified: Wed, 05 Oct 2022 18:54:03 GMT  
		Size: 18.9 KB (18927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf28ed8e24ef4dd92fc2723cf40dedaaf75a70be13ad13d3be5c1eac9bc861f`  
		Last Modified: Wed, 05 Oct 2022 18:54:02 GMT  
		Size: 5.3 MB (5311600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f68a4ed00832bf680f7e2fe176ab209eba210357df6673909e9a77c7c29db48`  
		Last Modified: Wed, 05 Oct 2022 18:54:01 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20b6fb0e55a66422ca3a4dc33d0f57ff703c312f90daf36ef9ae72e65d78967`  
		Last Modified: Wed, 05 Oct 2022 18:54:01 GMT  
		Size: 2.6 KB (2560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15706cbe7efe2bb2b3e00124a0418db1739c1e97c3d6dcdae27f2202c12a642`  
		Last Modified: Wed, 05 Oct 2022 18:54:01 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578fd1123e5fe53192fdbb72f1fe61bdbe1bf0fd65b21614381be09ecd1af576`  
		Last Modified: Wed, 05 Oct 2022 18:54:01 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:2021.0`

```console
$ docker pull php-zendserver@sha256:755e956bdcc675148cb4c388e7f0a95ce239bd39f2ef01bdbe219a7ce07875db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:2021.0` - linux; amd64

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

## `php-zendserver:5.6`

```console
$ docker pull php-zendserver@sha256:46087476dd829477b235937b1b774e539c67177fb9c637bde91b28b2e6cf9299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:5393691a9d8617643c002a7ec19c90639a480868ae335ab538499d1a05865d4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315608578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513ed7b8cb626435a0c10f51c07b1631f83e70f06549e79357644c19c6d30670`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 04:02:14 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Tue, 31 Aug 2021 04:02:15 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Tue, 31 Aug 2021 04:02:15 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Tue, 31 Aug 2021 04:04:03 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Tue, 31 Aug 2021 04:04:06 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Tue, 31 Aug 2021 04:04:06 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Tue, 31 Aug 2021 04:04:07 GMT
RUN /usr/sbin/a2enmod headers
# Tue, 31 Aug 2021 04:04:07 GMT
ENV ZS_INIT_VERSION=0.3
# Tue, 31 Aug 2021 04:04:08 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Tue, 31 Aug 2021 04:04:09 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Tue, 31 Aug 2021 04:04:09 GMT
WORKDIR /usr/local/zs-init
# Tue, 31 Aug 2021 04:04:16 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Tue, 31 Aug 2021 04:04:16 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Tue, 31 Aug 2021 04:04:16 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Tue, 31 Aug 2021 04:04:17 GMT
RUN rm /var/www/html/index.html
# Tue, 31 Aug 2021 04:04:17 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Tue, 31 Aug 2021 04:04:17 GMT
EXPOSE 80
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 443
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 10081
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 10082
# Tue, 31 Aug 2021 04:04:18 GMT
WORKDIR /var/www/html
# Tue, 31 Aug 2021 04:04:18 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2102dd9376f61b14df18139d78a96caeb38426131bb6a85847a5733f84d83c32`  
		Last Modified: Tue, 31 Aug 2021 04:11:12 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae050479344fbb7ea0f86b97e8c772b7ae45103fa5cfc2bea2a4b79c631a1534`  
		Last Modified: Tue, 31 Aug 2021 04:11:11 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d990e63418cea6828a1754a0cfd88662fe780fa88dd2de23528d624ab6bc35`  
		Last Modified: Tue, 31 Aug 2021 04:11:11 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e78264dffd8afd8084e307db7cfd44f971f55d76534559ccd72b50b64108726`  
		Last Modified: Tue, 31 Aug 2021 04:11:40 GMT  
		Size: 263.9 MB (263910611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd783101a133a035071fca065237130e373e2f4cc4151957c9c461ae9a79cdf2`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19cbd07b1b667393092b9d2df1833f0b331cfe1eb5e6ad304f4acbda03136ab`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21aeee9b83798ca4fd42d7e5aa46ecd288c027160673f1be4f3d9d57b70a383`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7e05a640abfb3d3865705d1a482da844acc818d5c32089ee78ec8ba477136d`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be58af708ccc85c876f8148b3f7af699d37b1d23a25d76c1c8eaedd03b6dcc9b`  
		Last Modified: Tue, 31 Aug 2021 04:11:08 GMT  
		Size: 5.1 MB (5146536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1df10206b55b2eb8839919bb0d056e7256e1dd2bb398a492c5b8317235fe6d`  
		Last Modified: Tue, 31 Aug 2021 04:11:07 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d37b5f26f094cbc47c55b9abf4e3fe103e96208d7e102c579384ffe6add64`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 2.6 KB (2566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15716512d8f97648b13d29fdbc7df5b8f6ec04e2ca06aa9447b31525f08c1c2c`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72ae8545d8a1d76de6aadb8a94a839c2d60e2f164e0323e0ad4cc73a1853110`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5`

```console
$ docker pull php-zendserver@sha256:46087476dd829477b235937b1b774e539c67177fb9c637bde91b28b2e6cf9299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:8.5` - linux; amd64

```console
$ docker pull php-zendserver@sha256:5393691a9d8617643c002a7ec19c90639a480868ae335ab538499d1a05865d4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315608578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513ed7b8cb626435a0c10f51c07b1631f83e70f06549e79357644c19c6d30670`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 04:02:14 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Tue, 31 Aug 2021 04:02:15 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Tue, 31 Aug 2021 04:02:15 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Tue, 31 Aug 2021 04:04:03 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Tue, 31 Aug 2021 04:04:06 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Tue, 31 Aug 2021 04:04:06 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Tue, 31 Aug 2021 04:04:07 GMT
RUN /usr/sbin/a2enmod headers
# Tue, 31 Aug 2021 04:04:07 GMT
ENV ZS_INIT_VERSION=0.3
# Tue, 31 Aug 2021 04:04:08 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Tue, 31 Aug 2021 04:04:09 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Tue, 31 Aug 2021 04:04:09 GMT
WORKDIR /usr/local/zs-init
# Tue, 31 Aug 2021 04:04:16 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Tue, 31 Aug 2021 04:04:16 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Tue, 31 Aug 2021 04:04:16 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Tue, 31 Aug 2021 04:04:17 GMT
RUN rm /var/www/html/index.html
# Tue, 31 Aug 2021 04:04:17 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Tue, 31 Aug 2021 04:04:17 GMT
EXPOSE 80
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 443
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 10081
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 10082
# Tue, 31 Aug 2021 04:04:18 GMT
WORKDIR /var/www/html
# Tue, 31 Aug 2021 04:04:18 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2102dd9376f61b14df18139d78a96caeb38426131bb6a85847a5733f84d83c32`  
		Last Modified: Tue, 31 Aug 2021 04:11:12 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae050479344fbb7ea0f86b97e8c772b7ae45103fa5cfc2bea2a4b79c631a1534`  
		Last Modified: Tue, 31 Aug 2021 04:11:11 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d990e63418cea6828a1754a0cfd88662fe780fa88dd2de23528d624ab6bc35`  
		Last Modified: Tue, 31 Aug 2021 04:11:11 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e78264dffd8afd8084e307db7cfd44f971f55d76534559ccd72b50b64108726`  
		Last Modified: Tue, 31 Aug 2021 04:11:40 GMT  
		Size: 263.9 MB (263910611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd783101a133a035071fca065237130e373e2f4cc4151957c9c461ae9a79cdf2`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19cbd07b1b667393092b9d2df1833f0b331cfe1eb5e6ad304f4acbda03136ab`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21aeee9b83798ca4fd42d7e5aa46ecd288c027160673f1be4f3d9d57b70a383`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7e05a640abfb3d3865705d1a482da844acc818d5c32089ee78ec8ba477136d`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be58af708ccc85c876f8148b3f7af699d37b1d23a25d76c1c8eaedd03b6dcc9b`  
		Last Modified: Tue, 31 Aug 2021 04:11:08 GMT  
		Size: 5.1 MB (5146536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1df10206b55b2eb8839919bb0d056e7256e1dd2bb398a492c5b8317235fe6d`  
		Last Modified: Tue, 31 Aug 2021 04:11:07 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d37b5f26f094cbc47c55b9abf4e3fe103e96208d7e102c579384ffe6add64`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 2.6 KB (2566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15716512d8f97648b13d29fdbc7df5b8f6ec04e2ca06aa9447b31525f08c1c2c`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72ae8545d8a1d76de6aadb8a94a839c2d60e2f164e0323e0ad4cc73a1853110`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5-php5.6`

```console
$ docker pull php-zendserver@sha256:46087476dd829477b235937b1b774e539c67177fb9c637bde91b28b2e6cf9299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:8.5-php5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:5393691a9d8617643c002a7ec19c90639a480868ae335ab538499d1a05865d4d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315608578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513ed7b8cb626435a0c10f51c07b1631f83e70f06549e79357644c19c6d30670`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 04:02:14 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Tue, 31 Aug 2021 04:02:15 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Tue, 31 Aug 2021 04:02:15 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Tue, 31 Aug 2021 04:04:03 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Tue, 31 Aug 2021 04:04:06 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Tue, 31 Aug 2021 04:04:06 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Tue, 31 Aug 2021 04:04:07 GMT
RUN /usr/sbin/a2enmod headers
# Tue, 31 Aug 2021 04:04:07 GMT
ENV ZS_INIT_VERSION=0.3
# Tue, 31 Aug 2021 04:04:08 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Tue, 31 Aug 2021 04:04:09 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Tue, 31 Aug 2021 04:04:09 GMT
WORKDIR /usr/local/zs-init
# Tue, 31 Aug 2021 04:04:16 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Tue, 31 Aug 2021 04:04:16 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Tue, 31 Aug 2021 04:04:16 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Tue, 31 Aug 2021 04:04:17 GMT
RUN rm /var/www/html/index.html
# Tue, 31 Aug 2021 04:04:17 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Tue, 31 Aug 2021 04:04:17 GMT
EXPOSE 80
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 443
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 10081
# Tue, 31 Aug 2021 04:04:18 GMT
EXPOSE 10082
# Tue, 31 Aug 2021 04:04:18 GMT
WORKDIR /var/www/html
# Tue, 31 Aug 2021 04:04:18 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2102dd9376f61b14df18139d78a96caeb38426131bb6a85847a5733f84d83c32`  
		Last Modified: Tue, 31 Aug 2021 04:11:12 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae050479344fbb7ea0f86b97e8c772b7ae45103fa5cfc2bea2a4b79c631a1534`  
		Last Modified: Tue, 31 Aug 2021 04:11:11 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d990e63418cea6828a1754a0cfd88662fe780fa88dd2de23528d624ab6bc35`  
		Last Modified: Tue, 31 Aug 2021 04:11:11 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e78264dffd8afd8084e307db7cfd44f971f55d76534559ccd72b50b64108726`  
		Last Modified: Tue, 31 Aug 2021 04:11:40 GMT  
		Size: 263.9 MB (263910611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd783101a133a035071fca065237130e373e2f4cc4151957c9c461ae9a79cdf2`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19cbd07b1b667393092b9d2df1833f0b331cfe1eb5e6ad304f4acbda03136ab`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21aeee9b83798ca4fd42d7e5aa46ecd288c027160673f1be4f3d9d57b70a383`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7e05a640abfb3d3865705d1a482da844acc818d5c32089ee78ec8ba477136d`  
		Last Modified: Tue, 31 Aug 2021 04:11:09 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be58af708ccc85c876f8148b3f7af699d37b1d23a25d76c1c8eaedd03b6dcc9b`  
		Last Modified: Tue, 31 Aug 2021 04:11:08 GMT  
		Size: 5.1 MB (5146536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1df10206b55b2eb8839919bb0d056e7256e1dd2bb398a492c5b8317235fe6d`  
		Last Modified: Tue, 31 Aug 2021 04:11:07 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703d37b5f26f094cbc47c55b9abf4e3fe103e96208d7e102c579384ffe6add64`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 2.6 KB (2566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15716512d8f97648b13d29fdbc7df5b8f6ec04e2ca06aa9447b31525f08c1c2c`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72ae8545d8a1d76de6aadb8a94a839c2d60e2f164e0323e0ad4cc73a1853110`  
		Last Modified: Tue, 31 Aug 2021 04:11:06 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:9.1`

```console
$ docker pull php-zendserver@sha256:cc80372d5dcac564f69bb3c8c066a46638ee40115142f5247079084a5ddc1179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `php-zendserver:9.1` - linux; amd64

```console
$ docker pull php-zendserver@sha256:7b079ac3a11ceab944593ab3fbfbbac482a4d6611fa431c710e2bd0472c87888
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 MB (399260011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ac8051a5f543e6f729a4fc404e53a1f68ef6dc6c6443b992634a95664429c3`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 04:02:14 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Tue, 31 Aug 2021 04:04:22 GMT
COPY file:0d4830b5060fb75cec6a47b30d343d82f9c3d6f95f20c11635618b93dedb5720 in /etc/apt/sources.list.d/zend-server.list 
# Tue, 31 Aug 2021 04:05:46 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server-php-7.1=9.1.12+b211     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Tue, 31 Aug 2021 04:05:50 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Tue, 31 Aug 2021 04:05:51 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Tue, 31 Aug 2021 04:05:52 GMT
RUN /usr/sbin/a2enmod headers
# Tue, 31 Aug 2021 04:05:52 GMT
ENV ZS_INIT_VERSION=0.3
# Tue, 31 Aug 2021 04:05:52 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Tue, 31 Aug 2021 04:05:53 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Tue, 31 Aug 2021 04:05:53 GMT
WORKDIR /usr/local/zs-init
# Tue, 31 Aug 2021 04:06:00 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Tue, 31 Aug 2021 04:06:00 GMT
COPY dir:5966ca4828c37f68d48d11da814350a590451453f42aa83ef2eab6893db3e4cc in /usr/local/bin 
# Tue, 31 Aug 2021 04:06:01 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Tue, 31 Aug 2021 04:06:01 GMT
RUN rm /var/www/html/index.html
# Tue, 31 Aug 2021 04:06:02 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Tue, 31 Aug 2021 04:06:02 GMT
EXPOSE 80
# Tue, 31 Aug 2021 04:06:02 GMT
EXPOSE 443
# Tue, 31 Aug 2021 04:06:02 GMT
EXPOSE 10081
# Tue, 31 Aug 2021 04:06:02 GMT
EXPOSE 10082
# Tue, 31 Aug 2021 04:06:03 GMT
WORKDIR /var/www/html
# Tue, 31 Aug 2021 04:06:03 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2102dd9376f61b14df18139d78a96caeb38426131bb6a85847a5733f84d83c32`  
		Last Modified: Tue, 31 Aug 2021 04:11:12 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef9ee709ba9d99042fc4eae3385479692614cfd72cbc83c98522170944f9f1a`  
		Last Modified: Tue, 31 Aug 2021 04:12:01 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837980bcf5c021764e8ff0b5e1826fa0d23d4d4bbd2fe02962a470f7d8df8f11`  
		Last Modified: Tue, 31 Aug 2021 04:12:43 GMT  
		Size: 347.6 MB (347557251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f311d7aa89c09f28fce59942e782699474050c73dc60b2c0570f5eb2fe64c4fc`  
		Last Modified: Tue, 31 Aug 2021 04:11:59 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c9384096c8027661058200d5dd435498203ae6cea4ffada13ffcc34a17f730`  
		Last Modified: Tue, 31 Aug 2021 04:11:59 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a391773894550b0dcf95133d7a0ebfc325acd5a660c35f96c77133e3fd8f740c`  
		Last Modified: Tue, 31 Aug 2021 04:11:59 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99104e97158863a1815e4b564104f84c3c0671a3ef2a49ddf935cb20a41e537`  
		Last Modified: Tue, 31 Aug 2021 04:11:59 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc404237abddc7a47d1e606dc92470e0035dcd32745c3c0bf383528304c96d7`  
		Last Modified: Tue, 31 Aug 2021 04:11:58 GMT  
		Size: 5.2 MB (5150653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63099d2783ee41f72d28cc95ab35ba28c5674108eead4fba7719574ecddb2c99`  
		Last Modified: Tue, 31 Aug 2021 04:11:57 GMT  
		Size: 14.3 KB (14320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16df2874073685e8fadc4aa9c04fc75132336de6749145d708e7d664cc03a03f`  
		Last Modified: Tue, 31 Aug 2021 04:11:57 GMT  
		Size: 2.6 KB (2559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b978107de3a3767f2ffe65e620f34ce62d93b74cbd20b77b1821327e7458539b`  
		Last Modified: Tue, 31 Aug 2021 04:11:57 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3a81a9d2085d59971d4608251a552a6c9631466fcac109142e49c26602cf12`  
		Last Modified: Tue, 31 Aug 2021 04:11:57 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
