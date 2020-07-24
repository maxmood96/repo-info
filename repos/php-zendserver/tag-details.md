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
$ docker pull php-zendserver@sha256:6a384e05db2d751cab3fd2be5deda8f2a4213e9a1186606e49958bbae66a4ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:2019.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:04c0526c639254e6e214c0729302c3f81fe8cb3c7eb311e1c02e734c813c4884
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.3 MB (492331882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49771660717527f62e7fce9e5e62ea67d6ff93f965bdb4a54db781d79935598c`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:36:17 GMT
RUN apt-get update && apt-get install -y       gnupg
# Fri, 24 Jul 2020 16:36:18 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 24 Jul 2020 16:36:18 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 24 Jul 2020 16:38:02 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.4+b392     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 24 Jul 2020 16:38:02 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 24 Jul 2020 16:38:02 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 24 Jul 2020 16:38:03 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Fri, 24 Jul 2020 16:38:03 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Fri, 24 Jul 2020 16:38:04 GMT
WORKDIR /usr/local/zs-init
# Fri, 24 Jul 2020 16:38:12 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Fri, 24 Jul 2020 16:38:12 GMT
COPY dir:7937a6223a1e7805720eca1fbf8c2ccd37938f8f8aa175ae003d409459d49380 in /usr/local/bin 
# Fri, 24 Jul 2020 16:38:12 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 24 Jul 2020 16:38:13 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Fri, 24 Jul 2020 16:38:13 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 24 Jul 2020 16:38:14 GMT
EXPOSE 80
# Fri, 24 Jul 2020 16:38:14 GMT
EXPOSE 443
# Fri, 24 Jul 2020 16:38:14 GMT
EXPOSE 10081
# Fri, 24 Jul 2020 16:38:14 GMT
EXPOSE 10082
# Fri, 24 Jul 2020 16:38:14 GMT
WORKDIR /var/www/html
# Fri, 24 Jul 2020 16:38:14 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e8bd0044bba53b957398126fd92cf0f60a5eb2668783884c1ece2a31f4fc46`  
		Last Modified: Fri, 24 Jul 2020 16:40:29 GMT  
		Size: 28.2 MB (28166831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620517cf9e126051cdd98208134f893446b23dcd79debf3a78c4dd30ecac159f`  
		Last Modified: Fri, 24 Jul 2020 16:40:25 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d01b62b7af11403eeeb9de0c191228214c182242d713914b2d6e7241d29c512`  
		Last Modified: Fri, 24 Jul 2020 16:40:25 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b715824e1c3f7f4472ba80b696fd43ad175265fb5ca1057f64581ac7fc560ee`  
		Last Modified: Fri, 24 Jul 2020 16:41:27 GMT  
		Size: 417.6 MB (417569103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2936f13a221de6a10aaa96c4a17d365f1db96580b5da9f8d83311cf010ceb646`  
		Last Modified: Fri, 24 Jul 2020 16:40:24 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88603cba5cc964d47dbe77ab0ceabbad028f9ce116cdc43ab993f9d3f9751c15`  
		Last Modified: Fri, 24 Jul 2020 16:40:24 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb808167bec8dc558fa7338ae27b1bbfbd018ee8cab15671abc5113dae73308`  
		Last Modified: Fri, 24 Jul 2020 16:40:27 GMT  
		Size: 19.8 MB (19823259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794a944b7e73810295c8c5bd497ceb77bc5dec0176b2ce1495dff3c0da53f2c0`  
		Last Modified: Fri, 24 Jul 2020 16:40:23 GMT  
		Size: 14.3 KB (14255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f098431e37eca64534dfdf3eee74a93796ebc79f0b648538cb76906fbf812ef8`  
		Last Modified: Fri, 24 Jul 2020 16:40:23 GMT  
		Size: 2.5 KB (2530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab295e921ddffdf496b080a9dd83b55c02ebe00e30f293cfdb51af66408fd9f`  
		Last Modified: Fri, 24 Jul 2020 16:40:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd08bd0e69bae973715f91c30b3715fc91cf2fde2f3e5df6b68a14343158a076`  
		Last Modified: Fri, 24 Jul 2020 16:40:23 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:5.6`

```console
$ docker pull php-zendserver@sha256:285707664d621644902102d46c121ead9b93871a1fb5af1e537408e842baed5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:1b8c3b6ddfae8465074a137bedc6d3cee7ffb3efe578548a0db3ced5a30821fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.1 MB (328140810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7855506b68fafd3081b7d2e53bfbd364661cd305c3a344b3226392cd1227723c`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 24 Jul 2020 14:39:06 GMT
ADD file:513ae777bc4042f8446c0454f8cffc9a94f8429de963651d9a6dab95d4502007 in / 
# Fri, 24 Jul 2020 14:39:07 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:39:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:39:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:39:08 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:31:48 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 24 Jul 2020 16:31:49 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 24 Jul 2020 16:31:49 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Fri, 24 Jul 2020 16:33:38 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 24 Jul 2020 16:33:39 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Fri, 24 Jul 2020 16:33:39 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Fri, 24 Jul 2020 16:33:40 GMT
RUN /usr/sbin/a2enmod headers
# Fri, 24 Jul 2020 16:33:40 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 24 Jul 2020 16:33:41 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 24 Jul 2020 16:33:41 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Fri, 24 Jul 2020 16:33:42 GMT
WORKDIR /usr/local/zs-init
# Fri, 24 Jul 2020 16:33:55 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Fri, 24 Jul 2020 16:33:56 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Fri, 24 Jul 2020 16:33:56 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 24 Jul 2020 16:33:57 GMT
RUN rm /var/www/html/index.html
# Fri, 24 Jul 2020 16:33:57 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 24 Jul 2020 16:33:57 GMT
EXPOSE 80
# Fri, 24 Jul 2020 16:33:57 GMT
EXPOSE 443
# Fri, 24 Jul 2020 16:33:57 GMT
EXPOSE 10081
# Fri, 24 Jul 2020 16:33:58 GMT
EXPOSE 10082
# Fri, 24 Jul 2020 16:33:58 GMT
WORKDIR /var/www/html
# Fri, 24 Jul 2020 16:33:58 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:7b378fa0f9085667ced1c76c9919cde8663becf2218e8d20e2df8d0824311531`  
		Last Modified: Tue, 07 Jul 2020 13:19:56 GMT  
		Size: 44.4 MB (44401021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d77b1b29f2e9b6f141b9d8f74b601f40eb998544783f4a0a3cdc384873c1a4e`  
		Last Modified: Fri, 24 Jul 2020 14:39:50 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c793be88baee3f3204444e4d4e49c4e44c1709d40182c131cd5681c94e17227`  
		Last Modified: Fri, 24 Jul 2020 14:39:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc05c8a19c0cf83f2f44263c967c3fe81fffc4b41b592ad088fb1534c206e70`  
		Last Modified: Fri, 24 Jul 2020 14:39:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748f9d7b4e3266b22bb306c205cb89f601fdd6b96e70651f786712c9409aacea`  
		Last Modified: Fri, 24 Jul 2020 16:38:33 GMT  
		Size: 14.7 KB (14703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556df6871dacfa73d17bdf6b436a65961234bd062c447f24310e57ef35d19ad4`  
		Last Modified: Fri, 24 Jul 2020 16:38:33 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd9a86a42a9061da28825dccd0fde75a4895e3f43928ee40eb02cd95f7fd2c5`  
		Last Modified: Fri, 24 Jul 2020 16:38:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac0fc122a919b8fb975a8585123a0ecacf5ddde90939e6c7947d2fb64384b89`  
		Last Modified: Fri, 24 Jul 2020 16:39:19 GMT  
		Size: 263.9 MB (263866105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a065508f106c264bbd3658a020e2882e4731af4e85732234af242d4df43c8efd`  
		Last Modified: Fri, 24 Jul 2020 16:38:32 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303a15eaec7c361c9965cd59cc3a6cfdaff5615d7baf3e7572c3e7d1026b8a8f`  
		Last Modified: Fri, 24 Jul 2020 16:38:32 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb14a7a9d1a97cb4524bd531d626ca1ab7f20c19a25a788f347d48848bf4bcca`  
		Last Modified: Fri, 24 Jul 2020 16:38:31 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762af8b4380e3217f6c49f0b21e643a050540ea64bc195fa1fb907fb7c6c1b39`  
		Last Modified: Fri, 24 Jul 2020 16:38:30 GMT  
		Size: 18.8 KB (18827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb3c2a105068d08dd6835b8696cdaf0b6d68d1cbafd2709f744947dc3e52907`  
		Last Modified: Fri, 24 Jul 2020 16:38:36 GMT  
		Size: 19.8 MB (19819899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e43f14cc2f45ccaf064571f3ef5bd682db7d26a36c1ccd3dfe785a3d804cd4`  
		Last Modified: Fri, 24 Jul 2020 16:38:28 GMT  
		Size: 13.4 KB (13355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57911b14af53e3a36438d53cbe41c72f025f01060bf529acea43b044efb99d3b`  
		Last Modified: Fri, 24 Jul 2020 16:38:28 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce8bdd23ab08af121417c92421b0f901255ea4dde9486b0a8dbad10a19ff956`  
		Last Modified: Fri, 24 Jul 2020 16:38:29 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c02264a3e40951a31d746dba3bd356e03c6cd41ee3346baa302556c8278191`  
		Last Modified: Fri, 24 Jul 2020 16:38:28 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5`

```console
$ docker pull php-zendserver@sha256:285707664d621644902102d46c121ead9b93871a1fb5af1e537408e842baed5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5` - linux; amd64

```console
$ docker pull php-zendserver@sha256:1b8c3b6ddfae8465074a137bedc6d3cee7ffb3efe578548a0db3ced5a30821fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.1 MB (328140810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7855506b68fafd3081b7d2e53bfbd364661cd305c3a344b3226392cd1227723c`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 24 Jul 2020 14:39:06 GMT
ADD file:513ae777bc4042f8446c0454f8cffc9a94f8429de963651d9a6dab95d4502007 in / 
# Fri, 24 Jul 2020 14:39:07 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:39:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:39:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:39:08 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:31:48 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 24 Jul 2020 16:31:49 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 24 Jul 2020 16:31:49 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Fri, 24 Jul 2020 16:33:38 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 24 Jul 2020 16:33:39 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Fri, 24 Jul 2020 16:33:39 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Fri, 24 Jul 2020 16:33:40 GMT
RUN /usr/sbin/a2enmod headers
# Fri, 24 Jul 2020 16:33:40 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 24 Jul 2020 16:33:41 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 24 Jul 2020 16:33:41 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Fri, 24 Jul 2020 16:33:42 GMT
WORKDIR /usr/local/zs-init
# Fri, 24 Jul 2020 16:33:55 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Fri, 24 Jul 2020 16:33:56 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Fri, 24 Jul 2020 16:33:56 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 24 Jul 2020 16:33:57 GMT
RUN rm /var/www/html/index.html
# Fri, 24 Jul 2020 16:33:57 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 24 Jul 2020 16:33:57 GMT
EXPOSE 80
# Fri, 24 Jul 2020 16:33:57 GMT
EXPOSE 443
# Fri, 24 Jul 2020 16:33:57 GMT
EXPOSE 10081
# Fri, 24 Jul 2020 16:33:58 GMT
EXPOSE 10082
# Fri, 24 Jul 2020 16:33:58 GMT
WORKDIR /var/www/html
# Fri, 24 Jul 2020 16:33:58 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:7b378fa0f9085667ced1c76c9919cde8663becf2218e8d20e2df8d0824311531`  
		Last Modified: Tue, 07 Jul 2020 13:19:56 GMT  
		Size: 44.4 MB (44401021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d77b1b29f2e9b6f141b9d8f74b601f40eb998544783f4a0a3cdc384873c1a4e`  
		Last Modified: Fri, 24 Jul 2020 14:39:50 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c793be88baee3f3204444e4d4e49c4e44c1709d40182c131cd5681c94e17227`  
		Last Modified: Fri, 24 Jul 2020 14:39:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc05c8a19c0cf83f2f44263c967c3fe81fffc4b41b592ad088fb1534c206e70`  
		Last Modified: Fri, 24 Jul 2020 14:39:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748f9d7b4e3266b22bb306c205cb89f601fdd6b96e70651f786712c9409aacea`  
		Last Modified: Fri, 24 Jul 2020 16:38:33 GMT  
		Size: 14.7 KB (14703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556df6871dacfa73d17bdf6b436a65961234bd062c447f24310e57ef35d19ad4`  
		Last Modified: Fri, 24 Jul 2020 16:38:33 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd9a86a42a9061da28825dccd0fde75a4895e3f43928ee40eb02cd95f7fd2c5`  
		Last Modified: Fri, 24 Jul 2020 16:38:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac0fc122a919b8fb975a8585123a0ecacf5ddde90939e6c7947d2fb64384b89`  
		Last Modified: Fri, 24 Jul 2020 16:39:19 GMT  
		Size: 263.9 MB (263866105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a065508f106c264bbd3658a020e2882e4731af4e85732234af242d4df43c8efd`  
		Last Modified: Fri, 24 Jul 2020 16:38:32 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303a15eaec7c361c9965cd59cc3a6cfdaff5615d7baf3e7572c3e7d1026b8a8f`  
		Last Modified: Fri, 24 Jul 2020 16:38:32 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb14a7a9d1a97cb4524bd531d626ca1ab7f20c19a25a788f347d48848bf4bcca`  
		Last Modified: Fri, 24 Jul 2020 16:38:31 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762af8b4380e3217f6c49f0b21e643a050540ea64bc195fa1fb907fb7c6c1b39`  
		Last Modified: Fri, 24 Jul 2020 16:38:30 GMT  
		Size: 18.8 KB (18827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb3c2a105068d08dd6835b8696cdaf0b6d68d1cbafd2709f744947dc3e52907`  
		Last Modified: Fri, 24 Jul 2020 16:38:36 GMT  
		Size: 19.8 MB (19819899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e43f14cc2f45ccaf064571f3ef5bd682db7d26a36c1ccd3dfe785a3d804cd4`  
		Last Modified: Fri, 24 Jul 2020 16:38:28 GMT  
		Size: 13.4 KB (13355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57911b14af53e3a36438d53cbe41c72f025f01060bf529acea43b044efb99d3b`  
		Last Modified: Fri, 24 Jul 2020 16:38:28 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce8bdd23ab08af121417c92421b0f901255ea4dde9486b0a8dbad10a19ff956`  
		Last Modified: Fri, 24 Jul 2020 16:38:29 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c02264a3e40951a31d746dba3bd356e03c6cd41ee3346baa302556c8278191`  
		Last Modified: Fri, 24 Jul 2020 16:38:28 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5-php5.6`

```console
$ docker pull php-zendserver@sha256:285707664d621644902102d46c121ead9b93871a1fb5af1e537408e842baed5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5-php5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:1b8c3b6ddfae8465074a137bedc6d3cee7ffb3efe578548a0db3ced5a30821fd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.1 MB (328140810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7855506b68fafd3081b7d2e53bfbd364661cd305c3a344b3226392cd1227723c`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 24 Jul 2020 14:39:06 GMT
ADD file:513ae777bc4042f8446c0454f8cffc9a94f8429de963651d9a6dab95d4502007 in / 
# Fri, 24 Jul 2020 14:39:07 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:39:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:39:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:39:08 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:31:48 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 24 Jul 2020 16:31:49 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 24 Jul 2020 16:31:49 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Fri, 24 Jul 2020 16:33:38 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.15+b8     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 24 Jul 2020 16:33:39 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Fri, 24 Jul 2020 16:33:39 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Fri, 24 Jul 2020 16:33:40 GMT
RUN /usr/sbin/a2enmod headers
# Fri, 24 Jul 2020 16:33:40 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 24 Jul 2020 16:33:41 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 24 Jul 2020 16:33:41 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Fri, 24 Jul 2020 16:33:42 GMT
WORKDIR /usr/local/zs-init
# Fri, 24 Jul 2020 16:33:55 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Fri, 24 Jul 2020 16:33:56 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Fri, 24 Jul 2020 16:33:56 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 24 Jul 2020 16:33:57 GMT
RUN rm /var/www/html/index.html
# Fri, 24 Jul 2020 16:33:57 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 24 Jul 2020 16:33:57 GMT
EXPOSE 80
# Fri, 24 Jul 2020 16:33:57 GMT
EXPOSE 443
# Fri, 24 Jul 2020 16:33:57 GMT
EXPOSE 10081
# Fri, 24 Jul 2020 16:33:58 GMT
EXPOSE 10082
# Fri, 24 Jul 2020 16:33:58 GMT
WORKDIR /var/www/html
# Fri, 24 Jul 2020 16:33:58 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:7b378fa0f9085667ced1c76c9919cde8663becf2218e8d20e2df8d0824311531`  
		Last Modified: Tue, 07 Jul 2020 13:19:56 GMT  
		Size: 44.4 MB (44401021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d77b1b29f2e9b6f141b9d8f74b601f40eb998544783f4a0a3cdc384873c1a4e`  
		Last Modified: Fri, 24 Jul 2020 14:39:50 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c793be88baee3f3204444e4d4e49c4e44c1709d40182c131cd5681c94e17227`  
		Last Modified: Fri, 24 Jul 2020 14:39:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc05c8a19c0cf83f2f44263c967c3fe81fffc4b41b592ad088fb1534c206e70`  
		Last Modified: Fri, 24 Jul 2020 14:39:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748f9d7b4e3266b22bb306c205cb89f601fdd6b96e70651f786712c9409aacea`  
		Last Modified: Fri, 24 Jul 2020 16:38:33 GMT  
		Size: 14.7 KB (14703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556df6871dacfa73d17bdf6b436a65961234bd062c447f24310e57ef35d19ad4`  
		Last Modified: Fri, 24 Jul 2020 16:38:33 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd9a86a42a9061da28825dccd0fde75a4895e3f43928ee40eb02cd95f7fd2c5`  
		Last Modified: Fri, 24 Jul 2020 16:38:32 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac0fc122a919b8fb975a8585123a0ecacf5ddde90939e6c7947d2fb64384b89`  
		Last Modified: Fri, 24 Jul 2020 16:39:19 GMT  
		Size: 263.9 MB (263866105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a065508f106c264bbd3658a020e2882e4731af4e85732234af242d4df43c8efd`  
		Last Modified: Fri, 24 Jul 2020 16:38:32 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303a15eaec7c361c9965cd59cc3a6cfdaff5615d7baf3e7572c3e7d1026b8a8f`  
		Last Modified: Fri, 24 Jul 2020 16:38:32 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb14a7a9d1a97cb4524bd531d626ca1ab7f20c19a25a788f347d48848bf4bcca`  
		Last Modified: Fri, 24 Jul 2020 16:38:31 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762af8b4380e3217f6c49f0b21e643a050540ea64bc195fa1fb907fb7c6c1b39`  
		Last Modified: Fri, 24 Jul 2020 16:38:30 GMT  
		Size: 18.8 KB (18827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb3c2a105068d08dd6835b8696cdaf0b6d68d1cbafd2709f744947dc3e52907`  
		Last Modified: Fri, 24 Jul 2020 16:38:36 GMT  
		Size: 19.8 MB (19819899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70e43f14cc2f45ccaf064571f3ef5bd682db7d26a36c1ccd3dfe785a3d804cd4`  
		Last Modified: Fri, 24 Jul 2020 16:38:28 GMT  
		Size: 13.4 KB (13355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57911b14af53e3a36438d53cbe41c72f025f01060bf529acea43b044efb99d3b`  
		Last Modified: Fri, 24 Jul 2020 16:38:28 GMT  
		Size: 2.5 KB (2536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce8bdd23ab08af121417c92421b0f901255ea4dde9486b0a8dbad10a19ff956`  
		Last Modified: Fri, 24 Jul 2020 16:38:29 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c02264a3e40951a31d746dba3bd356e03c6cd41ee3346baa302556c8278191`  
		Last Modified: Fri, 24 Jul 2020 16:38:28 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:9.1`

```console
$ docker pull php-zendserver@sha256:cc456bcd53dd393e1508c060333de71450970743bda44f12f72c242c9d004e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:9.1` - linux; amd64

```console
$ docker pull php-zendserver@sha256:864746b2164890a376e19e5f37a781e6d7406f39973eba9de5512f3fa839c6e2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.8 MB (411798733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245d456a68b4aabd5b3b98f6e26177222acc6dbef3add55eed7db4677c4a01a6`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 24 Jul 2020 14:39:06 GMT
ADD file:513ae777bc4042f8446c0454f8cffc9a94f8429de963651d9a6dab95d4502007 in / 
# Fri, 24 Jul 2020 14:39:07 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:39:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:39:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:39:08 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:31:48 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 24 Jul 2020 16:34:05 GMT
COPY file:0d4830b5060fb75cec6a47b30d343d82f9c3d6f95f20c11635618b93dedb5720 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 24 Jul 2020 16:35:33 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server-php-7.1=9.1.10+b202     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 24 Jul 2020 16:35:34 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Fri, 24 Jul 2020 16:35:35 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Fri, 24 Jul 2020 16:35:36 GMT
RUN /usr/sbin/a2enmod headers
# Fri, 24 Jul 2020 16:35:36 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 24 Jul 2020 16:35:36 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 24 Jul 2020 16:35:37 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Fri, 24 Jul 2020 16:35:37 GMT
WORKDIR /usr/local/zs-init
# Fri, 24 Jul 2020 16:35:53 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Fri, 24 Jul 2020 16:35:53 GMT
COPY dir:864637d3fa0817ce3be0c7e34e1298851fa2ea4cfb86583e2ec811f00c6a95fd in /usr/local/bin 
# Fri, 24 Jul 2020 16:35:53 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 24 Jul 2020 16:35:54 GMT
RUN rm /var/www/html/index.html
# Fri, 24 Jul 2020 16:35:54 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 24 Jul 2020 16:35:54 GMT
EXPOSE 80
# Fri, 24 Jul 2020 16:35:55 GMT
EXPOSE 443
# Fri, 24 Jul 2020 16:35:55 GMT
EXPOSE 10081
# Fri, 24 Jul 2020 16:35:55 GMT
EXPOSE 10082
# Fri, 24 Jul 2020 16:35:55 GMT
WORKDIR /var/www/html
# Fri, 24 Jul 2020 16:35:55 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:7b378fa0f9085667ced1c76c9919cde8663becf2218e8d20e2df8d0824311531`  
		Last Modified: Tue, 07 Jul 2020 13:19:56 GMT  
		Size: 44.4 MB (44401021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d77b1b29f2e9b6f141b9d8f74b601f40eb998544783f4a0a3cdc384873c1a4e`  
		Last Modified: Fri, 24 Jul 2020 14:39:50 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c793be88baee3f3204444e4d4e49c4e44c1709d40182c131cd5681c94e17227`  
		Last Modified: Fri, 24 Jul 2020 14:39:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc05c8a19c0cf83f2f44263c967c3fe81fffc4b41b592ad088fb1534c206e70`  
		Last Modified: Fri, 24 Jul 2020 14:39:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748f9d7b4e3266b22bb306c205cb89f601fdd6b96e70651f786712c9409aacea`  
		Last Modified: Fri, 24 Jul 2020 16:38:33 GMT  
		Size: 14.7 KB (14703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968372964db46db0723e500a1afa02b4a891b2c1ba98e88f29ab5df0fb9a0835`  
		Last Modified: Fri, 24 Jul 2020 16:39:27 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cb905c691f9fba4f2754cf4521617f749e7c81112fc035258d62ba8e549d38`  
		Last Modified: Fri, 24 Jul 2020 16:40:17 GMT  
		Size: 347.5 MB (347520166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a724f632db8a139bfe58172f8470ce0c94660959e8840caa86421da5a711ccde`  
		Last Modified: Fri, 24 Jul 2020 16:39:26 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb50a4813aedcc99eecb7aa82b806539f594cf9b9c63191608eeacd99fd535a6`  
		Last Modified: Fri, 24 Jul 2020 16:39:26 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4544f5b34bbec3f9fd34cb662153238717839bc6510d61d6bd285619ac3cb900`  
		Last Modified: Fri, 24 Jul 2020 16:39:26 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0340669fedd7d398945e3748445a6440bff3430e5aa290ff8813c6231ea2c763`  
		Last Modified: Fri, 24 Jul 2020 16:39:25 GMT  
		Size: 18.8 KB (18828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbce02013590aa0dacf9863d5760d818a19da77e64d5cceff1f7689ee2feceb`  
		Last Modified: Fri, 24 Jul 2020 16:39:28 GMT  
		Size: 19.8 MB (19823093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d621646184347452e5928fffaa450f7e5dc9b5433d7671e0f59c0cf625ec91`  
		Last Modified: Fri, 24 Jul 2020 16:39:25 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c881ae5dbcc69600b649e1d4dfce28d4725ee975945890bf9fa3256c9ba5d651`  
		Last Modified: Fri, 24 Jul 2020 16:39:24 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520b5ceee7e8eff64377c49cf6d372275ed2596b6141fe79d32bd69eac7e8151`  
		Last Modified: Fri, 24 Jul 2020 16:39:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8837572f8217346403b51d961df37c8492956dcf9eb8c6621e118b7aa807662e`  
		Last Modified: Fri, 24 Jul 2020 16:39:25 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:6a384e05db2d751cab3fd2be5deda8f2a4213e9a1186606e49958bbae66a4ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:04c0526c639254e6e214c0729302c3f81fe8cb3c7eb311e1c02e734c813c4884
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.3 MB (492331882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49771660717527f62e7fce9e5e62ea67d6ff93f965bdb4a54db781d79935598c`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:36:17 GMT
RUN apt-get update && apt-get install -y       gnupg
# Fri, 24 Jul 2020 16:36:18 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 24 Jul 2020 16:36:18 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 24 Jul 2020 16:38:02 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.4+b392     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 24 Jul 2020 16:38:02 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 24 Jul 2020 16:38:02 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 24 Jul 2020 16:38:03 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Fri, 24 Jul 2020 16:38:03 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Fri, 24 Jul 2020 16:38:04 GMT
WORKDIR /usr/local/zs-init
# Fri, 24 Jul 2020 16:38:12 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Fri, 24 Jul 2020 16:38:12 GMT
COPY dir:7937a6223a1e7805720eca1fbf8c2ccd37938f8f8aa175ae003d409459d49380 in /usr/local/bin 
# Fri, 24 Jul 2020 16:38:12 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 24 Jul 2020 16:38:13 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Fri, 24 Jul 2020 16:38:13 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 24 Jul 2020 16:38:14 GMT
EXPOSE 80
# Fri, 24 Jul 2020 16:38:14 GMT
EXPOSE 443
# Fri, 24 Jul 2020 16:38:14 GMT
EXPOSE 10081
# Fri, 24 Jul 2020 16:38:14 GMT
EXPOSE 10082
# Fri, 24 Jul 2020 16:38:14 GMT
WORKDIR /var/www/html
# Fri, 24 Jul 2020 16:38:14 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e8bd0044bba53b957398126fd92cf0f60a5eb2668783884c1ece2a31f4fc46`  
		Last Modified: Fri, 24 Jul 2020 16:40:29 GMT  
		Size: 28.2 MB (28166831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620517cf9e126051cdd98208134f893446b23dcd79debf3a78c4dd30ecac159f`  
		Last Modified: Fri, 24 Jul 2020 16:40:25 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d01b62b7af11403eeeb9de0c191228214c182242d713914b2d6e7241d29c512`  
		Last Modified: Fri, 24 Jul 2020 16:40:25 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b715824e1c3f7f4472ba80b696fd43ad175265fb5ca1057f64581ac7fc560ee`  
		Last Modified: Fri, 24 Jul 2020 16:41:27 GMT  
		Size: 417.6 MB (417569103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2936f13a221de6a10aaa96c4a17d365f1db96580b5da9f8d83311cf010ceb646`  
		Last Modified: Fri, 24 Jul 2020 16:40:24 GMT  
		Size: 445.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88603cba5cc964d47dbe77ab0ceabbad028f9ce116cdc43ab993f9d3f9751c15`  
		Last Modified: Fri, 24 Jul 2020 16:40:24 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb808167bec8dc558fa7338ae27b1bbfbd018ee8cab15671abc5113dae73308`  
		Last Modified: Fri, 24 Jul 2020 16:40:27 GMT  
		Size: 19.8 MB (19823259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794a944b7e73810295c8c5bd497ceb77bc5dec0176b2ce1495dff3c0da53f2c0`  
		Last Modified: Fri, 24 Jul 2020 16:40:23 GMT  
		Size: 14.3 KB (14255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f098431e37eca64534dfdf3eee74a93796ebc79f0b648538cb76906fbf812ef8`  
		Last Modified: Fri, 24 Jul 2020 16:40:23 GMT  
		Size: 2.5 KB (2530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab295e921ddffdf496b080a9dd83b55c02ebe00e30f293cfdb51af66408fd9f`  
		Last Modified: Fri, 24 Jul 2020 16:40:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd08bd0e69bae973715f91c30b3715fc91cf2fde2f3e5df6b68a14343158a076`  
		Last Modified: Fri, 24 Jul 2020 16:40:23 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
