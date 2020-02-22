<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `php-zendserver`

-	[`php-zendserver:2019.0`](#php-zendserver20190)
-	[`php-zendserver:9.1`](#php-zendserver91)
-	[`php-zendserver:latest`](#php-zendserverlatest)

## `php-zendserver:2019.0`

```console
$ docker pull php-zendserver@sha256:48502759e5ba39d563a18c5e59721346367e60182151a062d052ed9e796613b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:2019.0` - linux; amd64

```console
$ docker pull php-zendserver@sha256:451493593ea52b67771e890f7e1bda545f1349e1bd6af7fdd57469a3f89ac3bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.1 MB (451059936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17c59a2778aa6a54dd80d1f13b1e7e9af2c159204f093d7a6443184449fc5b7`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:10:37 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 21 Feb 2020 23:12:39 GMT
COPY file:64f63be6042521a7e257b6755c9344694bbe4c59cd3c677e8df3dc06c795a802 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 21 Feb 2020 23:14:06 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server=2019.0.3+b345     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 21 Feb 2020 23:14:07 GMT
COPY file:26009fd1b91c8a82cfe83d983f9357a5914e70e1b464baf9d4d99dd284c5f310 in /etc/zend.lic 
# Fri, 21 Feb 2020 23:14:07 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Fri, 21 Feb 2020 23:14:08 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Fri, 21 Feb 2020 23:14:09 GMT
RUN /usr/sbin/a2enmod headers
# Fri, 21 Feb 2020 23:14:09 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 21 Feb 2020 23:14:09 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 21 Feb 2020 23:14:10 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Fri, 21 Feb 2020 23:14:10 GMT
WORKDIR /usr/local/zs-init
# Fri, 21 Feb 2020 23:14:19 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Fri, 21 Feb 2020 23:14:19 GMT
COPY dir:2503294e06c787d82d501853381aa61cd4a7bf7e5f082292d4aba573b9bbf2e2 in /usr/local/bin 
# Fri, 21 Feb 2020 23:14:19 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 21 Feb 2020 23:14:20 GMT
RUN rm /var/www/html/index.html
# Fri, 21 Feb 2020 23:14:20 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 21 Feb 2020 23:14:20 GMT
EXPOSE 80
# Fri, 21 Feb 2020 23:14:21 GMT
EXPOSE 443
# Fri, 21 Feb 2020 23:14:21 GMT
EXPOSE 10081
# Fri, 21 Feb 2020 23:14:21 GMT
EXPOSE 10082
# Fri, 21 Feb 2020 23:14:21 GMT
WORKDIR /var/www/html
# Fri, 21 Feb 2020 23:14:21 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b204d6c7313832d2fbd9d1bfcf5d6a080fbf7d9de9ecc28a267c8007577b71a8`  
		Last Modified: Fri, 21 Feb 2020 23:14:45 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2aba748bb9dfe89848070a5e6ad0dffff34a55a08aa898b7b6839819efcad7`  
		Last Modified: Fri, 21 Feb 2020 23:15:43 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37fdb70d677ce5352ea1824a9f3ab255773a42c5a19b71339b25b5dfc4c6484`  
		Last Modified: Fri, 21 Feb 2020 23:16:42 GMT  
		Size: 388.3 MB (388274707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ba0e9d2fc1f5b9b1e324ab97787a7d075b22eb7813168fe8ec1ff2de89d68e`  
		Last Modified: Fri, 21 Feb 2020 23:15:42 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c0c1865f99c35bc58204479b99e54bc159f91b6452dd8fc1366903a66e1155`  
		Last Modified: Fri, 21 Feb 2020 23:15:42 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef11124aab853c24b171bb20f1f07175ee199616829a8c067779fa17aaf0274c`  
		Last Modified: Fri, 21 Feb 2020 23:15:41 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71802188d7e47f533e47f54f2eb797a19a96f7a4dbae115195888e95f5bae228`  
		Last Modified: Fri, 21 Feb 2020 23:15:41 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb70b45dfd6effaef6ba44b617515cffd3650ef4862034d5f7dc64d256e1b129`  
		Last Modified: Fri, 21 Feb 2020 23:15:41 GMT  
		Size: 18.8 KB (18830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77852d4170347dc2b048255b88894139c2287131c122cb574c413130843cc11c`  
		Last Modified: Fri, 21 Feb 2020 23:15:43 GMT  
		Size: 18.5 MB (18540471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e1714d7dc5b9a46a896048f55450973c0b71c9cca2ef69e7bbf48bb08d0650`  
		Last Modified: Fri, 21 Feb 2020 23:15:40 GMT  
		Size: 14.3 KB (14297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3afc73e381496b2f024f0a0f00c11d8bf36ab6cb3dec0cdfbf297375218508`  
		Last Modified: Fri, 21 Feb 2020 23:15:40 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba2ee3f1f05cff5b558bfe1aaa35997f558328287ada889b10ff0508e6c0dfb`  
		Last Modified: Fri, 21 Feb 2020 23:15:40 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39ad01e225f02f840c8aa1c1fe39faa1c376756b7693a7053fab87f9ce09d22`  
		Last Modified: Fri, 21 Feb 2020 23:15:40 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:9.1`

```console
$ docker pull php-zendserver@sha256:fa308a897c274215162655b7ce5c2def43222196d43bd99546043df40499bc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:9.1` - linux; amd64

```console
$ docker pull php-zendserver@sha256:5d4967fbdbd602fe67879d384bd57dcd1bc4ce01e71062bf90896b874332d7f4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.3 MB (410337380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbd29b4c94b0c4f4493bf02ba75dddb62ff6382d85eaa7b19b8736069a86369`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:10:37 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 21 Feb 2020 23:10:38 GMT
COPY file:0d4830b5060fb75cec6a47b30d343d82f9c3d6f95f20c11635618b93dedb5720 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 21 Feb 2020 23:12:08 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server-php-7.1=9.1.10+b202     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 21 Feb 2020 23:12:09 GMT
COPY file:26009fd1b91c8a82cfe83d983f9357a5914e70e1b464baf9d4d99dd284c5f310 in /etc/zend.lic 
# Fri, 21 Feb 2020 23:12:10 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Fri, 21 Feb 2020 23:12:10 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Fri, 21 Feb 2020 23:12:11 GMT
RUN /usr/sbin/a2enmod headers
# Fri, 21 Feb 2020 23:12:11 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 21 Feb 2020 23:12:12 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 21 Feb 2020 23:12:12 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Fri, 21 Feb 2020 23:12:13 GMT
WORKDIR /usr/local/zs-init
# Fri, 21 Feb 2020 23:12:25 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Fri, 21 Feb 2020 23:12:25 GMT
COPY dir:864637d3fa0817ce3be0c7e34e1298851fa2ea4cfb86583e2ec811f00c6a95fd in /usr/local/bin 
# Fri, 21 Feb 2020 23:12:25 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 21 Feb 2020 23:12:26 GMT
RUN rm /var/www/html/index.html
# Fri, 21 Feb 2020 23:12:26 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 21 Feb 2020 23:12:26 GMT
EXPOSE 80
# Fri, 21 Feb 2020 23:12:27 GMT
EXPOSE 443
# Fri, 21 Feb 2020 23:12:27 GMT
EXPOSE 10081
# Fri, 21 Feb 2020 23:12:27 GMT
EXPOSE 10082
# Fri, 21 Feb 2020 23:12:27 GMT
WORKDIR /var/www/html
# Fri, 21 Feb 2020 23:12:27 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b204d6c7313832d2fbd9d1bfcf5d6a080fbf7d9de9ecc28a267c8007577b71a8`  
		Last Modified: Fri, 21 Feb 2020 23:14:45 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb744c102babb768a6df8876a595349b99daace1cf6ed36643a689d9361d49d`  
		Last Modified: Fri, 21 Feb 2020 23:14:45 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30450e80bb2c0f1f9a72834d0977ef37d4b40a2258b7f61cf91bf82180a7e7`  
		Last Modified: Fri, 21 Feb 2020 23:15:35 GMT  
		Size: 347.6 MB (347552395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480db9ee6bb1292db5ef6763935ab31fde6e5b566b98e3abf486a72cd66e93ee`  
		Last Modified: Fri, 21 Feb 2020 23:14:45 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5508db750b01d28c6a4b053a7d99091f369f52a7179d81d02be04e5b63391f2f`  
		Last Modified: Fri, 21 Feb 2020 23:14:44 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03fc4e86d24e49439e52fd5c7868ec198418b5834ee8e5f83ca4cd874b5a1f7`  
		Last Modified: Fri, 21 Feb 2020 23:14:43 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed62ed5c0c5b9e353c333c2e6e9b880c51d45179ecc9e06cb7b3352ea21a9d5c`  
		Last Modified: Fri, 21 Feb 2020 23:14:43 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30892b040c9764a5b41e25bbad5a715771ef200d201abbf30770f2f523f9a07b`  
		Last Modified: Fri, 21 Feb 2020 23:14:43 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef2e248bc5946be33ff2808622eb7cf46e7f83a3598549d7a9da764523f3b2d`  
		Last Modified: Fri, 21 Feb 2020 23:14:46 GMT  
		Size: 18.5 MB (18540226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0199fd1a64d6bda943fdddfaf3b24f993242c180f9d5f46feb10df91b1369cd`  
		Last Modified: Fri, 21 Feb 2020 23:14:42 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25a18c68a56be44e93755b6a0346cb56aac5e75efa7e26e70bd8d13e87ac06d`  
		Last Modified: Fri, 21 Feb 2020 23:14:42 GMT  
		Size: 2.5 KB (2531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b363110b569565bbd3f19fc85a5557bf357110a3a916953ae50a337f7bfa15`  
		Last Modified: Fri, 21 Feb 2020 23:14:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52438b3788e4afe7fc6902ed45854eeb4a67b3a9e5e3c351e5350759148cb356`  
		Last Modified: Fri, 21 Feb 2020 23:14:42 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `php-zendserver:latest`

```console
$ docker pull php-zendserver@sha256:48502759e5ba39d563a18c5e59721346367e60182151a062d052ed9e796613b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `php-zendserver:latest` - linux; amd64

```console
$ docker pull php-zendserver@sha256:451493593ea52b67771e890f7e1bda545f1349e1bd6af7fdd57469a3f89ac3bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.1 MB (451059936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17c59a2778aa6a54dd80d1f13b1e7e9af2c159204f093d7a6443184449fc5b7`
-	Default Command: `["\/usr\/local\/bin\/run"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 23:10:37 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-key 799058698E65316A2E7A4FF42EAE1437F7D2C623
# Fri, 21 Feb 2020 23:12:39 GMT
COPY file:64f63be6042521a7e257b6755c9344694bbe4c59cd3c677e8df3dc06c795a802 in /etc/apt/sources.list.d/zend-server.list 
# Fri, 21 Feb 2020 23:14:06 GMT
RUN apt-get update     && apt-get install -y       curl       libmysqlclient20       unzip       git       zend-server=2019.0.3+b345     && rm -rf /var/lib/apt/lists/*     && /usr/local/zend/bin/zendctl.sh stop
# Fri, 21 Feb 2020 23:14:07 GMT
COPY file:26009fd1b91c8a82cfe83d983f9357a5914e70e1b464baf9d4d99dd284c5f310 in /etc/zend.lic 
# Fri, 21 Feb 2020 23:14:07 GMT
COPY file:def46bbc651bcb61f92bcaa2f8d6edec0c22e51e86132fabd2e47542dcbec0bf in /etc/apache2/conf-available 
# Fri, 21 Feb 2020 23:14:08 GMT
RUN /usr/sbin/a2enconf drop-http-proxy-header
# Fri, 21 Feb 2020 23:14:09 GMT
RUN /usr/sbin/a2enmod headers
# Fri, 21 Feb 2020 23:14:09 GMT
ENV ZS_INIT_VERSION=0.3
# Fri, 21 Feb 2020 23:14:09 GMT
ENV ZS_INIT_SHA256=e8d441d8503808e9fc0fafc762b2cb80d4a6e68b94fede0fe41efdeac10800cb
# Fri, 21 Feb 2020 23:14:10 GMT
RUN curl -fSL -o zs-init.tar.gz "http://repos.zend.com/zs-init/zs-init-docker-${ZS_INIT_VERSION}.tar.gz"     && echo "${ZS_INIT_SHA256} *zs-init.tar.gz" | sha256sum -c -     && mkdir /usr/local/zs-init     && tar xzf zs-init.tar.gz --strip-components=1 -C /usr/local/zs-init     && rm zs-init.tar.gz
# Fri, 21 Feb 2020 23:14:10 GMT
WORKDIR /usr/local/zs-init
# Fri, 21 Feb 2020 23:14:19 GMT
RUN /usr/local/zend/bin/php -r "readfile('https://getcomposer.org/installer');" | /usr/local/zend/bin/php     && /usr/local/zend/bin/php composer.phar self-update && /usr/local/zend/bin/php composer.phar update
# Fri, 21 Feb 2020 23:14:19 GMT
COPY dir:2503294e06c787d82d501853381aa61cd4a7bf7e5f082292d4aba573b9bbf2e2 in /usr/local/bin 
# Fri, 21 Feb 2020 23:14:19 GMT
COPY dir:80bde0d50316e7c9350262fe3b75826a91d075303027787e759d703b60df13d6 in /usr/local/zend/var/plugins/ 
# Fri, 21 Feb 2020 23:14:20 GMT
RUN rm /var/www/html/index.html
# Fri, 21 Feb 2020 23:14:20 GMT
COPY dir:d174a5d34625889b4356c566972566e0ca7da618b01ea42276562f8186517a67 in /var/www/html 
# Fri, 21 Feb 2020 23:14:20 GMT
EXPOSE 80
# Fri, 21 Feb 2020 23:14:21 GMT
EXPOSE 443
# Fri, 21 Feb 2020 23:14:21 GMT
EXPOSE 10081
# Fri, 21 Feb 2020 23:14:21 GMT
EXPOSE 10082
# Fri, 21 Feb 2020 23:14:21 GMT
WORKDIR /var/www/html
# Fri, 21 Feb 2020 23:14:21 GMT
CMD ["/usr/local/bin/run"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b204d6c7313832d2fbd9d1bfcf5d6a080fbf7d9de9ecc28a267c8007577b71a8`  
		Last Modified: Fri, 21 Feb 2020 23:14:45 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2aba748bb9dfe89848070a5e6ad0dffff34a55a08aa898b7b6839819efcad7`  
		Last Modified: Fri, 21 Feb 2020 23:15:43 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37fdb70d677ce5352ea1824a9f3ab255773a42c5a19b71339b25b5dfc4c6484`  
		Last Modified: Fri, 21 Feb 2020 23:16:42 GMT  
		Size: 388.3 MB (388274707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ba0e9d2fc1f5b9b1e324ab97787a7d075b22eb7813168fe8ec1ff2de89d68e`  
		Last Modified: Fri, 21 Feb 2020 23:15:42 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c0c1865f99c35bc58204479b99e54bc159f91b6452dd8fc1366903a66e1155`  
		Last Modified: Fri, 21 Feb 2020 23:15:42 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef11124aab853c24b171bb20f1f07175ee199616829a8c067779fa17aaf0274c`  
		Last Modified: Fri, 21 Feb 2020 23:15:41 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71802188d7e47f533e47f54f2eb797a19a96f7a4dbae115195888e95f5bae228`  
		Last Modified: Fri, 21 Feb 2020 23:15:41 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb70b45dfd6effaef6ba44b617515cffd3650ef4862034d5f7dc64d256e1b129`  
		Last Modified: Fri, 21 Feb 2020 23:15:41 GMT  
		Size: 18.8 KB (18830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77852d4170347dc2b048255b88894139c2287131c122cb574c413130843cc11c`  
		Last Modified: Fri, 21 Feb 2020 23:15:43 GMT  
		Size: 18.5 MB (18540471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e1714d7dc5b9a46a896048f55450973c0b71c9cca2ef69e7bbf48bb08d0650`  
		Last Modified: Fri, 21 Feb 2020 23:15:40 GMT  
		Size: 14.3 KB (14297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3afc73e381496b2f024f0a0f00c11d8bf36ab6cb3dec0cdfbf297375218508`  
		Last Modified: Fri, 21 Feb 2020 23:15:40 GMT  
		Size: 2.5 KB (2532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba2ee3f1f05cff5b558bfe1aaa35997f558328287ada889b10ff0508e6c0dfb`  
		Last Modified: Fri, 21 Feb 2020 23:15:40 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39ad01e225f02f840c8aa1c1fe39faa1c376756b7693a7053fab87f9ce09d22`  
		Last Modified: Fri, 21 Feb 2020 23:15:40 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
