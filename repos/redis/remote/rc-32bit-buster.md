## `redis:rc-32bit-buster`

```console
$ docker pull redis@sha256:465a81cbe1c34ca04506428b2fae355d9ffd622950f70b1434ad8bf3dcac140a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redis:rc-32bit-buster` - linux; amd64

```console
$ docker pull redis@sha256:384fc8e96f991a4d634889c895f0506525e7a244a477394fbc483b35a63a2e51
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41213110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0258d8d2a01fd086d5cbc4b5477746bfd024ca85b0454f5d4952e057320d24d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 22 Nov 2019 14:55:09 GMT
ADD file:bc8179c87c8dbb3d962bed1801f99e7c860ff03797cde6ad19b107d43b973ada in / 
# Fri, 22 Nov 2019 14:55:10 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 07:53:06 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 23 Nov 2019 07:53:06 GMT
ENV GOSU_VERSION=1.11
# Sat, 23 Nov 2019 07:53:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		dirmngr 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 23 Dec 2019 17:53:31 GMT
ENV REDIS_VERSION=6.0-rc1
# Mon, 23 Dec 2019 17:53:31 GMT
ENV REDIS_DOWNLOAD_URL=https://github.com/antirez/redis/archive/6.0-rc1.tar.gz
# Mon, 23 Dec 2019 17:53:31 GMT
ENV REDIS_DOWNLOAD_SHA=2676012e2fcfe8d41e594b2ae8a05d0a050d2d84c38a0471ae5fe0143e4b0eca
# Mon, 23 Dec 2019 17:55:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends libc6-i386; 	rm -rf /var/lib/apt/lists/*
# Mon, 23 Dec 2019 17:57:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		gcc-multilib 		libc6-dev-i386 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Mon, 23 Dec 2019 17:57:18 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 23 Dec 2019 17:57:18 GMT
VOLUME [/data]
# Mon, 23 Dec 2019 17:57:18 GMT
WORKDIR /data
# Mon, 23 Dec 2019 17:57:19 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Mon, 23 Dec 2019 17:57:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Dec 2019 17:57:19 GMT
EXPOSE 6379
# Mon, 23 Dec 2019 17:57:19 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:000eee12ec04cc914bf96e8f5dee7767510c2aca3816af6078bd9fbe3150920c`  
		Last Modified: Fri, 22 Nov 2019 15:02:49 GMT  
		Size: 27.1 MB (27092654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc53381c1953dc81111d443ae997f9cb546d8fcd6aa60f3fab856886f763180`  
		Last Modified: Sat, 23 Nov 2019 08:00:01 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bb7bcb5fbfae89c842f664312edcd3065a7afa1c39cdcd8612d2a09d7201a3`  
		Last Modified: Sat, 23 Nov 2019 08:00:07 GMT  
		Size: 1.4 MB (1357612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94c34648898a715abf837f6cc54e14695f9a2a0cd2d36244c2df3a9c604afbd`  
		Last Modified: Mon, 23 Dec 2019 18:03:55 GMT  
		Size: 5.3 MB (5295633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b1694159c9b96b1981a522c5660c325de828bc9aca22d1ff1a42cfd34d19ca`  
		Last Modified: Mon, 23 Dec 2019 18:03:56 GMT  
		Size: 7.5 MB (7464962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcee531e14c27da687dde26d3e67c08f9e143f77142a9b521b8a2f915649659f`  
		Last Modified: Mon, 23 Dec 2019 18:03:54 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9775f0c12b36a4501e85e9a41d5b6876214f76e282a12471c67399c65ff94c2`  
		Last Modified: Mon, 23 Dec 2019 18:03:54 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
