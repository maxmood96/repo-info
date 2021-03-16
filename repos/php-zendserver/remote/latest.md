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
