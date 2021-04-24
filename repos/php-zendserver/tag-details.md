<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `php-zendserver`

-	[`php-zendserver:2019.0`](#php-zendserver20190)
-	[`php-zendserver:5.6`](#php-zendserver56)
-	[`php-zendserver:8.5`](#php-zendserver85)
-	[`php-zendserver:8.5-php5.6`](#php-zendserver85-php56)
-	[`php-zendserver:9.1`](#php-zendserver91)
-	[`php-zendserver:latest`](#php-zendserverlatest)

## `php-zendserver:2019.0`

```console
$ docker pull php-zendserver@sha256:5258246ae923b2b6060f59c27b127b1b6f96553f2cd5278bc691adf6d3c64bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:2019.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:5a435c8a14b79ee96f0b7235a008ff32f047d8c98203375e1446264cb46f03e6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.1 MB (483084122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da6a16d27c5e80a8938034acbd4b2ef019307634347d9df88df01a1eb7aef99`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:22 GMT
ADD file:d7fa3c26651f9204a5629287a1a9a6e7dc6a0bc6eb499e82c433c0c8f67ff46b in / 
# Fri, 23 Apr 2021 22:21:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:25 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:50:46 GMT
RUN apt-get update && apt-get install -y       gnupg
# Sat, 24 Apr 2021 00:50:48 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Sat, 24 Apr 2021 00:50:48 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Sat, 24 Apr 2021 00:52:39 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.7+b403     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Sat, 24 Apr 2021 00:52:43 GMT
ENV ZS_INIT_VERSION=0.3
# Sat, 24 Apr 2021 00:52:43 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Sat, 24 Apr 2021 00:52:43 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Sat, 24 Apr 2021 00:52:45 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Sat, 24 Apr 2021 00:52:45 GMT
WORKDIR /usr/local/zs-init
# Sat, 24 Apr 2021 00:52:50 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Sat, 24 Apr 2021 00:52:51 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Sat, 24 Apr 2021 00:52:51 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Sat, 24 Apr 2021 00:52:52 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Sat, 24 Apr 2021 00:52:52 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Sat, 24 Apr 2021 00:52:52 GMT
EXPOSE 80
# Sat, 24 Apr 2021 00:52:52 GMT
EXPOSE 443
# Sat, 24 Apr 2021 00:52:52 GMT
EXPOSE 10081
# Sat, 24 Apr 2021 00:52:53 GMT
EXPOSE 10082
# Sat, 24 Apr 2021 00:52:53 GMT
WORKDIR /var/www/html
# Sat, 24 Apr 2021 00:52:53 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:01bf7da0a88c9e37ae418d17c0aeed0621524848d80ccb9e38c67e7ab8e11928`  
		Last Modified: Fri, 16 Apr 2021 15:20:23 GMT  
		Size: 26.7 MB (26697009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b4a5f15c7a0722b4f22e61b5387317eaf2602c27ffb2bceac9a25f19fbd156`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffbe87baa135002dddb7a7460082c5d6a352186e1be9464c5f31db81378824`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7d62791fa0a385b587b39ce627c6366d818915daa3fd5249efc8e65cf7e3b5`  
		Last Modified: Sat, 24 Apr 2021 00:55:12 GMT  
		Size: 32.6 MB (32593961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e4138be4e7d7cced4e8f685f761def5efd0d4fd34750c87251abaa5a0be60b`  
		Last Modified: Sat, 24 Apr 2021 00:55:07 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c7066bb89eb736421e8f21a68d8a6888d4e9c5515a0cf2a7d9271f0cc695c6`  
		Last Modified: Sat, 24 Apr 2021 00:55:10 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bb58657eb8cf2d906b5436ef1e81d32810cc256d7ab0bfe6f0c38016937522`  
		Last Modified: Sat, 24 Apr 2021 00:56:02 GMT  
		Size: 418.6 MB (418610599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f7f377e1ee8fcc30d19029a92cf8ac725c1c77ef0d4edd6126220c55b67bf7`  
		Last Modified: Sat, 24 Apr 2021 00:55:06 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7229f56582434810cc0172b1ab94d2245e94e4a52d2abe6f1e2d0632704480d6`  
		Last Modified: Sat, 24 Apr 2021 00:55:06 GMT  
		Size: 18.9 KB (18925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8977937b34ab1bc8b100cb3e9bf627fd8643caa99cd696c40fd497119b678038`  
		Last Modified: Sat, 24 Apr 2021 00:55:04 GMT  
		Size: 5.1 MB (5142214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b151256662c87c6de6737172bc324d14aa6e16d552342d09ab701bf142c75b35`  
		Last Modified: Sat, 24 Apr 2021 00:55:03 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2490224bdef5c1b50e34af13f7e5d4565469bfd931802c28556275a27a75dd5a`  
		Last Modified: Sat, 24 Apr 2021 00:55:03 GMT  
		Size: 2.6 KB (2562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b212d9f1e8e907221b8613e69e432ec3ba93b298e73eb2f3835f5ee73f795a27`  
		Last Modified: Sat, 24 Apr 2021 00:55:03 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fc99bf9249536417dd1141f6bf5a6e98d8801f2baf87c0aa32a9888c84e338`  
		Last Modified: Sat, 24 Apr 2021 00:55:03 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:5.6`

```console
$ docker pull php-zendserver@sha256:8d2b2a4ddfcf5887fd41d9c039e9a08f3d763a4b342338cf0eb5a96c567f3d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:6de9a293f840fc940d520176bf76b549880aa7712f6cac11205fc9b833342ad5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315354644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce845f8093ca05f7e8a4e93213d3645701da7b6c36940ebb3a9800ca1bae94e9`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:45:18 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Sat, 24 Apr 2021 00:45:18 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Sat, 24 Apr 2021 00:45:19 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Sat, 24 Apr 2021 00:47:25 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Sat, 24 Apr 2021 00:47:28 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Sat, 24 Apr 2021 00:47:29 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Sat, 24 Apr 2021 00:47:30 GMT
RUN /usr/sbin/a2enmod headers
# Sat, 24 Apr 2021 00:47:30 GMT
ENV ZS_INIT_VERSION=0.3
# Sat, 24 Apr 2021 00:47:30 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Sat, 24 Apr 2021 00:47:32 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Sat, 24 Apr 2021 00:47:32 GMT
WORKDIR /usr/local/zs-init
# Sat, 24 Apr 2021 00:47:39 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Sat, 24 Apr 2021 00:47:39 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Sat, 24 Apr 2021 00:47:39 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Sat, 24 Apr 2021 00:47:40 GMT
RUN rm /var/www/html/index.html
# Sat, 24 Apr 2021 00:47:40 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Sat, 24 Apr 2021 00:47:40 GMT
EXPOSE 80
# Sat, 24 Apr 2021 00:47:41 GMT
EXPOSE 443
# Sat, 24 Apr 2021 00:47:41 GMT
EXPOSE 10081
# Sat, 24 Apr 2021 00:47:41 GMT
EXPOSE 10082
# Sat, 24 Apr 2021 00:47:41 GMT
WORKDIR /var/www/html
# Sat, 24 Apr 2021 00:47:41 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85961e1e4626d4dc2f230ffbaff5d9c22a41e63ec5e52578bea50e1bdaccd64f`  
		Last Modified: Sat, 24 Apr 2021 00:53:22 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184ae4c042f7e81d0546987ef5a70ba5694f799a8be7d73b1b8a54ad29d977db`  
		Last Modified: Sat, 24 Apr 2021 00:53:21 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2492da4a62443c131490a846b432d277438a6260526660977e08f4118f3cca2b`  
		Last Modified: Sat, 24 Apr 2021 00:53:20 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00e56fcc6c444536ed7df3121f37764f4e9498f514bde8d6c1fc600056b78ce`  
		Last Modified: Sat, 24 Apr 2021 00:53:51 GMT  
		Size: 263.9 MB (263908294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc206385ca40709ab508b2900a6a40816aeb9ac879d713fb0e49cdd4c9e6144`  
		Last Modified: Sat, 24 Apr 2021 00:53:18 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c2177f7da66985036beb835fc1c24a0c4f3b6c7797670f0c5fcf35eb18c9b4`  
		Last Modified: Sat, 24 Apr 2021 00:53:19 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6348c1d8e15a136a4253616a46f52a35223830e1e645fe1fc3d93d4c205d6419`  
		Last Modified: Sat, 24 Apr 2021 00:53:17 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d38962ee9685d03df9dc0afb1722b41412f462e66e6bcc61b9fa09afef09239`  
		Last Modified: Sat, 24 Apr 2021 00:53:19 GMT  
		Size: 18.9 KB (18860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3777d12003a64087c8b755e62680da6396b3b060a312b7c5610063ec571a3473`  
		Last Modified: Sat, 24 Apr 2021 00:53:16 GMT  
		Size: 5.1 MB (5138029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8537b6a47df5b10377b5316e57f0e824ba52620ffb81f6e3b0fded7e1113f2ef`  
		Last Modified: Sat, 24 Apr 2021 00:53:15 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09ec708afb32e9ec1ab67be08eabaeb3ceb77f54acb615bc9931aaccf463bac`  
		Last Modified: Sat, 24 Apr 2021 00:53:15 GMT  
		Size: 2.6 KB (2566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb4b38b2a349eb1b99b8cfd190c671e140be5fddbe99f980f36d42880c3216a`  
		Last Modified: Sat, 24 Apr 2021 00:53:15 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed786a0ae090814f5a8e4f7fe09ccb946607225523bf7109e4a73015c0cd13ee`  
		Last Modified: Sat, 24 Apr 2021 00:53:15 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5`

```console
$ docker pull php-zendserver@sha256:8d2b2a4ddfcf5887fd41d9c039e9a08f3d763a4b342338cf0eb5a96c567f3d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5` - linux; amd64

```console
$ docker pull php-zendserver@sha256:6de9a293f840fc940d520176bf76b549880aa7712f6cac11205fc9b833342ad5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315354644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce845f8093ca05f7e8a4e93213d3645701da7b6c36940ebb3a9800ca1bae94e9`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:45:18 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Sat, 24 Apr 2021 00:45:18 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Sat, 24 Apr 2021 00:45:19 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Sat, 24 Apr 2021 00:47:25 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Sat, 24 Apr 2021 00:47:28 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Sat, 24 Apr 2021 00:47:29 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Sat, 24 Apr 2021 00:47:30 GMT
RUN /usr/sbin/a2enmod headers
# Sat, 24 Apr 2021 00:47:30 GMT
ENV ZS_INIT_VERSION=0.3
# Sat, 24 Apr 2021 00:47:30 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Sat, 24 Apr 2021 00:47:32 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Sat, 24 Apr 2021 00:47:32 GMT
WORKDIR /usr/local/zs-init
# Sat, 24 Apr 2021 00:47:39 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Sat, 24 Apr 2021 00:47:39 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Sat, 24 Apr 2021 00:47:39 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Sat, 24 Apr 2021 00:47:40 GMT
RUN rm /var/www/html/index.html
# Sat, 24 Apr 2021 00:47:40 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Sat, 24 Apr 2021 00:47:40 GMT
EXPOSE 80
# Sat, 24 Apr 2021 00:47:41 GMT
EXPOSE 443
# Sat, 24 Apr 2021 00:47:41 GMT
EXPOSE 10081
# Sat, 24 Apr 2021 00:47:41 GMT
EXPOSE 10082
# Sat, 24 Apr 2021 00:47:41 GMT
WORKDIR /var/www/html
# Sat, 24 Apr 2021 00:47:41 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85961e1e4626d4dc2f230ffbaff5d9c22a41e63ec5e52578bea50e1bdaccd64f`  
		Last Modified: Sat, 24 Apr 2021 00:53:22 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184ae4c042f7e81d0546987ef5a70ba5694f799a8be7d73b1b8a54ad29d977db`  
		Last Modified: Sat, 24 Apr 2021 00:53:21 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2492da4a62443c131490a846b432d277438a6260526660977e08f4118f3cca2b`  
		Last Modified: Sat, 24 Apr 2021 00:53:20 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00e56fcc6c444536ed7df3121f37764f4e9498f514bde8d6c1fc600056b78ce`  
		Last Modified: Sat, 24 Apr 2021 00:53:51 GMT  
		Size: 263.9 MB (263908294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc206385ca40709ab508b2900a6a40816aeb9ac879d713fb0e49cdd4c9e6144`  
		Last Modified: Sat, 24 Apr 2021 00:53:18 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c2177f7da66985036beb835fc1c24a0c4f3b6c7797670f0c5fcf35eb18c9b4`  
		Last Modified: Sat, 24 Apr 2021 00:53:19 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6348c1d8e15a136a4253616a46f52a35223830e1e645fe1fc3d93d4c205d6419`  
		Last Modified: Sat, 24 Apr 2021 00:53:17 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d38962ee9685d03df9dc0afb1722b41412f462e66e6bcc61b9fa09afef09239`  
		Last Modified: Sat, 24 Apr 2021 00:53:19 GMT  
		Size: 18.9 KB (18860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3777d12003a64087c8b755e62680da6396b3b060a312b7c5610063ec571a3473`  
		Last Modified: Sat, 24 Apr 2021 00:53:16 GMT  
		Size: 5.1 MB (5138029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8537b6a47df5b10377b5316e57f0e824ba52620ffb81f6e3b0fded7e1113f2ef`  
		Last Modified: Sat, 24 Apr 2021 00:53:15 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09ec708afb32e9ec1ab67be08eabaeb3ceb77f54acb615bc9931aaccf463bac`  
		Last Modified: Sat, 24 Apr 2021 00:53:15 GMT  
		Size: 2.6 KB (2566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb4b38b2a349eb1b99b8cfd190c671e140be5fddbe99f980f36d42880c3216a`  
		Last Modified: Sat, 24 Apr 2021 00:53:15 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed786a0ae090814f5a8e4f7fe09ccb946607225523bf7109e4a73015c0cd13ee`  
		Last Modified: Sat, 24 Apr 2021 00:53:15 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5-php5.6`

```console
$ docker pull php-zendserver@sha256:8d2b2a4ddfcf5887fd41d9c039e9a08f3d763a4b342338cf0eb5a96c567f3d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5-php5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:6de9a293f840fc940d520176bf76b549880aa7712f6cac11205fc9b833342ad5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315354644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce845f8093ca05f7e8a4e93213d3645701da7b6c36940ebb3a9800ca1bae94e9`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:45:18 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Sat, 24 Apr 2021 00:45:18 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Sat, 24 Apr 2021 00:45:19 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Sat, 24 Apr 2021 00:47:25 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Sat, 24 Apr 2021 00:47:28 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Sat, 24 Apr 2021 00:47:29 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Sat, 24 Apr 2021 00:47:30 GMT
RUN /usr/sbin/a2enmod headers
# Sat, 24 Apr 2021 00:47:30 GMT
ENV ZS_INIT_VERSION=0.3
# Sat, 24 Apr 2021 00:47:30 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Sat, 24 Apr 2021 00:47:32 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Sat, 24 Apr 2021 00:47:32 GMT
WORKDIR /usr/local/zs-init
# Sat, 24 Apr 2021 00:47:39 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Sat, 24 Apr 2021 00:47:39 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Sat, 24 Apr 2021 00:47:39 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Sat, 24 Apr 2021 00:47:40 GMT
RUN rm /var/www/html/index.html
# Sat, 24 Apr 2021 00:47:40 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Sat, 24 Apr 2021 00:47:40 GMT
EXPOSE 80
# Sat, 24 Apr 2021 00:47:41 GMT
EXPOSE 443
# Sat, 24 Apr 2021 00:47:41 GMT
EXPOSE 10081
# Sat, 24 Apr 2021 00:47:41 GMT
EXPOSE 10082
# Sat, 24 Apr 2021 00:47:41 GMT
WORKDIR /var/www/html
# Sat, 24 Apr 2021 00:47:41 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85961e1e4626d4dc2f230ffbaff5d9c22a41e63ec5e52578bea50e1bdaccd64f`  
		Last Modified: Sat, 24 Apr 2021 00:53:22 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184ae4c042f7e81d0546987ef5a70ba5694f799a8be7d73b1b8a54ad29d977db`  
		Last Modified: Sat, 24 Apr 2021 00:53:21 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2492da4a62443c131490a846b432d277438a6260526660977e08f4118f3cca2b`  
		Last Modified: Sat, 24 Apr 2021 00:53:20 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00e56fcc6c444536ed7df3121f37764f4e9498f514bde8d6c1fc600056b78ce`  
		Last Modified: Sat, 24 Apr 2021 00:53:51 GMT  
		Size: 263.9 MB (263908294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc206385ca40709ab508b2900a6a40816aeb9ac879d713fb0e49cdd4c9e6144`  
		Last Modified: Sat, 24 Apr 2021 00:53:18 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c2177f7da66985036beb835fc1c24a0c4f3b6c7797670f0c5fcf35eb18c9b4`  
		Last Modified: Sat, 24 Apr 2021 00:53:19 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6348c1d8e15a136a4253616a46f52a35223830e1e645fe1fc3d93d4c205d6419`  
		Last Modified: Sat, 24 Apr 2021 00:53:17 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d38962ee9685d03df9dc0afb1722b41412f462e66e6bcc61b9fa09afef09239`  
		Last Modified: Sat, 24 Apr 2021 00:53:19 GMT  
		Size: 18.9 KB (18860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3777d12003a64087c8b755e62680da6396b3b060a312b7c5610063ec571a3473`  
		Last Modified: Sat, 24 Apr 2021 00:53:16 GMT  
		Size: 5.1 MB (5138029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8537b6a47df5b10377b5316e57f0e824ba52620ffb81f6e3b0fded7e1113f2ef`  
		Last Modified: Sat, 24 Apr 2021 00:53:15 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09ec708afb32e9ec1ab67be08eabaeb3ceb77f54acb615bc9931aaccf463bac`  
		Last Modified: Sat, 24 Apr 2021 00:53:15 GMT  
		Size: 2.6 KB (2566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb4b38b2a349eb1b99b8cfd190c671e140be5fddbe99f980f36d42880c3216a`  
		Last Modified: Sat, 24 Apr 2021 00:53:15 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed786a0ae090814f5a8e4f7fe09ccb946607225523bf7109e4a73015c0cd13ee`  
		Last Modified: Sat, 24 Apr 2021 00:53:15 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:9.1`

```console
$ docker pull php-zendserver@sha256:637c4fafd5de1abd44d3733dc51b7ba56c9fc313ae23ef082790d49767eb1639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:9.1` - linux; amd64

```console
$ docker pull php-zendserver@sha256:d8fdc72f90bc71bd228c805e22bae53268f2b9fb54aaeca9b3130d42ce18725b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.6 MB (395604800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff08da924c7517015bfc78087378da1f7a1d891d38b7bcb0af4f58e4cb7635f6`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:45:18 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Sat, 24 Apr 2021 00:47:58 GMT
COPY file:0d4830b5060fb75cec6a47b30d343d82f9c3d6f95f20c11635618b93dedb5720 in /etc/apt/sources.list.d/zend-server.list 
# Sat, 24 Apr 2021 00:50:16 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server-php-7.1=9.1.12+b211     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Sat, 24 Apr 2021 00:50:20 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Sat, 24 Apr 2021 00:50:21 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Sat, 24 Apr 2021 00:50:22 GMT
RUN /usr/sbin/a2enmod headers
# Sat, 24 Apr 2021 00:50:22 GMT
ENV ZS_INIT_VERSION=0.3
# Sat, 24 Apr 2021 00:50:22 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Sat, 24 Apr 2021 00:50:23 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Sat, 24 Apr 2021 00:50:23 GMT
WORKDIR /usr/local/zs-init
# Sat, 24 Apr 2021 00:50:30 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Sat, 24 Apr 2021 00:50:31 GMT
COPY dir:5966ca4828c37f68d48d11da814350a590451453f42aa83ef2eab6893db3e4cc in /usr/local/bin 
# Sat, 24 Apr 2021 00:50:31 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Sat, 24 Apr 2021 00:50:32 GMT
RUN rm /var/www/html/index.html
# Sat, 24 Apr 2021 00:50:32 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Sat, 24 Apr 2021 00:50:32 GMT
EXPOSE 80
# Sat, 24 Apr 2021 00:50:32 GMT
EXPOSE 443
# Sat, 24 Apr 2021 00:50:33 GMT
EXPOSE 10081
# Sat, 24 Apr 2021 00:50:33 GMT
EXPOSE 10082
# Sat, 24 Apr 2021 00:50:33 GMT
WORKDIR /var/www/html
# Sat, 24 Apr 2021 00:50:33 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85961e1e4626d4dc2f230ffbaff5d9c22a41e63ec5e52578bea50e1bdaccd64f`  
		Last Modified: Sat, 24 Apr 2021 00:53:22 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c5f983abd39d60b71653f50f78789e163b0aaaaf132a65e907dc168b79b50c`  
		Last Modified: Sat, 24 Apr 2021 00:54:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d0a24fc7b502f1d524b2540d335566f1f95b8e1aebb31ba6c2cd1e25c19c67`  
		Last Modified: Sat, 24 Apr 2021 00:54:53 GMT  
		Size: 344.2 MB (344153583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfe388ea3cfefb4baaa8205463566efbe25f07e06dc5dbba4b0fc350fbfc43f`  
		Last Modified: Sat, 24 Apr 2021 00:54:10 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9b048cb767e1630880f205b39ed61dea078f341b1c344113fdb781c5f6cb46`  
		Last Modified: Sat, 24 Apr 2021 00:54:10 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829da72e0f475219824431f5fd942daf925f31907bd7360475b11bd475d19a62`  
		Last Modified: Sat, 24 Apr 2021 00:54:10 GMT  
		Size: 307.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eac5271499ba1e84683b97438f618f19fa0c0ab02dfe5050409031c205f63fd`  
		Last Modified: Sat, 24 Apr 2021 00:54:10 GMT  
		Size: 18.9 KB (18859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0432ecc6ebd04529cc8a3a7ecc95d6d12f29fed65d59ac730534965c6f001e6`  
		Last Modified: Sat, 24 Apr 2021 00:54:08 GMT  
		Size: 5.1 MB (5142224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c811d037aeb31b85fcc98bef935ae2d167c5e1076b6c48161acafee25c3df0ff`  
		Last Modified: Sat, 24 Apr 2021 00:54:07 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718efe9ebce8fe327c1a5f954c797dabd429092c1261695d31aeea4c51a82348`  
		Last Modified: Sat, 24 Apr 2021 00:54:07 GMT  
		Size: 2.6 KB (2560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f51c3cade4887f996c93faace5307e0af4bb4a01aedc064ee2420fe4b6342d9`  
		Last Modified: Sat, 24 Apr 2021 00:54:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee500a970942a6a152333ad3f08fabf44c8cd9e004989f57dd2a61302753bad6`  
		Last Modified: Sat, 24 Apr 2021 00:54:07 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:5258246ae923b2b6060f59c27b127b1b6f96553f2cd5278bc691adf6d3c64bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:5a435c8a14b79ee96f0b7235a008ff32f047d8c98203375e1446264cb46f03e6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.1 MB (483084122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da6a16d27c5e80a8938034acbd4b2ef019307634347d9df88df01a1eb7aef99`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:22 GMT
ADD file:d7fa3c26651f9204a5629287a1a9a6e7dc6a0bc6eb499e82c433c0c8f67ff46b in / 
# Fri, 23 Apr 2021 22:21:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:25 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:50:46 GMT
RUN apt-get update && apt-get install -y       gnupg
# Sat, 24 Apr 2021 00:50:48 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Sat, 24 Apr 2021 00:50:48 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Sat, 24 Apr 2021 00:52:39 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.7+b403     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Sat, 24 Apr 2021 00:52:43 GMT
ENV ZS_INIT_VERSION=0.3
# Sat, 24 Apr 2021 00:52:43 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Sat, 24 Apr 2021 00:52:43 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Sat, 24 Apr 2021 00:52:45 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Sat, 24 Apr 2021 00:52:45 GMT
WORKDIR /usr/local/zs-init
# Sat, 24 Apr 2021 00:52:50 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Sat, 24 Apr 2021 00:52:51 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Sat, 24 Apr 2021 00:52:51 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Sat, 24 Apr 2021 00:52:52 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Sat, 24 Apr 2021 00:52:52 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Sat, 24 Apr 2021 00:52:52 GMT
EXPOSE 80
# Sat, 24 Apr 2021 00:52:52 GMT
EXPOSE 443
# Sat, 24 Apr 2021 00:52:52 GMT
EXPOSE 10081
# Sat, 24 Apr 2021 00:52:53 GMT
EXPOSE 10082
# Sat, 24 Apr 2021 00:52:53 GMT
WORKDIR /var/www/html
# Sat, 24 Apr 2021 00:52:53 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:01bf7da0a88c9e37ae418d17c0aeed0621524848d80ccb9e38c67e7ab8e11928`  
		Last Modified: Fri, 16 Apr 2021 15:20:23 GMT  
		Size: 26.7 MB (26697009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b4a5f15c7a0722b4f22e61b5387317eaf2602c27ffb2bceac9a25f19fbd156`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffbe87baa135002dddb7a7460082c5d6a352186e1be9464c5f31db81378824`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7d62791fa0a385b587b39ce627c6366d818915daa3fd5249efc8e65cf7e3b5`  
		Last Modified: Sat, 24 Apr 2021 00:55:12 GMT  
		Size: 32.6 MB (32593961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e4138be4e7d7cced4e8f685f761def5efd0d4fd34750c87251abaa5a0be60b`  
		Last Modified: Sat, 24 Apr 2021 00:55:07 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c7066bb89eb736421e8f21a68d8a6888d4e9c5515a0cf2a7d9271f0cc695c6`  
		Last Modified: Sat, 24 Apr 2021 00:55:10 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bb58657eb8cf2d906b5436ef1e81d32810cc256d7ab0bfe6f0c38016937522`  
		Last Modified: Sat, 24 Apr 2021 00:56:02 GMT  
		Size: 418.6 MB (418610599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f7f377e1ee8fcc30d19029a92cf8ac725c1c77ef0d4edd6126220c55b67bf7`  
		Last Modified: Sat, 24 Apr 2021 00:55:06 GMT  
		Size: 446.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7229f56582434810cc0172b1ab94d2245e94e4a52d2abe6f1e2d0632704480d6`  
		Last Modified: Sat, 24 Apr 2021 00:55:06 GMT  
		Size: 18.9 KB (18925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8977937b34ab1bc8b100cb3e9bf627fd8643caa99cd696c40fd497119b678038`  
		Last Modified: Sat, 24 Apr 2021 00:55:04 GMT  
		Size: 5.1 MB (5142214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b151256662c87c6de6737172bc324d14aa6e16d552342d09ab701bf142c75b35`  
		Last Modified: Sat, 24 Apr 2021 00:55:03 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2490224bdef5c1b50e34af13f7e5d4565469bfd931802c28556275a27a75dd5a`  
		Last Modified: Sat, 24 Apr 2021 00:55:03 GMT  
		Size: 2.6 KB (2562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b212d9f1e8e907221b8613e69e432ec3ba93b298e73eb2f3835f5ee73f795a27`  
		Last Modified: Sat, 24 Apr 2021 00:55:03 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fc99bf9249536417dd1141f6bf5a6e98d8801f2baf87c0aa32a9888c84e338`  
		Last Modified: Sat, 24 Apr 2021 00:55:03 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
