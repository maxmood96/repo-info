<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `redis`

-	[`redis:5`](#redis5)
-	[`redis:5.0`](#redis50)
-	[`redis:5.0-32bit`](#redis50-32bit)
-	[`redis:5.0-32bit-buster`](#redis50-32bit-buster)
-	[`redis:5.0.9`](#redis509)
-	[`redis:5.0.9-32bit`](#redis509-32bit)
-	[`redis:5.0.9-32bit-buster`](#redis509-32bit-buster)
-	[`redis:5.0.9-alpine`](#redis509-alpine)
-	[`redis:5.0.9-alpine3.11`](#redis509-alpine311)
-	[`redis:5.0.9-buster`](#redis509-buster)
-	[`redis:5.0-alpine`](#redis50-alpine)
-	[`redis:5.0-alpine3.11`](#redis50-alpine311)
-	[`redis:5.0-buster`](#redis50-buster)
-	[`redis:5-32bit`](#redis5-32bit)
-	[`redis:5-32bit-buster`](#redis5-32bit-buster)
-	[`redis:5-alpine`](#redis5-alpine)
-	[`redis:5-alpine3.11`](#redis5-alpine311)
-	[`redis:5-buster`](#redis5-buster)
-	[`redis:6`](#redis6)
-	[`redis:6.0`](#redis60)
-	[`redis:6.0.3`](#redis603)
-	[`redis:6.0.3-alpine`](#redis603-alpine)
-	[`redis:6.0.3-alpine3.11`](#redis603-alpine311)
-	[`redis:6.0.3-buster`](#redis603-buster)
-	[`redis:6.0-alpine`](#redis60-alpine)
-	[`redis:6.0-alpine3.11`](#redis60-alpine311)
-	[`redis:6.0-buster`](#redis60-buster)
-	[`redis:6-alpine`](#redis6-alpine)
-	[`redis:6-alpine3.11`](#redis6-alpine311)
-	[`redis:6-buster`](#redis6-buster)
-	[`redis:alpine`](#redisalpine)
-	[`redis:alpine3.11`](#redisalpine311)
-	[`redis:buster`](#redisbuster)
-	[`redis:latest`](#redislatest)

## `redis:5`

```console
$ docker pull redis@sha256:08aab527ca57f536f2805e031535a6881bab63171146aa6414de69d54b14a84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redis:5` - linux; amd64

```console
$ docker pull redis@sha256:ae4b7c01640a2688e9ef5dd630e2135df7a9e711e712e3d9eab05608d34e2b84
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35863829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5120d23bad51618dd0e19bddd616d555f3cb01753a930c9532364e0d2505b7e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 02:15:48 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 02:17:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:17:30 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:17:30 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:17:30 GMT
WORKDIR /data
# Sat, 16 May 2020 02:17:31 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:17:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:17:31 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:17:32 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846bf5faff48ca0599eb0ab51917d8471164ff02f04524d108bfc8b89dcf50cd`  
		Last Modified: Sat, 16 May 2020 02:20:41 GMT  
		Size: 7.3 MB (7345115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affafbdb5f81d8218bb0f3a60783e92e55fa09ba0a2488f3488488608fa1153d`  
		Last Modified: Sat, 16 May 2020 02:20:38 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdd19e5317241aa2fcd854961c766a5bfc18cbd0db01b18c91404ebdc2ccaa3`  
		Last Modified: Sat, 16 May 2020 02:20:39 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5` - linux; arm variant v5

```console
$ docker pull redis@sha256:aa487a40514e78f619cfcb9458a4cba51f5638916d8e4ed3bc10355d362963be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33396150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d3ebf62ba5747e68aa370dc62af6d166b2f494290cc0339c60f17aa271de77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 22:38:03 GMT
ADD file:cbd01ff8d2e40a25bcdb13dc19ffe124c2927b491997dc1c57d4f2c2a308e279 in / 
# Thu, 14 May 2020 22:38:05 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:40:59 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 04:40:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 04:41:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 04:43:01 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 04:43:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 04:43:02 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 04:44:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 04:44:09 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 04:44:09 GMT
VOLUME [/data]
# Fri, 15 May 2020 04:44:10 GMT
WORKDIR /data
# Fri, 15 May 2020 04:44:11 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 04:44:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 04:44:12 GMT
EXPOSE 6379
# Fri, 15 May 2020 04:44:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:24d81022117207b0239d8a8023ca1724b7dde38cb08ce5b9199f59d475d1e600`  
		Last Modified: Thu, 14 May 2020 22:46:51 GMT  
		Size: 24.8 MB (24838470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c13f680b58f95af37082529e8a1ecd6358e22a7e13a75344d8375a03cafb174`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2286bbfcebea1b30a2e862afd7742a7f65237dcabddc9486bfaaf5fd8ba0d65`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.4 MB (1376110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7deffa88c65075e285c0d27dc2aba2336a7a1779ed75bb2f32e760fbab785147`  
		Last Modified: Fri, 15 May 2020 04:44:47 GMT  
		Size: 7.2 MB (7179299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02c5ad0a586c0c745b5df9a3db37bcaf3213a48ab53be3446bd486fa5b85838`  
		Last Modified: Fri, 15 May 2020 04:44:44 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9850cd504042ad62e1898b73b9a1d5d4a95d80bf65a5909d238d56a640697226`  
		Last Modified: Fri, 15 May 2020 04:44:44 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5` - linux; arm variant v7

```console
$ docker pull redis@sha256:428b7a31e32fb1a39cc9d41b113e6051359572d96ae9d9906089f4c324a07173
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31109932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3abf0ee6b0b5453a72669cb38743da5af51666c9b3e18ab680cfb0c65e3241a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 01:00:06 GMT
ADD file:e3f9a454eccb40b4d7bf1dcc17ec29589a007ac67545d1cb5b6fa213c872c8f2 in / 
# Fri, 15 May 2020 01:00:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 16:49:40 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 16:49:40 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 16:50:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 16:51:47 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 16:51:48 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 16:51:49 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 16:52:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 16:52:49 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 16:52:50 GMT
VOLUME [/data]
# Fri, 15 May 2020 16:52:51 GMT
WORKDIR /data
# Fri, 15 May 2020 16:52:51 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 16:52:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 16:52:53 GMT
EXPOSE 6379
# Fri, 15 May 2020 16:52:53 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e41e28500352be59188c3d871a4b5a3f594350b860a9a36ed5808a35920bdae4`  
		Last Modified: Fri, 15 May 2020 01:11:21 GMT  
		Size: 22.7 MB (22705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6732859766aedad40f91cd96df6b5a6930efe6614b0f084b8459d93c22a69`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed92b736a14b52db74c7cd9919c66ce953393f0544906969081702697d5a6b54`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.4 MB (1368207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114f7e7289bd10cc75ccedb5c36ef2ef1bcdd04a0d015af0e3f5dbca67c2e2d9`  
		Last Modified: Fri, 15 May 2020 16:53:44 GMT  
		Size: 7.0 MB (7033534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e37951fe3e21e2afb2d25fe8ec18da89f27d40c88b7e83b5991380af42227`  
		Last Modified: Fri, 15 May 2020 16:53:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b778ce965d8bdff427c804f43a751b2c4e1dc26ba152f53d4abe56a8b4014174`  
		Last Modified: Fri, 15 May 2020 16:53:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:457f1b0ba059ac05ce46805c92967506f61bb69a38eea8a5aaebf1d5d8da5017
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34547915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ef03b25863b64392c6d8ff085e6b0768f88c8b95692196f79c4846e8f38277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 12:44:06 GMT
ADD file:b305c1792102142f183d3084026f0fc6be3ddf8d1959b32f0a5d22d35eebcd15 in / 
# Fri, 15 May 2020 12:44:07 GMT
CMD ["bash"]
# Sat, 16 May 2020 08:24:10 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 08:24:10 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 08:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 08:27:04 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 08:27:05 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 08:27:05 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 08:28:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:28:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:28:09 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:28:10 GMT
WORKDIR /data
# Sat, 16 May 2020 08:28:11 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 08:28:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:28:12 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:28:12 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8a7e1e68c24e5cac20ef26d29505c58456b561c431f0c683b66d1a0943f40dd4`  
		Last Modified: Fri, 15 May 2020 12:53:36 GMT  
		Size: 25.9 MB (25857195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc5ca4e8f484b410989ac557169938b5fe6288ed5add0839e05a790ef47676`  
		Last Modified: Sat, 16 May 2020 08:28:42 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eccfc30e2be16f57d04f487ed80dd2b52ada557753eca7c79eb2ff88ab421f2`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 1.4 MB (1352995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27089b3134bdd932f8ebb93aef02f95e6883cebfef343a3caad67c05fcc554d9`  
		Last Modified: Sat, 16 May 2020 08:29:17 GMT  
		Size: 7.3 MB (7335450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35769aa5a1907ee966e04244b585d65a7a780c87efb002cf6abdbe16f153d7b`  
		Last Modified: Sat, 16 May 2020 08:29:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e99e4e05b4653f243c0f8a635a0cb3fb3c367a3d2b73667db0301d0f869f14e`  
		Last Modified: Sat, 16 May 2020 08:29:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5` - linux; 386

```console
$ docker pull redis@sha256:cbd966cd9fdfda6ba7a4ae65566b21c986580d26bccd7648b431417c79a8797e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372a1f57ccac9f9940a9a3ef51392b6ae15c3b1102c3494fb808505bdc549b2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Sat, 16 May 2020 00:07:24 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 00:07:24 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 00:07:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 00:13:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:13:21 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:13:21 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:13:21 GMT
WORKDIR /data
# Sat, 16 May 2020 00:13:22 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 00:13:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:13:22 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:13:23 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157733bfb7391a76ac45c4aa7ed1ea9e99ee6b2f4f70fbbab7b48b514fff73fc`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7927326d7d556c02a6f3c72888c9f9d2beb780c097c9fb1ca55539afa2a42d`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.4 MB (1387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346dcb0e7c24e02011edcae7f0884ff428c9b01cd1361cfb068c4cb5ea6c3f5f`  
		Last Modified: Sat, 16 May 2020 00:14:11 GMT  
		Size: 7.0 MB (7008096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19378b87aaceac51732681a095c2679c50ac66b341a727cc4c59c7672e72642b`  
		Last Modified: Sat, 16 May 2020 00:14:09 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d89103e3ff26e632031f9510e343c0480df8aa67080da4f4fe1cd70671a94b2`  
		Last Modified: Sat, 16 May 2020 00:14:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5` - linux; mips64le

```console
$ docker pull redis@sha256:8b6a10293e59139fa6bcc9fc4b76fa1bece970cbca46f0d4f88ba87ca29fb38d
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34733957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14f6ea4c9fdcd70e15b3ec9963dbf5b3a0cba06b78eca3b49ede54d8eb74633`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 04:48:19 GMT
ADD file:1163d3a5831eb58d132b66b60303169816e7bd8289f19caaac1157179a95f6f9 in / 
# Fri, 15 May 2020 04:48:19 GMT
CMD ["bash"]
# Fri, 15 May 2020 15:35:02 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 15:35:02 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 15:35:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 15:39:12 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 15:39:12 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 15:39:13 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 15:42:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 15:42:32 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 15:42:33 GMT
VOLUME [/data]
# Fri, 15 May 2020 15:42:33 GMT
WORKDIR /data
# Fri, 15 May 2020 15:42:34 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 15:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 15:42:34 GMT
EXPOSE 6379
# Fri, 15 May 2020 15:42:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d22357c747999d33ec7501da2c05aa9e95079ebddefbcb326976c5ed5b176b3f`  
		Last Modified: Fri, 15 May 2020 04:57:10 GMT  
		Size: 25.8 MB (25764292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f562c9b9683468308a6f59cab7d724ffc3b35a66acd8ce093b288144db2b7c5`  
		Last Modified: Fri, 15 May 2020 15:42:49 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fda93ec518be6790dd5e435d4bb66cab95d5c14044f01c584fd463ca6ffd290`  
		Last Modified: Fri, 15 May 2020 15:42:50 GMT  
		Size: 1.3 MB (1305516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeb925910423da69c6eda33089a17133d5b1649da9305c560bb62548887111c`  
		Last Modified: Fri, 15 May 2020 15:43:33 GMT  
		Size: 7.7 MB (7661910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89a2cb8235be9f7742a87b9e6cb1a8e822fa316f9524eb2e63e180907993838`  
		Last Modified: Fri, 15 May 2020 15:43:26 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe01516addcda29424d0863a92cc972db77274689603262287f4383b2251fb0`  
		Last Modified: Fri, 15 May 2020 15:43:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5` - linux; ppc64le

```console
$ docker pull redis@sha256:c25f3deade6ecb0d0ab42fa53321c50806dd2471c0a06ec3180217c93e2b50e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39696499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7993e4f9c4d285dffe1be6b2eb7fc6e5872e4c23175ef0b2eecb2f4dfd9c09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 16 May 2020 17:14:59 GMT
ADD file:b2656a1711bd47585595ae2927cfd4ec00eb903d193583d945b6d60f0a2691bb in / 
# Sat, 16 May 2020 17:15:04 GMT
CMD ["bash"]
# Mon, 18 May 2020 13:30:23 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Mon, 18 May 2020 13:30:26 GMT
ENV GOSU_VERSION=1.12
# Mon, 18 May 2020 13:32:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 18 May 2020 13:38:55 GMT
ENV REDIS_VERSION=5.0.9
# Mon, 18 May 2020 13:38:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Mon, 18 May 2020 13:39:03 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Mon, 18 May 2020 13:41:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:41:57 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:41:59 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:42:03 GMT
WORKDIR /data
# Mon, 18 May 2020 13:42:06 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Mon, 18 May 2020 13:42:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:42:11 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:42:14 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:034d508ed7647e7139951a435acc95e0124f50c984670d0e53b4f5ba25cf6ed1`  
		Last Modified: Sat, 16 May 2020 18:31:49 GMT  
		Size: 30.5 MB (30524456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c613ed63b519e3a0419cf56e14127f5d25466416a8143341540d12cb99943b65`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec60488415c29ebe96bbfabff01925147e50ee55136fdf961fbe8526617f3b`  
		Last Modified: Mon, 18 May 2020 13:42:57 GMT  
		Size: 1.3 MB (1335429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8c21d1569eb7d014ba9bf44dee78260d5e4d8e456b37cb304b127c69940684`  
		Last Modified: Mon, 18 May 2020 13:43:54 GMT  
		Size: 7.8 MB (7834331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c759fe2a72a81200077dd4a171c8c95ea1cecdc62e8a2ae362e0d31f255fc9f9`  
		Last Modified: Mon, 18 May 2020 13:43:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da932920c36a309064e131257fe3ed53362fb1a0d18207a51e7a26735b066838`  
		Last Modified: Mon, 18 May 2020 13:43:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5` - linux; s390x

```console
$ docker pull redis@sha256:becaadf1b7481b782ca8d0ed939de5e00ca69064a94eef114d443bb75116c1f3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34710318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dba1a9e6bde97648f54ed3508c268f0671bdf3b171629e8a034800658e2ea36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 05:15:35 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 05:15:35 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 05:15:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 05:17:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 05:17:06 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 05:17:06 GMT
VOLUME [/data]
# Fri, 15 May 2020 05:17:06 GMT
WORKDIR /data
# Fri, 15 May 2020 05:17:07 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 05:17:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 05:17:07 GMT
EXPOSE 6379
# Fri, 15 May 2020 05:17:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e40cd0998be29e9cce5152b7d3644b03b888bcca5db2049d43c93bf53185d`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc1e5303c90f8fcd807a5042757fb4de087ae4b3319afca416b72e858de788c`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.4 MB (1403711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fff5a343dd72b836a3f99619249e4fd4b82b0d09950a9552781d2fcbe733c9`  
		Last Modified: Fri, 15 May 2020 05:17:43 GMT  
		Size: 7.6 MB (7591396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30482d87111f841181c863a01b1ad9890bab844f7bf3f24c8de746052ebc5d71`  
		Last Modified: Fri, 15 May 2020 05:17:42 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a814c5126e00d2ce60c95caacba2b4f8236c88df49bcaf578c2500a12404dc3`  
		Last Modified: Fri, 15 May 2020 05:17:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5.0`

```console
$ docker pull redis@sha256:08aab527ca57f536f2805e031535a6881bab63171146aa6414de69d54b14a84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redis:5.0` - linux; amd64

```console
$ docker pull redis@sha256:ae4b7c01640a2688e9ef5dd630e2135df7a9e711e712e3d9eab05608d34e2b84
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35863829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5120d23bad51618dd0e19bddd616d555f3cb01753a930c9532364e0d2505b7e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 02:15:48 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 02:17:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:17:30 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:17:30 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:17:30 GMT
WORKDIR /data
# Sat, 16 May 2020 02:17:31 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:17:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:17:31 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:17:32 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846bf5faff48ca0599eb0ab51917d8471164ff02f04524d108bfc8b89dcf50cd`  
		Last Modified: Sat, 16 May 2020 02:20:41 GMT  
		Size: 7.3 MB (7345115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affafbdb5f81d8218bb0f3a60783e92e55fa09ba0a2488f3488488608fa1153d`  
		Last Modified: Sat, 16 May 2020 02:20:38 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdd19e5317241aa2fcd854961c766a5bfc18cbd0db01b18c91404ebdc2ccaa3`  
		Last Modified: Sat, 16 May 2020 02:20:39 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0` - linux; arm variant v5

```console
$ docker pull redis@sha256:aa487a40514e78f619cfcb9458a4cba51f5638916d8e4ed3bc10355d362963be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33396150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d3ebf62ba5747e68aa370dc62af6d166b2f494290cc0339c60f17aa271de77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 22:38:03 GMT
ADD file:cbd01ff8d2e40a25bcdb13dc19ffe124c2927b491997dc1c57d4f2c2a308e279 in / 
# Thu, 14 May 2020 22:38:05 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:40:59 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 04:40:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 04:41:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 04:43:01 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 04:43:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 04:43:02 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 04:44:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 04:44:09 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 04:44:09 GMT
VOLUME [/data]
# Fri, 15 May 2020 04:44:10 GMT
WORKDIR /data
# Fri, 15 May 2020 04:44:11 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 04:44:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 04:44:12 GMT
EXPOSE 6379
# Fri, 15 May 2020 04:44:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:24d81022117207b0239d8a8023ca1724b7dde38cb08ce5b9199f59d475d1e600`  
		Last Modified: Thu, 14 May 2020 22:46:51 GMT  
		Size: 24.8 MB (24838470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c13f680b58f95af37082529e8a1ecd6358e22a7e13a75344d8375a03cafb174`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2286bbfcebea1b30a2e862afd7742a7f65237dcabddc9486bfaaf5fd8ba0d65`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.4 MB (1376110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7deffa88c65075e285c0d27dc2aba2336a7a1779ed75bb2f32e760fbab785147`  
		Last Modified: Fri, 15 May 2020 04:44:47 GMT  
		Size: 7.2 MB (7179299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02c5ad0a586c0c745b5df9a3db37bcaf3213a48ab53be3446bd486fa5b85838`  
		Last Modified: Fri, 15 May 2020 04:44:44 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9850cd504042ad62e1898b73b9a1d5d4a95d80bf65a5909d238d56a640697226`  
		Last Modified: Fri, 15 May 2020 04:44:44 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0` - linux; arm variant v7

```console
$ docker pull redis@sha256:428b7a31e32fb1a39cc9d41b113e6051359572d96ae9d9906089f4c324a07173
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31109932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3abf0ee6b0b5453a72669cb38743da5af51666c9b3e18ab680cfb0c65e3241a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 01:00:06 GMT
ADD file:e3f9a454eccb40b4d7bf1dcc17ec29589a007ac67545d1cb5b6fa213c872c8f2 in / 
# Fri, 15 May 2020 01:00:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 16:49:40 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 16:49:40 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 16:50:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 16:51:47 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 16:51:48 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 16:51:49 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 16:52:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 16:52:49 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 16:52:50 GMT
VOLUME [/data]
# Fri, 15 May 2020 16:52:51 GMT
WORKDIR /data
# Fri, 15 May 2020 16:52:51 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 16:52:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 16:52:53 GMT
EXPOSE 6379
# Fri, 15 May 2020 16:52:53 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e41e28500352be59188c3d871a4b5a3f594350b860a9a36ed5808a35920bdae4`  
		Last Modified: Fri, 15 May 2020 01:11:21 GMT  
		Size: 22.7 MB (22705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6732859766aedad40f91cd96df6b5a6930efe6614b0f084b8459d93c22a69`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed92b736a14b52db74c7cd9919c66ce953393f0544906969081702697d5a6b54`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.4 MB (1368207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114f7e7289bd10cc75ccedb5c36ef2ef1bcdd04a0d015af0e3f5dbca67c2e2d9`  
		Last Modified: Fri, 15 May 2020 16:53:44 GMT  
		Size: 7.0 MB (7033534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e37951fe3e21e2afb2d25fe8ec18da89f27d40c88b7e83b5991380af42227`  
		Last Modified: Fri, 15 May 2020 16:53:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b778ce965d8bdff427c804f43a751b2c4e1dc26ba152f53d4abe56a8b4014174`  
		Last Modified: Fri, 15 May 2020 16:53:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:457f1b0ba059ac05ce46805c92967506f61bb69a38eea8a5aaebf1d5d8da5017
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34547915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ef03b25863b64392c6d8ff085e6b0768f88c8b95692196f79c4846e8f38277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 12:44:06 GMT
ADD file:b305c1792102142f183d3084026f0fc6be3ddf8d1959b32f0a5d22d35eebcd15 in / 
# Fri, 15 May 2020 12:44:07 GMT
CMD ["bash"]
# Sat, 16 May 2020 08:24:10 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 08:24:10 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 08:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 08:27:04 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 08:27:05 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 08:27:05 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 08:28:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:28:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:28:09 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:28:10 GMT
WORKDIR /data
# Sat, 16 May 2020 08:28:11 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 08:28:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:28:12 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:28:12 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8a7e1e68c24e5cac20ef26d29505c58456b561c431f0c683b66d1a0943f40dd4`  
		Last Modified: Fri, 15 May 2020 12:53:36 GMT  
		Size: 25.9 MB (25857195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc5ca4e8f484b410989ac557169938b5fe6288ed5add0839e05a790ef47676`  
		Last Modified: Sat, 16 May 2020 08:28:42 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eccfc30e2be16f57d04f487ed80dd2b52ada557753eca7c79eb2ff88ab421f2`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 1.4 MB (1352995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27089b3134bdd932f8ebb93aef02f95e6883cebfef343a3caad67c05fcc554d9`  
		Last Modified: Sat, 16 May 2020 08:29:17 GMT  
		Size: 7.3 MB (7335450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35769aa5a1907ee966e04244b585d65a7a780c87efb002cf6abdbe16f153d7b`  
		Last Modified: Sat, 16 May 2020 08:29:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e99e4e05b4653f243c0f8a635a0cb3fb3c367a3d2b73667db0301d0f869f14e`  
		Last Modified: Sat, 16 May 2020 08:29:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0` - linux; 386

```console
$ docker pull redis@sha256:cbd966cd9fdfda6ba7a4ae65566b21c986580d26bccd7648b431417c79a8797e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372a1f57ccac9f9940a9a3ef51392b6ae15c3b1102c3494fb808505bdc549b2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Sat, 16 May 2020 00:07:24 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 00:07:24 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 00:07:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 00:13:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:13:21 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:13:21 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:13:21 GMT
WORKDIR /data
# Sat, 16 May 2020 00:13:22 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 00:13:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:13:22 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:13:23 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157733bfb7391a76ac45c4aa7ed1ea9e99ee6b2f4f70fbbab7b48b514fff73fc`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7927326d7d556c02a6f3c72888c9f9d2beb780c097c9fb1ca55539afa2a42d`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.4 MB (1387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346dcb0e7c24e02011edcae7f0884ff428c9b01cd1361cfb068c4cb5ea6c3f5f`  
		Last Modified: Sat, 16 May 2020 00:14:11 GMT  
		Size: 7.0 MB (7008096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19378b87aaceac51732681a095c2679c50ac66b341a727cc4c59c7672e72642b`  
		Last Modified: Sat, 16 May 2020 00:14:09 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d89103e3ff26e632031f9510e343c0480df8aa67080da4f4fe1cd70671a94b2`  
		Last Modified: Sat, 16 May 2020 00:14:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0` - linux; mips64le

```console
$ docker pull redis@sha256:8b6a10293e59139fa6bcc9fc4b76fa1bece970cbca46f0d4f88ba87ca29fb38d
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34733957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14f6ea4c9fdcd70e15b3ec9963dbf5b3a0cba06b78eca3b49ede54d8eb74633`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 04:48:19 GMT
ADD file:1163d3a5831eb58d132b66b60303169816e7bd8289f19caaac1157179a95f6f9 in / 
# Fri, 15 May 2020 04:48:19 GMT
CMD ["bash"]
# Fri, 15 May 2020 15:35:02 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 15:35:02 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 15:35:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 15:39:12 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 15:39:12 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 15:39:13 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 15:42:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 15:42:32 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 15:42:33 GMT
VOLUME [/data]
# Fri, 15 May 2020 15:42:33 GMT
WORKDIR /data
# Fri, 15 May 2020 15:42:34 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 15:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 15:42:34 GMT
EXPOSE 6379
# Fri, 15 May 2020 15:42:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d22357c747999d33ec7501da2c05aa9e95079ebddefbcb326976c5ed5b176b3f`  
		Last Modified: Fri, 15 May 2020 04:57:10 GMT  
		Size: 25.8 MB (25764292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f562c9b9683468308a6f59cab7d724ffc3b35a66acd8ce093b288144db2b7c5`  
		Last Modified: Fri, 15 May 2020 15:42:49 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fda93ec518be6790dd5e435d4bb66cab95d5c14044f01c584fd463ca6ffd290`  
		Last Modified: Fri, 15 May 2020 15:42:50 GMT  
		Size: 1.3 MB (1305516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeb925910423da69c6eda33089a17133d5b1649da9305c560bb62548887111c`  
		Last Modified: Fri, 15 May 2020 15:43:33 GMT  
		Size: 7.7 MB (7661910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89a2cb8235be9f7742a87b9e6cb1a8e822fa316f9524eb2e63e180907993838`  
		Last Modified: Fri, 15 May 2020 15:43:26 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe01516addcda29424d0863a92cc972db77274689603262287f4383b2251fb0`  
		Last Modified: Fri, 15 May 2020 15:43:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0` - linux; ppc64le

```console
$ docker pull redis@sha256:c25f3deade6ecb0d0ab42fa53321c50806dd2471c0a06ec3180217c93e2b50e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39696499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7993e4f9c4d285dffe1be6b2eb7fc6e5872e4c23175ef0b2eecb2f4dfd9c09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 16 May 2020 17:14:59 GMT
ADD file:b2656a1711bd47585595ae2927cfd4ec00eb903d193583d945b6d60f0a2691bb in / 
# Sat, 16 May 2020 17:15:04 GMT
CMD ["bash"]
# Mon, 18 May 2020 13:30:23 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Mon, 18 May 2020 13:30:26 GMT
ENV GOSU_VERSION=1.12
# Mon, 18 May 2020 13:32:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 18 May 2020 13:38:55 GMT
ENV REDIS_VERSION=5.0.9
# Mon, 18 May 2020 13:38:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Mon, 18 May 2020 13:39:03 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Mon, 18 May 2020 13:41:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:41:57 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:41:59 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:42:03 GMT
WORKDIR /data
# Mon, 18 May 2020 13:42:06 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Mon, 18 May 2020 13:42:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:42:11 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:42:14 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:034d508ed7647e7139951a435acc95e0124f50c984670d0e53b4f5ba25cf6ed1`  
		Last Modified: Sat, 16 May 2020 18:31:49 GMT  
		Size: 30.5 MB (30524456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c613ed63b519e3a0419cf56e14127f5d25466416a8143341540d12cb99943b65`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec60488415c29ebe96bbfabff01925147e50ee55136fdf961fbe8526617f3b`  
		Last Modified: Mon, 18 May 2020 13:42:57 GMT  
		Size: 1.3 MB (1335429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8c21d1569eb7d014ba9bf44dee78260d5e4d8e456b37cb304b127c69940684`  
		Last Modified: Mon, 18 May 2020 13:43:54 GMT  
		Size: 7.8 MB (7834331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c759fe2a72a81200077dd4a171c8c95ea1cecdc62e8a2ae362e0d31f255fc9f9`  
		Last Modified: Mon, 18 May 2020 13:43:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da932920c36a309064e131257fe3ed53362fb1a0d18207a51e7a26735b066838`  
		Last Modified: Mon, 18 May 2020 13:43:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0` - linux; s390x

```console
$ docker pull redis@sha256:becaadf1b7481b782ca8d0ed939de5e00ca69064a94eef114d443bb75116c1f3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34710318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dba1a9e6bde97648f54ed3508c268f0671bdf3b171629e8a034800658e2ea36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 05:15:35 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 05:15:35 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 05:15:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 05:17:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 05:17:06 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 05:17:06 GMT
VOLUME [/data]
# Fri, 15 May 2020 05:17:06 GMT
WORKDIR /data
# Fri, 15 May 2020 05:17:07 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 05:17:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 05:17:07 GMT
EXPOSE 6379
# Fri, 15 May 2020 05:17:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e40cd0998be29e9cce5152b7d3644b03b888bcca5db2049d43c93bf53185d`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc1e5303c90f8fcd807a5042757fb4de087ae4b3319afca416b72e858de788c`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.4 MB (1403711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fff5a343dd72b836a3f99619249e4fd4b82b0d09950a9552781d2fcbe733c9`  
		Last Modified: Fri, 15 May 2020 05:17:43 GMT  
		Size: 7.6 MB (7591396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30482d87111f841181c863a01b1ad9890bab844f7bf3f24c8de746052ebc5d71`  
		Last Modified: Fri, 15 May 2020 05:17:42 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a814c5126e00d2ce60c95caacba2b4f8236c88df49bcaf578c2500a12404dc3`  
		Last Modified: Fri, 15 May 2020 05:17:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5.0-32bit`

```console
$ docker pull redis@sha256:3b14d8ad7934452ffe28a95c5931ea8cf4a6e8771d2afc394836fc220c4ddf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redis:5.0-32bit` - linux; amd64

```console
$ docker pull redis@sha256:1c6e5965741e36f16ce589d4fbfce72fadc9d6bcf7b6f458e9d29772c8978275
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40577472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51da9d4e9b00184c7e706cc1f8471c8aafa7f5da3e92655613d5f4e2944ea82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 02:15:48 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 02:19:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev-i386 gcc-multilib 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:19:43 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:19:43 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:19:43 GMT
WORKDIR /data
# Sat, 16 May 2020 02:19:44 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:19:44 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:19:45 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52db9932f76ff160dd7194254956eccd2857a82675be95f689601345919dac8e`  
		Last Modified: Sat, 16 May 2020 02:20:50 GMT  
		Size: 12.1 MB (12058755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64def67d4f9860909ddb35febdfdf94e31ec29c620e2e207e20c2f0f1e92ab07`  
		Last Modified: Sat, 16 May 2020 02:20:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeed70e76f4d345e003e569a8ec0a354771d42efcbcb26b94aea29d64a85272e`  
		Last Modified: Sat, 16 May 2020 02:20:48 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5.0-32bit-buster`

```console
$ docker pull redis@sha256:3b14d8ad7934452ffe28a95c5931ea8cf4a6e8771d2afc394836fc220c4ddf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redis:5.0-32bit-buster` - linux; amd64

```console
$ docker pull redis@sha256:1c6e5965741e36f16ce589d4fbfce72fadc9d6bcf7b6f458e9d29772c8978275
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40577472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51da9d4e9b00184c7e706cc1f8471c8aafa7f5da3e92655613d5f4e2944ea82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 02:15:48 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 02:19:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev-i386 gcc-multilib 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:19:43 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:19:43 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:19:43 GMT
WORKDIR /data
# Sat, 16 May 2020 02:19:44 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:19:44 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:19:45 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52db9932f76ff160dd7194254956eccd2857a82675be95f689601345919dac8e`  
		Last Modified: Sat, 16 May 2020 02:20:50 GMT  
		Size: 12.1 MB (12058755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64def67d4f9860909ddb35febdfdf94e31ec29c620e2e207e20c2f0f1e92ab07`  
		Last Modified: Sat, 16 May 2020 02:20:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeed70e76f4d345e003e569a8ec0a354771d42efcbcb26b94aea29d64a85272e`  
		Last Modified: Sat, 16 May 2020 02:20:48 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5.0.9`

```console
$ docker pull redis@sha256:08aab527ca57f536f2805e031535a6881bab63171146aa6414de69d54b14a84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redis:5.0.9` - linux; amd64

```console
$ docker pull redis@sha256:ae4b7c01640a2688e9ef5dd630e2135df7a9e711e712e3d9eab05608d34e2b84
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35863829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5120d23bad51618dd0e19bddd616d555f3cb01753a930c9532364e0d2505b7e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 02:15:48 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 02:17:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:17:30 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:17:30 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:17:30 GMT
WORKDIR /data
# Sat, 16 May 2020 02:17:31 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:17:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:17:31 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:17:32 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846bf5faff48ca0599eb0ab51917d8471164ff02f04524d108bfc8b89dcf50cd`  
		Last Modified: Sat, 16 May 2020 02:20:41 GMT  
		Size: 7.3 MB (7345115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affafbdb5f81d8218bb0f3a60783e92e55fa09ba0a2488f3488488608fa1153d`  
		Last Modified: Sat, 16 May 2020 02:20:38 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdd19e5317241aa2fcd854961c766a5bfc18cbd0db01b18c91404ebdc2ccaa3`  
		Last Modified: Sat, 16 May 2020 02:20:39 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9` - linux; arm variant v5

```console
$ docker pull redis@sha256:aa487a40514e78f619cfcb9458a4cba51f5638916d8e4ed3bc10355d362963be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33396150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d3ebf62ba5747e68aa370dc62af6d166b2f494290cc0339c60f17aa271de77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 22:38:03 GMT
ADD file:cbd01ff8d2e40a25bcdb13dc19ffe124c2927b491997dc1c57d4f2c2a308e279 in / 
# Thu, 14 May 2020 22:38:05 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:40:59 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 04:40:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 04:41:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 04:43:01 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 04:43:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 04:43:02 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 04:44:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 04:44:09 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 04:44:09 GMT
VOLUME [/data]
# Fri, 15 May 2020 04:44:10 GMT
WORKDIR /data
# Fri, 15 May 2020 04:44:11 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 04:44:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 04:44:12 GMT
EXPOSE 6379
# Fri, 15 May 2020 04:44:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:24d81022117207b0239d8a8023ca1724b7dde38cb08ce5b9199f59d475d1e600`  
		Last Modified: Thu, 14 May 2020 22:46:51 GMT  
		Size: 24.8 MB (24838470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c13f680b58f95af37082529e8a1ecd6358e22a7e13a75344d8375a03cafb174`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2286bbfcebea1b30a2e862afd7742a7f65237dcabddc9486bfaaf5fd8ba0d65`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.4 MB (1376110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7deffa88c65075e285c0d27dc2aba2336a7a1779ed75bb2f32e760fbab785147`  
		Last Modified: Fri, 15 May 2020 04:44:47 GMT  
		Size: 7.2 MB (7179299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02c5ad0a586c0c745b5df9a3db37bcaf3213a48ab53be3446bd486fa5b85838`  
		Last Modified: Fri, 15 May 2020 04:44:44 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9850cd504042ad62e1898b73b9a1d5d4a95d80bf65a5909d238d56a640697226`  
		Last Modified: Fri, 15 May 2020 04:44:44 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9` - linux; arm variant v7

```console
$ docker pull redis@sha256:428b7a31e32fb1a39cc9d41b113e6051359572d96ae9d9906089f4c324a07173
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31109932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3abf0ee6b0b5453a72669cb38743da5af51666c9b3e18ab680cfb0c65e3241a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 01:00:06 GMT
ADD file:e3f9a454eccb40b4d7bf1dcc17ec29589a007ac67545d1cb5b6fa213c872c8f2 in / 
# Fri, 15 May 2020 01:00:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 16:49:40 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 16:49:40 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 16:50:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 16:51:47 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 16:51:48 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 16:51:49 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 16:52:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 16:52:49 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 16:52:50 GMT
VOLUME [/data]
# Fri, 15 May 2020 16:52:51 GMT
WORKDIR /data
# Fri, 15 May 2020 16:52:51 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 16:52:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 16:52:53 GMT
EXPOSE 6379
# Fri, 15 May 2020 16:52:53 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e41e28500352be59188c3d871a4b5a3f594350b860a9a36ed5808a35920bdae4`  
		Last Modified: Fri, 15 May 2020 01:11:21 GMT  
		Size: 22.7 MB (22705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6732859766aedad40f91cd96df6b5a6930efe6614b0f084b8459d93c22a69`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed92b736a14b52db74c7cd9919c66ce953393f0544906969081702697d5a6b54`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.4 MB (1368207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114f7e7289bd10cc75ccedb5c36ef2ef1bcdd04a0d015af0e3f5dbca67c2e2d9`  
		Last Modified: Fri, 15 May 2020 16:53:44 GMT  
		Size: 7.0 MB (7033534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e37951fe3e21e2afb2d25fe8ec18da89f27d40c88b7e83b5991380af42227`  
		Last Modified: Fri, 15 May 2020 16:53:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b778ce965d8bdff427c804f43a751b2c4e1dc26ba152f53d4abe56a8b4014174`  
		Last Modified: Fri, 15 May 2020 16:53:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:457f1b0ba059ac05ce46805c92967506f61bb69a38eea8a5aaebf1d5d8da5017
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34547915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ef03b25863b64392c6d8ff085e6b0768f88c8b95692196f79c4846e8f38277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 12:44:06 GMT
ADD file:b305c1792102142f183d3084026f0fc6be3ddf8d1959b32f0a5d22d35eebcd15 in / 
# Fri, 15 May 2020 12:44:07 GMT
CMD ["bash"]
# Sat, 16 May 2020 08:24:10 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 08:24:10 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 08:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 08:27:04 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 08:27:05 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 08:27:05 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 08:28:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:28:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:28:09 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:28:10 GMT
WORKDIR /data
# Sat, 16 May 2020 08:28:11 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 08:28:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:28:12 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:28:12 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8a7e1e68c24e5cac20ef26d29505c58456b561c431f0c683b66d1a0943f40dd4`  
		Last Modified: Fri, 15 May 2020 12:53:36 GMT  
		Size: 25.9 MB (25857195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc5ca4e8f484b410989ac557169938b5fe6288ed5add0839e05a790ef47676`  
		Last Modified: Sat, 16 May 2020 08:28:42 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eccfc30e2be16f57d04f487ed80dd2b52ada557753eca7c79eb2ff88ab421f2`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 1.4 MB (1352995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27089b3134bdd932f8ebb93aef02f95e6883cebfef343a3caad67c05fcc554d9`  
		Last Modified: Sat, 16 May 2020 08:29:17 GMT  
		Size: 7.3 MB (7335450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35769aa5a1907ee966e04244b585d65a7a780c87efb002cf6abdbe16f153d7b`  
		Last Modified: Sat, 16 May 2020 08:29:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e99e4e05b4653f243c0f8a635a0cb3fb3c367a3d2b73667db0301d0f869f14e`  
		Last Modified: Sat, 16 May 2020 08:29:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9` - linux; 386

```console
$ docker pull redis@sha256:cbd966cd9fdfda6ba7a4ae65566b21c986580d26bccd7648b431417c79a8797e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372a1f57ccac9f9940a9a3ef51392b6ae15c3b1102c3494fb808505bdc549b2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Sat, 16 May 2020 00:07:24 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 00:07:24 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 00:07:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 00:13:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:13:21 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:13:21 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:13:21 GMT
WORKDIR /data
# Sat, 16 May 2020 00:13:22 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 00:13:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:13:22 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:13:23 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157733bfb7391a76ac45c4aa7ed1ea9e99ee6b2f4f70fbbab7b48b514fff73fc`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7927326d7d556c02a6f3c72888c9f9d2beb780c097c9fb1ca55539afa2a42d`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.4 MB (1387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346dcb0e7c24e02011edcae7f0884ff428c9b01cd1361cfb068c4cb5ea6c3f5f`  
		Last Modified: Sat, 16 May 2020 00:14:11 GMT  
		Size: 7.0 MB (7008096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19378b87aaceac51732681a095c2679c50ac66b341a727cc4c59c7672e72642b`  
		Last Modified: Sat, 16 May 2020 00:14:09 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d89103e3ff26e632031f9510e343c0480df8aa67080da4f4fe1cd70671a94b2`  
		Last Modified: Sat, 16 May 2020 00:14:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9` - linux; mips64le

```console
$ docker pull redis@sha256:8b6a10293e59139fa6bcc9fc4b76fa1bece970cbca46f0d4f88ba87ca29fb38d
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34733957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14f6ea4c9fdcd70e15b3ec9963dbf5b3a0cba06b78eca3b49ede54d8eb74633`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 04:48:19 GMT
ADD file:1163d3a5831eb58d132b66b60303169816e7bd8289f19caaac1157179a95f6f9 in / 
# Fri, 15 May 2020 04:48:19 GMT
CMD ["bash"]
# Fri, 15 May 2020 15:35:02 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 15:35:02 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 15:35:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 15:39:12 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 15:39:12 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 15:39:13 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 15:42:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 15:42:32 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 15:42:33 GMT
VOLUME [/data]
# Fri, 15 May 2020 15:42:33 GMT
WORKDIR /data
# Fri, 15 May 2020 15:42:34 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 15:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 15:42:34 GMT
EXPOSE 6379
# Fri, 15 May 2020 15:42:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d22357c747999d33ec7501da2c05aa9e95079ebddefbcb326976c5ed5b176b3f`  
		Last Modified: Fri, 15 May 2020 04:57:10 GMT  
		Size: 25.8 MB (25764292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f562c9b9683468308a6f59cab7d724ffc3b35a66acd8ce093b288144db2b7c5`  
		Last Modified: Fri, 15 May 2020 15:42:49 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fda93ec518be6790dd5e435d4bb66cab95d5c14044f01c584fd463ca6ffd290`  
		Last Modified: Fri, 15 May 2020 15:42:50 GMT  
		Size: 1.3 MB (1305516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeb925910423da69c6eda33089a17133d5b1649da9305c560bb62548887111c`  
		Last Modified: Fri, 15 May 2020 15:43:33 GMT  
		Size: 7.7 MB (7661910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89a2cb8235be9f7742a87b9e6cb1a8e822fa316f9524eb2e63e180907993838`  
		Last Modified: Fri, 15 May 2020 15:43:26 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe01516addcda29424d0863a92cc972db77274689603262287f4383b2251fb0`  
		Last Modified: Fri, 15 May 2020 15:43:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9` - linux; ppc64le

```console
$ docker pull redis@sha256:c25f3deade6ecb0d0ab42fa53321c50806dd2471c0a06ec3180217c93e2b50e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39696499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7993e4f9c4d285dffe1be6b2eb7fc6e5872e4c23175ef0b2eecb2f4dfd9c09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 16 May 2020 17:14:59 GMT
ADD file:b2656a1711bd47585595ae2927cfd4ec00eb903d193583d945b6d60f0a2691bb in / 
# Sat, 16 May 2020 17:15:04 GMT
CMD ["bash"]
# Mon, 18 May 2020 13:30:23 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Mon, 18 May 2020 13:30:26 GMT
ENV GOSU_VERSION=1.12
# Mon, 18 May 2020 13:32:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 18 May 2020 13:38:55 GMT
ENV REDIS_VERSION=5.0.9
# Mon, 18 May 2020 13:38:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Mon, 18 May 2020 13:39:03 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Mon, 18 May 2020 13:41:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:41:57 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:41:59 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:42:03 GMT
WORKDIR /data
# Mon, 18 May 2020 13:42:06 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Mon, 18 May 2020 13:42:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:42:11 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:42:14 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:034d508ed7647e7139951a435acc95e0124f50c984670d0e53b4f5ba25cf6ed1`  
		Last Modified: Sat, 16 May 2020 18:31:49 GMT  
		Size: 30.5 MB (30524456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c613ed63b519e3a0419cf56e14127f5d25466416a8143341540d12cb99943b65`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec60488415c29ebe96bbfabff01925147e50ee55136fdf961fbe8526617f3b`  
		Last Modified: Mon, 18 May 2020 13:42:57 GMT  
		Size: 1.3 MB (1335429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8c21d1569eb7d014ba9bf44dee78260d5e4d8e456b37cb304b127c69940684`  
		Last Modified: Mon, 18 May 2020 13:43:54 GMT  
		Size: 7.8 MB (7834331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c759fe2a72a81200077dd4a171c8c95ea1cecdc62e8a2ae362e0d31f255fc9f9`  
		Last Modified: Mon, 18 May 2020 13:43:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da932920c36a309064e131257fe3ed53362fb1a0d18207a51e7a26735b066838`  
		Last Modified: Mon, 18 May 2020 13:43:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9` - linux; s390x

```console
$ docker pull redis@sha256:becaadf1b7481b782ca8d0ed939de5e00ca69064a94eef114d443bb75116c1f3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34710318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dba1a9e6bde97648f54ed3508c268f0671bdf3b171629e8a034800658e2ea36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 05:15:35 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 05:15:35 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 05:15:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 05:17:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 05:17:06 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 05:17:06 GMT
VOLUME [/data]
# Fri, 15 May 2020 05:17:06 GMT
WORKDIR /data
# Fri, 15 May 2020 05:17:07 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 05:17:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 05:17:07 GMT
EXPOSE 6379
# Fri, 15 May 2020 05:17:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e40cd0998be29e9cce5152b7d3644b03b888bcca5db2049d43c93bf53185d`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc1e5303c90f8fcd807a5042757fb4de087ae4b3319afca416b72e858de788c`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.4 MB (1403711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fff5a343dd72b836a3f99619249e4fd4b82b0d09950a9552781d2fcbe733c9`  
		Last Modified: Fri, 15 May 2020 05:17:43 GMT  
		Size: 7.6 MB (7591396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30482d87111f841181c863a01b1ad9890bab844f7bf3f24c8de746052ebc5d71`  
		Last Modified: Fri, 15 May 2020 05:17:42 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a814c5126e00d2ce60c95caacba2b4f8236c88df49bcaf578c2500a12404dc3`  
		Last Modified: Fri, 15 May 2020 05:17:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5.0.9-32bit`

```console
$ docker pull redis@sha256:3b14d8ad7934452ffe28a95c5931ea8cf4a6e8771d2afc394836fc220c4ddf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redis:5.0.9-32bit` - linux; amd64

```console
$ docker pull redis@sha256:1c6e5965741e36f16ce589d4fbfce72fadc9d6bcf7b6f458e9d29772c8978275
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40577472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51da9d4e9b00184c7e706cc1f8471c8aafa7f5da3e92655613d5f4e2944ea82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 02:15:48 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 02:19:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev-i386 gcc-multilib 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:19:43 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:19:43 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:19:43 GMT
WORKDIR /data
# Sat, 16 May 2020 02:19:44 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:19:44 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:19:45 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52db9932f76ff160dd7194254956eccd2857a82675be95f689601345919dac8e`  
		Last Modified: Sat, 16 May 2020 02:20:50 GMT  
		Size: 12.1 MB (12058755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64def67d4f9860909ddb35febdfdf94e31ec29c620e2e207e20c2f0f1e92ab07`  
		Last Modified: Sat, 16 May 2020 02:20:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeed70e76f4d345e003e569a8ec0a354771d42efcbcb26b94aea29d64a85272e`  
		Last Modified: Sat, 16 May 2020 02:20:48 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5.0.9-32bit-buster`

```console
$ docker pull redis@sha256:3b14d8ad7934452ffe28a95c5931ea8cf4a6e8771d2afc394836fc220c4ddf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redis:5.0.9-32bit-buster` - linux; amd64

```console
$ docker pull redis@sha256:1c6e5965741e36f16ce589d4fbfce72fadc9d6bcf7b6f458e9d29772c8978275
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40577472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51da9d4e9b00184c7e706cc1f8471c8aafa7f5da3e92655613d5f4e2944ea82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 02:15:48 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 02:19:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev-i386 gcc-multilib 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:19:43 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:19:43 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:19:43 GMT
WORKDIR /data
# Sat, 16 May 2020 02:19:44 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:19:44 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:19:45 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52db9932f76ff160dd7194254956eccd2857a82675be95f689601345919dac8e`  
		Last Modified: Sat, 16 May 2020 02:20:50 GMT  
		Size: 12.1 MB (12058755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64def67d4f9860909ddb35febdfdf94e31ec29c620e2e207e20c2f0f1e92ab07`  
		Last Modified: Sat, 16 May 2020 02:20:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeed70e76f4d345e003e569a8ec0a354771d42efcbcb26b94aea29d64a85272e`  
		Last Modified: Sat, 16 May 2020 02:20:48 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5.0.9-alpine`

```console
$ docker pull redis@sha256:83a3af36d5e57f2901b4783c313720e5fa3ecf0424ba86ad9775e06a9a5e35d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:5.0.9-alpine` - linux; amd64

```console
$ docker pull redis@sha256:d4ada5d910403607b3f579d7171f36108c2e1cf67da966a712812230171fc153
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9998790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3661c84ee9d0f6312a076b69eb2bd112674cadb70ef7e1594c4f00193f8df08e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:19:42 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 19:19:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 19:20:54 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 19:20:54 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 19:20:55 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 19:21:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 19:21:49 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 19:21:49 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 19:21:50 GMT
WORKDIR /data
# Fri, 24 Apr 2020 19:21:50 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 19:21:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 19:21:50 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 19:21:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0373118a0d956ca0ee963e307457f45f073db9096f7c6f87c10251d071f0dc`  
		Last Modified: Fri, 24 Apr 2020 19:23:01 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd369fe62565d644723bfdb734c4ecb2a96191366ec08424146aa9c5ff6b308`  
		Last Modified: Fri, 24 Apr 2020 19:23:02 GMT  
		Size: 402.6 KB (402568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e45770272d96deeb96c4bfa3cffde811f318823b4422bdbbf909148dc5669bb`  
		Last Modified: Fri, 24 Apr 2020 19:23:14 GMT  
		Size: 6.8 MB (6781166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558de8ea3153bdccfaf67fadf7bbbdc60bf357f33ff0070df617d6e22ad46a13`  
		Last Modified: Fri, 24 Apr 2020 19:23:13 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c65255161264f51556db666aa812834b3f51c8403b09799a46e4d0909e4aa4`  
		Last Modified: Fri, 24 Apr 2020 19:23:12 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:867b50998330ae4743e95c8be69dee7ad37cbba8057659bef4dc142838d7f3e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9725047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333723767b2b5747763b5483d4742558e9abe6d70b98ee05d527643b5eb088d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:30:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 23 Apr 2020 22:30:20 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 23 Apr 2020 22:31:34 GMT
ENV REDIS_VERSION=5.0.9
# Thu, 23 Apr 2020 22:31:35 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Thu, 23 Apr 2020 22:31:36 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Thu, 23 Apr 2020 22:32:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 23 Apr 2020 22:32:27 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 23 Apr 2020 22:32:29 GMT
VOLUME [/data]
# Thu, 23 Apr 2020 22:32:30 GMT
WORKDIR /data
# Thu, 23 Apr 2020 22:32:31 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 23 Apr 2020 22:32:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 22:32:33 GMT
EXPOSE 6379
# Thu, 23 Apr 2020 22:32:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab5b04292d1974b3feedf74dddf563efe3ba5b5c38239a49e8adf0ac8140028`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af20f6a7bee5bf869254b4964c1a5d8dd5ef1353ac48081a885920682312555b`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 405.8 KB (405799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a2919ec032b1198ca13b052499b7c193e45d93756a3b0d7bb10c8db4f3db65`  
		Last Modified: Thu, 23 Apr 2020 22:34:01 GMT  
		Size: 6.7 MB (6697511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b2e77e4c2604e8e74b4c471b4a04d1a768eb84eadcfcd3621f135f7d4d90ca`  
		Last Modified: Thu, 23 Apr 2020 22:33:57 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18df89faaf97292802f6bca82a98892b7b0a168230ca31ae16e3cf307614a7a8`  
		Last Modified: Thu, 23 Apr 2020 22:33:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:1c10570f57cb14b4fbd3446c61303aeb7db18b45abffc49974d5bde7e4a89de4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9394623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a7ba195be67da9c68c67aa8d6eefa737236f15d3a9b490504ce943465c3a9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:51:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 08:51:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 08:52:43 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 08:52:43 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 08:52:44 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 08:53:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 08:53:30 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 08:53:31 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 08:53:32 GMT
WORKDIR /data
# Fri, 24 Apr 2020 08:53:32 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 08:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 08:53:34 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 08:53:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0765e03c998449baf4c76a1011cf80e6ab974db3d5d8da3a361bfeeb875d96db`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07fda5f4761823162fa661b4466f517ad5db025d9689c123221af67af9b53f`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 399.8 KB (399779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531954b17ac2db3cd86f3ced48c7c4f9fe053fad0792b7038321a667c911953a`  
		Last Modified: Fri, 24 Apr 2020 08:55:41 GMT  
		Size: 6.6 MB (6570977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d550a31e99202186ed01f1a5a4c96bab49dc143ad2a113696ecb48947836c0`  
		Last Modified: Fri, 24 Apr 2020 08:55:38 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a842b77b23971198e093c671bcf1e2cf6df771a6138ffb4132bfb37af22f17`  
		Last Modified: Fri, 24 Apr 2020 08:55:38 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:2ebdecb52315772800ba4549b9dc83910d9ae7de5364c3092b0390d7266e94a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9918976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6acb4ad7ccdd962d8579a0929ab5920a1f58ff996cd4812188219c1eb74e91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:45:10 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 12:45:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 12:46:32 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 12:46:33 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 12:46:34 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 12:47:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 12:47:24 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 12:47:24 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 12:47:25 GMT
WORKDIR /data
# Fri, 24 Apr 2020 12:47:26 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 12:47:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 12:47:28 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 12:47:29 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7050d23898adae8e4a2e0ab67eaeab9f9a9ec0fa5b88b128eeff4de1570877`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8982b178d819b1f2f10c3375b2c7ed054157cc5e711b58b6a2dcb376686e5d59`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 404.7 KB (404661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ca1db598d2278e5526b65dcad0d96f0f0264060f879f1b437f58a467e27382`  
		Last Modified: Fri, 24 Apr 2020 12:49:17 GMT  
		Size: 6.8 MB (6788089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87542dce16ad38aeb18ffe2e2266f3bd9b8cbc70f6f4450be0e9f621022fabb5`  
		Last Modified: Fri, 24 Apr 2020 12:49:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a20d19811afde1a300515cade1279f18fb3ca0ef1800b52dcb45127731bd5f4`  
		Last Modified: Fri, 24 Apr 2020 12:49:15 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-alpine` - linux; 386

```console
$ docker pull redis@sha256:3ab6896b5efe215c5cc110a835fecb73d5f55672ad4443f4baf51822db1854c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9710040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba820d7067104939d7ec907ee1fa581e9c7d40b0a204a14caf709f4dce84732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:49:36 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 05:49:38 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 05:52:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 05:52:17 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 05:52:17 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 05:52:17 GMT
WORKDIR /data
# Fri, 24 Apr 2020 05:52:17 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 05:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 05:52:18 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 05:52:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4eb71d5f124b9b51684034d7d96fba6399ff6892995e51137d0c0617a11fb9`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7685edc32d5ef38faf3beb4310c119862b1dfa18ea58edb0dbca84e9417b267`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 407.9 KB (407901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed6bb387586efb069405e1b2fea60bf1718da22582dade16723a6ce6beb111c`  
		Last Modified: Fri, 24 Apr 2020 05:53:49 GMT  
		Size: 6.5 MB (6491980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ee2bc48c46cc40ec8951486a93e65583168f55239b5e10e350ceda82120fa3`  
		Last Modified: Fri, 24 Apr 2020 05:53:48 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae5b0c59c675cf868993ca6ec424636476caea5bc4e43525a866864d0b8bbd1`  
		Last Modified: Fri, 24 Apr 2020 05:53:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:14dfcd56148c897338a1306bf23b392e6ffce4ee486ddfcd77fb515e8f0f1557
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0a1b6eb6701cd8c4349958777c681d81e0520d3e82317e2419b56b4d4ce4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:02:06 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 09:02:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 09:03:45 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 09:03:48 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 09:03:50 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 09:04:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 09:04:46 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 09:04:50 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 09:04:53 GMT
WORKDIR /data
# Fri, 24 Apr 2020 09:04:56 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 09:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 09:05:01 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 09:05:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc79e36a18515157312416d029cb35887ee8668b53b6c0e3867a4d0dd8dd231`  
		Last Modified: Fri, 24 Apr 2020 09:06:56 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83078862453fa1de07d734ccc5b995c92cd74710488c11d066ad752e3402d`  
		Last Modified: Fri, 24 Apr 2020 09:06:57 GMT  
		Size: 409.9 KB (409875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad3f9cade0fa9bda2c0f45df3a77c780ebc4adea7badb3b8387fed928c60ed7`  
		Last Modified: Fri, 24 Apr 2020 09:07:21 GMT  
		Size: 7.3 MB (7260512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ad499a196593cd717672adacc0550293f8b2c00a5907255640b27d266bc05a`  
		Last Modified: Fri, 24 Apr 2020 09:07:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5831b0ffd2731f416315c93a640459b17492812a21b7a6fba00919faaeb1d5`  
		Last Modified: Fri, 24 Apr 2020 09:07:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-alpine` - linux; s390x

```console
$ docker pull redis@sha256:5ad55b9f660c1e3b315e26e3497b9e4d270a5dd7ff431b14d9a17cf78fcac287
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10008638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dd64fd99b54ef1c40f2cd3351efcaf43b4d026dfcfe78315787e7a8220ffee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:02:35 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 07:02:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 07:03:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 07:03:53 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 07:03:53 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 07:03:54 GMT
WORKDIR /data
# Fri, 24 Apr 2020 07:03:54 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 07:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 07:03:54 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 07:03:54 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2da1b54f68b54cfd646e4cf510a14593b857e3c6e7732985b5a3bc5e213a72a`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f0a46f7a997ac6f05cd804b3a0f56c74348f25fd9e164c66ab7c5c4a6a2c82`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 407.4 KB (407392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3c809e9bcb4892e2da01d3bae84664c06e6bb0929c6813ef47a1aaaa3d675f`  
		Last Modified: Fri, 24 Apr 2020 07:05:07 GMT  
		Size: 7.0 MB (7016584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1cb7e35314fbaf45935cb538fb36cc01e53dff4d37131a3497fd376720294e`  
		Last Modified: Fri, 24 Apr 2020 07:05:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529922dc84cb9fec77a0630b9ad535a7c843db2cd4518c25442c47fbc986d8b7`  
		Last Modified: Fri, 24 Apr 2020 07:05:06 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5.0.9-alpine3.11`

```console
$ docker pull redis@sha256:83a3af36d5e57f2901b4783c313720e5fa3ecf0424ba86ad9775e06a9a5e35d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:5.0.9-alpine3.11` - linux; amd64

```console
$ docker pull redis@sha256:d4ada5d910403607b3f579d7171f36108c2e1cf67da966a712812230171fc153
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9998790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3661c84ee9d0f6312a076b69eb2bd112674cadb70ef7e1594c4f00193f8df08e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:19:42 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 19:19:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 19:20:54 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 19:20:54 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 19:20:55 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 19:21:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 19:21:49 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 19:21:49 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 19:21:50 GMT
WORKDIR /data
# Fri, 24 Apr 2020 19:21:50 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 19:21:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 19:21:50 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 19:21:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0373118a0d956ca0ee963e307457f45f073db9096f7c6f87c10251d071f0dc`  
		Last Modified: Fri, 24 Apr 2020 19:23:01 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd369fe62565d644723bfdb734c4ecb2a96191366ec08424146aa9c5ff6b308`  
		Last Modified: Fri, 24 Apr 2020 19:23:02 GMT  
		Size: 402.6 KB (402568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e45770272d96deeb96c4bfa3cffde811f318823b4422bdbbf909148dc5669bb`  
		Last Modified: Fri, 24 Apr 2020 19:23:14 GMT  
		Size: 6.8 MB (6781166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558de8ea3153bdccfaf67fadf7bbbdc60bf357f33ff0070df617d6e22ad46a13`  
		Last Modified: Fri, 24 Apr 2020 19:23:13 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c65255161264f51556db666aa812834b3f51c8403b09799a46e4d0909e4aa4`  
		Last Modified: Fri, 24 Apr 2020 19:23:12 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-alpine3.11` - linux; arm variant v6

```console
$ docker pull redis@sha256:867b50998330ae4743e95c8be69dee7ad37cbba8057659bef4dc142838d7f3e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9725047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333723767b2b5747763b5483d4742558e9abe6d70b98ee05d527643b5eb088d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:30:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 23 Apr 2020 22:30:20 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 23 Apr 2020 22:31:34 GMT
ENV REDIS_VERSION=5.0.9
# Thu, 23 Apr 2020 22:31:35 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Thu, 23 Apr 2020 22:31:36 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Thu, 23 Apr 2020 22:32:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 23 Apr 2020 22:32:27 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 23 Apr 2020 22:32:29 GMT
VOLUME [/data]
# Thu, 23 Apr 2020 22:32:30 GMT
WORKDIR /data
# Thu, 23 Apr 2020 22:32:31 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 23 Apr 2020 22:32:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 22:32:33 GMT
EXPOSE 6379
# Thu, 23 Apr 2020 22:32:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab5b04292d1974b3feedf74dddf563efe3ba5b5c38239a49e8adf0ac8140028`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af20f6a7bee5bf869254b4964c1a5d8dd5ef1353ac48081a885920682312555b`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 405.8 KB (405799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a2919ec032b1198ca13b052499b7c193e45d93756a3b0d7bb10c8db4f3db65`  
		Last Modified: Thu, 23 Apr 2020 22:34:01 GMT  
		Size: 6.7 MB (6697511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b2e77e4c2604e8e74b4c471b4a04d1a768eb84eadcfcd3621f135f7d4d90ca`  
		Last Modified: Thu, 23 Apr 2020 22:33:57 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18df89faaf97292802f6bca82a98892b7b0a168230ca31ae16e3cf307614a7a8`  
		Last Modified: Thu, 23 Apr 2020 22:33:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-alpine3.11` - linux; arm variant v7

```console
$ docker pull redis@sha256:1c10570f57cb14b4fbd3446c61303aeb7db18b45abffc49974d5bde7e4a89de4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9394623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a7ba195be67da9c68c67aa8d6eefa737236f15d3a9b490504ce943465c3a9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:51:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 08:51:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 08:52:43 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 08:52:43 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 08:52:44 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 08:53:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 08:53:30 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 08:53:31 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 08:53:32 GMT
WORKDIR /data
# Fri, 24 Apr 2020 08:53:32 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 08:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 08:53:34 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 08:53:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0765e03c998449baf4c76a1011cf80e6ab974db3d5d8da3a361bfeeb875d96db`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07fda5f4761823162fa661b4466f517ad5db025d9689c123221af67af9b53f`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 399.8 KB (399779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531954b17ac2db3cd86f3ced48c7c4f9fe053fad0792b7038321a667c911953a`  
		Last Modified: Fri, 24 Apr 2020 08:55:41 GMT  
		Size: 6.6 MB (6570977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d550a31e99202186ed01f1a5a4c96bab49dc143ad2a113696ecb48947836c0`  
		Last Modified: Fri, 24 Apr 2020 08:55:38 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a842b77b23971198e093c671bcf1e2cf6df771a6138ffb4132bfb37af22f17`  
		Last Modified: Fri, 24 Apr 2020 08:55:38 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-alpine3.11` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:2ebdecb52315772800ba4549b9dc83910d9ae7de5364c3092b0390d7266e94a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9918976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6acb4ad7ccdd962d8579a0929ab5920a1f58ff996cd4812188219c1eb74e91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:45:10 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 12:45:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 12:46:32 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 12:46:33 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 12:46:34 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 12:47:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 12:47:24 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 12:47:24 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 12:47:25 GMT
WORKDIR /data
# Fri, 24 Apr 2020 12:47:26 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 12:47:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 12:47:28 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 12:47:29 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7050d23898adae8e4a2e0ab67eaeab9f9a9ec0fa5b88b128eeff4de1570877`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8982b178d819b1f2f10c3375b2c7ed054157cc5e711b58b6a2dcb376686e5d59`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 404.7 KB (404661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ca1db598d2278e5526b65dcad0d96f0f0264060f879f1b437f58a467e27382`  
		Last Modified: Fri, 24 Apr 2020 12:49:17 GMT  
		Size: 6.8 MB (6788089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87542dce16ad38aeb18ffe2e2266f3bd9b8cbc70f6f4450be0e9f621022fabb5`  
		Last Modified: Fri, 24 Apr 2020 12:49:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a20d19811afde1a300515cade1279f18fb3ca0ef1800b52dcb45127731bd5f4`  
		Last Modified: Fri, 24 Apr 2020 12:49:15 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-alpine3.11` - linux; 386

```console
$ docker pull redis@sha256:3ab6896b5efe215c5cc110a835fecb73d5f55672ad4443f4baf51822db1854c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9710040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba820d7067104939d7ec907ee1fa581e9c7d40b0a204a14caf709f4dce84732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:49:36 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 05:49:38 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 05:52:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 05:52:17 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 05:52:17 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 05:52:17 GMT
WORKDIR /data
# Fri, 24 Apr 2020 05:52:17 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 05:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 05:52:18 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 05:52:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4eb71d5f124b9b51684034d7d96fba6399ff6892995e51137d0c0617a11fb9`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7685edc32d5ef38faf3beb4310c119862b1dfa18ea58edb0dbca84e9417b267`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 407.9 KB (407901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed6bb387586efb069405e1b2fea60bf1718da22582dade16723a6ce6beb111c`  
		Last Modified: Fri, 24 Apr 2020 05:53:49 GMT  
		Size: 6.5 MB (6491980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ee2bc48c46cc40ec8951486a93e65583168f55239b5e10e350ceda82120fa3`  
		Last Modified: Fri, 24 Apr 2020 05:53:48 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae5b0c59c675cf868993ca6ec424636476caea5bc4e43525a866864d0b8bbd1`  
		Last Modified: Fri, 24 Apr 2020 05:53:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-alpine3.11` - linux; ppc64le

```console
$ docker pull redis@sha256:14dfcd56148c897338a1306bf23b392e6ffce4ee486ddfcd77fb515e8f0f1557
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0a1b6eb6701cd8c4349958777c681d81e0520d3e82317e2419b56b4d4ce4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:02:06 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 09:02:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 09:03:45 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 09:03:48 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 09:03:50 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 09:04:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 09:04:46 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 09:04:50 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 09:04:53 GMT
WORKDIR /data
# Fri, 24 Apr 2020 09:04:56 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 09:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 09:05:01 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 09:05:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc79e36a18515157312416d029cb35887ee8668b53b6c0e3867a4d0dd8dd231`  
		Last Modified: Fri, 24 Apr 2020 09:06:56 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83078862453fa1de07d734ccc5b995c92cd74710488c11d066ad752e3402d`  
		Last Modified: Fri, 24 Apr 2020 09:06:57 GMT  
		Size: 409.9 KB (409875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad3f9cade0fa9bda2c0f45df3a77c780ebc4adea7badb3b8387fed928c60ed7`  
		Last Modified: Fri, 24 Apr 2020 09:07:21 GMT  
		Size: 7.3 MB (7260512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ad499a196593cd717672adacc0550293f8b2c00a5907255640b27d266bc05a`  
		Last Modified: Fri, 24 Apr 2020 09:07:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5831b0ffd2731f416315c93a640459b17492812a21b7a6fba00919faaeb1d5`  
		Last Modified: Fri, 24 Apr 2020 09:07:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-alpine3.11` - linux; s390x

```console
$ docker pull redis@sha256:5ad55b9f660c1e3b315e26e3497b9e4d270a5dd7ff431b14d9a17cf78fcac287
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10008638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dd64fd99b54ef1c40f2cd3351efcaf43b4d026dfcfe78315787e7a8220ffee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:02:35 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 07:02:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 07:03:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 07:03:53 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 07:03:53 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 07:03:54 GMT
WORKDIR /data
# Fri, 24 Apr 2020 07:03:54 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 07:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 07:03:54 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 07:03:54 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2da1b54f68b54cfd646e4cf510a14593b857e3c6e7732985b5a3bc5e213a72a`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f0a46f7a997ac6f05cd804b3a0f56c74348f25fd9e164c66ab7c5c4a6a2c82`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 407.4 KB (407392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3c809e9bcb4892e2da01d3bae84664c06e6bb0929c6813ef47a1aaaa3d675f`  
		Last Modified: Fri, 24 Apr 2020 07:05:07 GMT  
		Size: 7.0 MB (7016584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1cb7e35314fbaf45935cb538fb36cc01e53dff4d37131a3497fd376720294e`  
		Last Modified: Fri, 24 Apr 2020 07:05:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529922dc84cb9fec77a0630b9ad535a7c843db2cd4518c25442c47fbc986d8b7`  
		Last Modified: Fri, 24 Apr 2020 07:05:06 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5.0.9-buster`

```console
$ docker pull redis@sha256:08aab527ca57f536f2805e031535a6881bab63171146aa6414de69d54b14a84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redis:5.0.9-buster` - linux; amd64

```console
$ docker pull redis@sha256:ae4b7c01640a2688e9ef5dd630e2135df7a9e711e712e3d9eab05608d34e2b84
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35863829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5120d23bad51618dd0e19bddd616d555f3cb01753a930c9532364e0d2505b7e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 02:15:48 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 02:17:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:17:30 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:17:30 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:17:30 GMT
WORKDIR /data
# Sat, 16 May 2020 02:17:31 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:17:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:17:31 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:17:32 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846bf5faff48ca0599eb0ab51917d8471164ff02f04524d108bfc8b89dcf50cd`  
		Last Modified: Sat, 16 May 2020 02:20:41 GMT  
		Size: 7.3 MB (7345115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affafbdb5f81d8218bb0f3a60783e92e55fa09ba0a2488f3488488608fa1153d`  
		Last Modified: Sat, 16 May 2020 02:20:38 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdd19e5317241aa2fcd854961c766a5bfc18cbd0db01b18c91404ebdc2ccaa3`  
		Last Modified: Sat, 16 May 2020 02:20:39 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-buster` - linux; arm variant v5

```console
$ docker pull redis@sha256:aa487a40514e78f619cfcb9458a4cba51f5638916d8e4ed3bc10355d362963be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33396150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d3ebf62ba5747e68aa370dc62af6d166b2f494290cc0339c60f17aa271de77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 22:38:03 GMT
ADD file:cbd01ff8d2e40a25bcdb13dc19ffe124c2927b491997dc1c57d4f2c2a308e279 in / 
# Thu, 14 May 2020 22:38:05 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:40:59 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 04:40:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 04:41:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 04:43:01 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 04:43:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 04:43:02 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 04:44:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 04:44:09 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 04:44:09 GMT
VOLUME [/data]
# Fri, 15 May 2020 04:44:10 GMT
WORKDIR /data
# Fri, 15 May 2020 04:44:11 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 04:44:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 04:44:12 GMT
EXPOSE 6379
# Fri, 15 May 2020 04:44:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:24d81022117207b0239d8a8023ca1724b7dde38cb08ce5b9199f59d475d1e600`  
		Last Modified: Thu, 14 May 2020 22:46:51 GMT  
		Size: 24.8 MB (24838470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c13f680b58f95af37082529e8a1ecd6358e22a7e13a75344d8375a03cafb174`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2286bbfcebea1b30a2e862afd7742a7f65237dcabddc9486bfaaf5fd8ba0d65`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.4 MB (1376110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7deffa88c65075e285c0d27dc2aba2336a7a1779ed75bb2f32e760fbab785147`  
		Last Modified: Fri, 15 May 2020 04:44:47 GMT  
		Size: 7.2 MB (7179299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02c5ad0a586c0c745b5df9a3db37bcaf3213a48ab53be3446bd486fa5b85838`  
		Last Modified: Fri, 15 May 2020 04:44:44 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9850cd504042ad62e1898b73b9a1d5d4a95d80bf65a5909d238d56a640697226`  
		Last Modified: Fri, 15 May 2020 04:44:44 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-buster` - linux; arm variant v7

```console
$ docker pull redis@sha256:428b7a31e32fb1a39cc9d41b113e6051359572d96ae9d9906089f4c324a07173
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31109932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3abf0ee6b0b5453a72669cb38743da5af51666c9b3e18ab680cfb0c65e3241a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 01:00:06 GMT
ADD file:e3f9a454eccb40b4d7bf1dcc17ec29589a007ac67545d1cb5b6fa213c872c8f2 in / 
# Fri, 15 May 2020 01:00:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 16:49:40 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 16:49:40 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 16:50:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 16:51:47 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 16:51:48 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 16:51:49 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 16:52:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 16:52:49 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 16:52:50 GMT
VOLUME [/data]
# Fri, 15 May 2020 16:52:51 GMT
WORKDIR /data
# Fri, 15 May 2020 16:52:51 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 16:52:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 16:52:53 GMT
EXPOSE 6379
# Fri, 15 May 2020 16:52:53 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e41e28500352be59188c3d871a4b5a3f594350b860a9a36ed5808a35920bdae4`  
		Last Modified: Fri, 15 May 2020 01:11:21 GMT  
		Size: 22.7 MB (22705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6732859766aedad40f91cd96df6b5a6930efe6614b0f084b8459d93c22a69`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed92b736a14b52db74c7cd9919c66ce953393f0544906969081702697d5a6b54`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.4 MB (1368207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114f7e7289bd10cc75ccedb5c36ef2ef1bcdd04a0d015af0e3f5dbca67c2e2d9`  
		Last Modified: Fri, 15 May 2020 16:53:44 GMT  
		Size: 7.0 MB (7033534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e37951fe3e21e2afb2d25fe8ec18da89f27d40c88b7e83b5991380af42227`  
		Last Modified: Fri, 15 May 2020 16:53:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b778ce965d8bdff427c804f43a751b2c4e1dc26ba152f53d4abe56a8b4014174`  
		Last Modified: Fri, 15 May 2020 16:53:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-buster` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:457f1b0ba059ac05ce46805c92967506f61bb69a38eea8a5aaebf1d5d8da5017
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34547915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ef03b25863b64392c6d8ff085e6b0768f88c8b95692196f79c4846e8f38277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 12:44:06 GMT
ADD file:b305c1792102142f183d3084026f0fc6be3ddf8d1959b32f0a5d22d35eebcd15 in / 
# Fri, 15 May 2020 12:44:07 GMT
CMD ["bash"]
# Sat, 16 May 2020 08:24:10 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 08:24:10 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 08:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 08:27:04 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 08:27:05 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 08:27:05 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 08:28:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:28:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:28:09 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:28:10 GMT
WORKDIR /data
# Sat, 16 May 2020 08:28:11 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 08:28:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:28:12 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:28:12 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8a7e1e68c24e5cac20ef26d29505c58456b561c431f0c683b66d1a0943f40dd4`  
		Last Modified: Fri, 15 May 2020 12:53:36 GMT  
		Size: 25.9 MB (25857195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc5ca4e8f484b410989ac557169938b5fe6288ed5add0839e05a790ef47676`  
		Last Modified: Sat, 16 May 2020 08:28:42 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eccfc30e2be16f57d04f487ed80dd2b52ada557753eca7c79eb2ff88ab421f2`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 1.4 MB (1352995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27089b3134bdd932f8ebb93aef02f95e6883cebfef343a3caad67c05fcc554d9`  
		Last Modified: Sat, 16 May 2020 08:29:17 GMT  
		Size: 7.3 MB (7335450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35769aa5a1907ee966e04244b585d65a7a780c87efb002cf6abdbe16f153d7b`  
		Last Modified: Sat, 16 May 2020 08:29:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e99e4e05b4653f243c0f8a635a0cb3fb3c367a3d2b73667db0301d0f869f14e`  
		Last Modified: Sat, 16 May 2020 08:29:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-buster` - linux; 386

```console
$ docker pull redis@sha256:cbd966cd9fdfda6ba7a4ae65566b21c986580d26bccd7648b431417c79a8797e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372a1f57ccac9f9940a9a3ef51392b6ae15c3b1102c3494fb808505bdc549b2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Sat, 16 May 2020 00:07:24 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 00:07:24 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 00:07:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 00:13:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:13:21 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:13:21 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:13:21 GMT
WORKDIR /data
# Sat, 16 May 2020 00:13:22 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 00:13:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:13:22 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:13:23 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157733bfb7391a76ac45c4aa7ed1ea9e99ee6b2f4f70fbbab7b48b514fff73fc`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7927326d7d556c02a6f3c72888c9f9d2beb780c097c9fb1ca55539afa2a42d`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.4 MB (1387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346dcb0e7c24e02011edcae7f0884ff428c9b01cd1361cfb068c4cb5ea6c3f5f`  
		Last Modified: Sat, 16 May 2020 00:14:11 GMT  
		Size: 7.0 MB (7008096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19378b87aaceac51732681a095c2679c50ac66b341a727cc4c59c7672e72642b`  
		Last Modified: Sat, 16 May 2020 00:14:09 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d89103e3ff26e632031f9510e343c0480df8aa67080da4f4fe1cd70671a94b2`  
		Last Modified: Sat, 16 May 2020 00:14:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-buster` - linux; mips64le

```console
$ docker pull redis@sha256:8b6a10293e59139fa6bcc9fc4b76fa1bece970cbca46f0d4f88ba87ca29fb38d
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34733957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14f6ea4c9fdcd70e15b3ec9963dbf5b3a0cba06b78eca3b49ede54d8eb74633`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 04:48:19 GMT
ADD file:1163d3a5831eb58d132b66b60303169816e7bd8289f19caaac1157179a95f6f9 in / 
# Fri, 15 May 2020 04:48:19 GMT
CMD ["bash"]
# Fri, 15 May 2020 15:35:02 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 15:35:02 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 15:35:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 15:39:12 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 15:39:12 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 15:39:13 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 15:42:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 15:42:32 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 15:42:33 GMT
VOLUME [/data]
# Fri, 15 May 2020 15:42:33 GMT
WORKDIR /data
# Fri, 15 May 2020 15:42:34 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 15:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 15:42:34 GMT
EXPOSE 6379
# Fri, 15 May 2020 15:42:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d22357c747999d33ec7501da2c05aa9e95079ebddefbcb326976c5ed5b176b3f`  
		Last Modified: Fri, 15 May 2020 04:57:10 GMT  
		Size: 25.8 MB (25764292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f562c9b9683468308a6f59cab7d724ffc3b35a66acd8ce093b288144db2b7c5`  
		Last Modified: Fri, 15 May 2020 15:42:49 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fda93ec518be6790dd5e435d4bb66cab95d5c14044f01c584fd463ca6ffd290`  
		Last Modified: Fri, 15 May 2020 15:42:50 GMT  
		Size: 1.3 MB (1305516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeb925910423da69c6eda33089a17133d5b1649da9305c560bb62548887111c`  
		Last Modified: Fri, 15 May 2020 15:43:33 GMT  
		Size: 7.7 MB (7661910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89a2cb8235be9f7742a87b9e6cb1a8e822fa316f9524eb2e63e180907993838`  
		Last Modified: Fri, 15 May 2020 15:43:26 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe01516addcda29424d0863a92cc972db77274689603262287f4383b2251fb0`  
		Last Modified: Fri, 15 May 2020 15:43:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-buster` - linux; ppc64le

```console
$ docker pull redis@sha256:c25f3deade6ecb0d0ab42fa53321c50806dd2471c0a06ec3180217c93e2b50e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39696499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7993e4f9c4d285dffe1be6b2eb7fc6e5872e4c23175ef0b2eecb2f4dfd9c09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 16 May 2020 17:14:59 GMT
ADD file:b2656a1711bd47585595ae2927cfd4ec00eb903d193583d945b6d60f0a2691bb in / 
# Sat, 16 May 2020 17:15:04 GMT
CMD ["bash"]
# Mon, 18 May 2020 13:30:23 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Mon, 18 May 2020 13:30:26 GMT
ENV GOSU_VERSION=1.12
# Mon, 18 May 2020 13:32:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 18 May 2020 13:38:55 GMT
ENV REDIS_VERSION=5.0.9
# Mon, 18 May 2020 13:38:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Mon, 18 May 2020 13:39:03 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Mon, 18 May 2020 13:41:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:41:57 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:41:59 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:42:03 GMT
WORKDIR /data
# Mon, 18 May 2020 13:42:06 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Mon, 18 May 2020 13:42:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:42:11 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:42:14 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:034d508ed7647e7139951a435acc95e0124f50c984670d0e53b4f5ba25cf6ed1`  
		Last Modified: Sat, 16 May 2020 18:31:49 GMT  
		Size: 30.5 MB (30524456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c613ed63b519e3a0419cf56e14127f5d25466416a8143341540d12cb99943b65`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec60488415c29ebe96bbfabff01925147e50ee55136fdf961fbe8526617f3b`  
		Last Modified: Mon, 18 May 2020 13:42:57 GMT  
		Size: 1.3 MB (1335429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8c21d1569eb7d014ba9bf44dee78260d5e4d8e456b37cb304b127c69940684`  
		Last Modified: Mon, 18 May 2020 13:43:54 GMT  
		Size: 7.8 MB (7834331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c759fe2a72a81200077dd4a171c8c95ea1cecdc62e8a2ae362e0d31f255fc9f9`  
		Last Modified: Mon, 18 May 2020 13:43:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da932920c36a309064e131257fe3ed53362fb1a0d18207a51e7a26735b066838`  
		Last Modified: Mon, 18 May 2020 13:43:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0.9-buster` - linux; s390x

```console
$ docker pull redis@sha256:becaadf1b7481b782ca8d0ed939de5e00ca69064a94eef114d443bb75116c1f3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34710318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dba1a9e6bde97648f54ed3508c268f0671bdf3b171629e8a034800658e2ea36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 05:15:35 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 05:15:35 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 05:15:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 05:17:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 05:17:06 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 05:17:06 GMT
VOLUME [/data]
# Fri, 15 May 2020 05:17:06 GMT
WORKDIR /data
# Fri, 15 May 2020 05:17:07 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 05:17:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 05:17:07 GMT
EXPOSE 6379
# Fri, 15 May 2020 05:17:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e40cd0998be29e9cce5152b7d3644b03b888bcca5db2049d43c93bf53185d`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc1e5303c90f8fcd807a5042757fb4de087ae4b3319afca416b72e858de788c`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.4 MB (1403711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fff5a343dd72b836a3f99619249e4fd4b82b0d09950a9552781d2fcbe733c9`  
		Last Modified: Fri, 15 May 2020 05:17:43 GMT  
		Size: 7.6 MB (7591396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30482d87111f841181c863a01b1ad9890bab844f7bf3f24c8de746052ebc5d71`  
		Last Modified: Fri, 15 May 2020 05:17:42 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a814c5126e00d2ce60c95caacba2b4f8236c88df49bcaf578c2500a12404dc3`  
		Last Modified: Fri, 15 May 2020 05:17:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5.0-alpine`

```console
$ docker pull redis@sha256:83a3af36d5e57f2901b4783c313720e5fa3ecf0424ba86ad9775e06a9a5e35d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:5.0-alpine` - linux; amd64

```console
$ docker pull redis@sha256:d4ada5d910403607b3f579d7171f36108c2e1cf67da966a712812230171fc153
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9998790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3661c84ee9d0f6312a076b69eb2bd112674cadb70ef7e1594c4f00193f8df08e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:19:42 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 19:19:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 19:20:54 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 19:20:54 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 19:20:55 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 19:21:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 19:21:49 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 19:21:49 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 19:21:50 GMT
WORKDIR /data
# Fri, 24 Apr 2020 19:21:50 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 19:21:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 19:21:50 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 19:21:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0373118a0d956ca0ee963e307457f45f073db9096f7c6f87c10251d071f0dc`  
		Last Modified: Fri, 24 Apr 2020 19:23:01 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd369fe62565d644723bfdb734c4ecb2a96191366ec08424146aa9c5ff6b308`  
		Last Modified: Fri, 24 Apr 2020 19:23:02 GMT  
		Size: 402.6 KB (402568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e45770272d96deeb96c4bfa3cffde811f318823b4422bdbbf909148dc5669bb`  
		Last Modified: Fri, 24 Apr 2020 19:23:14 GMT  
		Size: 6.8 MB (6781166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558de8ea3153bdccfaf67fadf7bbbdc60bf357f33ff0070df617d6e22ad46a13`  
		Last Modified: Fri, 24 Apr 2020 19:23:13 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c65255161264f51556db666aa812834b3f51c8403b09799a46e4d0909e4aa4`  
		Last Modified: Fri, 24 Apr 2020 19:23:12 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:867b50998330ae4743e95c8be69dee7ad37cbba8057659bef4dc142838d7f3e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9725047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333723767b2b5747763b5483d4742558e9abe6d70b98ee05d527643b5eb088d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:30:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 23 Apr 2020 22:30:20 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 23 Apr 2020 22:31:34 GMT
ENV REDIS_VERSION=5.0.9
# Thu, 23 Apr 2020 22:31:35 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Thu, 23 Apr 2020 22:31:36 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Thu, 23 Apr 2020 22:32:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 23 Apr 2020 22:32:27 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 23 Apr 2020 22:32:29 GMT
VOLUME [/data]
# Thu, 23 Apr 2020 22:32:30 GMT
WORKDIR /data
# Thu, 23 Apr 2020 22:32:31 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 23 Apr 2020 22:32:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 22:32:33 GMT
EXPOSE 6379
# Thu, 23 Apr 2020 22:32:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab5b04292d1974b3feedf74dddf563efe3ba5b5c38239a49e8adf0ac8140028`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af20f6a7bee5bf869254b4964c1a5d8dd5ef1353ac48081a885920682312555b`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 405.8 KB (405799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a2919ec032b1198ca13b052499b7c193e45d93756a3b0d7bb10c8db4f3db65`  
		Last Modified: Thu, 23 Apr 2020 22:34:01 GMT  
		Size: 6.7 MB (6697511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b2e77e4c2604e8e74b4c471b4a04d1a768eb84eadcfcd3621f135f7d4d90ca`  
		Last Modified: Thu, 23 Apr 2020 22:33:57 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18df89faaf97292802f6bca82a98892b7b0a168230ca31ae16e3cf307614a7a8`  
		Last Modified: Thu, 23 Apr 2020 22:33:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:1c10570f57cb14b4fbd3446c61303aeb7db18b45abffc49974d5bde7e4a89de4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9394623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a7ba195be67da9c68c67aa8d6eefa737236f15d3a9b490504ce943465c3a9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:51:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 08:51:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 08:52:43 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 08:52:43 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 08:52:44 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 08:53:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 08:53:30 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 08:53:31 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 08:53:32 GMT
WORKDIR /data
# Fri, 24 Apr 2020 08:53:32 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 08:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 08:53:34 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 08:53:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0765e03c998449baf4c76a1011cf80e6ab974db3d5d8da3a361bfeeb875d96db`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07fda5f4761823162fa661b4466f517ad5db025d9689c123221af67af9b53f`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 399.8 KB (399779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531954b17ac2db3cd86f3ced48c7c4f9fe053fad0792b7038321a667c911953a`  
		Last Modified: Fri, 24 Apr 2020 08:55:41 GMT  
		Size: 6.6 MB (6570977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d550a31e99202186ed01f1a5a4c96bab49dc143ad2a113696ecb48947836c0`  
		Last Modified: Fri, 24 Apr 2020 08:55:38 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a842b77b23971198e093c671bcf1e2cf6df771a6138ffb4132bfb37af22f17`  
		Last Modified: Fri, 24 Apr 2020 08:55:38 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:2ebdecb52315772800ba4549b9dc83910d9ae7de5364c3092b0390d7266e94a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9918976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6acb4ad7ccdd962d8579a0929ab5920a1f58ff996cd4812188219c1eb74e91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:45:10 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 12:45:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 12:46:32 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 12:46:33 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 12:46:34 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 12:47:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 12:47:24 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 12:47:24 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 12:47:25 GMT
WORKDIR /data
# Fri, 24 Apr 2020 12:47:26 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 12:47:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 12:47:28 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 12:47:29 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7050d23898adae8e4a2e0ab67eaeab9f9a9ec0fa5b88b128eeff4de1570877`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8982b178d819b1f2f10c3375b2c7ed054157cc5e711b58b6a2dcb376686e5d59`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 404.7 KB (404661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ca1db598d2278e5526b65dcad0d96f0f0264060f879f1b437f58a467e27382`  
		Last Modified: Fri, 24 Apr 2020 12:49:17 GMT  
		Size: 6.8 MB (6788089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87542dce16ad38aeb18ffe2e2266f3bd9b8cbc70f6f4450be0e9f621022fabb5`  
		Last Modified: Fri, 24 Apr 2020 12:49:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a20d19811afde1a300515cade1279f18fb3ca0ef1800b52dcb45127731bd5f4`  
		Last Modified: Fri, 24 Apr 2020 12:49:15 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-alpine` - linux; 386

```console
$ docker pull redis@sha256:3ab6896b5efe215c5cc110a835fecb73d5f55672ad4443f4baf51822db1854c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9710040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba820d7067104939d7ec907ee1fa581e9c7d40b0a204a14caf709f4dce84732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:49:36 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 05:49:38 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 05:52:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 05:52:17 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 05:52:17 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 05:52:17 GMT
WORKDIR /data
# Fri, 24 Apr 2020 05:52:17 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 05:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 05:52:18 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 05:52:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4eb71d5f124b9b51684034d7d96fba6399ff6892995e51137d0c0617a11fb9`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7685edc32d5ef38faf3beb4310c119862b1dfa18ea58edb0dbca84e9417b267`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 407.9 KB (407901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed6bb387586efb069405e1b2fea60bf1718da22582dade16723a6ce6beb111c`  
		Last Modified: Fri, 24 Apr 2020 05:53:49 GMT  
		Size: 6.5 MB (6491980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ee2bc48c46cc40ec8951486a93e65583168f55239b5e10e350ceda82120fa3`  
		Last Modified: Fri, 24 Apr 2020 05:53:48 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae5b0c59c675cf868993ca6ec424636476caea5bc4e43525a866864d0b8bbd1`  
		Last Modified: Fri, 24 Apr 2020 05:53:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:14dfcd56148c897338a1306bf23b392e6ffce4ee486ddfcd77fb515e8f0f1557
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0a1b6eb6701cd8c4349958777c681d81e0520d3e82317e2419b56b4d4ce4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:02:06 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 09:02:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 09:03:45 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 09:03:48 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 09:03:50 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 09:04:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 09:04:46 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 09:04:50 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 09:04:53 GMT
WORKDIR /data
# Fri, 24 Apr 2020 09:04:56 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 09:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 09:05:01 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 09:05:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc79e36a18515157312416d029cb35887ee8668b53b6c0e3867a4d0dd8dd231`  
		Last Modified: Fri, 24 Apr 2020 09:06:56 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83078862453fa1de07d734ccc5b995c92cd74710488c11d066ad752e3402d`  
		Last Modified: Fri, 24 Apr 2020 09:06:57 GMT  
		Size: 409.9 KB (409875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad3f9cade0fa9bda2c0f45df3a77c780ebc4adea7badb3b8387fed928c60ed7`  
		Last Modified: Fri, 24 Apr 2020 09:07:21 GMT  
		Size: 7.3 MB (7260512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ad499a196593cd717672adacc0550293f8b2c00a5907255640b27d266bc05a`  
		Last Modified: Fri, 24 Apr 2020 09:07:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5831b0ffd2731f416315c93a640459b17492812a21b7a6fba00919faaeb1d5`  
		Last Modified: Fri, 24 Apr 2020 09:07:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-alpine` - linux; s390x

```console
$ docker pull redis@sha256:5ad55b9f660c1e3b315e26e3497b9e4d270a5dd7ff431b14d9a17cf78fcac287
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10008638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dd64fd99b54ef1c40f2cd3351efcaf43b4d026dfcfe78315787e7a8220ffee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:02:35 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 07:02:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 07:03:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 07:03:53 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 07:03:53 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 07:03:54 GMT
WORKDIR /data
# Fri, 24 Apr 2020 07:03:54 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 07:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 07:03:54 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 07:03:54 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2da1b54f68b54cfd646e4cf510a14593b857e3c6e7732985b5a3bc5e213a72a`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f0a46f7a997ac6f05cd804b3a0f56c74348f25fd9e164c66ab7c5c4a6a2c82`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 407.4 KB (407392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3c809e9bcb4892e2da01d3bae84664c06e6bb0929c6813ef47a1aaaa3d675f`  
		Last Modified: Fri, 24 Apr 2020 07:05:07 GMT  
		Size: 7.0 MB (7016584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1cb7e35314fbaf45935cb538fb36cc01e53dff4d37131a3497fd376720294e`  
		Last Modified: Fri, 24 Apr 2020 07:05:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529922dc84cb9fec77a0630b9ad535a7c843db2cd4518c25442c47fbc986d8b7`  
		Last Modified: Fri, 24 Apr 2020 07:05:06 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5.0-alpine3.11`

```console
$ docker pull redis@sha256:83a3af36d5e57f2901b4783c313720e5fa3ecf0424ba86ad9775e06a9a5e35d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:5.0-alpine3.11` - linux; amd64

```console
$ docker pull redis@sha256:d4ada5d910403607b3f579d7171f36108c2e1cf67da966a712812230171fc153
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9998790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3661c84ee9d0f6312a076b69eb2bd112674cadb70ef7e1594c4f00193f8df08e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:19:42 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 19:19:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 19:20:54 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 19:20:54 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 19:20:55 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 19:21:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 19:21:49 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 19:21:49 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 19:21:50 GMT
WORKDIR /data
# Fri, 24 Apr 2020 19:21:50 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 19:21:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 19:21:50 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 19:21:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0373118a0d956ca0ee963e307457f45f073db9096f7c6f87c10251d071f0dc`  
		Last Modified: Fri, 24 Apr 2020 19:23:01 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd369fe62565d644723bfdb734c4ecb2a96191366ec08424146aa9c5ff6b308`  
		Last Modified: Fri, 24 Apr 2020 19:23:02 GMT  
		Size: 402.6 KB (402568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e45770272d96deeb96c4bfa3cffde811f318823b4422bdbbf909148dc5669bb`  
		Last Modified: Fri, 24 Apr 2020 19:23:14 GMT  
		Size: 6.8 MB (6781166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558de8ea3153bdccfaf67fadf7bbbdc60bf357f33ff0070df617d6e22ad46a13`  
		Last Modified: Fri, 24 Apr 2020 19:23:13 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c65255161264f51556db666aa812834b3f51c8403b09799a46e4d0909e4aa4`  
		Last Modified: Fri, 24 Apr 2020 19:23:12 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-alpine3.11` - linux; arm variant v6

```console
$ docker pull redis@sha256:867b50998330ae4743e95c8be69dee7ad37cbba8057659bef4dc142838d7f3e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9725047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333723767b2b5747763b5483d4742558e9abe6d70b98ee05d527643b5eb088d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:30:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 23 Apr 2020 22:30:20 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 23 Apr 2020 22:31:34 GMT
ENV REDIS_VERSION=5.0.9
# Thu, 23 Apr 2020 22:31:35 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Thu, 23 Apr 2020 22:31:36 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Thu, 23 Apr 2020 22:32:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 23 Apr 2020 22:32:27 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 23 Apr 2020 22:32:29 GMT
VOLUME [/data]
# Thu, 23 Apr 2020 22:32:30 GMT
WORKDIR /data
# Thu, 23 Apr 2020 22:32:31 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 23 Apr 2020 22:32:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 22:32:33 GMT
EXPOSE 6379
# Thu, 23 Apr 2020 22:32:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab5b04292d1974b3feedf74dddf563efe3ba5b5c38239a49e8adf0ac8140028`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af20f6a7bee5bf869254b4964c1a5d8dd5ef1353ac48081a885920682312555b`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 405.8 KB (405799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a2919ec032b1198ca13b052499b7c193e45d93756a3b0d7bb10c8db4f3db65`  
		Last Modified: Thu, 23 Apr 2020 22:34:01 GMT  
		Size: 6.7 MB (6697511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b2e77e4c2604e8e74b4c471b4a04d1a768eb84eadcfcd3621f135f7d4d90ca`  
		Last Modified: Thu, 23 Apr 2020 22:33:57 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18df89faaf97292802f6bca82a98892b7b0a168230ca31ae16e3cf307614a7a8`  
		Last Modified: Thu, 23 Apr 2020 22:33:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-alpine3.11` - linux; arm variant v7

```console
$ docker pull redis@sha256:1c10570f57cb14b4fbd3446c61303aeb7db18b45abffc49974d5bde7e4a89de4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9394623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a7ba195be67da9c68c67aa8d6eefa737236f15d3a9b490504ce943465c3a9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:51:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 08:51:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 08:52:43 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 08:52:43 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 08:52:44 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 08:53:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 08:53:30 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 08:53:31 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 08:53:32 GMT
WORKDIR /data
# Fri, 24 Apr 2020 08:53:32 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 08:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 08:53:34 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 08:53:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0765e03c998449baf4c76a1011cf80e6ab974db3d5d8da3a361bfeeb875d96db`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07fda5f4761823162fa661b4466f517ad5db025d9689c123221af67af9b53f`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 399.8 KB (399779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531954b17ac2db3cd86f3ced48c7c4f9fe053fad0792b7038321a667c911953a`  
		Last Modified: Fri, 24 Apr 2020 08:55:41 GMT  
		Size: 6.6 MB (6570977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d550a31e99202186ed01f1a5a4c96bab49dc143ad2a113696ecb48947836c0`  
		Last Modified: Fri, 24 Apr 2020 08:55:38 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a842b77b23971198e093c671bcf1e2cf6df771a6138ffb4132bfb37af22f17`  
		Last Modified: Fri, 24 Apr 2020 08:55:38 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-alpine3.11` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:2ebdecb52315772800ba4549b9dc83910d9ae7de5364c3092b0390d7266e94a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9918976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6acb4ad7ccdd962d8579a0929ab5920a1f58ff996cd4812188219c1eb74e91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:45:10 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 12:45:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 12:46:32 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 12:46:33 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 12:46:34 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 12:47:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 12:47:24 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 12:47:24 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 12:47:25 GMT
WORKDIR /data
# Fri, 24 Apr 2020 12:47:26 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 12:47:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 12:47:28 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 12:47:29 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7050d23898adae8e4a2e0ab67eaeab9f9a9ec0fa5b88b128eeff4de1570877`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8982b178d819b1f2f10c3375b2c7ed054157cc5e711b58b6a2dcb376686e5d59`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 404.7 KB (404661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ca1db598d2278e5526b65dcad0d96f0f0264060f879f1b437f58a467e27382`  
		Last Modified: Fri, 24 Apr 2020 12:49:17 GMT  
		Size: 6.8 MB (6788089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87542dce16ad38aeb18ffe2e2266f3bd9b8cbc70f6f4450be0e9f621022fabb5`  
		Last Modified: Fri, 24 Apr 2020 12:49:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a20d19811afde1a300515cade1279f18fb3ca0ef1800b52dcb45127731bd5f4`  
		Last Modified: Fri, 24 Apr 2020 12:49:15 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-alpine3.11` - linux; 386

```console
$ docker pull redis@sha256:3ab6896b5efe215c5cc110a835fecb73d5f55672ad4443f4baf51822db1854c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9710040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba820d7067104939d7ec907ee1fa581e9c7d40b0a204a14caf709f4dce84732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:49:36 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 05:49:38 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 05:52:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 05:52:17 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 05:52:17 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 05:52:17 GMT
WORKDIR /data
# Fri, 24 Apr 2020 05:52:17 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 05:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 05:52:18 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 05:52:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4eb71d5f124b9b51684034d7d96fba6399ff6892995e51137d0c0617a11fb9`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7685edc32d5ef38faf3beb4310c119862b1dfa18ea58edb0dbca84e9417b267`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 407.9 KB (407901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed6bb387586efb069405e1b2fea60bf1718da22582dade16723a6ce6beb111c`  
		Last Modified: Fri, 24 Apr 2020 05:53:49 GMT  
		Size: 6.5 MB (6491980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ee2bc48c46cc40ec8951486a93e65583168f55239b5e10e350ceda82120fa3`  
		Last Modified: Fri, 24 Apr 2020 05:53:48 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae5b0c59c675cf868993ca6ec424636476caea5bc4e43525a866864d0b8bbd1`  
		Last Modified: Fri, 24 Apr 2020 05:53:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-alpine3.11` - linux; ppc64le

```console
$ docker pull redis@sha256:14dfcd56148c897338a1306bf23b392e6ffce4ee486ddfcd77fb515e8f0f1557
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0a1b6eb6701cd8c4349958777c681d81e0520d3e82317e2419b56b4d4ce4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:02:06 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 09:02:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 09:03:45 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 09:03:48 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 09:03:50 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 09:04:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 09:04:46 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 09:04:50 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 09:04:53 GMT
WORKDIR /data
# Fri, 24 Apr 2020 09:04:56 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 09:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 09:05:01 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 09:05:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc79e36a18515157312416d029cb35887ee8668b53b6c0e3867a4d0dd8dd231`  
		Last Modified: Fri, 24 Apr 2020 09:06:56 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83078862453fa1de07d734ccc5b995c92cd74710488c11d066ad752e3402d`  
		Last Modified: Fri, 24 Apr 2020 09:06:57 GMT  
		Size: 409.9 KB (409875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad3f9cade0fa9bda2c0f45df3a77c780ebc4adea7badb3b8387fed928c60ed7`  
		Last Modified: Fri, 24 Apr 2020 09:07:21 GMT  
		Size: 7.3 MB (7260512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ad499a196593cd717672adacc0550293f8b2c00a5907255640b27d266bc05a`  
		Last Modified: Fri, 24 Apr 2020 09:07:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5831b0ffd2731f416315c93a640459b17492812a21b7a6fba00919faaeb1d5`  
		Last Modified: Fri, 24 Apr 2020 09:07:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-alpine3.11` - linux; s390x

```console
$ docker pull redis@sha256:5ad55b9f660c1e3b315e26e3497b9e4d270a5dd7ff431b14d9a17cf78fcac287
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10008638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dd64fd99b54ef1c40f2cd3351efcaf43b4d026dfcfe78315787e7a8220ffee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:02:35 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 07:02:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 07:03:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 07:03:53 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 07:03:53 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 07:03:54 GMT
WORKDIR /data
# Fri, 24 Apr 2020 07:03:54 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 07:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 07:03:54 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 07:03:54 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2da1b54f68b54cfd646e4cf510a14593b857e3c6e7732985b5a3bc5e213a72a`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f0a46f7a997ac6f05cd804b3a0f56c74348f25fd9e164c66ab7c5c4a6a2c82`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 407.4 KB (407392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3c809e9bcb4892e2da01d3bae84664c06e6bb0929c6813ef47a1aaaa3d675f`  
		Last Modified: Fri, 24 Apr 2020 07:05:07 GMT  
		Size: 7.0 MB (7016584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1cb7e35314fbaf45935cb538fb36cc01e53dff4d37131a3497fd376720294e`  
		Last Modified: Fri, 24 Apr 2020 07:05:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529922dc84cb9fec77a0630b9ad535a7c843db2cd4518c25442c47fbc986d8b7`  
		Last Modified: Fri, 24 Apr 2020 07:05:06 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5.0-buster`

```console
$ docker pull redis@sha256:08aab527ca57f536f2805e031535a6881bab63171146aa6414de69d54b14a84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redis:5.0-buster` - linux; amd64

```console
$ docker pull redis@sha256:ae4b7c01640a2688e9ef5dd630e2135df7a9e711e712e3d9eab05608d34e2b84
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35863829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5120d23bad51618dd0e19bddd616d555f3cb01753a930c9532364e0d2505b7e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 02:15:48 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 02:17:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:17:30 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:17:30 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:17:30 GMT
WORKDIR /data
# Sat, 16 May 2020 02:17:31 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:17:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:17:31 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:17:32 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846bf5faff48ca0599eb0ab51917d8471164ff02f04524d108bfc8b89dcf50cd`  
		Last Modified: Sat, 16 May 2020 02:20:41 GMT  
		Size: 7.3 MB (7345115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affafbdb5f81d8218bb0f3a60783e92e55fa09ba0a2488f3488488608fa1153d`  
		Last Modified: Sat, 16 May 2020 02:20:38 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdd19e5317241aa2fcd854961c766a5bfc18cbd0db01b18c91404ebdc2ccaa3`  
		Last Modified: Sat, 16 May 2020 02:20:39 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-buster` - linux; arm variant v5

```console
$ docker pull redis@sha256:aa487a40514e78f619cfcb9458a4cba51f5638916d8e4ed3bc10355d362963be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33396150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d3ebf62ba5747e68aa370dc62af6d166b2f494290cc0339c60f17aa271de77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 22:38:03 GMT
ADD file:cbd01ff8d2e40a25bcdb13dc19ffe124c2927b491997dc1c57d4f2c2a308e279 in / 
# Thu, 14 May 2020 22:38:05 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:40:59 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 04:40:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 04:41:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 04:43:01 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 04:43:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 04:43:02 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 04:44:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 04:44:09 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 04:44:09 GMT
VOLUME [/data]
# Fri, 15 May 2020 04:44:10 GMT
WORKDIR /data
# Fri, 15 May 2020 04:44:11 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 04:44:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 04:44:12 GMT
EXPOSE 6379
# Fri, 15 May 2020 04:44:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:24d81022117207b0239d8a8023ca1724b7dde38cb08ce5b9199f59d475d1e600`  
		Last Modified: Thu, 14 May 2020 22:46:51 GMT  
		Size: 24.8 MB (24838470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c13f680b58f95af37082529e8a1ecd6358e22a7e13a75344d8375a03cafb174`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2286bbfcebea1b30a2e862afd7742a7f65237dcabddc9486bfaaf5fd8ba0d65`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.4 MB (1376110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7deffa88c65075e285c0d27dc2aba2336a7a1779ed75bb2f32e760fbab785147`  
		Last Modified: Fri, 15 May 2020 04:44:47 GMT  
		Size: 7.2 MB (7179299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02c5ad0a586c0c745b5df9a3db37bcaf3213a48ab53be3446bd486fa5b85838`  
		Last Modified: Fri, 15 May 2020 04:44:44 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9850cd504042ad62e1898b73b9a1d5d4a95d80bf65a5909d238d56a640697226`  
		Last Modified: Fri, 15 May 2020 04:44:44 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-buster` - linux; arm variant v7

```console
$ docker pull redis@sha256:428b7a31e32fb1a39cc9d41b113e6051359572d96ae9d9906089f4c324a07173
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31109932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3abf0ee6b0b5453a72669cb38743da5af51666c9b3e18ab680cfb0c65e3241a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 01:00:06 GMT
ADD file:e3f9a454eccb40b4d7bf1dcc17ec29589a007ac67545d1cb5b6fa213c872c8f2 in / 
# Fri, 15 May 2020 01:00:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 16:49:40 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 16:49:40 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 16:50:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 16:51:47 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 16:51:48 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 16:51:49 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 16:52:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 16:52:49 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 16:52:50 GMT
VOLUME [/data]
# Fri, 15 May 2020 16:52:51 GMT
WORKDIR /data
# Fri, 15 May 2020 16:52:51 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 16:52:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 16:52:53 GMT
EXPOSE 6379
# Fri, 15 May 2020 16:52:53 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e41e28500352be59188c3d871a4b5a3f594350b860a9a36ed5808a35920bdae4`  
		Last Modified: Fri, 15 May 2020 01:11:21 GMT  
		Size: 22.7 MB (22705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6732859766aedad40f91cd96df6b5a6930efe6614b0f084b8459d93c22a69`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed92b736a14b52db74c7cd9919c66ce953393f0544906969081702697d5a6b54`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.4 MB (1368207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114f7e7289bd10cc75ccedb5c36ef2ef1bcdd04a0d015af0e3f5dbca67c2e2d9`  
		Last Modified: Fri, 15 May 2020 16:53:44 GMT  
		Size: 7.0 MB (7033534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e37951fe3e21e2afb2d25fe8ec18da89f27d40c88b7e83b5991380af42227`  
		Last Modified: Fri, 15 May 2020 16:53:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b778ce965d8bdff427c804f43a751b2c4e1dc26ba152f53d4abe56a8b4014174`  
		Last Modified: Fri, 15 May 2020 16:53:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-buster` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:457f1b0ba059ac05ce46805c92967506f61bb69a38eea8a5aaebf1d5d8da5017
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34547915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ef03b25863b64392c6d8ff085e6b0768f88c8b95692196f79c4846e8f38277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 12:44:06 GMT
ADD file:b305c1792102142f183d3084026f0fc6be3ddf8d1959b32f0a5d22d35eebcd15 in / 
# Fri, 15 May 2020 12:44:07 GMT
CMD ["bash"]
# Sat, 16 May 2020 08:24:10 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 08:24:10 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 08:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 08:27:04 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 08:27:05 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 08:27:05 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 08:28:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:28:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:28:09 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:28:10 GMT
WORKDIR /data
# Sat, 16 May 2020 08:28:11 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 08:28:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:28:12 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:28:12 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8a7e1e68c24e5cac20ef26d29505c58456b561c431f0c683b66d1a0943f40dd4`  
		Last Modified: Fri, 15 May 2020 12:53:36 GMT  
		Size: 25.9 MB (25857195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc5ca4e8f484b410989ac557169938b5fe6288ed5add0839e05a790ef47676`  
		Last Modified: Sat, 16 May 2020 08:28:42 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eccfc30e2be16f57d04f487ed80dd2b52ada557753eca7c79eb2ff88ab421f2`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 1.4 MB (1352995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27089b3134bdd932f8ebb93aef02f95e6883cebfef343a3caad67c05fcc554d9`  
		Last Modified: Sat, 16 May 2020 08:29:17 GMT  
		Size: 7.3 MB (7335450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35769aa5a1907ee966e04244b585d65a7a780c87efb002cf6abdbe16f153d7b`  
		Last Modified: Sat, 16 May 2020 08:29:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e99e4e05b4653f243c0f8a635a0cb3fb3c367a3d2b73667db0301d0f869f14e`  
		Last Modified: Sat, 16 May 2020 08:29:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-buster` - linux; 386

```console
$ docker pull redis@sha256:cbd966cd9fdfda6ba7a4ae65566b21c986580d26bccd7648b431417c79a8797e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372a1f57ccac9f9940a9a3ef51392b6ae15c3b1102c3494fb808505bdc549b2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Sat, 16 May 2020 00:07:24 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 00:07:24 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 00:07:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 00:13:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:13:21 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:13:21 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:13:21 GMT
WORKDIR /data
# Sat, 16 May 2020 00:13:22 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 00:13:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:13:22 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:13:23 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157733bfb7391a76ac45c4aa7ed1ea9e99ee6b2f4f70fbbab7b48b514fff73fc`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7927326d7d556c02a6f3c72888c9f9d2beb780c097c9fb1ca55539afa2a42d`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.4 MB (1387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346dcb0e7c24e02011edcae7f0884ff428c9b01cd1361cfb068c4cb5ea6c3f5f`  
		Last Modified: Sat, 16 May 2020 00:14:11 GMT  
		Size: 7.0 MB (7008096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19378b87aaceac51732681a095c2679c50ac66b341a727cc4c59c7672e72642b`  
		Last Modified: Sat, 16 May 2020 00:14:09 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d89103e3ff26e632031f9510e343c0480df8aa67080da4f4fe1cd70671a94b2`  
		Last Modified: Sat, 16 May 2020 00:14:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-buster` - linux; mips64le

```console
$ docker pull redis@sha256:8b6a10293e59139fa6bcc9fc4b76fa1bece970cbca46f0d4f88ba87ca29fb38d
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34733957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14f6ea4c9fdcd70e15b3ec9963dbf5b3a0cba06b78eca3b49ede54d8eb74633`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 04:48:19 GMT
ADD file:1163d3a5831eb58d132b66b60303169816e7bd8289f19caaac1157179a95f6f9 in / 
# Fri, 15 May 2020 04:48:19 GMT
CMD ["bash"]
# Fri, 15 May 2020 15:35:02 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 15:35:02 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 15:35:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 15:39:12 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 15:39:12 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 15:39:13 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 15:42:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 15:42:32 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 15:42:33 GMT
VOLUME [/data]
# Fri, 15 May 2020 15:42:33 GMT
WORKDIR /data
# Fri, 15 May 2020 15:42:34 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 15:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 15:42:34 GMT
EXPOSE 6379
# Fri, 15 May 2020 15:42:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d22357c747999d33ec7501da2c05aa9e95079ebddefbcb326976c5ed5b176b3f`  
		Last Modified: Fri, 15 May 2020 04:57:10 GMT  
		Size: 25.8 MB (25764292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f562c9b9683468308a6f59cab7d724ffc3b35a66acd8ce093b288144db2b7c5`  
		Last Modified: Fri, 15 May 2020 15:42:49 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fda93ec518be6790dd5e435d4bb66cab95d5c14044f01c584fd463ca6ffd290`  
		Last Modified: Fri, 15 May 2020 15:42:50 GMT  
		Size: 1.3 MB (1305516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeb925910423da69c6eda33089a17133d5b1649da9305c560bb62548887111c`  
		Last Modified: Fri, 15 May 2020 15:43:33 GMT  
		Size: 7.7 MB (7661910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89a2cb8235be9f7742a87b9e6cb1a8e822fa316f9524eb2e63e180907993838`  
		Last Modified: Fri, 15 May 2020 15:43:26 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe01516addcda29424d0863a92cc972db77274689603262287f4383b2251fb0`  
		Last Modified: Fri, 15 May 2020 15:43:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-buster` - linux; ppc64le

```console
$ docker pull redis@sha256:c25f3deade6ecb0d0ab42fa53321c50806dd2471c0a06ec3180217c93e2b50e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39696499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7993e4f9c4d285dffe1be6b2eb7fc6e5872e4c23175ef0b2eecb2f4dfd9c09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 16 May 2020 17:14:59 GMT
ADD file:b2656a1711bd47585595ae2927cfd4ec00eb903d193583d945b6d60f0a2691bb in / 
# Sat, 16 May 2020 17:15:04 GMT
CMD ["bash"]
# Mon, 18 May 2020 13:30:23 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Mon, 18 May 2020 13:30:26 GMT
ENV GOSU_VERSION=1.12
# Mon, 18 May 2020 13:32:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 18 May 2020 13:38:55 GMT
ENV REDIS_VERSION=5.0.9
# Mon, 18 May 2020 13:38:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Mon, 18 May 2020 13:39:03 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Mon, 18 May 2020 13:41:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:41:57 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:41:59 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:42:03 GMT
WORKDIR /data
# Mon, 18 May 2020 13:42:06 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Mon, 18 May 2020 13:42:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:42:11 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:42:14 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:034d508ed7647e7139951a435acc95e0124f50c984670d0e53b4f5ba25cf6ed1`  
		Last Modified: Sat, 16 May 2020 18:31:49 GMT  
		Size: 30.5 MB (30524456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c613ed63b519e3a0419cf56e14127f5d25466416a8143341540d12cb99943b65`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec60488415c29ebe96bbfabff01925147e50ee55136fdf961fbe8526617f3b`  
		Last Modified: Mon, 18 May 2020 13:42:57 GMT  
		Size: 1.3 MB (1335429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8c21d1569eb7d014ba9bf44dee78260d5e4d8e456b37cb304b127c69940684`  
		Last Modified: Mon, 18 May 2020 13:43:54 GMT  
		Size: 7.8 MB (7834331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c759fe2a72a81200077dd4a171c8c95ea1cecdc62e8a2ae362e0d31f255fc9f9`  
		Last Modified: Mon, 18 May 2020 13:43:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da932920c36a309064e131257fe3ed53362fb1a0d18207a51e7a26735b066838`  
		Last Modified: Mon, 18 May 2020 13:43:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5.0-buster` - linux; s390x

```console
$ docker pull redis@sha256:becaadf1b7481b782ca8d0ed939de5e00ca69064a94eef114d443bb75116c1f3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34710318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dba1a9e6bde97648f54ed3508c268f0671bdf3b171629e8a034800658e2ea36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 05:15:35 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 05:15:35 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 05:15:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 05:17:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 05:17:06 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 05:17:06 GMT
VOLUME [/data]
# Fri, 15 May 2020 05:17:06 GMT
WORKDIR /data
# Fri, 15 May 2020 05:17:07 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 05:17:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 05:17:07 GMT
EXPOSE 6379
# Fri, 15 May 2020 05:17:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e40cd0998be29e9cce5152b7d3644b03b888bcca5db2049d43c93bf53185d`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc1e5303c90f8fcd807a5042757fb4de087ae4b3319afca416b72e858de788c`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.4 MB (1403711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fff5a343dd72b836a3f99619249e4fd4b82b0d09950a9552781d2fcbe733c9`  
		Last Modified: Fri, 15 May 2020 05:17:43 GMT  
		Size: 7.6 MB (7591396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30482d87111f841181c863a01b1ad9890bab844f7bf3f24c8de746052ebc5d71`  
		Last Modified: Fri, 15 May 2020 05:17:42 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a814c5126e00d2ce60c95caacba2b4f8236c88df49bcaf578c2500a12404dc3`  
		Last Modified: Fri, 15 May 2020 05:17:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5-32bit`

```console
$ docker pull redis@sha256:3b14d8ad7934452ffe28a95c5931ea8cf4a6e8771d2afc394836fc220c4ddf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redis:5-32bit` - linux; amd64

```console
$ docker pull redis@sha256:1c6e5965741e36f16ce589d4fbfce72fadc9d6bcf7b6f458e9d29772c8978275
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40577472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51da9d4e9b00184c7e706cc1f8471c8aafa7f5da3e92655613d5f4e2944ea82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 02:15:48 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 02:19:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev-i386 gcc-multilib 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:19:43 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:19:43 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:19:43 GMT
WORKDIR /data
# Sat, 16 May 2020 02:19:44 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:19:44 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:19:45 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52db9932f76ff160dd7194254956eccd2857a82675be95f689601345919dac8e`  
		Last Modified: Sat, 16 May 2020 02:20:50 GMT  
		Size: 12.1 MB (12058755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64def67d4f9860909ddb35febdfdf94e31ec29c620e2e207e20c2f0f1e92ab07`  
		Last Modified: Sat, 16 May 2020 02:20:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeed70e76f4d345e003e569a8ec0a354771d42efcbcb26b94aea29d64a85272e`  
		Last Modified: Sat, 16 May 2020 02:20:48 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5-32bit-buster`

```console
$ docker pull redis@sha256:3b14d8ad7934452ffe28a95c5931ea8cf4a6e8771d2afc394836fc220c4ddf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redis:5-32bit-buster` - linux; amd64

```console
$ docker pull redis@sha256:1c6e5965741e36f16ce589d4fbfce72fadc9d6bcf7b6f458e9d29772c8978275
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40577472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51da9d4e9b00184c7e706cc1f8471c8aafa7f5da3e92655613d5f4e2944ea82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 02:15:48 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 02:19:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev-i386 gcc-multilib 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:19:43 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:19:43 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:19:43 GMT
WORKDIR /data
# Sat, 16 May 2020 02:19:44 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:19:44 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:19:45 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52db9932f76ff160dd7194254956eccd2857a82675be95f689601345919dac8e`  
		Last Modified: Sat, 16 May 2020 02:20:50 GMT  
		Size: 12.1 MB (12058755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64def67d4f9860909ddb35febdfdf94e31ec29c620e2e207e20c2f0f1e92ab07`  
		Last Modified: Sat, 16 May 2020 02:20:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeed70e76f4d345e003e569a8ec0a354771d42efcbcb26b94aea29d64a85272e`  
		Last Modified: Sat, 16 May 2020 02:20:48 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5-alpine`

```console
$ docker pull redis@sha256:83a3af36d5e57f2901b4783c313720e5fa3ecf0424ba86ad9775e06a9a5e35d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:5-alpine` - linux; amd64

```console
$ docker pull redis@sha256:d4ada5d910403607b3f579d7171f36108c2e1cf67da966a712812230171fc153
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9998790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3661c84ee9d0f6312a076b69eb2bd112674cadb70ef7e1594c4f00193f8df08e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:19:42 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 19:19:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 19:20:54 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 19:20:54 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 19:20:55 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 19:21:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 19:21:49 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 19:21:49 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 19:21:50 GMT
WORKDIR /data
# Fri, 24 Apr 2020 19:21:50 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 19:21:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 19:21:50 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 19:21:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0373118a0d956ca0ee963e307457f45f073db9096f7c6f87c10251d071f0dc`  
		Last Modified: Fri, 24 Apr 2020 19:23:01 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd369fe62565d644723bfdb734c4ecb2a96191366ec08424146aa9c5ff6b308`  
		Last Modified: Fri, 24 Apr 2020 19:23:02 GMT  
		Size: 402.6 KB (402568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e45770272d96deeb96c4bfa3cffde811f318823b4422bdbbf909148dc5669bb`  
		Last Modified: Fri, 24 Apr 2020 19:23:14 GMT  
		Size: 6.8 MB (6781166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558de8ea3153bdccfaf67fadf7bbbdc60bf357f33ff0070df617d6e22ad46a13`  
		Last Modified: Fri, 24 Apr 2020 19:23:13 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c65255161264f51556db666aa812834b3f51c8403b09799a46e4d0909e4aa4`  
		Last Modified: Fri, 24 Apr 2020 19:23:12 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:867b50998330ae4743e95c8be69dee7ad37cbba8057659bef4dc142838d7f3e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9725047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333723767b2b5747763b5483d4742558e9abe6d70b98ee05d527643b5eb088d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:30:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 23 Apr 2020 22:30:20 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 23 Apr 2020 22:31:34 GMT
ENV REDIS_VERSION=5.0.9
# Thu, 23 Apr 2020 22:31:35 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Thu, 23 Apr 2020 22:31:36 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Thu, 23 Apr 2020 22:32:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 23 Apr 2020 22:32:27 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 23 Apr 2020 22:32:29 GMT
VOLUME [/data]
# Thu, 23 Apr 2020 22:32:30 GMT
WORKDIR /data
# Thu, 23 Apr 2020 22:32:31 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 23 Apr 2020 22:32:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 22:32:33 GMT
EXPOSE 6379
# Thu, 23 Apr 2020 22:32:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab5b04292d1974b3feedf74dddf563efe3ba5b5c38239a49e8adf0ac8140028`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af20f6a7bee5bf869254b4964c1a5d8dd5ef1353ac48081a885920682312555b`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 405.8 KB (405799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a2919ec032b1198ca13b052499b7c193e45d93756a3b0d7bb10c8db4f3db65`  
		Last Modified: Thu, 23 Apr 2020 22:34:01 GMT  
		Size: 6.7 MB (6697511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b2e77e4c2604e8e74b4c471b4a04d1a768eb84eadcfcd3621f135f7d4d90ca`  
		Last Modified: Thu, 23 Apr 2020 22:33:57 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18df89faaf97292802f6bca82a98892b7b0a168230ca31ae16e3cf307614a7a8`  
		Last Modified: Thu, 23 Apr 2020 22:33:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:1c10570f57cb14b4fbd3446c61303aeb7db18b45abffc49974d5bde7e4a89de4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9394623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a7ba195be67da9c68c67aa8d6eefa737236f15d3a9b490504ce943465c3a9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:51:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 08:51:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 08:52:43 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 08:52:43 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 08:52:44 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 08:53:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 08:53:30 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 08:53:31 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 08:53:32 GMT
WORKDIR /data
# Fri, 24 Apr 2020 08:53:32 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 08:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 08:53:34 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 08:53:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0765e03c998449baf4c76a1011cf80e6ab974db3d5d8da3a361bfeeb875d96db`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07fda5f4761823162fa661b4466f517ad5db025d9689c123221af67af9b53f`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 399.8 KB (399779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531954b17ac2db3cd86f3ced48c7c4f9fe053fad0792b7038321a667c911953a`  
		Last Modified: Fri, 24 Apr 2020 08:55:41 GMT  
		Size: 6.6 MB (6570977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d550a31e99202186ed01f1a5a4c96bab49dc143ad2a113696ecb48947836c0`  
		Last Modified: Fri, 24 Apr 2020 08:55:38 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a842b77b23971198e093c671bcf1e2cf6df771a6138ffb4132bfb37af22f17`  
		Last Modified: Fri, 24 Apr 2020 08:55:38 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:2ebdecb52315772800ba4549b9dc83910d9ae7de5364c3092b0390d7266e94a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9918976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6acb4ad7ccdd962d8579a0929ab5920a1f58ff996cd4812188219c1eb74e91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:45:10 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 12:45:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 12:46:32 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 12:46:33 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 12:46:34 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 12:47:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 12:47:24 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 12:47:24 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 12:47:25 GMT
WORKDIR /data
# Fri, 24 Apr 2020 12:47:26 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 12:47:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 12:47:28 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 12:47:29 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7050d23898adae8e4a2e0ab67eaeab9f9a9ec0fa5b88b128eeff4de1570877`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8982b178d819b1f2f10c3375b2c7ed054157cc5e711b58b6a2dcb376686e5d59`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 404.7 KB (404661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ca1db598d2278e5526b65dcad0d96f0f0264060f879f1b437f58a467e27382`  
		Last Modified: Fri, 24 Apr 2020 12:49:17 GMT  
		Size: 6.8 MB (6788089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87542dce16ad38aeb18ffe2e2266f3bd9b8cbc70f6f4450be0e9f621022fabb5`  
		Last Modified: Fri, 24 Apr 2020 12:49:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a20d19811afde1a300515cade1279f18fb3ca0ef1800b52dcb45127731bd5f4`  
		Last Modified: Fri, 24 Apr 2020 12:49:15 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine` - linux; 386

```console
$ docker pull redis@sha256:3ab6896b5efe215c5cc110a835fecb73d5f55672ad4443f4baf51822db1854c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9710040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba820d7067104939d7ec907ee1fa581e9c7d40b0a204a14caf709f4dce84732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:49:36 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 05:49:38 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 05:52:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 05:52:17 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 05:52:17 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 05:52:17 GMT
WORKDIR /data
# Fri, 24 Apr 2020 05:52:17 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 05:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 05:52:18 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 05:52:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4eb71d5f124b9b51684034d7d96fba6399ff6892995e51137d0c0617a11fb9`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7685edc32d5ef38faf3beb4310c119862b1dfa18ea58edb0dbca84e9417b267`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 407.9 KB (407901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed6bb387586efb069405e1b2fea60bf1718da22582dade16723a6ce6beb111c`  
		Last Modified: Fri, 24 Apr 2020 05:53:49 GMT  
		Size: 6.5 MB (6491980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ee2bc48c46cc40ec8951486a93e65583168f55239b5e10e350ceda82120fa3`  
		Last Modified: Fri, 24 Apr 2020 05:53:48 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae5b0c59c675cf868993ca6ec424636476caea5bc4e43525a866864d0b8bbd1`  
		Last Modified: Fri, 24 Apr 2020 05:53:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:14dfcd56148c897338a1306bf23b392e6ffce4ee486ddfcd77fb515e8f0f1557
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0a1b6eb6701cd8c4349958777c681d81e0520d3e82317e2419b56b4d4ce4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:02:06 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 09:02:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 09:03:45 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 09:03:48 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 09:03:50 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 09:04:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 09:04:46 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 09:04:50 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 09:04:53 GMT
WORKDIR /data
# Fri, 24 Apr 2020 09:04:56 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 09:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 09:05:01 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 09:05:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc79e36a18515157312416d029cb35887ee8668b53b6c0e3867a4d0dd8dd231`  
		Last Modified: Fri, 24 Apr 2020 09:06:56 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83078862453fa1de07d734ccc5b995c92cd74710488c11d066ad752e3402d`  
		Last Modified: Fri, 24 Apr 2020 09:06:57 GMT  
		Size: 409.9 KB (409875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad3f9cade0fa9bda2c0f45df3a77c780ebc4adea7badb3b8387fed928c60ed7`  
		Last Modified: Fri, 24 Apr 2020 09:07:21 GMT  
		Size: 7.3 MB (7260512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ad499a196593cd717672adacc0550293f8b2c00a5907255640b27d266bc05a`  
		Last Modified: Fri, 24 Apr 2020 09:07:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5831b0ffd2731f416315c93a640459b17492812a21b7a6fba00919faaeb1d5`  
		Last Modified: Fri, 24 Apr 2020 09:07:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine` - linux; s390x

```console
$ docker pull redis@sha256:5ad55b9f660c1e3b315e26e3497b9e4d270a5dd7ff431b14d9a17cf78fcac287
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10008638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dd64fd99b54ef1c40f2cd3351efcaf43b4d026dfcfe78315787e7a8220ffee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:02:35 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 07:02:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 07:03:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 07:03:53 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 07:03:53 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 07:03:54 GMT
WORKDIR /data
# Fri, 24 Apr 2020 07:03:54 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 07:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 07:03:54 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 07:03:54 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2da1b54f68b54cfd646e4cf510a14593b857e3c6e7732985b5a3bc5e213a72a`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f0a46f7a997ac6f05cd804b3a0f56c74348f25fd9e164c66ab7c5c4a6a2c82`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 407.4 KB (407392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3c809e9bcb4892e2da01d3bae84664c06e6bb0929c6813ef47a1aaaa3d675f`  
		Last Modified: Fri, 24 Apr 2020 07:05:07 GMT  
		Size: 7.0 MB (7016584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1cb7e35314fbaf45935cb538fb36cc01e53dff4d37131a3497fd376720294e`  
		Last Modified: Fri, 24 Apr 2020 07:05:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529922dc84cb9fec77a0630b9ad535a7c843db2cd4518c25442c47fbc986d8b7`  
		Last Modified: Fri, 24 Apr 2020 07:05:06 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5-alpine3.11`

```console
$ docker pull redis@sha256:83a3af36d5e57f2901b4783c313720e5fa3ecf0424ba86ad9775e06a9a5e35d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:5-alpine3.11` - linux; amd64

```console
$ docker pull redis@sha256:d4ada5d910403607b3f579d7171f36108c2e1cf67da966a712812230171fc153
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9998790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3661c84ee9d0f6312a076b69eb2bd112674cadb70ef7e1594c4f00193f8df08e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:19:42 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 19:19:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 19:20:54 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 19:20:54 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 19:20:55 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 19:21:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 19:21:49 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 19:21:49 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 19:21:50 GMT
WORKDIR /data
# Fri, 24 Apr 2020 19:21:50 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 19:21:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 19:21:50 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 19:21:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0373118a0d956ca0ee963e307457f45f073db9096f7c6f87c10251d071f0dc`  
		Last Modified: Fri, 24 Apr 2020 19:23:01 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd369fe62565d644723bfdb734c4ecb2a96191366ec08424146aa9c5ff6b308`  
		Last Modified: Fri, 24 Apr 2020 19:23:02 GMT  
		Size: 402.6 KB (402568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e45770272d96deeb96c4bfa3cffde811f318823b4422bdbbf909148dc5669bb`  
		Last Modified: Fri, 24 Apr 2020 19:23:14 GMT  
		Size: 6.8 MB (6781166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558de8ea3153bdccfaf67fadf7bbbdc60bf357f33ff0070df617d6e22ad46a13`  
		Last Modified: Fri, 24 Apr 2020 19:23:13 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c65255161264f51556db666aa812834b3f51c8403b09799a46e4d0909e4aa4`  
		Last Modified: Fri, 24 Apr 2020 19:23:12 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.11` - linux; arm variant v6

```console
$ docker pull redis@sha256:867b50998330ae4743e95c8be69dee7ad37cbba8057659bef4dc142838d7f3e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9725047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333723767b2b5747763b5483d4742558e9abe6d70b98ee05d527643b5eb088d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:30:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 23 Apr 2020 22:30:20 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Thu, 23 Apr 2020 22:31:34 GMT
ENV REDIS_VERSION=5.0.9
# Thu, 23 Apr 2020 22:31:35 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Thu, 23 Apr 2020 22:31:36 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Thu, 23 Apr 2020 22:32:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Thu, 23 Apr 2020 22:32:27 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 23 Apr 2020 22:32:29 GMT
VOLUME [/data]
# Thu, 23 Apr 2020 22:32:30 GMT
WORKDIR /data
# Thu, 23 Apr 2020 22:32:31 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Thu, 23 Apr 2020 22:32:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2020 22:32:33 GMT
EXPOSE 6379
# Thu, 23 Apr 2020 22:32:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab5b04292d1974b3feedf74dddf563efe3ba5b5c38239a49e8adf0ac8140028`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af20f6a7bee5bf869254b4964c1a5d8dd5ef1353ac48081a885920682312555b`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 405.8 KB (405799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a2919ec032b1198ca13b052499b7c193e45d93756a3b0d7bb10c8db4f3db65`  
		Last Modified: Thu, 23 Apr 2020 22:34:01 GMT  
		Size: 6.7 MB (6697511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b2e77e4c2604e8e74b4c471b4a04d1a768eb84eadcfcd3621f135f7d4d90ca`  
		Last Modified: Thu, 23 Apr 2020 22:33:57 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18df89faaf97292802f6bca82a98892b7b0a168230ca31ae16e3cf307614a7a8`  
		Last Modified: Thu, 23 Apr 2020 22:33:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.11` - linux; arm variant v7

```console
$ docker pull redis@sha256:1c10570f57cb14b4fbd3446c61303aeb7db18b45abffc49974d5bde7e4a89de4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9394623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a7ba195be67da9c68c67aa8d6eefa737236f15d3a9b490504ce943465c3a9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:51:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 08:51:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 08:52:43 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 08:52:43 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 08:52:44 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 08:53:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 08:53:30 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 08:53:31 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 08:53:32 GMT
WORKDIR /data
# Fri, 24 Apr 2020 08:53:32 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 08:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 08:53:34 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 08:53:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0765e03c998449baf4c76a1011cf80e6ab974db3d5d8da3a361bfeeb875d96db`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07fda5f4761823162fa661b4466f517ad5db025d9689c123221af67af9b53f`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 399.8 KB (399779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531954b17ac2db3cd86f3ced48c7c4f9fe053fad0792b7038321a667c911953a`  
		Last Modified: Fri, 24 Apr 2020 08:55:41 GMT  
		Size: 6.6 MB (6570977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d550a31e99202186ed01f1a5a4c96bab49dc143ad2a113696ecb48947836c0`  
		Last Modified: Fri, 24 Apr 2020 08:55:38 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a842b77b23971198e093c671bcf1e2cf6df771a6138ffb4132bfb37af22f17`  
		Last Modified: Fri, 24 Apr 2020 08:55:38 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.11` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:2ebdecb52315772800ba4549b9dc83910d9ae7de5364c3092b0390d7266e94a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9918976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6acb4ad7ccdd962d8579a0929ab5920a1f58ff996cd4812188219c1eb74e91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:45:10 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 12:45:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 12:46:32 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 12:46:33 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 12:46:34 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 12:47:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 12:47:24 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 12:47:24 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 12:47:25 GMT
WORKDIR /data
# Fri, 24 Apr 2020 12:47:26 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 12:47:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 12:47:28 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 12:47:29 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7050d23898adae8e4a2e0ab67eaeab9f9a9ec0fa5b88b128eeff4de1570877`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8982b178d819b1f2f10c3375b2c7ed054157cc5e711b58b6a2dcb376686e5d59`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 404.7 KB (404661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ca1db598d2278e5526b65dcad0d96f0f0264060f879f1b437f58a467e27382`  
		Last Modified: Fri, 24 Apr 2020 12:49:17 GMT  
		Size: 6.8 MB (6788089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87542dce16ad38aeb18ffe2e2266f3bd9b8cbc70f6f4450be0e9f621022fabb5`  
		Last Modified: Fri, 24 Apr 2020 12:49:15 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a20d19811afde1a300515cade1279f18fb3ca0ef1800b52dcb45127731bd5f4`  
		Last Modified: Fri, 24 Apr 2020 12:49:15 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.11` - linux; 386

```console
$ docker pull redis@sha256:3ab6896b5efe215c5cc110a835fecb73d5f55672ad4443f4baf51822db1854c6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9710040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba820d7067104939d7ec907ee1fa581e9c7d40b0a204a14caf709f4dce84732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:49:36 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 05:49:38 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 05:51:10 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 05:52:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 05:52:17 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 05:52:17 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 05:52:17 GMT
WORKDIR /data
# Fri, 24 Apr 2020 05:52:17 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 05:52:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 05:52:18 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 05:52:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4eb71d5f124b9b51684034d7d96fba6399ff6892995e51137d0c0617a11fb9`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7685edc32d5ef38faf3beb4310c119862b1dfa18ea58edb0dbca84e9417b267`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 407.9 KB (407901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed6bb387586efb069405e1b2fea60bf1718da22582dade16723a6ce6beb111c`  
		Last Modified: Fri, 24 Apr 2020 05:53:49 GMT  
		Size: 6.5 MB (6491980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ee2bc48c46cc40ec8951486a93e65583168f55239b5e10e350ceda82120fa3`  
		Last Modified: Fri, 24 Apr 2020 05:53:48 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae5b0c59c675cf868993ca6ec424636476caea5bc4e43525a866864d0b8bbd1`  
		Last Modified: Fri, 24 Apr 2020 05:53:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.11` - linux; ppc64le

```console
$ docker pull redis@sha256:14dfcd56148c897338a1306bf23b392e6ffce4ee486ddfcd77fb515e8f0f1557
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0a1b6eb6701cd8c4349958777c681d81e0520d3e82317e2419b56b4d4ce4bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:02:06 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 09:02:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 09:03:45 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 09:03:48 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 09:03:50 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 09:04:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 09:04:46 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 09:04:50 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 09:04:53 GMT
WORKDIR /data
# Fri, 24 Apr 2020 09:04:56 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 09:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 09:05:01 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 09:05:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc79e36a18515157312416d029cb35887ee8668b53b6c0e3867a4d0dd8dd231`  
		Last Modified: Fri, 24 Apr 2020 09:06:56 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83078862453fa1de07d734ccc5b995c92cd74710488c11d066ad752e3402d`  
		Last Modified: Fri, 24 Apr 2020 09:06:57 GMT  
		Size: 409.9 KB (409875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad3f9cade0fa9bda2c0f45df3a77c780ebc4adea7badb3b8387fed928c60ed7`  
		Last Modified: Fri, 24 Apr 2020 09:07:21 GMT  
		Size: 7.3 MB (7260512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ad499a196593cd717672adacc0550293f8b2c00a5907255640b27d266bc05a`  
		Last Modified: Fri, 24 Apr 2020 09:07:21 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5831b0ffd2731f416315c93a640459b17492812a21b7a6fba00919faaeb1d5`  
		Last Modified: Fri, 24 Apr 2020 09:07:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-alpine3.11` - linux; s390x

```console
$ docker pull redis@sha256:5ad55b9f660c1e3b315e26e3497b9e4d270a5dd7ff431b14d9a17cf78fcac287
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10008638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dd64fd99b54ef1c40f2cd3351efcaf43b4d026dfcfe78315787e7a8220ffee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:02:35 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 07:02:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 24 Apr 2020 07:03:22 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 24 Apr 2020 07:03:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 24 Apr 2020 07:03:53 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 24 Apr 2020 07:03:53 GMT
VOLUME [/data]
# Fri, 24 Apr 2020 07:03:54 GMT
WORKDIR /data
# Fri, 24 Apr 2020 07:03:54 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 24 Apr 2020 07:03:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 07:03:54 GMT
EXPOSE 6379
# Fri, 24 Apr 2020 07:03:54 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2da1b54f68b54cfd646e4cf510a14593b857e3c6e7732985b5a3bc5e213a72a`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f0a46f7a997ac6f05cd804b3a0f56c74348f25fd9e164c66ab7c5c4a6a2c82`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 407.4 KB (407392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3c809e9bcb4892e2da01d3bae84664c06e6bb0929c6813ef47a1aaaa3d675f`  
		Last Modified: Fri, 24 Apr 2020 07:05:07 GMT  
		Size: 7.0 MB (7016584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1cb7e35314fbaf45935cb538fb36cc01e53dff4d37131a3497fd376720294e`  
		Last Modified: Fri, 24 Apr 2020 07:05:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529922dc84cb9fec77a0630b9ad535a7c843db2cd4518c25442c47fbc986d8b7`  
		Last Modified: Fri, 24 Apr 2020 07:05:06 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:5-buster`

```console
$ docker pull redis@sha256:08aab527ca57f536f2805e031535a6881bab63171146aa6414de69d54b14a84d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redis:5-buster` - linux; amd64

```console
$ docker pull redis@sha256:ae4b7c01640a2688e9ef5dd630e2135df7a9e711e712e3d9eab05608d34e2b84
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35863829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5120d23bad51618dd0e19bddd616d555f3cb01753a930c9532364e0d2505b7e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 02:15:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 02:15:48 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 02:17:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:17:30 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:17:30 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:17:30 GMT
WORKDIR /data
# Sat, 16 May 2020 02:17:31 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:17:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:17:31 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:17:32 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846bf5faff48ca0599eb0ab51917d8471164ff02f04524d108bfc8b89dcf50cd`  
		Last Modified: Sat, 16 May 2020 02:20:41 GMT  
		Size: 7.3 MB (7345115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affafbdb5f81d8218bb0f3a60783e92e55fa09ba0a2488f3488488608fa1153d`  
		Last Modified: Sat, 16 May 2020 02:20:38 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdd19e5317241aa2fcd854961c766a5bfc18cbd0db01b18c91404ebdc2ccaa3`  
		Last Modified: Sat, 16 May 2020 02:20:39 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-buster` - linux; arm variant v5

```console
$ docker pull redis@sha256:aa487a40514e78f619cfcb9458a4cba51f5638916d8e4ed3bc10355d362963be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33396150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d3ebf62ba5747e68aa370dc62af6d166b2f494290cc0339c60f17aa271de77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 22:38:03 GMT
ADD file:cbd01ff8d2e40a25bcdb13dc19ffe124c2927b491997dc1c57d4f2c2a308e279 in / 
# Thu, 14 May 2020 22:38:05 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:40:59 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 04:40:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 04:41:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 04:43:01 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 04:43:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 04:43:02 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 04:44:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 04:44:09 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 04:44:09 GMT
VOLUME [/data]
# Fri, 15 May 2020 04:44:10 GMT
WORKDIR /data
# Fri, 15 May 2020 04:44:11 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 04:44:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 04:44:12 GMT
EXPOSE 6379
# Fri, 15 May 2020 04:44:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:24d81022117207b0239d8a8023ca1724b7dde38cb08ce5b9199f59d475d1e600`  
		Last Modified: Thu, 14 May 2020 22:46:51 GMT  
		Size: 24.8 MB (24838470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c13f680b58f95af37082529e8a1ecd6358e22a7e13a75344d8375a03cafb174`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2286bbfcebea1b30a2e862afd7742a7f65237dcabddc9486bfaaf5fd8ba0d65`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.4 MB (1376110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7deffa88c65075e285c0d27dc2aba2336a7a1779ed75bb2f32e760fbab785147`  
		Last Modified: Fri, 15 May 2020 04:44:47 GMT  
		Size: 7.2 MB (7179299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02c5ad0a586c0c745b5df9a3db37bcaf3213a48ab53be3446bd486fa5b85838`  
		Last Modified: Fri, 15 May 2020 04:44:44 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9850cd504042ad62e1898b73b9a1d5d4a95d80bf65a5909d238d56a640697226`  
		Last Modified: Fri, 15 May 2020 04:44:44 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-buster` - linux; arm variant v7

```console
$ docker pull redis@sha256:428b7a31e32fb1a39cc9d41b113e6051359572d96ae9d9906089f4c324a07173
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31109932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3abf0ee6b0b5453a72669cb38743da5af51666c9b3e18ab680cfb0c65e3241a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 01:00:06 GMT
ADD file:e3f9a454eccb40b4d7bf1dcc17ec29589a007ac67545d1cb5b6fa213c872c8f2 in / 
# Fri, 15 May 2020 01:00:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 16:49:40 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 16:49:40 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 16:50:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 16:51:47 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 16:51:48 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 16:51:49 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 16:52:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 16:52:49 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 16:52:50 GMT
VOLUME [/data]
# Fri, 15 May 2020 16:52:51 GMT
WORKDIR /data
# Fri, 15 May 2020 16:52:51 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 16:52:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 16:52:53 GMT
EXPOSE 6379
# Fri, 15 May 2020 16:52:53 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e41e28500352be59188c3d871a4b5a3f594350b860a9a36ed5808a35920bdae4`  
		Last Modified: Fri, 15 May 2020 01:11:21 GMT  
		Size: 22.7 MB (22705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6732859766aedad40f91cd96df6b5a6930efe6614b0f084b8459d93c22a69`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed92b736a14b52db74c7cd9919c66ce953393f0544906969081702697d5a6b54`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.4 MB (1368207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114f7e7289bd10cc75ccedb5c36ef2ef1bcdd04a0d015af0e3f5dbca67c2e2d9`  
		Last Modified: Fri, 15 May 2020 16:53:44 GMT  
		Size: 7.0 MB (7033534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9e37951fe3e21e2afb2d25fe8ec18da89f27d40c88b7e83b5991380af42227`  
		Last Modified: Fri, 15 May 2020 16:53:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b778ce965d8bdff427c804f43a751b2c4e1dc26ba152f53d4abe56a8b4014174`  
		Last Modified: Fri, 15 May 2020 16:53:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-buster` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:457f1b0ba059ac05ce46805c92967506f61bb69a38eea8a5aaebf1d5d8da5017
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34547915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ef03b25863b64392c6d8ff085e6b0768f88c8b95692196f79c4846e8f38277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 12:44:06 GMT
ADD file:b305c1792102142f183d3084026f0fc6be3ddf8d1959b32f0a5d22d35eebcd15 in / 
# Fri, 15 May 2020 12:44:07 GMT
CMD ["bash"]
# Sat, 16 May 2020 08:24:10 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 08:24:10 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 08:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 08:27:04 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 08:27:05 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 08:27:05 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 08:28:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:28:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:28:09 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:28:10 GMT
WORKDIR /data
# Sat, 16 May 2020 08:28:11 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 08:28:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:28:12 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:28:12 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8a7e1e68c24e5cac20ef26d29505c58456b561c431f0c683b66d1a0943f40dd4`  
		Last Modified: Fri, 15 May 2020 12:53:36 GMT  
		Size: 25.9 MB (25857195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc5ca4e8f484b410989ac557169938b5fe6288ed5add0839e05a790ef47676`  
		Last Modified: Sat, 16 May 2020 08:28:42 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eccfc30e2be16f57d04f487ed80dd2b52ada557753eca7c79eb2ff88ab421f2`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 1.4 MB (1352995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27089b3134bdd932f8ebb93aef02f95e6883cebfef343a3caad67c05fcc554d9`  
		Last Modified: Sat, 16 May 2020 08:29:17 GMT  
		Size: 7.3 MB (7335450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35769aa5a1907ee966e04244b585d65a7a780c87efb002cf6abdbe16f153d7b`  
		Last Modified: Sat, 16 May 2020 08:29:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e99e4e05b4653f243c0f8a635a0cb3fb3c367a3d2b73667db0301d0f869f14e`  
		Last Modified: Sat, 16 May 2020 08:29:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-buster` - linux; 386

```console
$ docker pull redis@sha256:cbd966cd9fdfda6ba7a4ae65566b21c986580d26bccd7648b431417c79a8797e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372a1f57ccac9f9940a9a3ef51392b6ae15c3b1102c3494fb808505bdc549b2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Sat, 16 May 2020 00:07:24 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 00:07:24 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 00:07:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_VERSION=5.0.9
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Sat, 16 May 2020 00:11:26 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Sat, 16 May 2020 00:13:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:13:21 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:13:21 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:13:21 GMT
WORKDIR /data
# Sat, 16 May 2020 00:13:22 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 00:13:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:13:22 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:13:23 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157733bfb7391a76ac45c4aa7ed1ea9e99ee6b2f4f70fbbab7b48b514fff73fc`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7927326d7d556c02a6f3c72888c9f9d2beb780c097c9fb1ca55539afa2a42d`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.4 MB (1387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346dcb0e7c24e02011edcae7f0884ff428c9b01cd1361cfb068c4cb5ea6c3f5f`  
		Last Modified: Sat, 16 May 2020 00:14:11 GMT  
		Size: 7.0 MB (7008096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19378b87aaceac51732681a095c2679c50ac66b341a727cc4c59c7672e72642b`  
		Last Modified: Sat, 16 May 2020 00:14:09 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d89103e3ff26e632031f9510e343c0480df8aa67080da4f4fe1cd70671a94b2`  
		Last Modified: Sat, 16 May 2020 00:14:09 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-buster` - linux; mips64le

```console
$ docker pull redis@sha256:8b6a10293e59139fa6bcc9fc4b76fa1bece970cbca46f0d4f88ba87ca29fb38d
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34733957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14f6ea4c9fdcd70e15b3ec9963dbf5b3a0cba06b78eca3b49ede54d8eb74633`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 04:48:19 GMT
ADD file:1163d3a5831eb58d132b66b60303169816e7bd8289f19caaac1157179a95f6f9 in / 
# Fri, 15 May 2020 04:48:19 GMT
CMD ["bash"]
# Fri, 15 May 2020 15:35:02 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 15:35:02 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 15:35:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 15:39:12 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 15:39:12 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 15:39:13 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 15:42:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 15:42:32 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 15:42:33 GMT
VOLUME [/data]
# Fri, 15 May 2020 15:42:33 GMT
WORKDIR /data
# Fri, 15 May 2020 15:42:34 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 15:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 15:42:34 GMT
EXPOSE 6379
# Fri, 15 May 2020 15:42:34 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d22357c747999d33ec7501da2c05aa9e95079ebddefbcb326976c5ed5b176b3f`  
		Last Modified: Fri, 15 May 2020 04:57:10 GMT  
		Size: 25.8 MB (25764292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f562c9b9683468308a6f59cab7d724ffc3b35a66acd8ce093b288144db2b7c5`  
		Last Modified: Fri, 15 May 2020 15:42:49 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fda93ec518be6790dd5e435d4bb66cab95d5c14044f01c584fd463ca6ffd290`  
		Last Modified: Fri, 15 May 2020 15:42:50 GMT  
		Size: 1.3 MB (1305516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeb925910423da69c6eda33089a17133d5b1649da9305c560bb62548887111c`  
		Last Modified: Fri, 15 May 2020 15:43:33 GMT  
		Size: 7.7 MB (7661910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89a2cb8235be9f7742a87b9e6cb1a8e822fa316f9524eb2e63e180907993838`  
		Last Modified: Fri, 15 May 2020 15:43:26 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe01516addcda29424d0863a92cc972db77274689603262287f4383b2251fb0`  
		Last Modified: Fri, 15 May 2020 15:43:26 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-buster` - linux; ppc64le

```console
$ docker pull redis@sha256:c25f3deade6ecb0d0ab42fa53321c50806dd2471c0a06ec3180217c93e2b50e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39696499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7993e4f9c4d285dffe1be6b2eb7fc6e5872e4c23175ef0b2eecb2f4dfd9c09f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 16 May 2020 17:14:59 GMT
ADD file:b2656a1711bd47585595ae2927cfd4ec00eb903d193583d945b6d60f0a2691bb in / 
# Sat, 16 May 2020 17:15:04 GMT
CMD ["bash"]
# Mon, 18 May 2020 13:30:23 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Mon, 18 May 2020 13:30:26 GMT
ENV GOSU_VERSION=1.12
# Mon, 18 May 2020 13:32:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 18 May 2020 13:38:55 GMT
ENV REDIS_VERSION=5.0.9
# Mon, 18 May 2020 13:38:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Mon, 18 May 2020 13:39:03 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Mon, 18 May 2020 13:41:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:41:57 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:41:59 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:42:03 GMT
WORKDIR /data
# Mon, 18 May 2020 13:42:06 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Mon, 18 May 2020 13:42:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:42:11 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:42:14 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:034d508ed7647e7139951a435acc95e0124f50c984670d0e53b4f5ba25cf6ed1`  
		Last Modified: Sat, 16 May 2020 18:31:49 GMT  
		Size: 30.5 MB (30524456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c613ed63b519e3a0419cf56e14127f5d25466416a8143341540d12cb99943b65`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec60488415c29ebe96bbfabff01925147e50ee55136fdf961fbe8526617f3b`  
		Last Modified: Mon, 18 May 2020 13:42:57 GMT  
		Size: 1.3 MB (1335429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8c21d1569eb7d014ba9bf44dee78260d5e4d8e456b37cb304b127c69940684`  
		Last Modified: Mon, 18 May 2020 13:43:54 GMT  
		Size: 7.8 MB (7834331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c759fe2a72a81200077dd4a171c8c95ea1cecdc62e8a2ae362e0d31f255fc9f9`  
		Last Modified: Mon, 18 May 2020 13:43:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da932920c36a309064e131257fe3ed53362fb1a0d18207a51e7a26735b066838`  
		Last Modified: Mon, 18 May 2020 13:43:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:5-buster` - linux; s390x

```console
$ docker pull redis@sha256:becaadf1b7481b782ca8d0ed939de5e00ca69064a94eef114d443bb75116c1f3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34710318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dba1a9e6bde97648f54ed3508c268f0671bdf3b171629e8a034800658e2ea36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 05:15:35 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 05:15:35 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 05:15:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_VERSION=5.0.9
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-5.0.9.tar.gz
# Fri, 15 May 2020 05:16:36 GMT
ENV REDIS_DOWNLOAD_SHA=53d0ae164cd33536c3d4b720ae9a128ea6166ebf04ff1add3b85f1242090cb85
# Fri, 15 May 2020 05:17:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 05:17:06 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 05:17:06 GMT
VOLUME [/data]
# Fri, 15 May 2020 05:17:06 GMT
WORKDIR /data
# Fri, 15 May 2020 05:17:07 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 05:17:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 05:17:07 GMT
EXPOSE 6379
# Fri, 15 May 2020 05:17:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e40cd0998be29e9cce5152b7d3644b03b888bcca5db2049d43c93bf53185d`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc1e5303c90f8fcd807a5042757fb4de087ae4b3319afca416b72e858de788c`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.4 MB (1403711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fff5a343dd72b836a3f99619249e4fd4b82b0d09950a9552781d2fcbe733c9`  
		Last Modified: Fri, 15 May 2020 05:17:43 GMT  
		Size: 7.6 MB (7591396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30482d87111f841181c863a01b1ad9890bab844f7bf3f24c8de746052ebc5d71`  
		Last Modified: Fri, 15 May 2020 05:17:42 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a814c5126e00d2ce60c95caacba2b4f8236c88df49bcaf578c2500a12404dc3`  
		Last Modified: Fri, 15 May 2020 05:17:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:6`

```console
$ docker pull redis@sha256:f345892f9889fbd14e46eb00ae06f99da2190cfcbfbf2d0d6e71f6d4571eb11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redis:6` - linux; amd64

```console
$ docker pull redis@sha256:ab54d0eafe20eeb825ab7b5a58d317cae5a4388c3acf1d91f9c33985b20ff273
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38167360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c654ea77ff723987795e7ce2ef47dbe8e40d5a0f819c04a19be78b95b3b5e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:13:33 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:13:33 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:13:33 GMT
WORKDIR /data
# Sat, 16 May 2020 02:13:34 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:13:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:13:34 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:13:35 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23612dae160f1ec7bcb03995f6511b98869720a2af255e8ed290591b402246b5`  
		Last Modified: Sat, 16 May 2020 02:20:21 GMT  
		Size: 9.6 MB (9648645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c369ccd196fb08d91f340da5260c798cadbadfbb4ab1e323cbbf6b7478a6aa`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a702f65a6a9fe28799e5d494490ab96d303ba44fc2286c2c65775b95de371f2`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6` - linux; arm variant v5

```console
$ docker pull redis@sha256:1047d344de59e9413a8a6e2e394f9ff411516a2ef2fea4aee693a781a5eb7bf9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35393451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1c15fd4eb475c34af8c1fa99e894a544b78230f55e77b10eab309385f3e0e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 22:38:03 GMT
ADD file:cbd01ff8d2e40a25bcdb13dc19ffe124c2927b491997dc1c57d4f2c2a308e279 in / 
# Thu, 14 May 2020 22:38:05 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:40:59 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 04:40:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 04:41:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 23:12:39 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 23:12:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 23:12:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 23:14:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 23:14:55 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 23:14:56 GMT
VOLUME [/data]
# Fri, 15 May 2020 23:14:57 GMT
WORKDIR /data
# Fri, 15 May 2020 23:14:58 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 23:14:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 23:15:00 GMT
EXPOSE 6379
# Fri, 15 May 2020 23:15:00 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:24d81022117207b0239d8a8023ca1724b7dde38cb08ce5b9199f59d475d1e600`  
		Last Modified: Thu, 14 May 2020 22:46:51 GMT  
		Size: 24.8 MB (24838470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c13f680b58f95af37082529e8a1ecd6358e22a7e13a75344d8375a03cafb174`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2286bbfcebea1b30a2e862afd7742a7f65237dcabddc9486bfaaf5fd8ba0d65`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.4 MB (1376110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f639441dae5f4f944717cd02a5f128e4758eac38d8ab22f77b69484becc555`  
		Last Modified: Fri, 15 May 2020 23:15:35 GMT  
		Size: 9.2 MB (9176601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c577f5c08a0c4b296439ea910cc8bd148bd1e69058c7af5d40c87b0e825b27`  
		Last Modified: Fri, 15 May 2020 23:15:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dfe2add81403d228b336a3189e8aa2903f266cb813294e4b69d558d25d34919`  
		Last Modified: Fri, 15 May 2020 23:15:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6` - linux; arm variant v7

```console
$ docker pull redis@sha256:c682e2bc4474179d62f5943399e78ac9fa38797880bdbdef7615ec58559d6fb6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33018384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc7563c765d7fbfa56e311c229f98caa69bb0cd10e17d2f2344df5911079ba2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 01:00:06 GMT
ADD file:e3f9a454eccb40b4d7bf1dcc17ec29589a007ac67545d1cb5b6fa213c872c8f2 in / 
# Fri, 15 May 2020 01:00:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 16:49:40 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 16:49:40 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 16:50:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 06:31:45 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 06:31:45 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 06:31:46 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 06:32:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 06:33:00 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 06:33:00 GMT
VOLUME [/data]
# Sat, 16 May 2020 06:33:01 GMT
WORKDIR /data
# Sat, 16 May 2020 06:33:02 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 06:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 06:33:03 GMT
EXPOSE 6379
# Sat, 16 May 2020 06:33:04 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e41e28500352be59188c3d871a4b5a3f594350b860a9a36ed5808a35920bdae4`  
		Last Modified: Fri, 15 May 2020 01:11:21 GMT  
		Size: 22.7 MB (22705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6732859766aedad40f91cd96df6b5a6930efe6614b0f084b8459d93c22a69`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed92b736a14b52db74c7cd9919c66ce953393f0544906969081702697d5a6b54`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.4 MB (1368207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae49590ac9360b33276abbdc9f1f45988c0c47b5efbd5b0f55d5dfa258b9ba5a`  
		Last Modified: Sat, 16 May 2020 06:35:15 GMT  
		Size: 8.9 MB (8941986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc7ac3e6ef453bf3e43ffc9747527339b36ba8a594ed32e4e32cd445f706bd2`  
		Last Modified: Sat, 16 May 2020 06:35:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8549d28648c0fd590b2bb28888a0f398a9c44497fdc234419f1c06fdc807eb7`  
		Last Modified: Sat, 16 May 2020 06:35:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:fefa8a4cc0bd93b3323c54e3f3aa33ced6f32c9471e5857b067cbf775d7cc918
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36725296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8727a8f0bd0aa8dc538822706743dcc10299697988254fbb44dfec9676eb56b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 12:44:06 GMT
ADD file:b305c1792102142f183d3084026f0fc6be3ddf8d1959b32f0a5d22d35eebcd15 in / 
# Fri, 15 May 2020 12:44:07 GMT
CMD ["bash"]
# Sat, 16 May 2020 08:24:10 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 08:24:10 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 08:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 08:24:37 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 08:24:37 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 08:24:38 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 08:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:25:46 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:25:46 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:25:47 GMT
WORKDIR /data
# Sat, 16 May 2020 08:25:48 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 08:25:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:25:49 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:25:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8a7e1e68c24e5cac20ef26d29505c58456b561c431f0c683b66d1a0943f40dd4`  
		Last Modified: Fri, 15 May 2020 12:53:36 GMT  
		Size: 25.9 MB (25857195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc5ca4e8f484b410989ac557169938b5fe6288ed5add0839e05a790ef47676`  
		Last Modified: Sat, 16 May 2020 08:28:42 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eccfc30e2be16f57d04f487ed80dd2b52ada557753eca7c79eb2ff88ab421f2`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 1.4 MB (1352995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16b8ee6261f593931e5c80c002e18026c3b7bb7d343befbc1fa756ed97c267b`  
		Last Modified: Sat, 16 May 2020 08:28:46 GMT  
		Size: 9.5 MB (9512830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cc79ffa02956bccb011cc1ff2235860b2826a4728941da06492bd6e52f443e`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235fadffc19d75adb68374da679a5c9976a38b0474e07ce04bab7d7093b121b6`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6` - linux; 386

```console
$ docker pull redis@sha256:4171a489575082d2d6af76fa8638109e257d3c413eff0b47746288d64b7c5161
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38426981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1dbd0ad2ae3cebd5b89eeb326a1602a2e5f070d58fc8b5f7ef2a8f13f447fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Sat, 16 May 2020 00:07:24 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 00:07:24 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 00:07:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 00:09:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:09:23 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:09:23 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:09:24 GMT
WORKDIR /data
# Sat, 16 May 2020 00:09:24 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 00:09:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:09:25 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:09:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157733bfb7391a76ac45c4aa7ed1ea9e99ee6b2f4f70fbbab7b48b514fff73fc`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7927326d7d556c02a6f3c72888c9f9d2beb780c097c9fb1ca55539afa2a42d`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.4 MB (1387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f28c9a9abf780003c46983a03474d1009255ee52e02e3d6b5387645a25676`  
		Last Modified: Sat, 16 May 2020 00:13:51 GMT  
		Size: 9.3 MB (9282358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4252a3c771aac801bae55f4d6153efe090eae2e87d538bb540d9bfdabf1c07`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7baa10daa19f6859f36ad1667478b73ec03e78417cce615c228b8ff5f468e13`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6` - linux; mips64le

```console
$ docker pull redis@sha256:5be8885d29600ec5aa62a44c884f05a27a85156be9bcb6ee7fc5fc51abb06840
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36602715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386312a161a758c285fb32d1403def9b9a2ccd8089f8fde65b3c939dce9244b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 04:48:19 GMT
ADD file:1163d3a5831eb58d132b66b60303169816e7bd8289f19caaac1157179a95f6f9 in / 
# Fri, 15 May 2020 04:48:19 GMT
CMD ["bash"]
# Fri, 15 May 2020 15:35:02 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 15:35:02 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 15:35:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 01:59:50 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 01:59:50 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 01:59:51 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:03:22 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:03:23 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:03:23 GMT
WORKDIR /data
# Sat, 16 May 2020 02:03:23 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:03:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:03:24 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:03:24 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d22357c747999d33ec7501da2c05aa9e95079ebddefbcb326976c5ed5b176b3f`  
		Last Modified: Fri, 15 May 2020 04:57:10 GMT  
		Size: 25.8 MB (25764292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f562c9b9683468308a6f59cab7d724ffc3b35a66acd8ce093b288144db2b7c5`  
		Last Modified: Fri, 15 May 2020 15:42:49 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fda93ec518be6790dd5e435d4bb66cab95d5c14044f01c584fd463ca6ffd290`  
		Last Modified: Fri, 15 May 2020 15:42:50 GMT  
		Size: 1.3 MB (1305516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb60cef9605760eb551d25d4fd2012fbfee55e53a2fc8015e348b35d1c605fe1`  
		Last Modified: Sat, 16 May 2020 02:03:57 GMT  
		Size: 9.5 MB (9530668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0260009eaa931057e783dd3d048e8380b054f9217f32ed1a22b242df7faaff`  
		Last Modified: Sat, 16 May 2020 02:03:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc70c6ee351687f96473d0a015d3ef6e321df0663132a51f3de2d4422313dfed`  
		Last Modified: Sat, 16 May 2020 02:03:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6` - linux; ppc64le

```console
$ docker pull redis@sha256:a08a8ff07e718a2a11e9de8d732ed3b9c8ddf9f6aa3914cc71c18e94de4bd5fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42115418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6f886000af62e580a3a50954e45ae47e2207c358362bea46ddd0b2242f0cc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 16 May 2020 17:14:59 GMT
ADD file:b2656a1711bd47585595ae2927cfd4ec00eb903d193583d945b6d60f0a2691bb in / 
# Sat, 16 May 2020 17:15:04 GMT
CMD ["bash"]
# Mon, 18 May 2020 13:30:23 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Mon, 18 May 2020 13:30:26 GMT
ENV GOSU_VERSION=1.12
# Mon, 18 May 2020 13:32:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 18 May 2020 13:32:31 GMT
ENV REDIS_VERSION=6.0.2
# Mon, 18 May 2020 13:32:34 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Mon, 18 May 2020 13:32:36 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Mon, 18 May 2020 13:35:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:35:48 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:35:53 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:35:59 GMT
WORKDIR /data
# Mon, 18 May 2020 13:36:02 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Mon, 18 May 2020 13:36:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:36:13 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:36:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:034d508ed7647e7139951a435acc95e0124f50c984670d0e53b4f5ba25cf6ed1`  
		Last Modified: Sat, 16 May 2020 18:31:49 GMT  
		Size: 30.5 MB (30524456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c613ed63b519e3a0419cf56e14127f5d25466416a8143341540d12cb99943b65`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec60488415c29ebe96bbfabff01925147e50ee55136fdf961fbe8526617f3b`  
		Last Modified: Mon, 18 May 2020 13:42:57 GMT  
		Size: 1.3 MB (1335429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaf24998a2bd9be32258b02fa8e7f6f41d0eda42d774cac44dcabd35978f81d`  
		Last Modified: Mon, 18 May 2020 13:42:59 GMT  
		Size: 10.3 MB (10253250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6948fa0de358f9d87f91ee1e03e42297fb7f70db44a3fc74091faac19916c2`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24281879de8036ec53f002b70225e29b23542cc353d0189e2cf41dd4db52e89a`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6` - linux; s390x

```console
$ docker pull redis@sha256:9ef11ffd48bd63460ec92a2e14ef5b3fce4eaa785fbdec11751a934ad38d601d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36741516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e6564e23714b9e21badf63a7c7ce03ab2de0060269e6b9aa3644a656750072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 05:15:35 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 05:15:35 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 05:15:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 22:41:40 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 22:41:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 22:41:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 22:42:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 22:42:14 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 22:42:15 GMT
VOLUME [/data]
# Fri, 15 May 2020 22:42:15 GMT
WORKDIR /data
# Fri, 15 May 2020 22:42:15 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 22:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 22:42:15 GMT
EXPOSE 6379
# Fri, 15 May 2020 22:42:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e40cd0998be29e9cce5152b7d3644b03b888bcca5db2049d43c93bf53185d`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc1e5303c90f8fcd807a5042757fb4de087ae4b3319afca416b72e858de788c`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.4 MB (1403711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5d61c1be6277797ce170d2b088f07f55873edc9b1a71d02a2d155dd4e00c6`  
		Last Modified: Fri, 15 May 2020 22:43:45 GMT  
		Size: 9.6 MB (9622596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e520dcecd5852ea3751c3d41ca8c103d95984d027003a983f3c118645530282`  
		Last Modified: Fri, 15 May 2020 22:43:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89764005f67e8cd243c7c732985b0b2b9863ded8a6f2fa729c6c8102aa6bf73d`  
		Last Modified: Fri, 15 May 2020 22:43:48 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:6.0`

```console
$ docker pull redis@sha256:f345892f9889fbd14e46eb00ae06f99da2190cfcbfbf2d0d6e71f6d4571eb11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redis:6.0` - linux; amd64

```console
$ docker pull redis@sha256:ab54d0eafe20eeb825ab7b5a58d317cae5a4388c3acf1d91f9c33985b20ff273
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38167360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c654ea77ff723987795e7ce2ef47dbe8e40d5a0f819c04a19be78b95b3b5e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:13:33 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:13:33 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:13:33 GMT
WORKDIR /data
# Sat, 16 May 2020 02:13:34 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:13:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:13:34 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:13:35 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23612dae160f1ec7bcb03995f6511b98869720a2af255e8ed290591b402246b5`  
		Last Modified: Sat, 16 May 2020 02:20:21 GMT  
		Size: 9.6 MB (9648645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c369ccd196fb08d91f340da5260c798cadbadfbb4ab1e323cbbf6b7478a6aa`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a702f65a6a9fe28799e5d494490ab96d303ba44fc2286c2c65775b95de371f2`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0` - linux; arm variant v5

```console
$ docker pull redis@sha256:1047d344de59e9413a8a6e2e394f9ff411516a2ef2fea4aee693a781a5eb7bf9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35393451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1c15fd4eb475c34af8c1fa99e894a544b78230f55e77b10eab309385f3e0e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 22:38:03 GMT
ADD file:cbd01ff8d2e40a25bcdb13dc19ffe124c2927b491997dc1c57d4f2c2a308e279 in / 
# Thu, 14 May 2020 22:38:05 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:40:59 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 04:40:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 04:41:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 23:12:39 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 23:12:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 23:12:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 23:14:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 23:14:55 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 23:14:56 GMT
VOLUME [/data]
# Fri, 15 May 2020 23:14:57 GMT
WORKDIR /data
# Fri, 15 May 2020 23:14:58 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 23:14:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 23:15:00 GMT
EXPOSE 6379
# Fri, 15 May 2020 23:15:00 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:24d81022117207b0239d8a8023ca1724b7dde38cb08ce5b9199f59d475d1e600`  
		Last Modified: Thu, 14 May 2020 22:46:51 GMT  
		Size: 24.8 MB (24838470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c13f680b58f95af37082529e8a1ecd6358e22a7e13a75344d8375a03cafb174`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2286bbfcebea1b30a2e862afd7742a7f65237dcabddc9486bfaaf5fd8ba0d65`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.4 MB (1376110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f639441dae5f4f944717cd02a5f128e4758eac38d8ab22f77b69484becc555`  
		Last Modified: Fri, 15 May 2020 23:15:35 GMT  
		Size: 9.2 MB (9176601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c577f5c08a0c4b296439ea910cc8bd148bd1e69058c7af5d40c87b0e825b27`  
		Last Modified: Fri, 15 May 2020 23:15:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dfe2add81403d228b336a3189e8aa2903f266cb813294e4b69d558d25d34919`  
		Last Modified: Fri, 15 May 2020 23:15:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0` - linux; arm variant v7

```console
$ docker pull redis@sha256:c682e2bc4474179d62f5943399e78ac9fa38797880bdbdef7615ec58559d6fb6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33018384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc7563c765d7fbfa56e311c229f98caa69bb0cd10e17d2f2344df5911079ba2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 01:00:06 GMT
ADD file:e3f9a454eccb40b4d7bf1dcc17ec29589a007ac67545d1cb5b6fa213c872c8f2 in / 
# Fri, 15 May 2020 01:00:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 16:49:40 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 16:49:40 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 16:50:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 06:31:45 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 06:31:45 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 06:31:46 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 06:32:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 06:33:00 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 06:33:00 GMT
VOLUME [/data]
# Sat, 16 May 2020 06:33:01 GMT
WORKDIR /data
# Sat, 16 May 2020 06:33:02 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 06:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 06:33:03 GMT
EXPOSE 6379
# Sat, 16 May 2020 06:33:04 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e41e28500352be59188c3d871a4b5a3f594350b860a9a36ed5808a35920bdae4`  
		Last Modified: Fri, 15 May 2020 01:11:21 GMT  
		Size: 22.7 MB (22705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6732859766aedad40f91cd96df6b5a6930efe6614b0f084b8459d93c22a69`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed92b736a14b52db74c7cd9919c66ce953393f0544906969081702697d5a6b54`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.4 MB (1368207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae49590ac9360b33276abbdc9f1f45988c0c47b5efbd5b0f55d5dfa258b9ba5a`  
		Last Modified: Sat, 16 May 2020 06:35:15 GMT  
		Size: 8.9 MB (8941986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc7ac3e6ef453bf3e43ffc9747527339b36ba8a594ed32e4e32cd445f706bd2`  
		Last Modified: Sat, 16 May 2020 06:35:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8549d28648c0fd590b2bb28888a0f398a9c44497fdc234419f1c06fdc807eb7`  
		Last Modified: Sat, 16 May 2020 06:35:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:fefa8a4cc0bd93b3323c54e3f3aa33ced6f32c9471e5857b067cbf775d7cc918
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36725296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8727a8f0bd0aa8dc538822706743dcc10299697988254fbb44dfec9676eb56b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 12:44:06 GMT
ADD file:b305c1792102142f183d3084026f0fc6be3ddf8d1959b32f0a5d22d35eebcd15 in / 
# Fri, 15 May 2020 12:44:07 GMT
CMD ["bash"]
# Sat, 16 May 2020 08:24:10 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 08:24:10 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 08:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 08:24:37 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 08:24:37 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 08:24:38 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 08:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:25:46 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:25:46 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:25:47 GMT
WORKDIR /data
# Sat, 16 May 2020 08:25:48 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 08:25:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:25:49 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:25:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8a7e1e68c24e5cac20ef26d29505c58456b561c431f0c683b66d1a0943f40dd4`  
		Last Modified: Fri, 15 May 2020 12:53:36 GMT  
		Size: 25.9 MB (25857195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc5ca4e8f484b410989ac557169938b5fe6288ed5add0839e05a790ef47676`  
		Last Modified: Sat, 16 May 2020 08:28:42 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eccfc30e2be16f57d04f487ed80dd2b52ada557753eca7c79eb2ff88ab421f2`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 1.4 MB (1352995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16b8ee6261f593931e5c80c002e18026c3b7bb7d343befbc1fa756ed97c267b`  
		Last Modified: Sat, 16 May 2020 08:28:46 GMT  
		Size: 9.5 MB (9512830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cc79ffa02956bccb011cc1ff2235860b2826a4728941da06492bd6e52f443e`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235fadffc19d75adb68374da679a5c9976a38b0474e07ce04bab7d7093b121b6`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0` - linux; 386

```console
$ docker pull redis@sha256:4171a489575082d2d6af76fa8638109e257d3c413eff0b47746288d64b7c5161
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38426981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1dbd0ad2ae3cebd5b89eeb326a1602a2e5f070d58fc8b5f7ef2a8f13f447fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Sat, 16 May 2020 00:07:24 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 00:07:24 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 00:07:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 00:09:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:09:23 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:09:23 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:09:24 GMT
WORKDIR /data
# Sat, 16 May 2020 00:09:24 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 00:09:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:09:25 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:09:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157733bfb7391a76ac45c4aa7ed1ea9e99ee6b2f4f70fbbab7b48b514fff73fc`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7927326d7d556c02a6f3c72888c9f9d2beb780c097c9fb1ca55539afa2a42d`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.4 MB (1387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f28c9a9abf780003c46983a03474d1009255ee52e02e3d6b5387645a25676`  
		Last Modified: Sat, 16 May 2020 00:13:51 GMT  
		Size: 9.3 MB (9282358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4252a3c771aac801bae55f4d6153efe090eae2e87d538bb540d9bfdabf1c07`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7baa10daa19f6859f36ad1667478b73ec03e78417cce615c228b8ff5f468e13`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0` - linux; mips64le

```console
$ docker pull redis@sha256:5be8885d29600ec5aa62a44c884f05a27a85156be9bcb6ee7fc5fc51abb06840
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36602715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386312a161a758c285fb32d1403def9b9a2ccd8089f8fde65b3c939dce9244b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 04:48:19 GMT
ADD file:1163d3a5831eb58d132b66b60303169816e7bd8289f19caaac1157179a95f6f9 in / 
# Fri, 15 May 2020 04:48:19 GMT
CMD ["bash"]
# Fri, 15 May 2020 15:35:02 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 15:35:02 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 15:35:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 01:59:50 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 01:59:50 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 01:59:51 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:03:22 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:03:23 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:03:23 GMT
WORKDIR /data
# Sat, 16 May 2020 02:03:23 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:03:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:03:24 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:03:24 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d22357c747999d33ec7501da2c05aa9e95079ebddefbcb326976c5ed5b176b3f`  
		Last Modified: Fri, 15 May 2020 04:57:10 GMT  
		Size: 25.8 MB (25764292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f562c9b9683468308a6f59cab7d724ffc3b35a66acd8ce093b288144db2b7c5`  
		Last Modified: Fri, 15 May 2020 15:42:49 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fda93ec518be6790dd5e435d4bb66cab95d5c14044f01c584fd463ca6ffd290`  
		Last Modified: Fri, 15 May 2020 15:42:50 GMT  
		Size: 1.3 MB (1305516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb60cef9605760eb551d25d4fd2012fbfee55e53a2fc8015e348b35d1c605fe1`  
		Last Modified: Sat, 16 May 2020 02:03:57 GMT  
		Size: 9.5 MB (9530668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0260009eaa931057e783dd3d048e8380b054f9217f32ed1a22b242df7faaff`  
		Last Modified: Sat, 16 May 2020 02:03:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc70c6ee351687f96473d0a015d3ef6e321df0663132a51f3de2d4422313dfed`  
		Last Modified: Sat, 16 May 2020 02:03:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0` - linux; ppc64le

```console
$ docker pull redis@sha256:a08a8ff07e718a2a11e9de8d732ed3b9c8ddf9f6aa3914cc71c18e94de4bd5fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42115418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6f886000af62e580a3a50954e45ae47e2207c358362bea46ddd0b2242f0cc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 16 May 2020 17:14:59 GMT
ADD file:b2656a1711bd47585595ae2927cfd4ec00eb903d193583d945b6d60f0a2691bb in / 
# Sat, 16 May 2020 17:15:04 GMT
CMD ["bash"]
# Mon, 18 May 2020 13:30:23 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Mon, 18 May 2020 13:30:26 GMT
ENV GOSU_VERSION=1.12
# Mon, 18 May 2020 13:32:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 18 May 2020 13:32:31 GMT
ENV REDIS_VERSION=6.0.2
# Mon, 18 May 2020 13:32:34 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Mon, 18 May 2020 13:32:36 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Mon, 18 May 2020 13:35:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:35:48 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:35:53 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:35:59 GMT
WORKDIR /data
# Mon, 18 May 2020 13:36:02 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Mon, 18 May 2020 13:36:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:36:13 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:36:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:034d508ed7647e7139951a435acc95e0124f50c984670d0e53b4f5ba25cf6ed1`  
		Last Modified: Sat, 16 May 2020 18:31:49 GMT  
		Size: 30.5 MB (30524456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c613ed63b519e3a0419cf56e14127f5d25466416a8143341540d12cb99943b65`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec60488415c29ebe96bbfabff01925147e50ee55136fdf961fbe8526617f3b`  
		Last Modified: Mon, 18 May 2020 13:42:57 GMT  
		Size: 1.3 MB (1335429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaf24998a2bd9be32258b02fa8e7f6f41d0eda42d774cac44dcabd35978f81d`  
		Last Modified: Mon, 18 May 2020 13:42:59 GMT  
		Size: 10.3 MB (10253250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6948fa0de358f9d87f91ee1e03e42297fb7f70db44a3fc74091faac19916c2`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24281879de8036ec53f002b70225e29b23542cc353d0189e2cf41dd4db52e89a`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0` - linux; s390x

```console
$ docker pull redis@sha256:9ef11ffd48bd63460ec92a2e14ef5b3fce4eaa785fbdec11751a934ad38d601d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36741516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e6564e23714b9e21badf63a7c7ce03ab2de0060269e6b9aa3644a656750072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 05:15:35 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 05:15:35 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 05:15:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 22:41:40 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 22:41:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 22:41:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 22:42:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 22:42:14 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 22:42:15 GMT
VOLUME [/data]
# Fri, 15 May 2020 22:42:15 GMT
WORKDIR /data
# Fri, 15 May 2020 22:42:15 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 22:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 22:42:15 GMT
EXPOSE 6379
# Fri, 15 May 2020 22:42:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e40cd0998be29e9cce5152b7d3644b03b888bcca5db2049d43c93bf53185d`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc1e5303c90f8fcd807a5042757fb4de087ae4b3319afca416b72e858de788c`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.4 MB (1403711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5d61c1be6277797ce170d2b088f07f55873edc9b1a71d02a2d155dd4e00c6`  
		Last Modified: Fri, 15 May 2020 22:43:45 GMT  
		Size: 9.6 MB (9622596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e520dcecd5852ea3751c3d41ca8c103d95984d027003a983f3c118645530282`  
		Last Modified: Fri, 15 May 2020 22:43:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89764005f67e8cd243c7c732985b0b2b9863ded8a6f2fa729c6c8102aa6bf73d`  
		Last Modified: Fri, 15 May 2020 22:43:48 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:6.0.3`

**does not exist** (yet?)

## `redis:6.0.3-alpine`

**does not exist** (yet?)

## `redis:6.0.3-alpine3.11`

**does not exist** (yet?)

## `redis:6.0.3-buster`

**does not exist** (yet?)

## `redis:6.0-alpine`

```console
$ docker pull redis@sha256:b7e093c1a1cd040698fc28e4be453d8df1a46323fa4178d6d2d5fcb3bff88c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:6.0-alpine` - linux; amd64

```console
$ docker pull redis@sha256:e5146a61518fef302756bd0bf226ac530fc23d7537097fa378cc50fcb5778b64
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10615454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ceee5c3fa3cea2607d5e2bcc54d019be616e322979be8fc7a8d0d78b59a1f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:19:42 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 19:19:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:15:36 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:15:36 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:15:37 GMT
WORKDIR /data
# Sat, 16 May 2020 02:15:37 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 02:15:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:15:38 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:15:38 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0373118a0d956ca0ee963e307457f45f073db9096f7c6f87c10251d071f0dc`  
		Last Modified: Fri, 24 Apr 2020 19:23:01 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd369fe62565d644723bfdb734c4ecb2a96191366ec08424146aa9c5ff6b308`  
		Last Modified: Fri, 24 Apr 2020 19:23:02 GMT  
		Size: 402.6 KB (402568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d862fc04e31c48831cc75b3b3868126e27f4e51c45bdcddb6ffc7c94b9205a76`  
		Last Modified: Sat, 16 May 2020 02:20:31 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb087a9da0889770a90077b54e12441d375e7027b377997f98a5e6d827ab3fe`  
		Last Modified: Sat, 16 May 2020 02:20:29 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be29dc118a7a01cd97bac04e83376259dee6d48d1cf35a94a8d26d3a73159bb`  
		Last Modified: Sat, 16 May 2020 02:20:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:4057fbe62d49d301734916e4d6d7dd8f9c2d06ebfdad741698aa18ff152b642c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10312873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00275d208cadbfe750c573429cfd2721a47e1b792b022432d241395fbe82dbb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:30:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 23 Apr 2020 22:30:20 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 15 May 2020 23:24:21 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 23:24:22 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 23:24:23 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 23:25:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 23:25:28 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 23:25:30 GMT
VOLUME [/data]
# Fri, 15 May 2020 23:25:31 GMT
WORKDIR /data
# Fri, 15 May 2020 23:25:33 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 15 May 2020 23:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 23:25:36 GMT
EXPOSE 6379
# Fri, 15 May 2020 23:25:37 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab5b04292d1974b3feedf74dddf563efe3ba5b5c38239a49e8adf0ac8140028`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af20f6a7bee5bf869254b4964c1a5d8dd5ef1353ac48081a885920682312555b`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 405.8 KB (405799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cd828ef5be835bbd932776269cc78fa20d6597c5286a8301d9712ca6ba27e1`  
		Last Modified: Fri, 15 May 2020 23:26:27 GMT  
		Size: 7.3 MB (7285336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62363baf5a298c4aecde09c629388197091d261f20fd00863a1693c8847cc34`  
		Last Modified: Fri, 15 May 2020 23:26:27 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0e939b10f701fd67e6400e3d0193f9dbafde2f4bc53215a7305a7c7352bdcb`  
		Last Modified: Fri, 15 May 2020 23:26:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:a9395e60f632ac5808d01ff562ddafcccf44d254f634164eef079f86f0e4fcd3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9972279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af28cbbd6cfbc59e7a5f1a1855dd7caa878b4fd03a749db7b3e51823a58c6b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:51:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 08:51:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 06:33:17 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 06:33:18 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 06:33:20 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 06:34:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 06:34:13 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 06:34:14 GMT
VOLUME [/data]
# Sat, 16 May 2020 06:34:15 GMT
WORKDIR /data
# Sat, 16 May 2020 06:34:16 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 06:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 06:34:17 GMT
EXPOSE 6379
# Sat, 16 May 2020 06:34:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0765e03c998449baf4c76a1011cf80e6ab974db3d5d8da3a361bfeeb875d96db`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07fda5f4761823162fa661b4466f517ad5db025d9689c123221af67af9b53f`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 399.8 KB (399779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b80e8aaba692112e559076be6bb0334a707afdf5e98838a1871caa0866a8c0e`  
		Last Modified: Sat, 16 May 2020 06:35:45 GMT  
		Size: 7.1 MB (7148634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87bac8f769e16dcbd264fba3220e6015ebc7ade1c9dbbeaaf05826b5a181b86`  
		Last Modified: Sat, 16 May 2020 06:35:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb4e2186895e529da275fc0432b79e52a0bb9857639493ec62bcf3bf168531a`  
		Last Modified: Sat, 16 May 2020 06:35:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:745fe4f5f083ab735a17c56a7b213000f369f6cb8f44350c0d5e82db296dade8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10520097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26e9dafef70ab5ad06818ba5897d0d464402e823220faa6d106c50cb1f3828a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:45:10 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 12:45:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 08:25:57 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 08:25:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 08:25:59 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 08:26:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:26:52 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:26:52 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:26:53 GMT
WORKDIR /data
# Sat, 16 May 2020 08:26:54 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 08:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:26:55 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:26:56 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7050d23898adae8e4a2e0ab67eaeab9f9a9ec0fa5b88b128eeff4de1570877`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8982b178d819b1f2f10c3375b2c7ed054157cc5e711b58b6a2dcb376686e5d59`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 404.7 KB (404661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81e21ac53933c4757cd8a04fd0253d126746afcf7e023bbad9a93dec0acd26`  
		Last Modified: Sat, 16 May 2020 08:29:02 GMT  
		Size: 7.4 MB (7389208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e3ddab2b277bd44f7dc380187d16e5028acf9cc4dfee80f19494ea9e060aba`  
		Last Modified: Sat, 16 May 2020 08:28:58 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb66b8b7b33b484540124708f55d85ee24ea6274d5c4dc36ecbd1e84637e678e`  
		Last Modified: Sat, 16 May 2020 08:28:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-alpine` - linux; 386

```console
$ docker pull redis@sha256:bbfdc448dafad37023ae75c4fcfbd5d1ec7bd78aad8e769b62753c36c31757b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10290082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34322bf2334fed58c9521a918064a594354d513fbeec9b4b637dd5be45e8b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:49:36 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 05:49:38 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 00:09:40 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 00:09:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 00:09:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 00:11:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:11:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:11:09 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:11:10 GMT
WORKDIR /data
# Sat, 16 May 2020 00:11:10 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 00:11:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:11:10 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:11:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4eb71d5f124b9b51684034d7d96fba6399ff6892995e51137d0c0617a11fb9`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7685edc32d5ef38faf3beb4310c119862b1dfa18ea58edb0dbca84e9417b267`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 407.9 KB (407901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02f4cc0a73447e7af4c367a8efe6a3fe2e6b6cdf92088abd4c2b8f99f980af`  
		Last Modified: Sat, 16 May 2020 00:14:01 GMT  
		Size: 7.1 MB (7072021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd586489393880a99bcea0f145202694e2d8e8c438c7d6b44741073ea6d2c16`  
		Last Modified: Sat, 16 May 2020 00:13:59 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd50ae8a09e8979660d44015b05f83ff9419212dcd16c1dd9372263dfadaff9`  
		Last Modified: Sat, 16 May 2020 00:13:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:50b2e427f6b8a80a2532561509d6bb630381f1e73683bedb0723222a0391e5aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11129201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7ff884dff0f0f831a77c117ef871f6b9dfe526d553ea1a7178969d1b9abf56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:02:06 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 09:02:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 18 May 2020 13:36:42 GMT
ENV REDIS_VERSION=6.0.2
# Mon, 18 May 2020 13:36:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Mon, 18 May 2020 13:36:56 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Mon, 18 May 2020 13:38:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:38:08 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:38:11 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:38:20 GMT
WORKDIR /data
# Mon, 18 May 2020 13:38:23 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 18 May 2020 13:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:38:32 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:38:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc79e36a18515157312416d029cb35887ee8668b53b6c0e3867a4d0dd8dd231`  
		Last Modified: Fri, 24 Apr 2020 09:06:56 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83078862453fa1de07d734ccc5b995c92cd74710488c11d066ad752e3402d`  
		Last Modified: Fri, 24 Apr 2020 09:06:57 GMT  
		Size: 409.9 KB (409875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432ade9a2f2eaed492af9b2c567a554192ca3c2460cdf54cbdd74ef7e351b5c6`  
		Last Modified: Mon, 18 May 2020 13:43:25 GMT  
		Size: 7.9 MB (7895679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92956e0c94d7efbf996da0a821961e7e25d592d34d3f95cc7117d36ace6c4f8c`  
		Last Modified: Mon, 18 May 2020 13:43:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403543cf6789e71324a71e34551d530ede80b0836ac96a844a65ebb7c978de2`  
		Last Modified: Mon, 18 May 2020 13:43:22 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-alpine` - linux; s390x

```console
$ docker pull redis@sha256:7e87f23ad9c129bc30f56aa8881568fd3bae9fdcf1aca09f9fd15a145a8a78bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10647559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9dc6fb128105420046bfd04554e6dd0f328c259824417652aef3ff4986b8df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:02:35 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 07:02:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 15 May 2020 22:42:24 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 22:42:25 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 22:42:25 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 22:43:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 22:43:01 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 22:43:02 GMT
VOLUME [/data]
# Fri, 15 May 2020 22:43:02 GMT
WORKDIR /data
# Fri, 15 May 2020 22:43:02 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 15 May 2020 22:43:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 22:43:03 GMT
EXPOSE 6379
# Fri, 15 May 2020 22:43:03 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2da1b54f68b54cfd646e4cf510a14593b857e3c6e7732985b5a3bc5e213a72a`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f0a46f7a997ac6f05cd804b3a0f56c74348f25fd9e164c66ab7c5c4a6a2c82`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 407.4 KB (407392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d280287c062cfd9d589ad117076ba536339a11933f5cc8c50679b99a7d5a33`  
		Last Modified: Fri, 15 May 2020 22:43:59 GMT  
		Size: 7.7 MB (7655503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8cd36de079748236b7e47e5540b2968095a52c1e3eb820750e1eb95c3cf282`  
		Last Modified: Fri, 15 May 2020 22:43:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c5e784b212d08809045f9af3f7675dd7d74d224be6831c0bedaf3512f2d204`  
		Last Modified: Fri, 15 May 2020 22:43:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:6.0-alpine3.11`

```console
$ docker pull redis@sha256:b7e093c1a1cd040698fc28e4be453d8df1a46323fa4178d6d2d5fcb3bff88c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:6.0-alpine3.11` - linux; amd64

```console
$ docker pull redis@sha256:e5146a61518fef302756bd0bf226ac530fc23d7537097fa378cc50fcb5778b64
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10615454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ceee5c3fa3cea2607d5e2bcc54d019be616e322979be8fc7a8d0d78b59a1f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:19:42 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 19:19:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:15:36 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:15:36 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:15:37 GMT
WORKDIR /data
# Sat, 16 May 2020 02:15:37 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 02:15:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:15:38 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:15:38 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0373118a0d956ca0ee963e307457f45f073db9096f7c6f87c10251d071f0dc`  
		Last Modified: Fri, 24 Apr 2020 19:23:01 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd369fe62565d644723bfdb734c4ecb2a96191366ec08424146aa9c5ff6b308`  
		Last Modified: Fri, 24 Apr 2020 19:23:02 GMT  
		Size: 402.6 KB (402568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d862fc04e31c48831cc75b3b3868126e27f4e51c45bdcddb6ffc7c94b9205a76`  
		Last Modified: Sat, 16 May 2020 02:20:31 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb087a9da0889770a90077b54e12441d375e7027b377997f98a5e6d827ab3fe`  
		Last Modified: Sat, 16 May 2020 02:20:29 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be29dc118a7a01cd97bac04e83376259dee6d48d1cf35a94a8d26d3a73159bb`  
		Last Modified: Sat, 16 May 2020 02:20:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-alpine3.11` - linux; arm variant v6

```console
$ docker pull redis@sha256:4057fbe62d49d301734916e4d6d7dd8f9c2d06ebfdad741698aa18ff152b642c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10312873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00275d208cadbfe750c573429cfd2721a47e1b792b022432d241395fbe82dbb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:30:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 23 Apr 2020 22:30:20 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 15 May 2020 23:24:21 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 23:24:22 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 23:24:23 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 23:25:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 23:25:28 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 23:25:30 GMT
VOLUME [/data]
# Fri, 15 May 2020 23:25:31 GMT
WORKDIR /data
# Fri, 15 May 2020 23:25:33 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 15 May 2020 23:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 23:25:36 GMT
EXPOSE 6379
# Fri, 15 May 2020 23:25:37 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab5b04292d1974b3feedf74dddf563efe3ba5b5c38239a49e8adf0ac8140028`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af20f6a7bee5bf869254b4964c1a5d8dd5ef1353ac48081a885920682312555b`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 405.8 KB (405799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cd828ef5be835bbd932776269cc78fa20d6597c5286a8301d9712ca6ba27e1`  
		Last Modified: Fri, 15 May 2020 23:26:27 GMT  
		Size: 7.3 MB (7285336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62363baf5a298c4aecde09c629388197091d261f20fd00863a1693c8847cc34`  
		Last Modified: Fri, 15 May 2020 23:26:27 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0e939b10f701fd67e6400e3d0193f9dbafde2f4bc53215a7305a7c7352bdcb`  
		Last Modified: Fri, 15 May 2020 23:26:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-alpine3.11` - linux; arm variant v7

```console
$ docker pull redis@sha256:a9395e60f632ac5808d01ff562ddafcccf44d254f634164eef079f86f0e4fcd3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9972279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af28cbbd6cfbc59e7a5f1a1855dd7caa878b4fd03a749db7b3e51823a58c6b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:51:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 08:51:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 06:33:17 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 06:33:18 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 06:33:20 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 06:34:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 06:34:13 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 06:34:14 GMT
VOLUME [/data]
# Sat, 16 May 2020 06:34:15 GMT
WORKDIR /data
# Sat, 16 May 2020 06:34:16 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 06:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 06:34:17 GMT
EXPOSE 6379
# Sat, 16 May 2020 06:34:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0765e03c998449baf4c76a1011cf80e6ab974db3d5d8da3a361bfeeb875d96db`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07fda5f4761823162fa661b4466f517ad5db025d9689c123221af67af9b53f`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 399.8 KB (399779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b80e8aaba692112e559076be6bb0334a707afdf5e98838a1871caa0866a8c0e`  
		Last Modified: Sat, 16 May 2020 06:35:45 GMT  
		Size: 7.1 MB (7148634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87bac8f769e16dcbd264fba3220e6015ebc7ade1c9dbbeaaf05826b5a181b86`  
		Last Modified: Sat, 16 May 2020 06:35:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb4e2186895e529da275fc0432b79e52a0bb9857639493ec62bcf3bf168531a`  
		Last Modified: Sat, 16 May 2020 06:35:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-alpine3.11` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:745fe4f5f083ab735a17c56a7b213000f369f6cb8f44350c0d5e82db296dade8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10520097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26e9dafef70ab5ad06818ba5897d0d464402e823220faa6d106c50cb1f3828a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:45:10 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 12:45:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 08:25:57 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 08:25:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 08:25:59 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 08:26:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:26:52 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:26:52 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:26:53 GMT
WORKDIR /data
# Sat, 16 May 2020 08:26:54 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 08:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:26:55 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:26:56 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7050d23898adae8e4a2e0ab67eaeab9f9a9ec0fa5b88b128eeff4de1570877`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8982b178d819b1f2f10c3375b2c7ed054157cc5e711b58b6a2dcb376686e5d59`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 404.7 KB (404661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81e21ac53933c4757cd8a04fd0253d126746afcf7e023bbad9a93dec0acd26`  
		Last Modified: Sat, 16 May 2020 08:29:02 GMT  
		Size: 7.4 MB (7389208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e3ddab2b277bd44f7dc380187d16e5028acf9cc4dfee80f19494ea9e060aba`  
		Last Modified: Sat, 16 May 2020 08:28:58 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb66b8b7b33b484540124708f55d85ee24ea6274d5c4dc36ecbd1e84637e678e`  
		Last Modified: Sat, 16 May 2020 08:28:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-alpine3.11` - linux; 386

```console
$ docker pull redis@sha256:bbfdc448dafad37023ae75c4fcfbd5d1ec7bd78aad8e769b62753c36c31757b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10290082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34322bf2334fed58c9521a918064a594354d513fbeec9b4b637dd5be45e8b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:49:36 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 05:49:38 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 00:09:40 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 00:09:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 00:09:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 00:11:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:11:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:11:09 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:11:10 GMT
WORKDIR /data
# Sat, 16 May 2020 00:11:10 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 00:11:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:11:10 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:11:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4eb71d5f124b9b51684034d7d96fba6399ff6892995e51137d0c0617a11fb9`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7685edc32d5ef38faf3beb4310c119862b1dfa18ea58edb0dbca84e9417b267`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 407.9 KB (407901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02f4cc0a73447e7af4c367a8efe6a3fe2e6b6cdf92088abd4c2b8f99f980af`  
		Last Modified: Sat, 16 May 2020 00:14:01 GMT  
		Size: 7.1 MB (7072021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd586489393880a99bcea0f145202694e2d8e8c438c7d6b44741073ea6d2c16`  
		Last Modified: Sat, 16 May 2020 00:13:59 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd50ae8a09e8979660d44015b05f83ff9419212dcd16c1dd9372263dfadaff9`  
		Last Modified: Sat, 16 May 2020 00:13:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-alpine3.11` - linux; ppc64le

```console
$ docker pull redis@sha256:50b2e427f6b8a80a2532561509d6bb630381f1e73683bedb0723222a0391e5aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11129201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7ff884dff0f0f831a77c117ef871f6b9dfe526d553ea1a7178969d1b9abf56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:02:06 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 09:02:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 18 May 2020 13:36:42 GMT
ENV REDIS_VERSION=6.0.2
# Mon, 18 May 2020 13:36:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Mon, 18 May 2020 13:36:56 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Mon, 18 May 2020 13:38:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:38:08 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:38:11 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:38:20 GMT
WORKDIR /data
# Mon, 18 May 2020 13:38:23 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 18 May 2020 13:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:38:32 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:38:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc79e36a18515157312416d029cb35887ee8668b53b6c0e3867a4d0dd8dd231`  
		Last Modified: Fri, 24 Apr 2020 09:06:56 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83078862453fa1de07d734ccc5b995c92cd74710488c11d066ad752e3402d`  
		Last Modified: Fri, 24 Apr 2020 09:06:57 GMT  
		Size: 409.9 KB (409875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432ade9a2f2eaed492af9b2c567a554192ca3c2460cdf54cbdd74ef7e351b5c6`  
		Last Modified: Mon, 18 May 2020 13:43:25 GMT  
		Size: 7.9 MB (7895679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92956e0c94d7efbf996da0a821961e7e25d592d34d3f95cc7117d36ace6c4f8c`  
		Last Modified: Mon, 18 May 2020 13:43:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403543cf6789e71324a71e34551d530ede80b0836ac96a844a65ebb7c978de2`  
		Last Modified: Mon, 18 May 2020 13:43:22 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-alpine3.11` - linux; s390x

```console
$ docker pull redis@sha256:7e87f23ad9c129bc30f56aa8881568fd3bae9fdcf1aca09f9fd15a145a8a78bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10647559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9dc6fb128105420046bfd04554e6dd0f328c259824417652aef3ff4986b8df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:02:35 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 07:02:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 15 May 2020 22:42:24 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 22:42:25 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 22:42:25 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 22:43:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 22:43:01 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 22:43:02 GMT
VOLUME [/data]
# Fri, 15 May 2020 22:43:02 GMT
WORKDIR /data
# Fri, 15 May 2020 22:43:02 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 15 May 2020 22:43:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 22:43:03 GMT
EXPOSE 6379
# Fri, 15 May 2020 22:43:03 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2da1b54f68b54cfd646e4cf510a14593b857e3c6e7732985b5a3bc5e213a72a`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f0a46f7a997ac6f05cd804b3a0f56c74348f25fd9e164c66ab7c5c4a6a2c82`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 407.4 KB (407392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d280287c062cfd9d589ad117076ba536339a11933f5cc8c50679b99a7d5a33`  
		Last Modified: Fri, 15 May 2020 22:43:59 GMT  
		Size: 7.7 MB (7655503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8cd36de079748236b7e47e5540b2968095a52c1e3eb820750e1eb95c3cf282`  
		Last Modified: Fri, 15 May 2020 22:43:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c5e784b212d08809045f9af3f7675dd7d74d224be6831c0bedaf3512f2d204`  
		Last Modified: Fri, 15 May 2020 22:43:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:6.0-buster`

```console
$ docker pull redis@sha256:f345892f9889fbd14e46eb00ae06f99da2190cfcbfbf2d0d6e71f6d4571eb11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redis:6.0-buster` - linux; amd64

```console
$ docker pull redis@sha256:ab54d0eafe20eeb825ab7b5a58d317cae5a4388c3acf1d91f9c33985b20ff273
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38167360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c654ea77ff723987795e7ce2ef47dbe8e40d5a0f819c04a19be78b95b3b5e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:13:33 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:13:33 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:13:33 GMT
WORKDIR /data
# Sat, 16 May 2020 02:13:34 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:13:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:13:34 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:13:35 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23612dae160f1ec7bcb03995f6511b98869720a2af255e8ed290591b402246b5`  
		Last Modified: Sat, 16 May 2020 02:20:21 GMT  
		Size: 9.6 MB (9648645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c369ccd196fb08d91f340da5260c798cadbadfbb4ab1e323cbbf6b7478a6aa`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a702f65a6a9fe28799e5d494490ab96d303ba44fc2286c2c65775b95de371f2`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-buster` - linux; arm variant v5

```console
$ docker pull redis@sha256:1047d344de59e9413a8a6e2e394f9ff411516a2ef2fea4aee693a781a5eb7bf9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35393451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1c15fd4eb475c34af8c1fa99e894a544b78230f55e77b10eab309385f3e0e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 22:38:03 GMT
ADD file:cbd01ff8d2e40a25bcdb13dc19ffe124c2927b491997dc1c57d4f2c2a308e279 in / 
# Thu, 14 May 2020 22:38:05 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:40:59 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 04:40:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 04:41:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 23:12:39 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 23:12:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 23:12:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 23:14:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 23:14:55 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 23:14:56 GMT
VOLUME [/data]
# Fri, 15 May 2020 23:14:57 GMT
WORKDIR /data
# Fri, 15 May 2020 23:14:58 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 23:14:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 23:15:00 GMT
EXPOSE 6379
# Fri, 15 May 2020 23:15:00 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:24d81022117207b0239d8a8023ca1724b7dde38cb08ce5b9199f59d475d1e600`  
		Last Modified: Thu, 14 May 2020 22:46:51 GMT  
		Size: 24.8 MB (24838470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c13f680b58f95af37082529e8a1ecd6358e22a7e13a75344d8375a03cafb174`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2286bbfcebea1b30a2e862afd7742a7f65237dcabddc9486bfaaf5fd8ba0d65`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.4 MB (1376110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f639441dae5f4f944717cd02a5f128e4758eac38d8ab22f77b69484becc555`  
		Last Modified: Fri, 15 May 2020 23:15:35 GMT  
		Size: 9.2 MB (9176601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c577f5c08a0c4b296439ea910cc8bd148bd1e69058c7af5d40c87b0e825b27`  
		Last Modified: Fri, 15 May 2020 23:15:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dfe2add81403d228b336a3189e8aa2903f266cb813294e4b69d558d25d34919`  
		Last Modified: Fri, 15 May 2020 23:15:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-buster` - linux; arm variant v7

```console
$ docker pull redis@sha256:c682e2bc4474179d62f5943399e78ac9fa38797880bdbdef7615ec58559d6fb6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33018384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc7563c765d7fbfa56e311c229f98caa69bb0cd10e17d2f2344df5911079ba2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 01:00:06 GMT
ADD file:e3f9a454eccb40b4d7bf1dcc17ec29589a007ac67545d1cb5b6fa213c872c8f2 in / 
# Fri, 15 May 2020 01:00:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 16:49:40 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 16:49:40 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 16:50:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 06:31:45 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 06:31:45 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 06:31:46 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 06:32:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 06:33:00 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 06:33:00 GMT
VOLUME [/data]
# Sat, 16 May 2020 06:33:01 GMT
WORKDIR /data
# Sat, 16 May 2020 06:33:02 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 06:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 06:33:03 GMT
EXPOSE 6379
# Sat, 16 May 2020 06:33:04 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e41e28500352be59188c3d871a4b5a3f594350b860a9a36ed5808a35920bdae4`  
		Last Modified: Fri, 15 May 2020 01:11:21 GMT  
		Size: 22.7 MB (22705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6732859766aedad40f91cd96df6b5a6930efe6614b0f084b8459d93c22a69`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed92b736a14b52db74c7cd9919c66ce953393f0544906969081702697d5a6b54`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.4 MB (1368207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae49590ac9360b33276abbdc9f1f45988c0c47b5efbd5b0f55d5dfa258b9ba5a`  
		Last Modified: Sat, 16 May 2020 06:35:15 GMT  
		Size: 8.9 MB (8941986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc7ac3e6ef453bf3e43ffc9747527339b36ba8a594ed32e4e32cd445f706bd2`  
		Last Modified: Sat, 16 May 2020 06:35:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8549d28648c0fd590b2bb28888a0f398a9c44497fdc234419f1c06fdc807eb7`  
		Last Modified: Sat, 16 May 2020 06:35:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-buster` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:fefa8a4cc0bd93b3323c54e3f3aa33ced6f32c9471e5857b067cbf775d7cc918
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36725296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8727a8f0bd0aa8dc538822706743dcc10299697988254fbb44dfec9676eb56b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 12:44:06 GMT
ADD file:b305c1792102142f183d3084026f0fc6be3ddf8d1959b32f0a5d22d35eebcd15 in / 
# Fri, 15 May 2020 12:44:07 GMT
CMD ["bash"]
# Sat, 16 May 2020 08:24:10 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 08:24:10 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 08:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 08:24:37 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 08:24:37 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 08:24:38 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 08:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:25:46 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:25:46 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:25:47 GMT
WORKDIR /data
# Sat, 16 May 2020 08:25:48 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 08:25:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:25:49 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:25:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8a7e1e68c24e5cac20ef26d29505c58456b561c431f0c683b66d1a0943f40dd4`  
		Last Modified: Fri, 15 May 2020 12:53:36 GMT  
		Size: 25.9 MB (25857195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc5ca4e8f484b410989ac557169938b5fe6288ed5add0839e05a790ef47676`  
		Last Modified: Sat, 16 May 2020 08:28:42 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eccfc30e2be16f57d04f487ed80dd2b52ada557753eca7c79eb2ff88ab421f2`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 1.4 MB (1352995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16b8ee6261f593931e5c80c002e18026c3b7bb7d343befbc1fa756ed97c267b`  
		Last Modified: Sat, 16 May 2020 08:28:46 GMT  
		Size: 9.5 MB (9512830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cc79ffa02956bccb011cc1ff2235860b2826a4728941da06492bd6e52f443e`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235fadffc19d75adb68374da679a5c9976a38b0474e07ce04bab7d7093b121b6`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-buster` - linux; 386

```console
$ docker pull redis@sha256:4171a489575082d2d6af76fa8638109e257d3c413eff0b47746288d64b7c5161
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38426981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1dbd0ad2ae3cebd5b89eeb326a1602a2e5f070d58fc8b5f7ef2a8f13f447fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Sat, 16 May 2020 00:07:24 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 00:07:24 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 00:07:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 00:09:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:09:23 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:09:23 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:09:24 GMT
WORKDIR /data
# Sat, 16 May 2020 00:09:24 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 00:09:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:09:25 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:09:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157733bfb7391a76ac45c4aa7ed1ea9e99ee6b2f4f70fbbab7b48b514fff73fc`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7927326d7d556c02a6f3c72888c9f9d2beb780c097c9fb1ca55539afa2a42d`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.4 MB (1387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f28c9a9abf780003c46983a03474d1009255ee52e02e3d6b5387645a25676`  
		Last Modified: Sat, 16 May 2020 00:13:51 GMT  
		Size: 9.3 MB (9282358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4252a3c771aac801bae55f4d6153efe090eae2e87d538bb540d9bfdabf1c07`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7baa10daa19f6859f36ad1667478b73ec03e78417cce615c228b8ff5f468e13`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-buster` - linux; mips64le

```console
$ docker pull redis@sha256:5be8885d29600ec5aa62a44c884f05a27a85156be9bcb6ee7fc5fc51abb06840
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36602715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386312a161a758c285fb32d1403def9b9a2ccd8089f8fde65b3c939dce9244b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 04:48:19 GMT
ADD file:1163d3a5831eb58d132b66b60303169816e7bd8289f19caaac1157179a95f6f9 in / 
# Fri, 15 May 2020 04:48:19 GMT
CMD ["bash"]
# Fri, 15 May 2020 15:35:02 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 15:35:02 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 15:35:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 01:59:50 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 01:59:50 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 01:59:51 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:03:22 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:03:23 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:03:23 GMT
WORKDIR /data
# Sat, 16 May 2020 02:03:23 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:03:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:03:24 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:03:24 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d22357c747999d33ec7501da2c05aa9e95079ebddefbcb326976c5ed5b176b3f`  
		Last Modified: Fri, 15 May 2020 04:57:10 GMT  
		Size: 25.8 MB (25764292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f562c9b9683468308a6f59cab7d724ffc3b35a66acd8ce093b288144db2b7c5`  
		Last Modified: Fri, 15 May 2020 15:42:49 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fda93ec518be6790dd5e435d4bb66cab95d5c14044f01c584fd463ca6ffd290`  
		Last Modified: Fri, 15 May 2020 15:42:50 GMT  
		Size: 1.3 MB (1305516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb60cef9605760eb551d25d4fd2012fbfee55e53a2fc8015e348b35d1c605fe1`  
		Last Modified: Sat, 16 May 2020 02:03:57 GMT  
		Size: 9.5 MB (9530668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0260009eaa931057e783dd3d048e8380b054f9217f32ed1a22b242df7faaff`  
		Last Modified: Sat, 16 May 2020 02:03:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc70c6ee351687f96473d0a015d3ef6e321df0663132a51f3de2d4422313dfed`  
		Last Modified: Sat, 16 May 2020 02:03:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-buster` - linux; ppc64le

```console
$ docker pull redis@sha256:a08a8ff07e718a2a11e9de8d732ed3b9c8ddf9f6aa3914cc71c18e94de4bd5fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42115418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6f886000af62e580a3a50954e45ae47e2207c358362bea46ddd0b2242f0cc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 16 May 2020 17:14:59 GMT
ADD file:b2656a1711bd47585595ae2927cfd4ec00eb903d193583d945b6d60f0a2691bb in / 
# Sat, 16 May 2020 17:15:04 GMT
CMD ["bash"]
# Mon, 18 May 2020 13:30:23 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Mon, 18 May 2020 13:30:26 GMT
ENV GOSU_VERSION=1.12
# Mon, 18 May 2020 13:32:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 18 May 2020 13:32:31 GMT
ENV REDIS_VERSION=6.0.2
# Mon, 18 May 2020 13:32:34 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Mon, 18 May 2020 13:32:36 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Mon, 18 May 2020 13:35:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:35:48 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:35:53 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:35:59 GMT
WORKDIR /data
# Mon, 18 May 2020 13:36:02 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Mon, 18 May 2020 13:36:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:36:13 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:36:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:034d508ed7647e7139951a435acc95e0124f50c984670d0e53b4f5ba25cf6ed1`  
		Last Modified: Sat, 16 May 2020 18:31:49 GMT  
		Size: 30.5 MB (30524456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c613ed63b519e3a0419cf56e14127f5d25466416a8143341540d12cb99943b65`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec60488415c29ebe96bbfabff01925147e50ee55136fdf961fbe8526617f3b`  
		Last Modified: Mon, 18 May 2020 13:42:57 GMT  
		Size: 1.3 MB (1335429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaf24998a2bd9be32258b02fa8e7f6f41d0eda42d774cac44dcabd35978f81d`  
		Last Modified: Mon, 18 May 2020 13:42:59 GMT  
		Size: 10.3 MB (10253250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6948fa0de358f9d87f91ee1e03e42297fb7f70db44a3fc74091faac19916c2`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24281879de8036ec53f002b70225e29b23542cc353d0189e2cf41dd4db52e89a`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6.0-buster` - linux; s390x

```console
$ docker pull redis@sha256:9ef11ffd48bd63460ec92a2e14ef5b3fce4eaa785fbdec11751a934ad38d601d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36741516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e6564e23714b9e21badf63a7c7ce03ab2de0060269e6b9aa3644a656750072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 05:15:35 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 05:15:35 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 05:15:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 22:41:40 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 22:41:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 22:41:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 22:42:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 22:42:14 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 22:42:15 GMT
VOLUME [/data]
# Fri, 15 May 2020 22:42:15 GMT
WORKDIR /data
# Fri, 15 May 2020 22:42:15 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 22:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 22:42:15 GMT
EXPOSE 6379
# Fri, 15 May 2020 22:42:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e40cd0998be29e9cce5152b7d3644b03b888bcca5db2049d43c93bf53185d`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc1e5303c90f8fcd807a5042757fb4de087ae4b3319afca416b72e858de788c`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.4 MB (1403711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5d61c1be6277797ce170d2b088f07f55873edc9b1a71d02a2d155dd4e00c6`  
		Last Modified: Fri, 15 May 2020 22:43:45 GMT  
		Size: 9.6 MB (9622596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e520dcecd5852ea3751c3d41ca8c103d95984d027003a983f3c118645530282`  
		Last Modified: Fri, 15 May 2020 22:43:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89764005f67e8cd243c7c732985b0b2b9863ded8a6f2fa729c6c8102aa6bf73d`  
		Last Modified: Fri, 15 May 2020 22:43:48 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:6-alpine`

```console
$ docker pull redis@sha256:b7e093c1a1cd040698fc28e4be453d8df1a46323fa4178d6d2d5fcb3bff88c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:6-alpine` - linux; amd64

```console
$ docker pull redis@sha256:e5146a61518fef302756bd0bf226ac530fc23d7537097fa378cc50fcb5778b64
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10615454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ceee5c3fa3cea2607d5e2bcc54d019be616e322979be8fc7a8d0d78b59a1f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:19:42 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 19:19:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:15:36 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:15:36 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:15:37 GMT
WORKDIR /data
# Sat, 16 May 2020 02:15:37 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 02:15:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:15:38 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:15:38 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0373118a0d956ca0ee963e307457f45f073db9096f7c6f87c10251d071f0dc`  
		Last Modified: Fri, 24 Apr 2020 19:23:01 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd369fe62565d644723bfdb734c4ecb2a96191366ec08424146aa9c5ff6b308`  
		Last Modified: Fri, 24 Apr 2020 19:23:02 GMT  
		Size: 402.6 KB (402568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d862fc04e31c48831cc75b3b3868126e27f4e51c45bdcddb6ffc7c94b9205a76`  
		Last Modified: Sat, 16 May 2020 02:20:31 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb087a9da0889770a90077b54e12441d375e7027b377997f98a5e6d827ab3fe`  
		Last Modified: Sat, 16 May 2020 02:20:29 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be29dc118a7a01cd97bac04e83376259dee6d48d1cf35a94a8d26d3a73159bb`  
		Last Modified: Sat, 16 May 2020 02:20:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:4057fbe62d49d301734916e4d6d7dd8f9c2d06ebfdad741698aa18ff152b642c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10312873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00275d208cadbfe750c573429cfd2721a47e1b792b022432d241395fbe82dbb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:30:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 23 Apr 2020 22:30:20 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 15 May 2020 23:24:21 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 23:24:22 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 23:24:23 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 23:25:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 23:25:28 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 23:25:30 GMT
VOLUME [/data]
# Fri, 15 May 2020 23:25:31 GMT
WORKDIR /data
# Fri, 15 May 2020 23:25:33 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 15 May 2020 23:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 23:25:36 GMT
EXPOSE 6379
# Fri, 15 May 2020 23:25:37 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab5b04292d1974b3feedf74dddf563efe3ba5b5c38239a49e8adf0ac8140028`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af20f6a7bee5bf869254b4964c1a5d8dd5ef1353ac48081a885920682312555b`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 405.8 KB (405799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cd828ef5be835bbd932776269cc78fa20d6597c5286a8301d9712ca6ba27e1`  
		Last Modified: Fri, 15 May 2020 23:26:27 GMT  
		Size: 7.3 MB (7285336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62363baf5a298c4aecde09c629388197091d261f20fd00863a1693c8847cc34`  
		Last Modified: Fri, 15 May 2020 23:26:27 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0e939b10f701fd67e6400e3d0193f9dbafde2f4bc53215a7305a7c7352bdcb`  
		Last Modified: Fri, 15 May 2020 23:26:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:a9395e60f632ac5808d01ff562ddafcccf44d254f634164eef079f86f0e4fcd3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9972279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af28cbbd6cfbc59e7a5f1a1855dd7caa878b4fd03a749db7b3e51823a58c6b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:51:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 08:51:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 06:33:17 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 06:33:18 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 06:33:20 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 06:34:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 06:34:13 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 06:34:14 GMT
VOLUME [/data]
# Sat, 16 May 2020 06:34:15 GMT
WORKDIR /data
# Sat, 16 May 2020 06:34:16 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 06:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 06:34:17 GMT
EXPOSE 6379
# Sat, 16 May 2020 06:34:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0765e03c998449baf4c76a1011cf80e6ab974db3d5d8da3a361bfeeb875d96db`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07fda5f4761823162fa661b4466f517ad5db025d9689c123221af67af9b53f`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 399.8 KB (399779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b80e8aaba692112e559076be6bb0334a707afdf5e98838a1871caa0866a8c0e`  
		Last Modified: Sat, 16 May 2020 06:35:45 GMT  
		Size: 7.1 MB (7148634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87bac8f769e16dcbd264fba3220e6015ebc7ade1c9dbbeaaf05826b5a181b86`  
		Last Modified: Sat, 16 May 2020 06:35:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb4e2186895e529da275fc0432b79e52a0bb9857639493ec62bcf3bf168531a`  
		Last Modified: Sat, 16 May 2020 06:35:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:745fe4f5f083ab735a17c56a7b213000f369f6cb8f44350c0d5e82db296dade8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10520097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26e9dafef70ab5ad06818ba5897d0d464402e823220faa6d106c50cb1f3828a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:45:10 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 12:45:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 08:25:57 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 08:25:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 08:25:59 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 08:26:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:26:52 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:26:52 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:26:53 GMT
WORKDIR /data
# Sat, 16 May 2020 08:26:54 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 08:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:26:55 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:26:56 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7050d23898adae8e4a2e0ab67eaeab9f9a9ec0fa5b88b128eeff4de1570877`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8982b178d819b1f2f10c3375b2c7ed054157cc5e711b58b6a2dcb376686e5d59`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 404.7 KB (404661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81e21ac53933c4757cd8a04fd0253d126746afcf7e023bbad9a93dec0acd26`  
		Last Modified: Sat, 16 May 2020 08:29:02 GMT  
		Size: 7.4 MB (7389208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e3ddab2b277bd44f7dc380187d16e5028acf9cc4dfee80f19494ea9e060aba`  
		Last Modified: Sat, 16 May 2020 08:28:58 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb66b8b7b33b484540124708f55d85ee24ea6274d5c4dc36ecbd1e84637e678e`  
		Last Modified: Sat, 16 May 2020 08:28:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine` - linux; 386

```console
$ docker pull redis@sha256:bbfdc448dafad37023ae75c4fcfbd5d1ec7bd78aad8e769b62753c36c31757b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10290082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34322bf2334fed58c9521a918064a594354d513fbeec9b4b637dd5be45e8b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:49:36 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 05:49:38 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 00:09:40 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 00:09:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 00:09:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 00:11:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:11:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:11:09 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:11:10 GMT
WORKDIR /data
# Sat, 16 May 2020 00:11:10 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 00:11:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:11:10 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:11:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4eb71d5f124b9b51684034d7d96fba6399ff6892995e51137d0c0617a11fb9`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7685edc32d5ef38faf3beb4310c119862b1dfa18ea58edb0dbca84e9417b267`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 407.9 KB (407901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02f4cc0a73447e7af4c367a8efe6a3fe2e6b6cdf92088abd4c2b8f99f980af`  
		Last Modified: Sat, 16 May 2020 00:14:01 GMT  
		Size: 7.1 MB (7072021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd586489393880a99bcea0f145202694e2d8e8c438c7d6b44741073ea6d2c16`  
		Last Modified: Sat, 16 May 2020 00:13:59 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd50ae8a09e8979660d44015b05f83ff9419212dcd16c1dd9372263dfadaff9`  
		Last Modified: Sat, 16 May 2020 00:13:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:50b2e427f6b8a80a2532561509d6bb630381f1e73683bedb0723222a0391e5aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11129201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7ff884dff0f0f831a77c117ef871f6b9dfe526d553ea1a7178969d1b9abf56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:02:06 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 09:02:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 18 May 2020 13:36:42 GMT
ENV REDIS_VERSION=6.0.2
# Mon, 18 May 2020 13:36:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Mon, 18 May 2020 13:36:56 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Mon, 18 May 2020 13:38:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:38:08 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:38:11 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:38:20 GMT
WORKDIR /data
# Mon, 18 May 2020 13:38:23 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 18 May 2020 13:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:38:32 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:38:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc79e36a18515157312416d029cb35887ee8668b53b6c0e3867a4d0dd8dd231`  
		Last Modified: Fri, 24 Apr 2020 09:06:56 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83078862453fa1de07d734ccc5b995c92cd74710488c11d066ad752e3402d`  
		Last Modified: Fri, 24 Apr 2020 09:06:57 GMT  
		Size: 409.9 KB (409875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432ade9a2f2eaed492af9b2c567a554192ca3c2460cdf54cbdd74ef7e351b5c6`  
		Last Modified: Mon, 18 May 2020 13:43:25 GMT  
		Size: 7.9 MB (7895679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92956e0c94d7efbf996da0a821961e7e25d592d34d3f95cc7117d36ace6c4f8c`  
		Last Modified: Mon, 18 May 2020 13:43:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403543cf6789e71324a71e34551d530ede80b0836ac96a844a65ebb7c978de2`  
		Last Modified: Mon, 18 May 2020 13:43:22 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine` - linux; s390x

```console
$ docker pull redis@sha256:7e87f23ad9c129bc30f56aa8881568fd3bae9fdcf1aca09f9fd15a145a8a78bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10647559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9dc6fb128105420046bfd04554e6dd0f328c259824417652aef3ff4986b8df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:02:35 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 07:02:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 15 May 2020 22:42:24 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 22:42:25 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 22:42:25 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 22:43:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 22:43:01 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 22:43:02 GMT
VOLUME [/data]
# Fri, 15 May 2020 22:43:02 GMT
WORKDIR /data
# Fri, 15 May 2020 22:43:02 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 15 May 2020 22:43:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 22:43:03 GMT
EXPOSE 6379
# Fri, 15 May 2020 22:43:03 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2da1b54f68b54cfd646e4cf510a14593b857e3c6e7732985b5a3bc5e213a72a`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f0a46f7a997ac6f05cd804b3a0f56c74348f25fd9e164c66ab7c5c4a6a2c82`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 407.4 KB (407392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d280287c062cfd9d589ad117076ba536339a11933f5cc8c50679b99a7d5a33`  
		Last Modified: Fri, 15 May 2020 22:43:59 GMT  
		Size: 7.7 MB (7655503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8cd36de079748236b7e47e5540b2968095a52c1e3eb820750e1eb95c3cf282`  
		Last Modified: Fri, 15 May 2020 22:43:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c5e784b212d08809045f9af3f7675dd7d74d224be6831c0bedaf3512f2d204`  
		Last Modified: Fri, 15 May 2020 22:43:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:6-alpine3.11`

```console
$ docker pull redis@sha256:b7e093c1a1cd040698fc28e4be453d8df1a46323fa4178d6d2d5fcb3bff88c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:6-alpine3.11` - linux; amd64

```console
$ docker pull redis@sha256:e5146a61518fef302756bd0bf226ac530fc23d7537097fa378cc50fcb5778b64
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10615454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ceee5c3fa3cea2607d5e2bcc54d019be616e322979be8fc7a8d0d78b59a1f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:19:42 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 19:19:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:15:36 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:15:36 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:15:37 GMT
WORKDIR /data
# Sat, 16 May 2020 02:15:37 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 02:15:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:15:38 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:15:38 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0373118a0d956ca0ee963e307457f45f073db9096f7c6f87c10251d071f0dc`  
		Last Modified: Fri, 24 Apr 2020 19:23:01 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd369fe62565d644723bfdb734c4ecb2a96191366ec08424146aa9c5ff6b308`  
		Last Modified: Fri, 24 Apr 2020 19:23:02 GMT  
		Size: 402.6 KB (402568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d862fc04e31c48831cc75b3b3868126e27f4e51c45bdcddb6ffc7c94b9205a76`  
		Last Modified: Sat, 16 May 2020 02:20:31 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb087a9da0889770a90077b54e12441d375e7027b377997f98a5e6d827ab3fe`  
		Last Modified: Sat, 16 May 2020 02:20:29 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be29dc118a7a01cd97bac04e83376259dee6d48d1cf35a94a8d26d3a73159bb`  
		Last Modified: Sat, 16 May 2020 02:20:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.11` - linux; arm variant v6

```console
$ docker pull redis@sha256:4057fbe62d49d301734916e4d6d7dd8f9c2d06ebfdad741698aa18ff152b642c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10312873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00275d208cadbfe750c573429cfd2721a47e1b792b022432d241395fbe82dbb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:30:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 23 Apr 2020 22:30:20 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 15 May 2020 23:24:21 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 23:24:22 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 23:24:23 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 23:25:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 23:25:28 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 23:25:30 GMT
VOLUME [/data]
# Fri, 15 May 2020 23:25:31 GMT
WORKDIR /data
# Fri, 15 May 2020 23:25:33 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 15 May 2020 23:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 23:25:36 GMT
EXPOSE 6379
# Fri, 15 May 2020 23:25:37 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab5b04292d1974b3feedf74dddf563efe3ba5b5c38239a49e8adf0ac8140028`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af20f6a7bee5bf869254b4964c1a5d8dd5ef1353ac48081a885920682312555b`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 405.8 KB (405799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cd828ef5be835bbd932776269cc78fa20d6597c5286a8301d9712ca6ba27e1`  
		Last Modified: Fri, 15 May 2020 23:26:27 GMT  
		Size: 7.3 MB (7285336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62363baf5a298c4aecde09c629388197091d261f20fd00863a1693c8847cc34`  
		Last Modified: Fri, 15 May 2020 23:26:27 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0e939b10f701fd67e6400e3d0193f9dbafde2f4bc53215a7305a7c7352bdcb`  
		Last Modified: Fri, 15 May 2020 23:26:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.11` - linux; arm variant v7

```console
$ docker pull redis@sha256:a9395e60f632ac5808d01ff562ddafcccf44d254f634164eef079f86f0e4fcd3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9972279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af28cbbd6cfbc59e7a5f1a1855dd7caa878b4fd03a749db7b3e51823a58c6b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:51:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 08:51:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 06:33:17 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 06:33:18 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 06:33:20 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 06:34:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 06:34:13 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 06:34:14 GMT
VOLUME [/data]
# Sat, 16 May 2020 06:34:15 GMT
WORKDIR /data
# Sat, 16 May 2020 06:34:16 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 06:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 06:34:17 GMT
EXPOSE 6379
# Sat, 16 May 2020 06:34:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0765e03c998449baf4c76a1011cf80e6ab974db3d5d8da3a361bfeeb875d96db`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07fda5f4761823162fa661b4466f517ad5db025d9689c123221af67af9b53f`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 399.8 KB (399779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b80e8aaba692112e559076be6bb0334a707afdf5e98838a1871caa0866a8c0e`  
		Last Modified: Sat, 16 May 2020 06:35:45 GMT  
		Size: 7.1 MB (7148634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87bac8f769e16dcbd264fba3220e6015ebc7ade1c9dbbeaaf05826b5a181b86`  
		Last Modified: Sat, 16 May 2020 06:35:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb4e2186895e529da275fc0432b79e52a0bb9857639493ec62bcf3bf168531a`  
		Last Modified: Sat, 16 May 2020 06:35:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.11` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:745fe4f5f083ab735a17c56a7b213000f369f6cb8f44350c0d5e82db296dade8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10520097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26e9dafef70ab5ad06818ba5897d0d464402e823220faa6d106c50cb1f3828a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:45:10 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 12:45:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 08:25:57 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 08:25:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 08:25:59 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 08:26:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:26:52 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:26:52 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:26:53 GMT
WORKDIR /data
# Sat, 16 May 2020 08:26:54 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 08:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:26:55 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:26:56 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7050d23898adae8e4a2e0ab67eaeab9f9a9ec0fa5b88b128eeff4de1570877`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8982b178d819b1f2f10c3375b2c7ed054157cc5e711b58b6a2dcb376686e5d59`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 404.7 KB (404661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81e21ac53933c4757cd8a04fd0253d126746afcf7e023bbad9a93dec0acd26`  
		Last Modified: Sat, 16 May 2020 08:29:02 GMT  
		Size: 7.4 MB (7389208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e3ddab2b277bd44f7dc380187d16e5028acf9cc4dfee80f19494ea9e060aba`  
		Last Modified: Sat, 16 May 2020 08:28:58 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb66b8b7b33b484540124708f55d85ee24ea6274d5c4dc36ecbd1e84637e678e`  
		Last Modified: Sat, 16 May 2020 08:28:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.11` - linux; 386

```console
$ docker pull redis@sha256:bbfdc448dafad37023ae75c4fcfbd5d1ec7bd78aad8e769b62753c36c31757b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10290082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34322bf2334fed58c9521a918064a594354d513fbeec9b4b637dd5be45e8b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:49:36 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 05:49:38 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 00:09:40 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 00:09:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 00:09:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 00:11:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:11:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:11:09 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:11:10 GMT
WORKDIR /data
# Sat, 16 May 2020 00:11:10 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 00:11:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:11:10 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:11:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4eb71d5f124b9b51684034d7d96fba6399ff6892995e51137d0c0617a11fb9`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7685edc32d5ef38faf3beb4310c119862b1dfa18ea58edb0dbca84e9417b267`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 407.9 KB (407901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02f4cc0a73447e7af4c367a8efe6a3fe2e6b6cdf92088abd4c2b8f99f980af`  
		Last Modified: Sat, 16 May 2020 00:14:01 GMT  
		Size: 7.1 MB (7072021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd586489393880a99bcea0f145202694e2d8e8c438c7d6b44741073ea6d2c16`  
		Last Modified: Sat, 16 May 2020 00:13:59 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd50ae8a09e8979660d44015b05f83ff9419212dcd16c1dd9372263dfadaff9`  
		Last Modified: Sat, 16 May 2020 00:13:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.11` - linux; ppc64le

```console
$ docker pull redis@sha256:50b2e427f6b8a80a2532561509d6bb630381f1e73683bedb0723222a0391e5aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11129201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7ff884dff0f0f831a77c117ef871f6b9dfe526d553ea1a7178969d1b9abf56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:02:06 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 09:02:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 18 May 2020 13:36:42 GMT
ENV REDIS_VERSION=6.0.2
# Mon, 18 May 2020 13:36:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Mon, 18 May 2020 13:36:56 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Mon, 18 May 2020 13:38:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:38:08 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:38:11 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:38:20 GMT
WORKDIR /data
# Mon, 18 May 2020 13:38:23 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 18 May 2020 13:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:38:32 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:38:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc79e36a18515157312416d029cb35887ee8668b53b6c0e3867a4d0dd8dd231`  
		Last Modified: Fri, 24 Apr 2020 09:06:56 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83078862453fa1de07d734ccc5b995c92cd74710488c11d066ad752e3402d`  
		Last Modified: Fri, 24 Apr 2020 09:06:57 GMT  
		Size: 409.9 KB (409875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432ade9a2f2eaed492af9b2c567a554192ca3c2460cdf54cbdd74ef7e351b5c6`  
		Last Modified: Mon, 18 May 2020 13:43:25 GMT  
		Size: 7.9 MB (7895679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92956e0c94d7efbf996da0a821961e7e25d592d34d3f95cc7117d36ace6c4f8c`  
		Last Modified: Mon, 18 May 2020 13:43:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403543cf6789e71324a71e34551d530ede80b0836ac96a844a65ebb7c978de2`  
		Last Modified: Mon, 18 May 2020 13:43:22 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-alpine3.11` - linux; s390x

```console
$ docker pull redis@sha256:7e87f23ad9c129bc30f56aa8881568fd3bae9fdcf1aca09f9fd15a145a8a78bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10647559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9dc6fb128105420046bfd04554e6dd0f328c259824417652aef3ff4986b8df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:02:35 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 07:02:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 15 May 2020 22:42:24 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 22:42:25 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 22:42:25 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 22:43:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 22:43:01 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 22:43:02 GMT
VOLUME [/data]
# Fri, 15 May 2020 22:43:02 GMT
WORKDIR /data
# Fri, 15 May 2020 22:43:02 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 15 May 2020 22:43:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 22:43:03 GMT
EXPOSE 6379
# Fri, 15 May 2020 22:43:03 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2da1b54f68b54cfd646e4cf510a14593b857e3c6e7732985b5a3bc5e213a72a`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f0a46f7a997ac6f05cd804b3a0f56c74348f25fd9e164c66ab7c5c4a6a2c82`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 407.4 KB (407392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d280287c062cfd9d589ad117076ba536339a11933f5cc8c50679b99a7d5a33`  
		Last Modified: Fri, 15 May 2020 22:43:59 GMT  
		Size: 7.7 MB (7655503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8cd36de079748236b7e47e5540b2968095a52c1e3eb820750e1eb95c3cf282`  
		Last Modified: Fri, 15 May 2020 22:43:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c5e784b212d08809045f9af3f7675dd7d74d224be6831c0bedaf3512f2d204`  
		Last Modified: Fri, 15 May 2020 22:43:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:6-buster`

```console
$ docker pull redis@sha256:f345892f9889fbd14e46eb00ae06f99da2190cfcbfbf2d0d6e71f6d4571eb11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redis:6-buster` - linux; amd64

```console
$ docker pull redis@sha256:ab54d0eafe20eeb825ab7b5a58d317cae5a4388c3acf1d91f9c33985b20ff273
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38167360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c654ea77ff723987795e7ce2ef47dbe8e40d5a0f819c04a19be78b95b3b5e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:13:33 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:13:33 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:13:33 GMT
WORKDIR /data
# Sat, 16 May 2020 02:13:34 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:13:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:13:34 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:13:35 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23612dae160f1ec7bcb03995f6511b98869720a2af255e8ed290591b402246b5`  
		Last Modified: Sat, 16 May 2020 02:20:21 GMT  
		Size: 9.6 MB (9648645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c369ccd196fb08d91f340da5260c798cadbadfbb4ab1e323cbbf6b7478a6aa`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a702f65a6a9fe28799e5d494490ab96d303ba44fc2286c2c65775b95de371f2`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-buster` - linux; arm variant v5

```console
$ docker pull redis@sha256:1047d344de59e9413a8a6e2e394f9ff411516a2ef2fea4aee693a781a5eb7bf9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35393451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1c15fd4eb475c34af8c1fa99e894a544b78230f55e77b10eab309385f3e0e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 22:38:03 GMT
ADD file:cbd01ff8d2e40a25bcdb13dc19ffe124c2927b491997dc1c57d4f2c2a308e279 in / 
# Thu, 14 May 2020 22:38:05 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:40:59 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 04:40:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 04:41:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 23:12:39 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 23:12:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 23:12:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 23:14:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 23:14:55 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 23:14:56 GMT
VOLUME [/data]
# Fri, 15 May 2020 23:14:57 GMT
WORKDIR /data
# Fri, 15 May 2020 23:14:58 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 23:14:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 23:15:00 GMT
EXPOSE 6379
# Fri, 15 May 2020 23:15:00 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:24d81022117207b0239d8a8023ca1724b7dde38cb08ce5b9199f59d475d1e600`  
		Last Modified: Thu, 14 May 2020 22:46:51 GMT  
		Size: 24.8 MB (24838470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c13f680b58f95af37082529e8a1ecd6358e22a7e13a75344d8375a03cafb174`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2286bbfcebea1b30a2e862afd7742a7f65237dcabddc9486bfaaf5fd8ba0d65`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.4 MB (1376110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f639441dae5f4f944717cd02a5f128e4758eac38d8ab22f77b69484becc555`  
		Last Modified: Fri, 15 May 2020 23:15:35 GMT  
		Size: 9.2 MB (9176601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c577f5c08a0c4b296439ea910cc8bd148bd1e69058c7af5d40c87b0e825b27`  
		Last Modified: Fri, 15 May 2020 23:15:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dfe2add81403d228b336a3189e8aa2903f266cb813294e4b69d558d25d34919`  
		Last Modified: Fri, 15 May 2020 23:15:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-buster` - linux; arm variant v7

```console
$ docker pull redis@sha256:c682e2bc4474179d62f5943399e78ac9fa38797880bdbdef7615ec58559d6fb6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33018384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc7563c765d7fbfa56e311c229f98caa69bb0cd10e17d2f2344df5911079ba2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 01:00:06 GMT
ADD file:e3f9a454eccb40b4d7bf1dcc17ec29589a007ac67545d1cb5b6fa213c872c8f2 in / 
# Fri, 15 May 2020 01:00:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 16:49:40 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 16:49:40 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 16:50:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 06:31:45 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 06:31:45 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 06:31:46 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 06:32:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 06:33:00 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 06:33:00 GMT
VOLUME [/data]
# Sat, 16 May 2020 06:33:01 GMT
WORKDIR /data
# Sat, 16 May 2020 06:33:02 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 06:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 06:33:03 GMT
EXPOSE 6379
# Sat, 16 May 2020 06:33:04 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e41e28500352be59188c3d871a4b5a3f594350b860a9a36ed5808a35920bdae4`  
		Last Modified: Fri, 15 May 2020 01:11:21 GMT  
		Size: 22.7 MB (22705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6732859766aedad40f91cd96df6b5a6930efe6614b0f084b8459d93c22a69`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed92b736a14b52db74c7cd9919c66ce953393f0544906969081702697d5a6b54`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.4 MB (1368207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae49590ac9360b33276abbdc9f1f45988c0c47b5efbd5b0f55d5dfa258b9ba5a`  
		Last Modified: Sat, 16 May 2020 06:35:15 GMT  
		Size: 8.9 MB (8941986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc7ac3e6ef453bf3e43ffc9747527339b36ba8a594ed32e4e32cd445f706bd2`  
		Last Modified: Sat, 16 May 2020 06:35:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8549d28648c0fd590b2bb28888a0f398a9c44497fdc234419f1c06fdc807eb7`  
		Last Modified: Sat, 16 May 2020 06:35:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-buster` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:fefa8a4cc0bd93b3323c54e3f3aa33ced6f32c9471e5857b067cbf775d7cc918
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36725296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8727a8f0bd0aa8dc538822706743dcc10299697988254fbb44dfec9676eb56b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 12:44:06 GMT
ADD file:b305c1792102142f183d3084026f0fc6be3ddf8d1959b32f0a5d22d35eebcd15 in / 
# Fri, 15 May 2020 12:44:07 GMT
CMD ["bash"]
# Sat, 16 May 2020 08:24:10 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 08:24:10 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 08:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 08:24:37 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 08:24:37 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 08:24:38 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 08:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:25:46 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:25:46 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:25:47 GMT
WORKDIR /data
# Sat, 16 May 2020 08:25:48 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 08:25:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:25:49 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:25:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8a7e1e68c24e5cac20ef26d29505c58456b561c431f0c683b66d1a0943f40dd4`  
		Last Modified: Fri, 15 May 2020 12:53:36 GMT  
		Size: 25.9 MB (25857195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc5ca4e8f484b410989ac557169938b5fe6288ed5add0839e05a790ef47676`  
		Last Modified: Sat, 16 May 2020 08:28:42 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eccfc30e2be16f57d04f487ed80dd2b52ada557753eca7c79eb2ff88ab421f2`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 1.4 MB (1352995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16b8ee6261f593931e5c80c002e18026c3b7bb7d343befbc1fa756ed97c267b`  
		Last Modified: Sat, 16 May 2020 08:28:46 GMT  
		Size: 9.5 MB (9512830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cc79ffa02956bccb011cc1ff2235860b2826a4728941da06492bd6e52f443e`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235fadffc19d75adb68374da679a5c9976a38b0474e07ce04bab7d7093b121b6`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-buster` - linux; 386

```console
$ docker pull redis@sha256:4171a489575082d2d6af76fa8638109e257d3c413eff0b47746288d64b7c5161
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38426981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1dbd0ad2ae3cebd5b89eeb326a1602a2e5f070d58fc8b5f7ef2a8f13f447fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Sat, 16 May 2020 00:07:24 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 00:07:24 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 00:07:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 00:09:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:09:23 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:09:23 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:09:24 GMT
WORKDIR /data
# Sat, 16 May 2020 00:09:24 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 00:09:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:09:25 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:09:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157733bfb7391a76ac45c4aa7ed1ea9e99ee6b2f4f70fbbab7b48b514fff73fc`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7927326d7d556c02a6f3c72888c9f9d2beb780c097c9fb1ca55539afa2a42d`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.4 MB (1387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f28c9a9abf780003c46983a03474d1009255ee52e02e3d6b5387645a25676`  
		Last Modified: Sat, 16 May 2020 00:13:51 GMT  
		Size: 9.3 MB (9282358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4252a3c771aac801bae55f4d6153efe090eae2e87d538bb540d9bfdabf1c07`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7baa10daa19f6859f36ad1667478b73ec03e78417cce615c228b8ff5f468e13`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-buster` - linux; mips64le

```console
$ docker pull redis@sha256:5be8885d29600ec5aa62a44c884f05a27a85156be9bcb6ee7fc5fc51abb06840
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36602715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386312a161a758c285fb32d1403def9b9a2ccd8089f8fde65b3c939dce9244b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 04:48:19 GMT
ADD file:1163d3a5831eb58d132b66b60303169816e7bd8289f19caaac1157179a95f6f9 in / 
# Fri, 15 May 2020 04:48:19 GMT
CMD ["bash"]
# Fri, 15 May 2020 15:35:02 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 15:35:02 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 15:35:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 01:59:50 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 01:59:50 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 01:59:51 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:03:22 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:03:23 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:03:23 GMT
WORKDIR /data
# Sat, 16 May 2020 02:03:23 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:03:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:03:24 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:03:24 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d22357c747999d33ec7501da2c05aa9e95079ebddefbcb326976c5ed5b176b3f`  
		Last Modified: Fri, 15 May 2020 04:57:10 GMT  
		Size: 25.8 MB (25764292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f562c9b9683468308a6f59cab7d724ffc3b35a66acd8ce093b288144db2b7c5`  
		Last Modified: Fri, 15 May 2020 15:42:49 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fda93ec518be6790dd5e435d4bb66cab95d5c14044f01c584fd463ca6ffd290`  
		Last Modified: Fri, 15 May 2020 15:42:50 GMT  
		Size: 1.3 MB (1305516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb60cef9605760eb551d25d4fd2012fbfee55e53a2fc8015e348b35d1c605fe1`  
		Last Modified: Sat, 16 May 2020 02:03:57 GMT  
		Size: 9.5 MB (9530668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0260009eaa931057e783dd3d048e8380b054f9217f32ed1a22b242df7faaff`  
		Last Modified: Sat, 16 May 2020 02:03:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc70c6ee351687f96473d0a015d3ef6e321df0663132a51f3de2d4422313dfed`  
		Last Modified: Sat, 16 May 2020 02:03:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-buster` - linux; ppc64le

```console
$ docker pull redis@sha256:a08a8ff07e718a2a11e9de8d732ed3b9c8ddf9f6aa3914cc71c18e94de4bd5fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42115418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6f886000af62e580a3a50954e45ae47e2207c358362bea46ddd0b2242f0cc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 16 May 2020 17:14:59 GMT
ADD file:b2656a1711bd47585595ae2927cfd4ec00eb903d193583d945b6d60f0a2691bb in / 
# Sat, 16 May 2020 17:15:04 GMT
CMD ["bash"]
# Mon, 18 May 2020 13:30:23 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Mon, 18 May 2020 13:30:26 GMT
ENV GOSU_VERSION=1.12
# Mon, 18 May 2020 13:32:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 18 May 2020 13:32:31 GMT
ENV REDIS_VERSION=6.0.2
# Mon, 18 May 2020 13:32:34 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Mon, 18 May 2020 13:32:36 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Mon, 18 May 2020 13:35:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:35:48 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:35:53 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:35:59 GMT
WORKDIR /data
# Mon, 18 May 2020 13:36:02 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Mon, 18 May 2020 13:36:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:36:13 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:36:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:034d508ed7647e7139951a435acc95e0124f50c984670d0e53b4f5ba25cf6ed1`  
		Last Modified: Sat, 16 May 2020 18:31:49 GMT  
		Size: 30.5 MB (30524456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c613ed63b519e3a0419cf56e14127f5d25466416a8143341540d12cb99943b65`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec60488415c29ebe96bbfabff01925147e50ee55136fdf961fbe8526617f3b`  
		Last Modified: Mon, 18 May 2020 13:42:57 GMT  
		Size: 1.3 MB (1335429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaf24998a2bd9be32258b02fa8e7f6f41d0eda42d774cac44dcabd35978f81d`  
		Last Modified: Mon, 18 May 2020 13:42:59 GMT  
		Size: 10.3 MB (10253250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6948fa0de358f9d87f91ee1e03e42297fb7f70db44a3fc74091faac19916c2`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24281879de8036ec53f002b70225e29b23542cc353d0189e2cf41dd4db52e89a`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:6-buster` - linux; s390x

```console
$ docker pull redis@sha256:9ef11ffd48bd63460ec92a2e14ef5b3fce4eaa785fbdec11751a934ad38d601d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36741516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e6564e23714b9e21badf63a7c7ce03ab2de0060269e6b9aa3644a656750072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 05:15:35 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 05:15:35 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 05:15:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 22:41:40 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 22:41:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 22:41:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 22:42:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 22:42:14 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 22:42:15 GMT
VOLUME [/data]
# Fri, 15 May 2020 22:42:15 GMT
WORKDIR /data
# Fri, 15 May 2020 22:42:15 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 22:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 22:42:15 GMT
EXPOSE 6379
# Fri, 15 May 2020 22:42:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e40cd0998be29e9cce5152b7d3644b03b888bcca5db2049d43c93bf53185d`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc1e5303c90f8fcd807a5042757fb4de087ae4b3319afca416b72e858de788c`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.4 MB (1403711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5d61c1be6277797ce170d2b088f07f55873edc9b1a71d02a2d155dd4e00c6`  
		Last Modified: Fri, 15 May 2020 22:43:45 GMT  
		Size: 9.6 MB (9622596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e520dcecd5852ea3751c3d41ca8c103d95984d027003a983f3c118645530282`  
		Last Modified: Fri, 15 May 2020 22:43:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89764005f67e8cd243c7c732985b0b2b9863ded8a6f2fa729c6c8102aa6bf73d`  
		Last Modified: Fri, 15 May 2020 22:43:48 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:alpine`

```console
$ docker pull redis@sha256:b7e093c1a1cd040698fc28e4be453d8df1a46323fa4178d6d2d5fcb3bff88c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:alpine` - linux; amd64

```console
$ docker pull redis@sha256:e5146a61518fef302756bd0bf226ac530fc23d7537097fa378cc50fcb5778b64
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10615454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ceee5c3fa3cea2607d5e2bcc54d019be616e322979be8fc7a8d0d78b59a1f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:19:42 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 19:19:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:15:36 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:15:36 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:15:37 GMT
WORKDIR /data
# Sat, 16 May 2020 02:15:37 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 02:15:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:15:38 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:15:38 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0373118a0d956ca0ee963e307457f45f073db9096f7c6f87c10251d071f0dc`  
		Last Modified: Fri, 24 Apr 2020 19:23:01 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd369fe62565d644723bfdb734c4ecb2a96191366ec08424146aa9c5ff6b308`  
		Last Modified: Fri, 24 Apr 2020 19:23:02 GMT  
		Size: 402.6 KB (402568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d862fc04e31c48831cc75b3b3868126e27f4e51c45bdcddb6ffc7c94b9205a76`  
		Last Modified: Sat, 16 May 2020 02:20:31 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb087a9da0889770a90077b54e12441d375e7027b377997f98a5e6d827ab3fe`  
		Last Modified: Sat, 16 May 2020 02:20:29 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be29dc118a7a01cd97bac04e83376259dee6d48d1cf35a94a8d26d3a73159bb`  
		Last Modified: Sat, 16 May 2020 02:20:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:4057fbe62d49d301734916e4d6d7dd8f9c2d06ebfdad741698aa18ff152b642c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10312873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00275d208cadbfe750c573429cfd2721a47e1b792b022432d241395fbe82dbb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:30:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 23 Apr 2020 22:30:20 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 15 May 2020 23:24:21 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 23:24:22 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 23:24:23 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 23:25:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 23:25:28 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 23:25:30 GMT
VOLUME [/data]
# Fri, 15 May 2020 23:25:31 GMT
WORKDIR /data
# Fri, 15 May 2020 23:25:33 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 15 May 2020 23:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 23:25:36 GMT
EXPOSE 6379
# Fri, 15 May 2020 23:25:37 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab5b04292d1974b3feedf74dddf563efe3ba5b5c38239a49e8adf0ac8140028`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af20f6a7bee5bf869254b4964c1a5d8dd5ef1353ac48081a885920682312555b`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 405.8 KB (405799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cd828ef5be835bbd932776269cc78fa20d6597c5286a8301d9712ca6ba27e1`  
		Last Modified: Fri, 15 May 2020 23:26:27 GMT  
		Size: 7.3 MB (7285336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62363baf5a298c4aecde09c629388197091d261f20fd00863a1693c8847cc34`  
		Last Modified: Fri, 15 May 2020 23:26:27 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0e939b10f701fd67e6400e3d0193f9dbafde2f4bc53215a7305a7c7352bdcb`  
		Last Modified: Fri, 15 May 2020 23:26:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm variant v7

```console
$ docker pull redis@sha256:a9395e60f632ac5808d01ff562ddafcccf44d254f634164eef079f86f0e4fcd3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9972279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af28cbbd6cfbc59e7a5f1a1855dd7caa878b4fd03a749db7b3e51823a58c6b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:51:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 08:51:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 06:33:17 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 06:33:18 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 06:33:20 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 06:34:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 06:34:13 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 06:34:14 GMT
VOLUME [/data]
# Sat, 16 May 2020 06:34:15 GMT
WORKDIR /data
# Sat, 16 May 2020 06:34:16 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 06:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 06:34:17 GMT
EXPOSE 6379
# Sat, 16 May 2020 06:34:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0765e03c998449baf4c76a1011cf80e6ab974db3d5d8da3a361bfeeb875d96db`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07fda5f4761823162fa661b4466f517ad5db025d9689c123221af67af9b53f`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 399.8 KB (399779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b80e8aaba692112e559076be6bb0334a707afdf5e98838a1871caa0866a8c0e`  
		Last Modified: Sat, 16 May 2020 06:35:45 GMT  
		Size: 7.1 MB (7148634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87bac8f769e16dcbd264fba3220e6015ebc7ade1c9dbbeaaf05826b5a181b86`  
		Last Modified: Sat, 16 May 2020 06:35:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb4e2186895e529da275fc0432b79e52a0bb9857639493ec62bcf3bf168531a`  
		Last Modified: Sat, 16 May 2020 06:35:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:745fe4f5f083ab735a17c56a7b213000f369f6cb8f44350c0d5e82db296dade8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10520097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26e9dafef70ab5ad06818ba5897d0d464402e823220faa6d106c50cb1f3828a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:45:10 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 12:45:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 08:25:57 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 08:25:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 08:25:59 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 08:26:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:26:52 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:26:52 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:26:53 GMT
WORKDIR /data
# Sat, 16 May 2020 08:26:54 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 08:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:26:55 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:26:56 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7050d23898adae8e4a2e0ab67eaeab9f9a9ec0fa5b88b128eeff4de1570877`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8982b178d819b1f2f10c3375b2c7ed054157cc5e711b58b6a2dcb376686e5d59`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 404.7 KB (404661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81e21ac53933c4757cd8a04fd0253d126746afcf7e023bbad9a93dec0acd26`  
		Last Modified: Sat, 16 May 2020 08:29:02 GMT  
		Size: 7.4 MB (7389208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e3ddab2b277bd44f7dc380187d16e5028acf9cc4dfee80f19494ea9e060aba`  
		Last Modified: Sat, 16 May 2020 08:28:58 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb66b8b7b33b484540124708f55d85ee24ea6274d5c4dc36ecbd1e84637e678e`  
		Last Modified: Sat, 16 May 2020 08:28:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; 386

```console
$ docker pull redis@sha256:bbfdc448dafad37023ae75c4fcfbd5d1ec7bd78aad8e769b62753c36c31757b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10290082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34322bf2334fed58c9521a918064a594354d513fbeec9b4b637dd5be45e8b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:49:36 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 05:49:38 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 00:09:40 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 00:09:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 00:09:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 00:11:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:11:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:11:09 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:11:10 GMT
WORKDIR /data
# Sat, 16 May 2020 00:11:10 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 00:11:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:11:10 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:11:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4eb71d5f124b9b51684034d7d96fba6399ff6892995e51137d0c0617a11fb9`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7685edc32d5ef38faf3beb4310c119862b1dfa18ea58edb0dbca84e9417b267`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 407.9 KB (407901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02f4cc0a73447e7af4c367a8efe6a3fe2e6b6cdf92088abd4c2b8f99f980af`  
		Last Modified: Sat, 16 May 2020 00:14:01 GMT  
		Size: 7.1 MB (7072021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd586489393880a99bcea0f145202694e2d8e8c438c7d6b44741073ea6d2c16`  
		Last Modified: Sat, 16 May 2020 00:13:59 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd50ae8a09e8979660d44015b05f83ff9419212dcd16c1dd9372263dfadaff9`  
		Last Modified: Sat, 16 May 2020 00:13:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:50b2e427f6b8a80a2532561509d6bb630381f1e73683bedb0723222a0391e5aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11129201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7ff884dff0f0f831a77c117ef871f6b9dfe526d553ea1a7178969d1b9abf56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:02:06 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 09:02:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 18 May 2020 13:36:42 GMT
ENV REDIS_VERSION=6.0.2
# Mon, 18 May 2020 13:36:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Mon, 18 May 2020 13:36:56 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Mon, 18 May 2020 13:38:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:38:08 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:38:11 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:38:20 GMT
WORKDIR /data
# Mon, 18 May 2020 13:38:23 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 18 May 2020 13:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:38:32 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:38:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc79e36a18515157312416d029cb35887ee8668b53b6c0e3867a4d0dd8dd231`  
		Last Modified: Fri, 24 Apr 2020 09:06:56 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83078862453fa1de07d734ccc5b995c92cd74710488c11d066ad752e3402d`  
		Last Modified: Fri, 24 Apr 2020 09:06:57 GMT  
		Size: 409.9 KB (409875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432ade9a2f2eaed492af9b2c567a554192ca3c2460cdf54cbdd74ef7e351b5c6`  
		Last Modified: Mon, 18 May 2020 13:43:25 GMT  
		Size: 7.9 MB (7895679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92956e0c94d7efbf996da0a821961e7e25d592d34d3f95cc7117d36ace6c4f8c`  
		Last Modified: Mon, 18 May 2020 13:43:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403543cf6789e71324a71e34551d530ede80b0836ac96a844a65ebb7c978de2`  
		Last Modified: Mon, 18 May 2020 13:43:22 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; s390x

```console
$ docker pull redis@sha256:7e87f23ad9c129bc30f56aa8881568fd3bae9fdcf1aca09f9fd15a145a8a78bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10647559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9dc6fb128105420046bfd04554e6dd0f328c259824417652aef3ff4986b8df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:02:35 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 07:02:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 15 May 2020 22:42:24 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 22:42:25 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 22:42:25 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 22:43:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 22:43:01 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 22:43:02 GMT
VOLUME [/data]
# Fri, 15 May 2020 22:43:02 GMT
WORKDIR /data
# Fri, 15 May 2020 22:43:02 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 15 May 2020 22:43:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 22:43:03 GMT
EXPOSE 6379
# Fri, 15 May 2020 22:43:03 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2da1b54f68b54cfd646e4cf510a14593b857e3c6e7732985b5a3bc5e213a72a`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f0a46f7a997ac6f05cd804b3a0f56c74348f25fd9e164c66ab7c5c4a6a2c82`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 407.4 KB (407392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d280287c062cfd9d589ad117076ba536339a11933f5cc8c50679b99a7d5a33`  
		Last Modified: Fri, 15 May 2020 22:43:59 GMT  
		Size: 7.7 MB (7655503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8cd36de079748236b7e47e5540b2968095a52c1e3eb820750e1eb95c3cf282`  
		Last Modified: Fri, 15 May 2020 22:43:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c5e784b212d08809045f9af3f7675dd7d74d224be6831c0bedaf3512f2d204`  
		Last Modified: Fri, 15 May 2020 22:43:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:alpine3.11`

```console
$ docker pull redis@sha256:b7e093c1a1cd040698fc28e4be453d8df1a46323fa4178d6d2d5fcb3bff88c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:alpine3.11` - linux; amd64

```console
$ docker pull redis@sha256:e5146a61518fef302756bd0bf226ac530fc23d7537097fa378cc50fcb5778b64
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10615454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ceee5c3fa3cea2607d5e2bcc54d019be616e322979be8fc7a8d0d78b59a1f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 19:19:42 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 19:19:43 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 02:13:46 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:15:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:15:36 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:15:36 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:15:37 GMT
WORKDIR /data
# Sat, 16 May 2020 02:15:37 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 02:15:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:15:38 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:15:38 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0373118a0d956ca0ee963e307457f45f073db9096f7c6f87c10251d071f0dc`  
		Last Modified: Fri, 24 Apr 2020 19:23:01 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd369fe62565d644723bfdb734c4ecb2a96191366ec08424146aa9c5ff6b308`  
		Last Modified: Fri, 24 Apr 2020 19:23:02 GMT  
		Size: 402.6 KB (402568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d862fc04e31c48831cc75b3b3868126e27f4e51c45bdcddb6ffc7c94b9205a76`  
		Last Modified: Sat, 16 May 2020 02:20:31 GMT  
		Size: 7.4 MB (7397830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb087a9da0889770a90077b54e12441d375e7027b377997f98a5e6d827ab3fe`  
		Last Modified: Sat, 16 May 2020 02:20:29 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be29dc118a7a01cd97bac04e83376259dee6d48d1cf35a94a8d26d3a73159bb`  
		Last Modified: Sat, 16 May 2020 02:20:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.11` - linux; arm variant v6

```console
$ docker pull redis@sha256:4057fbe62d49d301734916e4d6d7dd8f9c2d06ebfdad741698aa18ff152b642c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10312873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00275d208cadbfe750c573429cfd2721a47e1b792b022432d241395fbe82dbb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:24 GMT
ADD file:cc0770cddff6b50d5e31f39886420eb8a0b4af55664d6f7599207c9aeaf6a501 in / 
# Thu, 23 Apr 2020 15:51:25 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 22:30:17 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Thu, 23 Apr 2020 22:30:20 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 15 May 2020 23:24:21 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 23:24:22 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 23:24:23 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 23:25:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 23:25:28 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 23:25:30 GMT
VOLUME [/data]
# Fri, 15 May 2020 23:25:31 GMT
WORKDIR /data
# Fri, 15 May 2020 23:25:33 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 15 May 2020 23:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 23:25:36 GMT
EXPOSE 6379
# Fri, 15 May 2020 23:25:37 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b9e3228833e92f0688e0f87234e75965e62e47cfbb9ca8cc5fa19c2e7cd13f80`  
		Last Modified: Thu, 23 Apr 2020 15:52:05 GMT  
		Size: 2.6 MB (2619936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab5b04292d1974b3feedf74dddf563efe3ba5b5c38239a49e8adf0ac8140028`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af20f6a7bee5bf869254b4964c1a5d8dd5ef1353ac48081a885920682312555b`  
		Last Modified: Thu, 23 Apr 2020 22:33:41 GMT  
		Size: 405.8 KB (405799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cd828ef5be835bbd932776269cc78fa20d6597c5286a8301d9712ca6ba27e1`  
		Last Modified: Fri, 15 May 2020 23:26:27 GMT  
		Size: 7.3 MB (7285336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62363baf5a298c4aecde09c629388197091d261f20fd00863a1693c8847cc34`  
		Last Modified: Fri, 15 May 2020 23:26:27 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0e939b10f701fd67e6400e3d0193f9dbafde2f4bc53215a7305a7c7352bdcb`  
		Last Modified: Fri, 15 May 2020 23:26:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.11` - linux; arm variant v7

```console
$ docker pull redis@sha256:a9395e60f632ac5808d01ff562ddafcccf44d254f634164eef079f86f0e4fcd3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9972279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af28cbbd6cfbc59e7a5f1a1855dd7caa878b4fd03a749db7b3e51823a58c6b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 22:04:19 GMT
ADD file:33578d3cacfab86c195d99396dd012ec511796a1d2d8d6f0a02b8a055673c294 in / 
# Thu, 23 Apr 2020 22:04:22 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:51:32 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 08:51:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 06:33:17 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 06:33:18 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 06:33:20 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 06:34:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 06:34:13 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 06:34:14 GMT
VOLUME [/data]
# Sat, 16 May 2020 06:34:15 GMT
WORKDIR /data
# Sat, 16 May 2020 06:34:16 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 06:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 06:34:17 GMT
EXPOSE 6379
# Sat, 16 May 2020 06:34:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:3cfb62949d9d8613854db4d5fe502a9219c2b55a153043500078a64e880ae234`  
		Last Modified: Thu, 23 Apr 2020 22:05:12 GMT  
		Size: 2.4 MB (2422063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0765e03c998449baf4c76a1011cf80e6ab974db3d5d8da3a361bfeeb875d96db`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc07fda5f4761823162fa661b4466f517ad5db025d9689c123221af67af9b53f`  
		Last Modified: Fri, 24 Apr 2020 08:55:16 GMT  
		Size: 399.8 KB (399779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b80e8aaba692112e559076be6bb0334a707afdf5e98838a1871caa0866a8c0e`  
		Last Modified: Sat, 16 May 2020 06:35:45 GMT  
		Size: 7.1 MB (7148634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87bac8f769e16dcbd264fba3220e6015ebc7ade1c9dbbeaaf05826b5a181b86`  
		Last Modified: Sat, 16 May 2020 06:35:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb4e2186895e529da275fc0432b79e52a0bb9857639493ec62bcf3bf168531a`  
		Last Modified: Sat, 16 May 2020 06:35:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.11` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:745fe4f5f083ab735a17c56a7b213000f369f6cb8f44350c0d5e82db296dade8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10520097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26e9dafef70ab5ad06818ba5897d0d464402e823220faa6d106c50cb1f3828a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:18 GMT
ADD file:85ae77bc1e43353ff14e6fe1658be1ed4ecbf4330212ac3d7ab7462add32dd39 in / 
# Fri, 24 Apr 2020 00:14:21 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 12:45:10 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 12:45:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 08:25:57 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 08:25:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 08:25:59 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 08:26:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:26:52 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:26:52 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:26:53 GMT
WORKDIR /data
# Sat, 16 May 2020 08:26:54 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 08:26:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:26:55 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:26:56 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:29e5d40040c18c692ed73df24511071725b74956ca1a61fe6056a651d86a13bd`  
		Last Modified: Fri, 24 Apr 2020 00:15:41 GMT  
		Size: 2.7 MB (2724424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7050d23898adae8e4a2e0ab67eaeab9f9a9ec0fa5b88b128eeff4de1570877`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8982b178d819b1f2f10c3375b2c7ed054157cc5e711b58b6a2dcb376686e5d59`  
		Last Modified: Fri, 24 Apr 2020 12:48:50 GMT  
		Size: 404.7 KB (404661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe81e21ac53933c4757cd8a04fd0253d126746afcf7e023bbad9a93dec0acd26`  
		Last Modified: Sat, 16 May 2020 08:29:02 GMT  
		Size: 7.4 MB (7389208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e3ddab2b277bd44f7dc380187d16e5028acf9cc4dfee80f19494ea9e060aba`  
		Last Modified: Sat, 16 May 2020 08:28:58 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb66b8b7b33b484540124708f55d85ee24ea6274d5c4dc36ecbd1e84637e678e`  
		Last Modified: Sat, 16 May 2020 08:28:58 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.11` - linux; 386

```console
$ docker pull redis@sha256:bbfdc448dafad37023ae75c4fcfbd5d1ec7bd78aad8e769b62753c36c31757b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10290082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34322bf2334fed58c9521a918064a594354d513fbeec9b4b637dd5be45e8b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 05:49:36 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 05:49:38 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Sat, 16 May 2020 00:09:40 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 00:09:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 00:09:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 00:11:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:11:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:11:09 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:11:10 GMT
WORKDIR /data
# Sat, 16 May 2020 00:11:10 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Sat, 16 May 2020 00:11:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:11:10 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:11:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4eb71d5f124b9b51684034d7d96fba6399ff6892995e51137d0c0617a11fb9`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7685edc32d5ef38faf3beb4310c119862b1dfa18ea58edb0dbca84e9417b267`  
		Last Modified: Fri, 24 Apr 2020 05:53:39 GMT  
		Size: 407.9 KB (407901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02f4cc0a73447e7af4c367a8efe6a3fe2e6b6cdf92088abd4c2b8f99f980af`  
		Last Modified: Sat, 16 May 2020 00:14:01 GMT  
		Size: 7.1 MB (7072021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd586489393880a99bcea0f145202694e2d8e8c438c7d6b44741073ea6d2c16`  
		Last Modified: Sat, 16 May 2020 00:13:59 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd50ae8a09e8979660d44015b05f83ff9419212dcd16c1dd9372263dfadaff9`  
		Last Modified: Sat, 16 May 2020 00:13:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.11` - linux; ppc64le

```console
$ docker pull redis@sha256:50b2e427f6b8a80a2532561509d6bb630381f1e73683bedb0723222a0391e5aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11129201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7ff884dff0f0f831a77c117ef871f6b9dfe526d553ea1a7178969d1b9abf56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:02:06 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 09:02:13 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Mon, 18 May 2020 13:36:42 GMT
ENV REDIS_VERSION=6.0.2
# Mon, 18 May 2020 13:36:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Mon, 18 May 2020 13:36:56 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Mon, 18 May 2020 13:38:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:38:08 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:38:11 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:38:20 GMT
WORKDIR /data
# Mon, 18 May 2020 13:38:23 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Mon, 18 May 2020 13:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:38:32 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:38:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc79e36a18515157312416d029cb35887ee8668b53b6c0e3867a4d0dd8dd231`  
		Last Modified: Fri, 24 Apr 2020 09:06:56 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83078862453fa1de07d734ccc5b995c92cd74710488c11d066ad752e3402d`  
		Last Modified: Fri, 24 Apr 2020 09:06:57 GMT  
		Size: 409.9 KB (409875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432ade9a2f2eaed492af9b2c567a554192ca3c2460cdf54cbdd74ef7e351b5c6`  
		Last Modified: Mon, 18 May 2020 13:43:25 GMT  
		Size: 7.9 MB (7895679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92956e0c94d7efbf996da0a821961e7e25d592d34d3f95cc7117d36ace6c4f8c`  
		Last Modified: Mon, 18 May 2020 13:43:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403543cf6789e71324a71e34551d530ede80b0836ac96a844a65ebb7c978de2`  
		Last Modified: Mon, 18 May 2020 13:43:22 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine3.11` - linux; s390x

```console
$ docker pull redis@sha256:7e87f23ad9c129bc30f56aa8881568fd3bae9fdcf1aca09f9fd15a145a8a78bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10647559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9dc6fb128105420046bfd04554e6dd0f328c259824417652aef3ff4986b8df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 23 Apr 2020 17:50:57 GMT
ADD file:a59a30c2fd43c9f3b820751a6f5a54688c14440a1ddace1ab255475f46e6ba2d in / 
# Thu, 23 Apr 2020 17:50:58 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:02:35 GMT
RUN addgroup -S -g 1000 redis && adduser -S -G redis -u 999 redis
# Fri, 24 Apr 2020 07:02:36 GMT
RUN apk add --no-cache 		'su-exec>=0.2' 		tzdata
# Fri, 15 May 2020 22:42:24 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 22:42:25 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 22:42:25 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 22:43:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 		openssl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .redis-rundeps $runDeps; 	apk del --no-network .build-deps; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 22:43:01 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 22:43:02 GMT
VOLUME [/data]
# Fri, 15 May 2020 22:43:02 GMT
WORKDIR /data
# Fri, 15 May 2020 22:43:02 GMT
COPY file:c48b97ea65422782310396358f838c38c0747767dd606a88d4c3d0b034a60762 in /usr/local/bin/ 
# Fri, 15 May 2020 22:43:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 22:43:03 GMT
EXPOSE 6379
# Fri, 15 May 2020 22:43:03 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7184c046fdf17da4c16ca482e5ede36e1f2d41ac8cea9c036e488fd149d6e8e7`  
		Last Modified: Thu, 23 Apr 2020 17:51:38 GMT  
		Size: 2.6 MB (2582859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2da1b54f68b54cfd646e4cf510a14593b857e3c6e7732985b5a3bc5e213a72a`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f0a46f7a997ac6f05cd804b3a0f56c74348f25fd9e164c66ab7c5c4a6a2c82`  
		Last Modified: Fri, 24 Apr 2020 07:04:54 GMT  
		Size: 407.4 KB (407392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d280287c062cfd9d589ad117076ba536339a11933f5cc8c50679b99a7d5a33`  
		Last Modified: Fri, 15 May 2020 22:43:59 GMT  
		Size: 7.7 MB (7655503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8cd36de079748236b7e47e5540b2968095a52c1e3eb820750e1eb95c3cf282`  
		Last Modified: Fri, 15 May 2020 22:43:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c5e784b212d08809045f9af3f7675dd7d74d224be6831c0bedaf3512f2d204`  
		Last Modified: Fri, 15 May 2020 22:43:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:buster`

```console
$ docker pull redis@sha256:f345892f9889fbd14e46eb00ae06f99da2190cfcbfbf2d0d6e71f6d4571eb11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redis:buster` - linux; amd64

```console
$ docker pull redis@sha256:ab54d0eafe20eeb825ab7b5a58d317cae5a4388c3acf1d91f9c33985b20ff273
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38167360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c654ea77ff723987795e7ce2ef47dbe8e40d5a0f819c04a19be78b95b3b5e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:13:33 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:13:33 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:13:33 GMT
WORKDIR /data
# Sat, 16 May 2020 02:13:34 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:13:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:13:34 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:13:35 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23612dae160f1ec7bcb03995f6511b98869720a2af255e8ed290591b402246b5`  
		Last Modified: Sat, 16 May 2020 02:20:21 GMT  
		Size: 9.6 MB (9648645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c369ccd196fb08d91f340da5260c798cadbadfbb4ab1e323cbbf6b7478a6aa`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a702f65a6a9fe28799e5d494490ab96d303ba44fc2286c2c65775b95de371f2`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:buster` - linux; arm variant v5

```console
$ docker pull redis@sha256:1047d344de59e9413a8a6e2e394f9ff411516a2ef2fea4aee693a781a5eb7bf9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35393451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1c15fd4eb475c34af8c1fa99e894a544b78230f55e77b10eab309385f3e0e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 22:38:03 GMT
ADD file:cbd01ff8d2e40a25bcdb13dc19ffe124c2927b491997dc1c57d4f2c2a308e279 in / 
# Thu, 14 May 2020 22:38:05 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:40:59 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 04:40:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 04:41:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 23:12:39 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 23:12:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 23:12:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 23:14:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 23:14:55 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 23:14:56 GMT
VOLUME [/data]
# Fri, 15 May 2020 23:14:57 GMT
WORKDIR /data
# Fri, 15 May 2020 23:14:58 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 23:14:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 23:15:00 GMT
EXPOSE 6379
# Fri, 15 May 2020 23:15:00 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:24d81022117207b0239d8a8023ca1724b7dde38cb08ce5b9199f59d475d1e600`  
		Last Modified: Thu, 14 May 2020 22:46:51 GMT  
		Size: 24.8 MB (24838470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c13f680b58f95af37082529e8a1ecd6358e22a7e13a75344d8375a03cafb174`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2286bbfcebea1b30a2e862afd7742a7f65237dcabddc9486bfaaf5fd8ba0d65`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.4 MB (1376110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f639441dae5f4f944717cd02a5f128e4758eac38d8ab22f77b69484becc555`  
		Last Modified: Fri, 15 May 2020 23:15:35 GMT  
		Size: 9.2 MB (9176601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c577f5c08a0c4b296439ea910cc8bd148bd1e69058c7af5d40c87b0e825b27`  
		Last Modified: Fri, 15 May 2020 23:15:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dfe2add81403d228b336a3189e8aa2903f266cb813294e4b69d558d25d34919`  
		Last Modified: Fri, 15 May 2020 23:15:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:buster` - linux; arm variant v7

```console
$ docker pull redis@sha256:c682e2bc4474179d62f5943399e78ac9fa38797880bdbdef7615ec58559d6fb6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33018384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc7563c765d7fbfa56e311c229f98caa69bb0cd10e17d2f2344df5911079ba2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 01:00:06 GMT
ADD file:e3f9a454eccb40b4d7bf1dcc17ec29589a007ac67545d1cb5b6fa213c872c8f2 in / 
# Fri, 15 May 2020 01:00:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 16:49:40 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 16:49:40 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 16:50:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 06:31:45 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 06:31:45 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 06:31:46 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 06:32:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 06:33:00 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 06:33:00 GMT
VOLUME [/data]
# Sat, 16 May 2020 06:33:01 GMT
WORKDIR /data
# Sat, 16 May 2020 06:33:02 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 06:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 06:33:03 GMT
EXPOSE 6379
# Sat, 16 May 2020 06:33:04 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e41e28500352be59188c3d871a4b5a3f594350b860a9a36ed5808a35920bdae4`  
		Last Modified: Fri, 15 May 2020 01:11:21 GMT  
		Size: 22.7 MB (22705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6732859766aedad40f91cd96df6b5a6930efe6614b0f084b8459d93c22a69`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed92b736a14b52db74c7cd9919c66ce953393f0544906969081702697d5a6b54`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.4 MB (1368207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae49590ac9360b33276abbdc9f1f45988c0c47b5efbd5b0f55d5dfa258b9ba5a`  
		Last Modified: Sat, 16 May 2020 06:35:15 GMT  
		Size: 8.9 MB (8941986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc7ac3e6ef453bf3e43ffc9747527339b36ba8a594ed32e4e32cd445f706bd2`  
		Last Modified: Sat, 16 May 2020 06:35:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8549d28648c0fd590b2bb28888a0f398a9c44497fdc234419f1c06fdc807eb7`  
		Last Modified: Sat, 16 May 2020 06:35:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:buster` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:fefa8a4cc0bd93b3323c54e3f3aa33ced6f32c9471e5857b067cbf775d7cc918
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36725296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8727a8f0bd0aa8dc538822706743dcc10299697988254fbb44dfec9676eb56b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 12:44:06 GMT
ADD file:b305c1792102142f183d3084026f0fc6be3ddf8d1959b32f0a5d22d35eebcd15 in / 
# Fri, 15 May 2020 12:44:07 GMT
CMD ["bash"]
# Sat, 16 May 2020 08:24:10 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 08:24:10 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 08:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 08:24:37 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 08:24:37 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 08:24:38 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 08:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:25:46 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:25:46 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:25:47 GMT
WORKDIR /data
# Sat, 16 May 2020 08:25:48 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 08:25:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:25:49 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:25:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8a7e1e68c24e5cac20ef26d29505c58456b561c431f0c683b66d1a0943f40dd4`  
		Last Modified: Fri, 15 May 2020 12:53:36 GMT  
		Size: 25.9 MB (25857195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc5ca4e8f484b410989ac557169938b5fe6288ed5add0839e05a790ef47676`  
		Last Modified: Sat, 16 May 2020 08:28:42 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eccfc30e2be16f57d04f487ed80dd2b52ada557753eca7c79eb2ff88ab421f2`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 1.4 MB (1352995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16b8ee6261f593931e5c80c002e18026c3b7bb7d343befbc1fa756ed97c267b`  
		Last Modified: Sat, 16 May 2020 08:28:46 GMT  
		Size: 9.5 MB (9512830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cc79ffa02956bccb011cc1ff2235860b2826a4728941da06492bd6e52f443e`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235fadffc19d75adb68374da679a5c9976a38b0474e07ce04bab7d7093b121b6`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:buster` - linux; 386

```console
$ docker pull redis@sha256:4171a489575082d2d6af76fa8638109e257d3c413eff0b47746288d64b7c5161
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38426981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1dbd0ad2ae3cebd5b89eeb326a1602a2e5f070d58fc8b5f7ef2a8f13f447fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Sat, 16 May 2020 00:07:24 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 00:07:24 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 00:07:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 00:09:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:09:23 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:09:23 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:09:24 GMT
WORKDIR /data
# Sat, 16 May 2020 00:09:24 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 00:09:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:09:25 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:09:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157733bfb7391a76ac45c4aa7ed1ea9e99ee6b2f4f70fbbab7b48b514fff73fc`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7927326d7d556c02a6f3c72888c9f9d2beb780c097c9fb1ca55539afa2a42d`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.4 MB (1387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f28c9a9abf780003c46983a03474d1009255ee52e02e3d6b5387645a25676`  
		Last Modified: Sat, 16 May 2020 00:13:51 GMT  
		Size: 9.3 MB (9282358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4252a3c771aac801bae55f4d6153efe090eae2e87d538bb540d9bfdabf1c07`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7baa10daa19f6859f36ad1667478b73ec03e78417cce615c228b8ff5f468e13`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:buster` - linux; mips64le

```console
$ docker pull redis@sha256:5be8885d29600ec5aa62a44c884f05a27a85156be9bcb6ee7fc5fc51abb06840
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36602715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386312a161a758c285fb32d1403def9b9a2ccd8089f8fde65b3c939dce9244b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 04:48:19 GMT
ADD file:1163d3a5831eb58d132b66b60303169816e7bd8289f19caaac1157179a95f6f9 in / 
# Fri, 15 May 2020 04:48:19 GMT
CMD ["bash"]
# Fri, 15 May 2020 15:35:02 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 15:35:02 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 15:35:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 01:59:50 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 01:59:50 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 01:59:51 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:03:22 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:03:23 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:03:23 GMT
WORKDIR /data
# Sat, 16 May 2020 02:03:23 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:03:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:03:24 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:03:24 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d22357c747999d33ec7501da2c05aa9e95079ebddefbcb326976c5ed5b176b3f`  
		Last Modified: Fri, 15 May 2020 04:57:10 GMT  
		Size: 25.8 MB (25764292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f562c9b9683468308a6f59cab7d724ffc3b35a66acd8ce093b288144db2b7c5`  
		Last Modified: Fri, 15 May 2020 15:42:49 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fda93ec518be6790dd5e435d4bb66cab95d5c14044f01c584fd463ca6ffd290`  
		Last Modified: Fri, 15 May 2020 15:42:50 GMT  
		Size: 1.3 MB (1305516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb60cef9605760eb551d25d4fd2012fbfee55e53a2fc8015e348b35d1c605fe1`  
		Last Modified: Sat, 16 May 2020 02:03:57 GMT  
		Size: 9.5 MB (9530668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0260009eaa931057e783dd3d048e8380b054f9217f32ed1a22b242df7faaff`  
		Last Modified: Sat, 16 May 2020 02:03:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc70c6ee351687f96473d0a015d3ef6e321df0663132a51f3de2d4422313dfed`  
		Last Modified: Sat, 16 May 2020 02:03:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:buster` - linux; ppc64le

```console
$ docker pull redis@sha256:a08a8ff07e718a2a11e9de8d732ed3b9c8ddf9f6aa3914cc71c18e94de4bd5fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42115418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6f886000af62e580a3a50954e45ae47e2207c358362bea46ddd0b2242f0cc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 16 May 2020 17:14:59 GMT
ADD file:b2656a1711bd47585595ae2927cfd4ec00eb903d193583d945b6d60f0a2691bb in / 
# Sat, 16 May 2020 17:15:04 GMT
CMD ["bash"]
# Mon, 18 May 2020 13:30:23 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Mon, 18 May 2020 13:30:26 GMT
ENV GOSU_VERSION=1.12
# Mon, 18 May 2020 13:32:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 18 May 2020 13:32:31 GMT
ENV REDIS_VERSION=6.0.2
# Mon, 18 May 2020 13:32:34 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Mon, 18 May 2020 13:32:36 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Mon, 18 May 2020 13:35:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:35:48 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:35:53 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:35:59 GMT
WORKDIR /data
# Mon, 18 May 2020 13:36:02 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Mon, 18 May 2020 13:36:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:36:13 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:36:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:034d508ed7647e7139951a435acc95e0124f50c984670d0e53b4f5ba25cf6ed1`  
		Last Modified: Sat, 16 May 2020 18:31:49 GMT  
		Size: 30.5 MB (30524456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c613ed63b519e3a0419cf56e14127f5d25466416a8143341540d12cb99943b65`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec60488415c29ebe96bbfabff01925147e50ee55136fdf961fbe8526617f3b`  
		Last Modified: Mon, 18 May 2020 13:42:57 GMT  
		Size: 1.3 MB (1335429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaf24998a2bd9be32258b02fa8e7f6f41d0eda42d774cac44dcabd35978f81d`  
		Last Modified: Mon, 18 May 2020 13:42:59 GMT  
		Size: 10.3 MB (10253250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6948fa0de358f9d87f91ee1e03e42297fb7f70db44a3fc74091faac19916c2`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24281879de8036ec53f002b70225e29b23542cc353d0189e2cf41dd4db52e89a`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:buster` - linux; s390x

```console
$ docker pull redis@sha256:9ef11ffd48bd63460ec92a2e14ef5b3fce4eaa785fbdec11751a934ad38d601d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36741516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e6564e23714b9e21badf63a7c7ce03ab2de0060269e6b9aa3644a656750072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 05:15:35 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 05:15:35 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 05:15:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 22:41:40 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 22:41:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 22:41:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 22:42:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 22:42:14 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 22:42:15 GMT
VOLUME [/data]
# Fri, 15 May 2020 22:42:15 GMT
WORKDIR /data
# Fri, 15 May 2020 22:42:15 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 22:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 22:42:15 GMT
EXPOSE 6379
# Fri, 15 May 2020 22:42:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e40cd0998be29e9cce5152b7d3644b03b888bcca5db2049d43c93bf53185d`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc1e5303c90f8fcd807a5042757fb4de087ae4b3319afca416b72e858de788c`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.4 MB (1403711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5d61c1be6277797ce170d2b088f07f55873edc9b1a71d02a2d155dd4e00c6`  
		Last Modified: Fri, 15 May 2020 22:43:45 GMT  
		Size: 9.6 MB (9622596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e520dcecd5852ea3751c3d41ca8c103d95984d027003a983f3c118645530282`  
		Last Modified: Fri, 15 May 2020 22:43:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89764005f67e8cd243c7c732985b0b2b9863ded8a6f2fa729c6c8102aa6bf73d`  
		Last Modified: Fri, 15 May 2020 22:43:48 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:latest`

```console
$ docker pull redis@sha256:f345892f9889fbd14e46eb00ae06f99da2190cfcbfbf2d0d6e71f6d4571eb11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `redis:latest` - linux; amd64

```console
$ docker pull redis@sha256:ab54d0eafe20eeb825ab7b5a58d317cae5a4388c3acf1d91f9c33985b20ff273
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38167360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c654ea77ff723987795e7ce2ef47dbe8e40d5a0f819c04a19be78b95b3b5e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 02:11:30 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 02:11:30 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 02:11:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 02:11:47 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:13:33 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:13:33 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:13:33 GMT
WORKDIR /data
# Sat, 16 May 2020 02:13:34 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:13:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:13:34 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:13:35 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608641ee4c3f7bdac1b03db86133a0b6226e07f38447a19b3797dd70fb7f99a0`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668ab9e1f4bcc5af5e04ab96cf260d2dcc8f2157fe768db1aa053c3045fedc03`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 1.4 MB (1417718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23612dae160f1ec7bcb03995f6511b98869720a2af255e8ed290591b402246b5`  
		Last Modified: Sat, 16 May 2020 02:20:21 GMT  
		Size: 9.6 MB (9648645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c369ccd196fb08d91f340da5260c798cadbadfbb4ab1e323cbbf6b7478a6aa`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a702f65a6a9fe28799e5d494490ab96d303ba44fc2286c2c65775b95de371f2`  
		Last Modified: Sat, 16 May 2020 02:20:19 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; arm variant v5

```console
$ docker pull redis@sha256:1047d344de59e9413a8a6e2e394f9ff411516a2ef2fea4aee693a781a5eb7bf9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 MB (35393451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1c15fd4eb475c34af8c1fa99e894a544b78230f55e77b10eab309385f3e0e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 22:38:03 GMT
ADD file:cbd01ff8d2e40a25bcdb13dc19ffe124c2927b491997dc1c57d4f2c2a308e279 in / 
# Thu, 14 May 2020 22:38:05 GMT
CMD ["bash"]
# Fri, 15 May 2020 04:40:59 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 04:40:59 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 04:41:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 23:12:39 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 23:12:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 23:12:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 23:14:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 23:14:55 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 23:14:56 GMT
VOLUME [/data]
# Fri, 15 May 2020 23:14:57 GMT
WORKDIR /data
# Fri, 15 May 2020 23:14:58 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 23:14:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 23:15:00 GMT
EXPOSE 6379
# Fri, 15 May 2020 23:15:00 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:24d81022117207b0239d8a8023ca1724b7dde38cb08ce5b9199f59d475d1e600`  
		Last Modified: Thu, 14 May 2020 22:46:51 GMT  
		Size: 24.8 MB (24838470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c13f680b58f95af37082529e8a1ecd6358e22a7e13a75344d8375a03cafb174`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2286bbfcebea1b30a2e862afd7742a7f65237dcabddc9486bfaaf5fd8ba0d65`  
		Last Modified: Fri, 15 May 2020 04:44:28 GMT  
		Size: 1.4 MB (1376110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f639441dae5f4f944717cd02a5f128e4758eac38d8ab22f77b69484becc555`  
		Last Modified: Fri, 15 May 2020 23:15:35 GMT  
		Size: 9.2 MB (9176601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c577f5c08a0c4b296439ea910cc8bd148bd1e69058c7af5d40c87b0e825b27`  
		Last Modified: Fri, 15 May 2020 23:15:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dfe2add81403d228b336a3189e8aa2903f266cb813294e4b69d558d25d34919`  
		Last Modified: Fri, 15 May 2020 23:15:32 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; arm variant v7

```console
$ docker pull redis@sha256:c682e2bc4474179d62f5943399e78ac9fa38797880bdbdef7615ec58559d6fb6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (33018384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc7563c765d7fbfa56e311c229f98caa69bb0cd10e17d2f2344df5911079ba2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 01:00:06 GMT
ADD file:e3f9a454eccb40b4d7bf1dcc17ec29589a007ac67545d1cb5b6fa213c872c8f2 in / 
# Fri, 15 May 2020 01:00:07 GMT
CMD ["bash"]
# Fri, 15 May 2020 16:49:40 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 16:49:40 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 16:50:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 06:31:45 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 06:31:45 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 06:31:46 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 06:32:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 06:33:00 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 06:33:00 GMT
VOLUME [/data]
# Sat, 16 May 2020 06:33:01 GMT
WORKDIR /data
# Sat, 16 May 2020 06:33:02 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 06:33:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 06:33:03 GMT
EXPOSE 6379
# Sat, 16 May 2020 06:33:04 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e41e28500352be59188c3d871a4b5a3f594350b860a9a36ed5808a35920bdae4`  
		Last Modified: Fri, 15 May 2020 01:11:21 GMT  
		Size: 22.7 MB (22705925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad6732859766aedad40f91cd96df6b5a6930efe6614b0f084b8459d93c22a69`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed92b736a14b52db74c7cd9919c66ce953393f0544906969081702697d5a6b54`  
		Last Modified: Fri, 15 May 2020 16:53:27 GMT  
		Size: 1.4 MB (1368207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae49590ac9360b33276abbdc9f1f45988c0c47b5efbd5b0f55d5dfa258b9ba5a`  
		Last Modified: Sat, 16 May 2020 06:35:15 GMT  
		Size: 8.9 MB (8941986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc7ac3e6ef453bf3e43ffc9747527339b36ba8a594ed32e4e32cd445f706bd2`  
		Last Modified: Sat, 16 May 2020 06:35:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8549d28648c0fd590b2bb28888a0f398a9c44497fdc234419f1c06fdc807eb7`  
		Last Modified: Sat, 16 May 2020 06:35:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:fefa8a4cc0bd93b3323c54e3f3aa33ced6f32c9471e5857b067cbf775d7cc918
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36725296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8727a8f0bd0aa8dc538822706743dcc10299697988254fbb44dfec9676eb56b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 12:44:06 GMT
ADD file:b305c1792102142f183d3084026f0fc6be3ddf8d1959b32f0a5d22d35eebcd15 in / 
# Fri, 15 May 2020 12:44:07 GMT
CMD ["bash"]
# Sat, 16 May 2020 08:24:10 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 08:24:10 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 08:24:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 08:24:37 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 08:24:37 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 08:24:38 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 08:25:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 08:25:46 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 08:25:46 GMT
VOLUME [/data]
# Sat, 16 May 2020 08:25:47 GMT
WORKDIR /data
# Sat, 16 May 2020 08:25:48 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 08:25:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 08:25:49 GMT
EXPOSE 6379
# Sat, 16 May 2020 08:25:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8a7e1e68c24e5cac20ef26d29505c58456b561c431f0c683b66d1a0943f40dd4`  
		Last Modified: Fri, 15 May 2020 12:53:36 GMT  
		Size: 25.9 MB (25857195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc5ca4e8f484b410989ac557169938b5fe6288ed5add0839e05a790ef47676`  
		Last Modified: Sat, 16 May 2020 08:28:42 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eccfc30e2be16f57d04f487ed80dd2b52ada557753eca7c79eb2ff88ab421f2`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 1.4 MB (1352995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16b8ee6261f593931e5c80c002e18026c3b7bb7d343befbc1fa756ed97c267b`  
		Last Modified: Sat, 16 May 2020 08:28:46 GMT  
		Size: 9.5 MB (9512830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13cc79ffa02956bccb011cc1ff2235860b2826a4728941da06492bd6e52f443e`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235fadffc19d75adb68374da679a5c9976a38b0474e07ce04bab7d7093b121b6`  
		Last Modified: Sat, 16 May 2020 08:28:43 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; 386

```console
$ docker pull redis@sha256:4171a489575082d2d6af76fa8638109e257d3c413eff0b47746288d64b7c5161
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38426981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1dbd0ad2ae3cebd5b89eeb326a1602a2e5f070d58fc8b5f7ef2a8f13f447fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Sat, 16 May 2020 00:07:24 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Sat, 16 May 2020 00:07:24 GMT
ENV GOSU_VERSION=1.12
# Sat, 16 May 2020 00:07:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 00:07:39 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 00:09:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 00:09:23 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 00:09:23 GMT
VOLUME [/data]
# Sat, 16 May 2020 00:09:24 GMT
WORKDIR /data
# Sat, 16 May 2020 00:09:24 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 00:09:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 00:09:25 GMT
EXPOSE 6379
# Sat, 16 May 2020 00:09:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157733bfb7391a76ac45c4aa7ed1ea9e99ee6b2f4f70fbbab7b48b514fff73fc`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7927326d7d556c02a6f3c72888c9f9d2beb780c097c9fb1ca55539afa2a42d`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 1.4 MB (1387467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186f28c9a9abf780003c46983a03474d1009255ee52e02e3d6b5387645a25676`  
		Last Modified: Sat, 16 May 2020 00:13:51 GMT  
		Size: 9.3 MB (9282358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4252a3c771aac801bae55f4d6153efe090eae2e87d538bb540d9bfdabf1c07`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7baa10daa19f6859f36ad1667478b73ec03e78417cce615c228b8ff5f468e13`  
		Last Modified: Sat, 16 May 2020 00:13:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; mips64le

```console
$ docker pull redis@sha256:5be8885d29600ec5aa62a44c884f05a27a85156be9bcb6ee7fc5fc51abb06840
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36602715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386312a161a758c285fb32d1403def9b9a2ccd8089f8fde65b3c939dce9244b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 15 May 2020 04:48:19 GMT
ADD file:1163d3a5831eb58d132b66b60303169816e7bd8289f19caaac1157179a95f6f9 in / 
# Fri, 15 May 2020 04:48:19 GMT
CMD ["bash"]
# Fri, 15 May 2020 15:35:02 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 15:35:02 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 15:35:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 16 May 2020 01:59:50 GMT
ENV REDIS_VERSION=6.0.2
# Sat, 16 May 2020 01:59:50 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Sat, 16 May 2020 01:59:51 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Sat, 16 May 2020 02:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Sat, 16 May 2020 02:03:22 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 16 May 2020 02:03:23 GMT
VOLUME [/data]
# Sat, 16 May 2020 02:03:23 GMT
WORKDIR /data
# Sat, 16 May 2020 02:03:23 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Sat, 16 May 2020 02:03:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2020 02:03:24 GMT
EXPOSE 6379
# Sat, 16 May 2020 02:03:24 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d22357c747999d33ec7501da2c05aa9e95079ebddefbcb326976c5ed5b176b3f`  
		Last Modified: Fri, 15 May 2020 04:57:10 GMT  
		Size: 25.8 MB (25764292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f562c9b9683468308a6f59cab7d724ffc3b35a66acd8ce093b288144db2b7c5`  
		Last Modified: Fri, 15 May 2020 15:42:49 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fda93ec518be6790dd5e435d4bb66cab95d5c14044f01c584fd463ca6ffd290`  
		Last Modified: Fri, 15 May 2020 15:42:50 GMT  
		Size: 1.3 MB (1305516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb60cef9605760eb551d25d4fd2012fbfee55e53a2fc8015e348b35d1c605fe1`  
		Last Modified: Sat, 16 May 2020 02:03:57 GMT  
		Size: 9.5 MB (9530668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0260009eaa931057e783dd3d048e8380b054f9217f32ed1a22b242df7faaff`  
		Last Modified: Sat, 16 May 2020 02:03:49 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc70c6ee351687f96473d0a015d3ef6e321df0663132a51f3de2d4422313dfed`  
		Last Modified: Sat, 16 May 2020 02:03:49 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; ppc64le

```console
$ docker pull redis@sha256:a08a8ff07e718a2a11e9de8d732ed3b9c8ddf9f6aa3914cc71c18e94de4bd5fa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42115418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6f886000af62e580a3a50954e45ae47e2207c358362bea46ddd0b2242f0cc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sat, 16 May 2020 17:14:59 GMT
ADD file:b2656a1711bd47585595ae2927cfd4ec00eb903d193583d945b6d60f0a2691bb in / 
# Sat, 16 May 2020 17:15:04 GMT
CMD ["bash"]
# Mon, 18 May 2020 13:30:23 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Mon, 18 May 2020 13:30:26 GMT
ENV GOSU_VERSION=1.12
# Mon, 18 May 2020 13:32:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 18 May 2020 13:32:31 GMT
ENV REDIS_VERSION=6.0.2
# Mon, 18 May 2020 13:32:34 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Mon, 18 May 2020 13:32:36 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Mon, 18 May 2020 13:35:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Mon, 18 May 2020 13:35:48 GMT
RUN mkdir /data && chown redis:redis /data
# Mon, 18 May 2020 13:35:53 GMT
VOLUME [/data]
# Mon, 18 May 2020 13:35:59 GMT
WORKDIR /data
# Mon, 18 May 2020 13:36:02 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Mon, 18 May 2020 13:36:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 May 2020 13:36:13 GMT
EXPOSE 6379
# Mon, 18 May 2020 13:36:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:034d508ed7647e7139951a435acc95e0124f50c984670d0e53b4f5ba25cf6ed1`  
		Last Modified: Sat, 16 May 2020 18:31:49 GMT  
		Size: 30.5 MB (30524456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c613ed63b519e3a0419cf56e14127f5d25466416a8143341540d12cb99943b65`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ec60488415c29ebe96bbfabff01925147e50ee55136fdf961fbe8526617f3b`  
		Last Modified: Mon, 18 May 2020 13:42:57 GMT  
		Size: 1.3 MB (1335429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaf24998a2bd9be32258b02fa8e7f6f41d0eda42d774cac44dcabd35978f81d`  
		Last Modified: Mon, 18 May 2020 13:42:59 GMT  
		Size: 10.3 MB (10253250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6948fa0de358f9d87f91ee1e03e42297fb7f70db44a3fc74091faac19916c2`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24281879de8036ec53f002b70225e29b23542cc353d0189e2cf41dd4db52e89a`  
		Last Modified: Mon, 18 May 2020 13:42:56 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; s390x

```console
$ docker pull redis@sha256:9ef11ffd48bd63460ec92a2e14ef5b3fce4eaa785fbdec11751a934ad38d601d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36741516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e6564e23714b9e21badf63a7c7ce03ab2de0060269e6b9aa3644a656750072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Fri, 15 May 2020 05:15:35 GMT
RUN groupadd -r -g 999 redis && useradd -r -g redis -u 999 redis
# Fri, 15 May 2020 05:15:35 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 05:15:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates dirmngr gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 22:41:40 GMT
ENV REDIS_VERSION=6.0.2
# Fri, 15 May 2020 22:41:41 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.0.2.tar.gz
# Fri, 15 May 2020 22:41:41 GMT
ENV REDIS_DOWNLOAD_SHA=9c37cd4228a57e82e7037094751c63349302b0b86c5e30b778a63a802dfd0109
# Fri, 15 May 2020 22:42:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version
# Fri, 15 May 2020 22:42:14 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 15 May 2020 22:42:15 GMT
VOLUME [/data]
# Fri, 15 May 2020 22:42:15 GMT
WORKDIR /data
# Fri, 15 May 2020 22:42:15 GMT
COPY file:df205a0ef6e6df8947ce0a7ae9e37b6a5588035647f38a49b8b07321003a8a01 in /usr/local/bin/ 
# Fri, 15 May 2020 22:42:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 22:42:15 GMT
EXPOSE 6379
# Fri, 15 May 2020 22:42:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e40cd0998be29e9cce5152b7d3644b03b888bcca5db2049d43c93bf53185d`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc1e5303c90f8fcd807a5042757fb4de087ae4b3319afca416b72e858de788c`  
		Last Modified: Fri, 15 May 2020 05:17:25 GMT  
		Size: 1.4 MB (1403711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5d61c1be6277797ce170d2b088f07f55873edc9b1a71d02a2d155dd4e00c6`  
		Last Modified: Fri, 15 May 2020 22:43:45 GMT  
		Size: 9.6 MB (9622596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e520dcecd5852ea3751c3d41ca8c103d95984d027003a983f3c118645530282`  
		Last Modified: Fri, 15 May 2020 22:43:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89764005f67e8cd243c7c732985b0b2b9863ded8a6f2fa729c6c8102aa6bf73d`  
		Last Modified: Fri, 15 May 2020 22:43:48 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
