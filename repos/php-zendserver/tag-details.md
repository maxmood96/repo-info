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
$ docker pull php-zendserver@sha256:77579594156f84c85eec8252335fb726086690bcaa589f61eff64eb12d5061c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:2019.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:137a1501e91850bde16589410ef7d3fb47a30af773d05f587a1829f9d99cb573
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.1 MB (482148866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca2c7f0edcd9c9569e3865086e83954e6a38454774df7407f5dfcf8a977faa5`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Mon, 15 Mar 2021 20:45:46 GMT
RUN apt-get update && apt-get install -y       gnupg
# Mon, 15 Mar 2021 20:45:47 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Mon, 15 Mar 2021 20:45:47 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Mon, 15 Mar 2021 20:48:00 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.7+b403     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Mon, 15 Mar 2021 20:48:01 GMT
ENV ZS_INIT_VERSION=0.3
# Mon, 15 Mar 2021 20:48:01 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Mon, 15 Mar 2021 20:48:01 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Mon, 15 Mar 2021 20:48:02 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Mon, 15 Mar 2021 20:48:03 GMT
WORKDIR /usr/local/zs-init
# Mon, 15 Mar 2021 20:48:07 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Mon, 15 Mar 2021 20:48:08 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Mon, 15 Mar 2021 20:48:08 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Mon, 15 Mar 2021 20:48:09 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Mon, 15 Mar 2021 20:48:09 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Mon, 15 Mar 2021 20:48:09 GMT
EXPOSE 80
# Mon, 15 Mar 2021 20:48:10 GMT
EXPOSE 443
# Mon, 15 Mar 2021 20:48:10 GMT
EXPOSE 10081
# Mon, 15 Mar 2021 20:48:10 GMT
EXPOSE 10082
# Mon, 15 Mar 2021 20:48:10 GMT
WORKDIR /var/www/html
# Mon, 15 Mar 2021 20:48:10 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e290e351c12ed85c9ad179fc38b7c7b5ab8a767451c5441d2237b6ad0fb11c`  
		Last Modified: Mon, 15 Mar 2021 20:50:33 GMT  
		Size: 32.2 MB (32171284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010647681eca536737cc1d007b3d23afa48d2d223903d7e6bf34b3946dfd6917`  
		Last Modified: Mon, 15 Mar 2021 20:50:28 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7199a6a761cc2499dbe5f04b61bd37d720ff92bf08d3d10393218d0fa3285d`  
		Last Modified: Mon, 15 Mar 2021 20:50:27 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a080984b659eb38c9a2700953e320a5486329c144555f1f6b7ccb78ef6887dd1`  
		Last Modified: Mon, 15 Mar 2021 20:51:25 GMT  
		Size: 418.1 MB (418086329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a05143ab7613c43a8e32505eb951ca1ec1c3ab0649adeb1358bc8ed01fe790b`  
		Last Modified: Mon, 15 Mar 2021 20:50:26 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d80e4985c873bb1bfab2d824be8cffca56a2135f977f40f6fbfa421cf14f035`  
		Last Modified: Mon, 15 Mar 2021 20:50:27 GMT  
		Size: 18.9 KB (18929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d043209abe1d9b7905e3eaa151b6889657e3c378c5e84b2936804f6a196924eb`  
		Last Modified: Mon, 15 Mar 2021 20:50:25 GMT  
		Size: 5.1 MB (5140792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e3deb0d911cd3d635303fd65c088af467ac37ee4a5ce3e151a81403275f482`  
		Last Modified: Mon, 15 Mar 2021 20:50:24 GMT  
		Size: 14.3 KB (14297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22d74dd27783994e64a716355dd34a5980e7abf80d91cf9439ac3ca6a19c68b`  
		Last Modified: Mon, 15 Mar 2021 20:50:24 GMT  
		Size: 2.6 KB (2560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203db714d0cacfc1b8b20608ddae3f7d292c87a272e05b7ed73deba687004e6a`  
		Last Modified: Mon, 15 Mar 2021 20:50:24 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f625a4ae14f414809212228dbfd556101043562af153018520b5aedf6923cf`  
		Last Modified: Mon, 15 Mar 2021 20:50:24 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:5.6`

```console
$ docker pull php-zendserver@sha256:41f34eb3497c6510dc2330f4eb9695f7767a4f8ab1cb9aecd21770e03d696e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:1bc6a8cbd8494937eeb8e24bb02cb21a190aa98a2d3879d58327135766175f2b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315054873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae9f0c0dd2ccd115ba4b4f64e337e5fa5090adc206405c78a59e191bdec8540`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Mon, 15 Mar 2021 20:39:49 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Mon, 15 Mar 2021 20:39:49 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Mon, 15 Mar 2021 20:39:49 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Mon, 15 Mar 2021 20:42:51 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Mon, 15 Mar 2021 20:42:53 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Mon, 15 Mar 2021 20:42:54 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Mon, 15 Mar 2021 20:42:56 GMT
RUN /usr/sbin/a2enmod headers
# Mon, 15 Mar 2021 20:42:56 GMT
ENV ZS_INIT_VERSION=0.3
# Mon, 15 Mar 2021 20:42:56 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Mon, 15 Mar 2021 20:42:58 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Mon, 15 Mar 2021 20:42:58 GMT
WORKDIR /usr/local/zs-init
# Mon, 15 Mar 2021 20:43:04 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Mon, 15 Mar 2021 20:43:04 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Mon, 15 Mar 2021 20:43:04 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Mon, 15 Mar 2021 20:43:05 GMT
RUN rm /var/www/html/index.html
# Mon, 15 Mar 2021 20:43:06 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Mon, 15 Mar 2021 20:43:06 GMT
EXPOSE 80
# Mon, 15 Mar 2021 20:43:06 GMT
EXPOSE 443
# Mon, 15 Mar 2021 20:43:06 GMT
EXPOSE 10081
# Mon, 15 Mar 2021 20:43:06 GMT
EXPOSE 10082
# Mon, 15 Mar 2021 20:43:07 GMT
WORKDIR /var/www/html
# Mon, 15 Mar 2021 20:43:07 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e5f37df02acbc935674aefdfed9ae8402a347e29cff0e86df1cdc5a5114ce0`  
		Last Modified: Mon, 15 Mar 2021 20:48:36 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53224df4341e048d4db91567270ca99c24300b249cccc943e0fea8d4deb2fcb4`  
		Last Modified: Mon, 15 Mar 2021 20:48:36 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d8b2e8330a81579599cc457de24a33e4393eab5cc7100b55a8d5d2e99b4b83`  
		Last Modified: Mon, 15 Mar 2021 20:48:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582857604810fc0ed1cea8d6e1ca234bc065383dcde8731bb33ea985edcda77e`  
		Last Modified: Mon, 15 Mar 2021 20:49:08 GMT  
		Size: 263.9 MB (263901490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1f3317de5ba5f144f28b3e28f8644892120437d2eb1de8e33bea53ca30630a`  
		Last Modified: Mon, 15 Mar 2021 20:48:34 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfdc37f6435334b2b280a4317c99fc54bbb825d3292fe229cb548e2435b5afb`  
		Last Modified: Mon, 15 Mar 2021 20:48:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5b787f36eff55b8835d908dfd902ddcaf7c913d78931fb7ab8f56efd68142`  
		Last Modified: Mon, 15 Mar 2021 20:48:33 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab1fce0776b756f689c784ae375be7486109cf1e501f48ba69a05f80ae24f32`  
		Last Modified: Mon, 15 Mar 2021 20:48:33 GMT  
		Size: 18.9 KB (18860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9a5402f0fd3d9b0e033c8cfc8478394158b46c2ceb819d4daeafcdcce96590`  
		Last Modified: Mon, 15 Mar 2021 20:48:32 GMT  
		Size: 5.1 MB (5137165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e12351b7eb1fa9ca12ec2041022e330ddfae250ff2d7d27751ab181e85b3f4`  
		Last Modified: Mon, 15 Mar 2021 20:48:31 GMT  
		Size: 13.4 KB (13352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bbd46ccbd697c6bbfaba23e162ab8820628e5300a5dac13c8f34e959fa106d`  
		Last Modified: Mon, 15 Mar 2021 20:48:30 GMT  
		Size: 2.6 KB (2562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063cded31dbad6717c933e243a715cb1dddfac17feb16a2359769ba9af0b7cae`  
		Last Modified: Mon, 15 Mar 2021 20:48:30 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6343abb5f69de912adcae61bf6f740c0509594444ede633966f1a706f9a111`  
		Last Modified: Mon, 15 Mar 2021 20:48:30 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5`

```console
$ docker pull php-zendserver@sha256:41f34eb3497c6510dc2330f4eb9695f7767a4f8ab1cb9aecd21770e03d696e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5` - linux; amd64

```console
$ docker pull php-zendserver@sha256:1bc6a8cbd8494937eeb8e24bb02cb21a190aa98a2d3879d58327135766175f2b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315054873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae9f0c0dd2ccd115ba4b4f64e337e5fa5090adc206405c78a59e191bdec8540`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Mon, 15 Mar 2021 20:39:49 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Mon, 15 Mar 2021 20:39:49 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Mon, 15 Mar 2021 20:39:49 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Mon, 15 Mar 2021 20:42:51 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Mon, 15 Mar 2021 20:42:53 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Mon, 15 Mar 2021 20:42:54 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Mon, 15 Mar 2021 20:42:56 GMT
RUN /usr/sbin/a2enmod headers
# Mon, 15 Mar 2021 20:42:56 GMT
ENV ZS_INIT_VERSION=0.3
# Mon, 15 Mar 2021 20:42:56 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Mon, 15 Mar 2021 20:42:58 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Mon, 15 Mar 2021 20:42:58 GMT
WORKDIR /usr/local/zs-init
# Mon, 15 Mar 2021 20:43:04 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Mon, 15 Mar 2021 20:43:04 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Mon, 15 Mar 2021 20:43:04 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Mon, 15 Mar 2021 20:43:05 GMT
RUN rm /var/www/html/index.html
# Mon, 15 Mar 2021 20:43:06 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Mon, 15 Mar 2021 20:43:06 GMT
EXPOSE 80
# Mon, 15 Mar 2021 20:43:06 GMT
EXPOSE 443
# Mon, 15 Mar 2021 20:43:06 GMT
EXPOSE 10081
# Mon, 15 Mar 2021 20:43:06 GMT
EXPOSE 10082
# Mon, 15 Mar 2021 20:43:07 GMT
WORKDIR /var/www/html
# Mon, 15 Mar 2021 20:43:07 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e5f37df02acbc935674aefdfed9ae8402a347e29cff0e86df1cdc5a5114ce0`  
		Last Modified: Mon, 15 Mar 2021 20:48:36 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53224df4341e048d4db91567270ca99c24300b249cccc943e0fea8d4deb2fcb4`  
		Last Modified: Mon, 15 Mar 2021 20:48:36 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d8b2e8330a81579599cc457de24a33e4393eab5cc7100b55a8d5d2e99b4b83`  
		Last Modified: Mon, 15 Mar 2021 20:48:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582857604810fc0ed1cea8d6e1ca234bc065383dcde8731bb33ea985edcda77e`  
		Last Modified: Mon, 15 Mar 2021 20:49:08 GMT  
		Size: 263.9 MB (263901490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1f3317de5ba5f144f28b3e28f8644892120437d2eb1de8e33bea53ca30630a`  
		Last Modified: Mon, 15 Mar 2021 20:48:34 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfdc37f6435334b2b280a4317c99fc54bbb825d3292fe229cb548e2435b5afb`  
		Last Modified: Mon, 15 Mar 2021 20:48:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5b787f36eff55b8835d908dfd902ddcaf7c913d78931fb7ab8f56efd68142`  
		Last Modified: Mon, 15 Mar 2021 20:48:33 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab1fce0776b756f689c784ae375be7486109cf1e501f48ba69a05f80ae24f32`  
		Last Modified: Mon, 15 Mar 2021 20:48:33 GMT  
		Size: 18.9 KB (18860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9a5402f0fd3d9b0e033c8cfc8478394158b46c2ceb819d4daeafcdcce96590`  
		Last Modified: Mon, 15 Mar 2021 20:48:32 GMT  
		Size: 5.1 MB (5137165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e12351b7eb1fa9ca12ec2041022e330ddfae250ff2d7d27751ab181e85b3f4`  
		Last Modified: Mon, 15 Mar 2021 20:48:31 GMT  
		Size: 13.4 KB (13352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bbd46ccbd697c6bbfaba23e162ab8820628e5300a5dac13c8f34e959fa106d`  
		Last Modified: Mon, 15 Mar 2021 20:48:30 GMT  
		Size: 2.6 KB (2562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063cded31dbad6717c933e243a715cb1dddfac17feb16a2359769ba9af0b7cae`  
		Last Modified: Mon, 15 Mar 2021 20:48:30 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6343abb5f69de912adcae61bf6f740c0509594444ede633966f1a706f9a111`  
		Last Modified: Mon, 15 Mar 2021 20:48:30 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:8.5-php5.6`

```console
$ docker pull php-zendserver@sha256:41f34eb3497c6510dc2330f4eb9695f7767a4f8ab1cb9aecd21770e03d696e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:8.5-php5.6` - linux; amd64

```console
$ docker pull php-zendserver@sha256:1bc6a8cbd8494937eeb8e24bb02cb21a190aa98a2d3879d58327135766175f2b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315054873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae9f0c0dd2ccd115ba4b4f64e337e5fa5090adc206405c78a59e191bdec8540`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Mon, 15 Mar 2021 20:39:49 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Mon, 15 Mar 2021 20:39:49 GMT
COPY file:6f0a5450842ae9c3e06d131c7180961d773ca33754e17af8ea2ac258fd0c6054 in /etc/apt/sources.list.d/zend-server.list 
# Mon, 15 Mar 2021 20:39:49 GMT
COPY file:7a9d81c6298f71cfad4408c8b3d7c3bf53bf90083221ec55686e12b2eb6f16a4 in /etc/apt/sources.list.d/ubuntu-trusty.list 
# Mon, 15 Mar 2021 20:42:51 GMT
RUN apt-get update     && apt-get install -y         curl         libmysqlclient18         unzip         git         zend-server-php-5.6=8.5.17+b19     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Mon, 15 Mar 2021 20:42:53 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Mon, 15 Mar 2021 20:42:54 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Mon, 15 Mar 2021 20:42:56 GMT
RUN /usr/sbin/a2enmod headers
# Mon, 15 Mar 2021 20:42:56 GMT
ENV ZS_INIT_VERSION=0.3
# Mon, 15 Mar 2021 20:42:56 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Mon, 15 Mar 2021 20:42:58 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Mon, 15 Mar 2021 20:42:58 GMT
WORKDIR /usr/local/zs-init
# Mon, 15 Mar 2021 20:43:04 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Mon, 15 Mar 2021 20:43:04 GMT
COPY dir:b75978d6e77900379bb898c52c86c408d7f6fcd06b5c66439d594a1a3dcca0b4 in /usr/local/bin 
# Mon, 15 Mar 2021 20:43:04 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Mon, 15 Mar 2021 20:43:05 GMT
RUN rm /var/www/html/index.html
# Mon, 15 Mar 2021 20:43:06 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Mon, 15 Mar 2021 20:43:06 GMT
EXPOSE 80
# Mon, 15 Mar 2021 20:43:06 GMT
EXPOSE 443
# Mon, 15 Mar 2021 20:43:06 GMT
EXPOSE 10081
# Mon, 15 Mar 2021 20:43:06 GMT
EXPOSE 10082
# Mon, 15 Mar 2021 20:43:07 GMT
WORKDIR /var/www/html
# Mon, 15 Mar 2021 20:43:07 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e5f37df02acbc935674aefdfed9ae8402a347e29cff0e86df1cdc5a5114ce0`  
		Last Modified: Mon, 15 Mar 2021 20:48:36 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53224df4341e048d4db91567270ca99c24300b249cccc943e0fea8d4deb2fcb4`  
		Last Modified: Mon, 15 Mar 2021 20:48:36 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d8b2e8330a81579599cc457de24a33e4393eab5cc7100b55a8d5d2e99b4b83`  
		Last Modified: Mon, 15 Mar 2021 20:48:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582857604810fc0ed1cea8d6e1ca234bc065383dcde8731bb33ea985edcda77e`  
		Last Modified: Mon, 15 Mar 2021 20:49:08 GMT  
		Size: 263.9 MB (263901490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1f3317de5ba5f144f28b3e28f8644892120437d2eb1de8e33bea53ca30630a`  
		Last Modified: Mon, 15 Mar 2021 20:48:34 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfdc37f6435334b2b280a4317c99fc54bbb825d3292fe229cb548e2435b5afb`  
		Last Modified: Mon, 15 Mar 2021 20:48:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5b787f36eff55b8835d908dfd902ddcaf7c913d78931fb7ab8f56efd68142`  
		Last Modified: Mon, 15 Mar 2021 20:48:33 GMT  
		Size: 306.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab1fce0776b756f689c784ae375be7486109cf1e501f48ba69a05f80ae24f32`  
		Last Modified: Mon, 15 Mar 2021 20:48:33 GMT  
		Size: 18.9 KB (18860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9a5402f0fd3d9b0e033c8cfc8478394158b46c2ceb819d4daeafcdcce96590`  
		Last Modified: Mon, 15 Mar 2021 20:48:32 GMT  
		Size: 5.1 MB (5137165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e12351b7eb1fa9ca12ec2041022e330ddfae250ff2d7d27751ab181e85b3f4`  
		Last Modified: Mon, 15 Mar 2021 20:48:31 GMT  
		Size: 13.4 KB (13352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bbd46ccbd697c6bbfaba23e162ab8820628e5300a5dac13c8f34e959fa106d`  
		Last Modified: Mon, 15 Mar 2021 20:48:30 GMT  
		Size: 2.6 KB (2562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063cded31dbad6717c933e243a715cb1dddfac17feb16a2359769ba9af0b7cae`  
		Last Modified: Mon, 15 Mar 2021 20:48:30 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6343abb5f69de912adcae61bf6f740c0509594444ede633966f1a706f9a111`  
		Last Modified: Mon, 15 Mar 2021 20:48:30 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:9.1`

```console
$ docker pull php-zendserver@sha256:d1b45ffd6fba1effb9d9dfb3ad45e5d96539e686cb252a71e900cc66c34f768d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:9.1` - linux; amd64

```console
$ docker pull php-zendserver@sha256:56783383a1934202d27f973ef1213fb8d7230f134b6e7d3bf1d4ff5b566a2532
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 MB (399302211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01c51c153d5de28171c4137d01edc7200dad6de0730ea886e924ec1f1eb42aa`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Mon, 15 Mar 2021 20:39:49 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Mon, 15 Mar 2021 20:43:13 GMT
COPY file:0d4830b5060fb75cec6a47b30d343d82f9c3d6f95f20c11635618b93dedb5720 in /etc/apt/sources.list.d/zend-server.list 
# Mon, 15 Mar 2021 20:44:39 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server-php-7.1=9.1.12+b211     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Mon, 15 Mar 2021 20:44:42 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Mon, 15 Mar 2021 20:44:43 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Mon, 15 Mar 2021 20:44:44 GMT
RUN /usr/sbin/a2enmod headers
# Mon, 15 Mar 2021 20:44:44 GMT
ENV ZS_INIT_VERSION=0.3
# Mon, 15 Mar 2021 20:44:44 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Mon, 15 Mar 2021 20:44:46 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Mon, 15 Mar 2021 20:44:46 GMT
WORKDIR /usr/local/zs-init
# Mon, 15 Mar 2021 20:44:52 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Mon, 15 Mar 2021 20:44:52 GMT
COPY dir:5966ca4828c37f68d48d11da814350a590451453f42aa83ef2eab6893db3e4cc in /usr/local/bin 
# Mon, 15 Mar 2021 20:44:53 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Mon, 15 Mar 2021 20:44:54 GMT
RUN rm /var/www/html/index.html
# Mon, 15 Mar 2021 20:44:54 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Mon, 15 Mar 2021 20:44:54 GMT
EXPOSE 80
# Mon, 15 Mar 2021 20:44:54 GMT
EXPOSE 443
# Mon, 15 Mar 2021 20:44:55 GMT
EXPOSE 10081
# Mon, 15 Mar 2021 20:44:55 GMT
EXPOSE 10082
# Mon, 15 Mar 2021 20:44:55 GMT
WORKDIR /var/www/html
# Mon, 15 Mar 2021 20:44:55 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e5f37df02acbc935674aefdfed9ae8402a347e29cff0e86df1cdc5a5114ce0`  
		Last Modified: Mon, 15 Mar 2021 20:48:36 GMT  
		Size: 14.7 KB (14704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de95d0aab1a337dd7863966d72e7d43b2fb5911f16a08e63f03a15bc49a61469`  
		Last Modified: Mon, 15 Mar 2021 20:49:30 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f8ce25c47b2ab7b4bdbcfac4c4986ae784643e9a780a197cf44ce8992d7053`  
		Last Modified: Mon, 15 Mar 2021 20:50:15 GMT  
		Size: 348.1 MB (348144504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59529d3e6808f7ca01cb84ed30835a5ce610a0b7ed37c77959006afd78ce2dcb`  
		Last Modified: Mon, 15 Mar 2021 20:49:28 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5004472ce571649855eb6f8d29f43e3adff0fdfee22778a111ce2d0995cd4a40`  
		Last Modified: Mon, 15 Mar 2021 20:49:28 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbb477dd51b4373b361301f1a7e1685922be9a1287fedc19b2b2b611fb248dc`  
		Last Modified: Mon, 15 Mar 2021 20:49:28 GMT  
		Size: 310.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b7f748e04ed51279dbe3d07debec82b176dd0cbbe50205aeb22efdc0366bf`  
		Last Modified: Mon, 15 Mar 2021 20:49:28 GMT  
		Size: 18.9 KB (18856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfa5a2a3274f5c47275931d1b808869d7acb922073da397769f9ca4cc0b77d5`  
		Last Modified: Mon, 15 Mar 2021 20:49:26 GMT  
		Size: 5.1 MB (5140799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9ea530f22023a1081dc8caa924f81e4d665535be46b9e429abcd35e55e7808`  
		Last Modified: Mon, 15 Mar 2021 20:49:25 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8132ba61fc5be328ebf2a2f3beaca12bbb2f3e278065bc605753ac1383d66fd9`  
		Last Modified: Mon, 15 Mar 2021 20:49:26 GMT  
		Size: 2.6 KB (2561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05aba7018405fc7d52562c32773d8d9e601ddd1aa34f9a64bdfa8a074e1f95b`  
		Last Modified: Mon, 15 Mar 2021 20:49:26 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2475e1385c32793b76c285f41829149f1a309e17d4cd7c7192edd599c26446e`  
		Last Modified: Mon, 15 Mar 2021 20:49:25 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:77579594156f84c85eec8252335fb726086690bcaa589f61eff64eb12d5061c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:137a1501e91850bde16589410ef7d3fb47a30af773d05f587a1829f9d99cb573
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.1 MB (482148866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca2c7f0edcd9c9569e3865086e83954e6a38454774df7407f5dfcf8a977faa5`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Mon, 15 Mar 2021 20:45:46 GMT
RUN apt-get update && apt-get install -y       gnupg
# Mon, 15 Mar 2021 20:45:47 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Mon, 15 Mar 2021 20:45:47 GMT
COPY file:23f8c2a96f087277b95ebfd7f401f5c1b95ec7f3443fa9231607566f1d8e7270 in /etc/apt/sources.list.d/zend-server.list 
# Mon, 15 Mar 2021 20:48:00 GMT
RUN apt-get update && apt-get install -y       iproute2       curl       libmysqlclient20       unzip       git       zend-server-nginx=2019.0.7+b403     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Mon, 15 Mar 2021 20:48:01 GMT
ENV ZS_INIT_VERSION=0.3
# Mon, 15 Mar 2021 20:48:01 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Mon, 15 Mar 2021 20:48:01 GMT
COPY file:ad21ce0b2dc8345be0ef63836774934d6b2045ddc3685411221a07dd10b649d1 in /tmp/zs-init.patch 
# Mon, 15 Mar 2021 20:48:02 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz     && patch -u /usr/local/zs-init/src/Init/Steps/AbstractStep.php -i /tmp/zs-init.patch     && rm /tmp/zs-init.patch
# Mon, 15 Mar 2021 20:48:03 GMT
WORKDIR /usr/local/zs-init
# Mon, 15 Mar 2021 20:48:07 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar update
# Mon, 15 Mar 2021 20:48:08 GMT
COPY dir:eecd98e9ebf1c61a12ae67558eb2a6ce846b9ebfadabbf08503e90b3e30d9496 in /usr/local/bin 
# Mon, 15 Mar 2021 20:48:08 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Mon, 15 Mar 2021 20:48:09 GMT
RUN rm /var/www/html/index.nginx-debian.html
# Mon, 15 Mar 2021 20:48:09 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Mon, 15 Mar 2021 20:48:09 GMT
EXPOSE 80
# Mon, 15 Mar 2021 20:48:10 GMT
EXPOSE 443
# Mon, 15 Mar 2021 20:48:10 GMT
EXPOSE 10081
# Mon, 15 Mar 2021 20:48:10 GMT
EXPOSE 10082
# Mon, 15 Mar 2021 20:48:10 GMT
WORKDIR /var/www/html
# Mon, 15 Mar 2021 20:48:10 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e290e351c12ed85c9ad179fc38b7c7b5ab8a767451c5441d2237b6ad0fb11c`  
		Last Modified: Mon, 15 Mar 2021 20:50:33 GMT  
		Size: 32.2 MB (32171284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010647681eca536737cc1d007b3d23afa48d2d223903d7e6bf34b3946dfd6917`  
		Last Modified: Mon, 15 Mar 2021 20:50:28 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7199a6a761cc2499dbe5f04b61bd37d720ff92bf08d3d10393218d0fa3285d`  
		Last Modified: Mon, 15 Mar 2021 20:50:27 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a080984b659eb38c9a2700953e320a5486329c144555f1f6b7ccb78ef6887dd1`  
		Last Modified: Mon, 15 Mar 2021 20:51:25 GMT  
		Size: 418.1 MB (418086329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a05143ab7613c43a8e32505eb951ca1ec1c3ab0649adeb1358bc8ed01fe790b`  
		Last Modified: Mon, 15 Mar 2021 20:50:26 GMT  
		Size: 447.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d80e4985c873bb1bfab2d824be8cffca56a2135f977f40f6fbfa421cf14f035`  
		Last Modified: Mon, 15 Mar 2021 20:50:27 GMT  
		Size: 18.9 KB (18929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d043209abe1d9b7905e3eaa151b6889657e3c378c5e84b2936804f6a196924eb`  
		Last Modified: Mon, 15 Mar 2021 20:50:25 GMT  
		Size: 5.1 MB (5140792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e3deb0d911cd3d635303fd65c088af467ac37ee4a5ce3e151a81403275f482`  
		Last Modified: Mon, 15 Mar 2021 20:50:24 GMT  
		Size: 14.3 KB (14297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22d74dd27783994e64a716355dd34a5980e7abf80d91cf9439ac3ca6a19c68b`  
		Last Modified: Mon, 15 Mar 2021 20:50:24 GMT  
		Size: 2.6 KB (2560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203db714d0cacfc1b8b20608ddae3f7d292c87a272e05b7ed73deba687004e6a`  
		Last Modified: Mon, 15 Mar 2021 20:50:24 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f625a4ae14f414809212228dbfd556101043562af153018520b5aedf6923cf`  
		Last Modified: Mon, 15 Mar 2021 20:50:24 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
