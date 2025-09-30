## `redis:7-bookworm`

```console
$ docker pull redis@sha256:4a36f83c7f44b96953a7691b949ec77d8b96723623dd0b984c63d8615accb99c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `redis:7-bookworm` - linux; amd64

```console
$ docker pull redis@sha256:e3c80ea4c9c583621a7ba3a148d825b9d05b0b39793912fff5af315369e73344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45009844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbfb199fe6c9acd1dcacba0e86908b27c0de864bb7fddad3be185d234f39378`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sun, 06 Jul 2025 16:51:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV GOSU_VERSION=1.17
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_VERSION=7.4.5
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.5.tar.gz
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_SHA=00bb280528f5d7934bec8ab309b8125088c209131e10609cb1563b91365633bb
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
VOLUME [/data]
# Sun, 06 Jul 2025 16:51:58 GMT
WORKDIR /data
# Sun, 06 Jul 2025 16:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 06 Jul 2025 16:51:58 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 06 Jul 2025 16:51:58 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9caed2d62ad14d719f39d7c21363569a1cbffd06d4df1dfa423e51a5271203`  
		Last Modified: Tue, 30 Sep 2025 00:10:03 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2bf5de1061639f7a404d5b863c35f03e6fe9fbf32791faf565baaab88a0b5`  
		Last Modified: Tue, 30 Sep 2025 00:10:03 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5b901cff18504e2b3eaf199637a93de90bf90a6ac3042056f2235e9cbf712a`  
		Last Modified: Tue, 30 Sep 2025 00:10:04 GMT  
		Size: 1.4 MB (1438021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e2d6e8121af1084bbf6f302ee222d84eeef645850cd04d5c5bca014ee94af7`  
		Last Modified: Tue, 30 Sep 2025 00:10:06 GMT  
		Size: 15.3 MB (15340811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d258d56809ea8dbb7193bddc51e089ff55a8c8ce74640ba23894d64433b73ebc`  
		Last Modified: Tue, 30 Sep 2025 00:10:03 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739508a8ab9509c5910337ccf976dc5c82605b24b7edfa1190685fc9a96f8b2e`  
		Last Modified: Tue, 30 Sep 2025 00:10:04 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:6d9d13718e8c0ece84810fc2f9805fb37d99f8ad6a0912ad008c89c9235e251b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2412351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80102242e3263c198ccb21db97ca6caa682d9c8acbf2519d9e429d08424e8fdb`

```dockerfile
```

-	Layers:
	-	`sha256:86b72490dd76435d8c9c7183f3eac126c9c930d48b97c1d6ce1662443af71687`  
		Last Modified: Tue, 30 Sep 2025 01:04:50 GMT  
		Size: 2.4 MB (2376598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:221185d23511967d6ab2e983c7ae2f9abb715913dde83aae1175d3b19108dc9e`  
		Last Modified: Tue, 30 Sep 2025 01:04:51 GMT  
		Size: 35.8 KB (35753 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; arm variant v5

```console
$ docker pull redis@sha256:0211b519f6097795e485b92e42dea5e7d33c87eeb8b02f17798e8081d4fb4ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42236407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e8c7a33c1647b2045fa526c06bd11616429569c78bda6fab129dc73e8fc7c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sun, 06 Jul 2025 16:51:58 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1757289600'
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV GOSU_VERSION=1.17
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_VERSION=7.4.5
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.5.tar.gz
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_SHA=00bb280528f5d7934bec8ab309b8125088c209131e10609cb1563b91365633bb
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
VOLUME [/data]
# Sun, 06 Jul 2025 16:51:58 GMT
WORKDIR /data
# Sun, 06 Jul 2025 16:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 06 Jul 2025 16:51:58 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 06 Jul 2025 16:51:58 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:952ba1cf349522edb7270da2ee606695f7a7b47b332674ee825bd31cd9ffac57`  
		Last Modified: Mon, 08 Sep 2025 21:17:19 GMT  
		Size: 25.8 MB (25757446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71c835aa50e5eb0302ebd383ae3b036eb1730d9d29de3bb31ff352fe2da8e63`  
		Last Modified: Mon, 08 Sep 2025 22:16:31 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12139e3bfd6de7af9bbef2aee87890a37b7668598b559d152d82d41045068abf`  
		Last Modified: Mon, 08 Sep 2025 22:16:35 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a866570b4918fedb85901d90ac7df72565d86b9b7d34fc319fa576bcea66142`  
		Last Modified: Mon, 08 Sep 2025 22:16:39 GMT  
		Size: 1.4 MB (1414415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8427b774336523cb01ff15ea7ca64ba388d28d0da6ecc4b8ea8af3cdfbac735`  
		Last Modified: Tue, 09 Sep 2025 01:08:54 GMT  
		Size: 15.1 MB (15061873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec7dd8434e8f73837ef50a3dfbea758cca5ddb10336986e4a209efb73707ba3`  
		Last Modified: Mon, 08 Sep 2025 21:59:52 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88407c6a3a1f904542d6b6e3a03b6df0abf817cf55a458cb6604cc38bf339d54`  
		Last Modified: Mon, 08 Sep 2025 22:16:48 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:95e3965f4a50540f22eb3e2c9341721a3ff78d64c08b92aeb16be74248d53d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cb33a0059a926a60987a4b0dc6430731ed35b1ae1d3205bdf16498ceed73e0`

```dockerfile
```

-	Layers:
	-	`sha256:7a96700cc0219368b5f2a27d919055208a9d1e61dbdddd8e196f54f7e3e2bed1`  
		Last Modified: Tue, 09 Sep 2025 01:04:58 GMT  
		Size: 2.4 MB (2380418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d76395fbc63a1bb4a9b9704eafe5943dafa70c80747c9fd51dd7a573f958a52`  
		Last Modified: Tue, 09 Sep 2025 01:04:59 GMT  
		Size: 35.9 KB (35902 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; arm variant v7

```console
$ docker pull redis@sha256:2d58411ab4f4baa4eee2b15a75628dcdc4ea1087c43c8c41064d2b28b32e1a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.1 MB (40060782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed06c8d137ca7b941d61d6b2768ba078b63601a8f9896397e43d25072505c2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sun, 06 Jul 2025 16:51:58 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV GOSU_VERSION=1.17
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_VERSION=7.4.5
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.5.tar.gz
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_SHA=00bb280528f5d7934bec8ab309b8125088c209131e10609cb1563b91365633bb
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
VOLUME [/data]
# Sun, 06 Jul 2025 16:51:58 GMT
WORKDIR /data
# Sun, 06 Jul 2025 16:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 06 Jul 2025 16:51:58 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 06 Jul 2025 16:51:58 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e747f8ef7f1d9a41c99bfb53889f7b8de3504300740a326627fc7522904708cc`  
		Last Modified: Mon, 08 Sep 2025 21:14:21 GMT  
		Size: 23.9 MB (23933904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e0fd197a597708093380fb403ab3455fd425982b6ff2a985773198143e3b0f`  
		Last Modified: Mon, 08 Sep 2025 22:36:48 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f57a25f0033e9fec2f528ce1b0feaa7cc80f82f5ec852f9bd813305b271d69`  
		Last Modified: Mon, 08 Sep 2025 22:36:51 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b5f010b69ffe1abbc44878c2d0e0d412a1d3600744a975094d3b51f9763b6b`  
		Last Modified: Mon, 08 Sep 2025 22:36:48 GMT  
		Size: 1.4 MB (1405618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b99e5eda0aae4bb650e296df273aaa9ec6ce1f66b8be5a97c90faccdb08bbac`  
		Last Modified: Tue, 09 Sep 2025 01:11:20 GMT  
		Size: 14.7 MB (14718584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ed6786d2355549224dd930a6b2daba5c2e32f35c77cca5cbaa82d3758cf63a`  
		Last Modified: Mon, 08 Sep 2025 22:36:48 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93d47f4da8c65c8ed1eb03f5575ffd5ff9d6d25576b8e915f3bbb436c50c2eb`  
		Last Modified: Mon, 08 Sep 2025 22:36:48 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:36754220920c34fb83e96f4940001f5db0880dc7f8266aa278a9195acd93ef23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2414737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56660fca6253cbc53366f8cce2a5edd105575c55fa790d437399c99bc841e111`

```dockerfile
```

-	Layers:
	-	`sha256:d0c4e95e017d80e13b0d3bb7357c6198bf0b18101dbb1bec651d94faa045430e`  
		Last Modified: Tue, 09 Sep 2025 01:05:03 GMT  
		Size: 2.4 MB (2378835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e07d36e3bd0a2d40e8570c24fab3045b9b1791f07edcbbe3fc1fb4ddb80a5f5`  
		Last Modified: Tue, 09 Sep 2025 01:05:04 GMT  
		Size: 35.9 KB (35902 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:d52ccf7305e6dd9cff0b47f93eb3586d6179b5e126e24729697cc624371cfa09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44816095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a385a351ffab3dd567bf16b80b822cd8a38208f7a0fdcba87c0b9694843c92b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sun, 06 Jul 2025 16:51:58 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV GOSU_VERSION=1.17
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_VERSION=7.4.5
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.5.tar.gz
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_SHA=00bb280528f5d7934bec8ab309b8125088c209131e10609cb1563b91365633bb
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
VOLUME [/data]
# Sun, 06 Jul 2025 16:51:58 GMT
WORKDIR /data
# Sun, 06 Jul 2025 16:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 06 Jul 2025 16:51:58 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 06 Jul 2025 16:51:58 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0490ce7da6f84f8a4a1fb2c763f8d582fcd5dc1e7fc4c1bb7c65a3567b53fb68`  
		Last Modified: Mon, 08 Sep 2025 22:04:39 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362cab1f9007384fad43811398384fe9afb299b5da86df10c6628a55e9ac66ac`  
		Last Modified: Mon, 08 Sep 2025 22:04:39 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f3601f663754e00d34bd8385f71b008cafc8190dccae844973ad195c9ccca5`  
		Last Modified: Mon, 08 Sep 2025 22:04:41 GMT  
		Size: 1.4 MB (1369518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e6dfd62e9384a72b0cbec22e90613d015129b1c797e03402fcec10e3453cb`  
		Last Modified: Mon, 08 Sep 2025 22:04:42 GMT  
		Size: 15.3 MB (15341804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f7e42359fcb61ee1755b054f4ea1cd080c7d5a9437433d580ea1b86ebaa0ab`  
		Last Modified: Mon, 08 Sep 2025 22:04:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9496266a78f1c0fd913b3f924810d59895aac2f904e4cffd14b8487656cb1ac`  
		Last Modified: Mon, 08 Sep 2025 22:04:43 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:b9ac65c444ae3d818295bbfdf1f357103d8b098bf1e23d6ce57b739c7ac3dc1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2412820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacbd9741d300000ce5ef086b7e99cc70399bc58640757da802fcc4d926a2fb8`

```dockerfile
```

-	Layers:
	-	`sha256:597943aa9a2d683e2ec71f04fc4a8cf6b460c420cf9a89160a22b333b40871a5`  
		Last Modified: Mon, 08 Sep 2025 22:05:14 GMT  
		Size: 2.4 MB (2376879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:183a91a4ecb52eb6ff243e4adedbc3dce201d1778af1fe00cd0118bc3b0c742f`  
		Last Modified: Mon, 08 Sep 2025 22:05:16 GMT  
		Size: 35.9 KB (35941 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; 386

```console
$ docker pull redis@sha256:2f6c79ffd4bc838954ce6bc97e48389e5e389af8c498f8edee106bd2c840d3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45489230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1daf437797b34d271a0e3abedabd9b897a4fdfac54cec7eebbb53c9c1ba8db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sun, 06 Jul 2025 16:51:58 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV GOSU_VERSION=1.17
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_VERSION=7.4.5
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.5.tar.gz
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_SHA=00bb280528f5d7934bec8ab309b8125088c209131e10609cb1563b91365633bb
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
VOLUME [/data]
# Sun, 06 Jul 2025 16:51:58 GMT
WORKDIR /data
# Sun, 06 Jul 2025 16:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 06 Jul 2025 16:51:58 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 06 Jul 2025 16:51:58 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:dc2a09b0db8b98044474925cacc9c009aa76e5883edf644cc36c3f6a2e3917ac`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 29.2 MB (29209634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b0d20a7e8aeac3b4cfa105398001cd3b00c750bc8a67e217f07d493a8d391d`  
		Last Modified: Mon, 08 Sep 2025 21:42:44 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d650e380c752be103464829da2ca98fb7cade425b941b533421c61c163d9294`  
		Last Modified: Mon, 08 Sep 2025 21:42:49 GMT  
		Size: 872.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d67b7912198dd55dd530a1474357bf05aed84bf60a07216e5682d720c56bf3`  
		Last Modified: Mon, 08 Sep 2025 21:42:52 GMT  
		Size: 1.4 MB (1413320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731da73eb143349b3603d29973ac3623e30d66453ff1012adac3a8c5cf04ff1b`  
		Last Modified: Mon, 08 Sep 2025 22:10:47 GMT  
		Size: 14.9 MB (14863605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd8d54fdfd679eaf8f66ac50e6b20af48614579877c9908f5397aab3c35134a`  
		Last Modified: Mon, 08 Sep 2025 21:42:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a375787d5a7c69899cf2e43b6b5379061115be864eb8f9860e87b04ea5aa2c`  
		Last Modified: Mon, 08 Sep 2025 21:43:01 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:334eac93bc0ae82252ff70435de692d8a75231b09d172aa9699d13bcaeb939df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2409473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141ab1c0db3e968b79fc29bed368384b5be73eac535e06f47b104edfb7e31fb2`

```dockerfile
```

-	Layers:
	-	`sha256:c1e736d016dd1491c11af97ce5c3e391f19ec400eb6ec63066cdd4b0587843c7`  
		Last Modified: Mon, 08 Sep 2025 22:05:20 GMT  
		Size: 2.4 MB (2373771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31ec28397cda0f40c48858b40638540c19ba296ca662484e123b273b637493e`  
		Last Modified: Mon, 08 Sep 2025 22:05:21 GMT  
		Size: 35.7 KB (35702 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; mips64le

```console
$ docker pull redis@sha256:8daca62da6d56aeae618270dd641fba98ecf1a465dd29639d81cc9d549b4e84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45268964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8327d13025f33abb53d2abd6f61e60e379e87bb63b3a7c4f7cec9cf9d8e3e79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sun, 06 Jul 2025 16:51:58 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1757289600'
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV GOSU_VERSION=1.17
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_VERSION=7.4.5
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.5.tar.gz
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_SHA=00bb280528f5d7934bec8ab309b8125088c209131e10609cb1563b91365633bb
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
VOLUME [/data]
# Sun, 06 Jul 2025 16:51:58 GMT
WORKDIR /data
# Sun, 06 Jul 2025 16:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 06 Jul 2025 16:51:58 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 06 Jul 2025 16:51:58 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:e312b85a00d79bdd7bd2503e855c13252d47980761b762b04df3d1399e2e3efa`  
		Last Modified: Mon, 08 Sep 2025 21:17:36 GMT  
		Size: 28.5 MB (28513643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d0f59871ead32d3b08eaab20936354fba295eef6095d4cad3eb85bba1da811`  
		Last Modified: Tue, 09 Sep 2025 04:01:00 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf199c63641024745a8ddc4438bdcb52af4bccb3eb28424bc18378b515e1228`  
		Last Modified: Tue, 09 Sep 2025 04:01:03 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6f6577429cad053478c56fef94f9bba7df653746c6401b717ae2f1488790d3`  
		Last Modified: Tue, 09 Sep 2025 04:01:08 GMT  
		Size: 1.3 MB (1325530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b505b9f9d1b0e22e108f59d16c0c87b7b18d11e66b5b7a22680ad06d3cbde84`  
		Last Modified: Tue, 09 Sep 2025 04:36:23 GMT  
		Size: 15.4 MB (15427108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554e9a446bd02320a0001457f2b8112235b22de6e5070d831a34d710fa8dfc2f`  
		Last Modified: Tue, 09 Sep 2025 04:27:08 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704f91eed8b228eaf25e497d4d962f33b594d3e5ade175ee5cbaadaf6e27efec`  
		Last Modified: Tue, 09 Sep 2025 04:27:09 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:f4effc0dd6d7b74c5fd88fe511f527b2fb4b0070296e7283d5ae0a4d8f2381dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72906253000ffcf55fcbe4b9fee28b8a04bdd785efc555289f9d091beb23b31a`

```dockerfile
```

-	Layers:
	-	`sha256:5af22fb856444dc0958f8e740bf7a3f3dc1d17c86987cd6e1abbce4cf6550ec6`  
		Last Modified: Tue, 09 Sep 2025 07:05:02 GMT  
		Size: 35.6 KB (35634 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; ppc64le

```console
$ docker pull redis@sha256:659c6c2b1bf9668d7696f6fb307984008ce968f1e476411ba4ad1a46b8c35b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49935323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a42efe7d0aae9bb2e566c646229171fab93542c736e1af0259b61fc5584566`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sun, 06 Jul 2025 16:51:58 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV GOSU_VERSION=1.17
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_VERSION=7.4.5
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.5.tar.gz
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_SHA=00bb280528f5d7934bec8ab309b8125088c209131e10609cb1563b91365633bb
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
VOLUME [/data]
# Sun, 06 Jul 2025 16:51:58 GMT
WORKDIR /data
# Sun, 06 Jul 2025 16:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 06 Jul 2025 16:51:58 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 06 Jul 2025 16:51:58 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8448e59bbf0bb72a995423025b9f4a7ba0053f4de865815d5cf3cfb23f401f3a`  
		Last Modified: Tue, 09 Sep 2025 02:13:54 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e705d20a114aa0819bc16091b90c60fe44d9bb8ffcaae34faf2f20754f1567d`  
		Last Modified: Tue, 09 Sep 2025 02:13:54 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ce139edc595aa48358594cdccf222f4a7ccb2b84e51cd7a58d7049f4abf96`  
		Last Modified: Tue, 09 Sep 2025 02:16:03 GMT  
		Size: 1.4 MB (1360215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d8ad4d509c1b42eee40f52cd80cb9a2ea3ccd061b49a4ef87949ebd528125b`  
		Last Modified: Tue, 09 Sep 2025 02:16:10 GMT  
		Size: 16.5 MB (16503672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de37734986156061650275f9bd6d0b7eb93339e974bc91eb79ee4acb953e1954`  
		Last Modified: Tue, 09 Sep 2025 02:16:04 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa5657e322b6e36a8fed590f10ff4481c6fd4af180600436438e4d23b6b1d49`  
		Last Modified: Tue, 09 Sep 2025 02:16:06 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:f358f2179dea85a18cc74b2f7d3b4dbc13cc23f18c905e9ced222b04ddc63155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c17e888aa16463fc3a0ea1cff77703a39759507b512765216d864d4cd421112`

```dockerfile
```

-	Layers:
	-	`sha256:fe8e6d288e320f4bc982d9c86770b07f89226013bdac162e644028ae3b966092`  
		Last Modified: Tue, 09 Sep 2025 04:05:08 GMT  
		Size: 2.4 MB (2380992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31627339d55fa29ac0d2ac60441efce1c3fd5554ceb3a78bbe2e38754126594a`  
		Last Modified: Tue, 09 Sep 2025 04:05:09 GMT  
		Size: 35.8 KB (35818 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; s390x

```console
$ docker pull redis@sha256:80d97cfc1c551ce907e2d90ae647aacf16c17383cc5bb5ce2477791fcdae2c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43667515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afd49f4806982eeb0dc2b79c4d3cc751742da79185f00db36c125cd5a077014`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Sun, 06 Jul 2025 16:51:58 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV GOSU_VERSION=1.17
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_VERSION=7.4.5
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.5.tar.gz
# Sun, 06 Jul 2025 16:51:58 GMT
ENV REDIS_DOWNLOAD_SHA=00bb280528f5d7934bec8ab309b8125088c209131e10609cb1563b91365633bb
# Sun, 06 Jul 2025 16:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
VOLUME [/data]
# Sun, 06 Jul 2025 16:51:58 GMT
WORKDIR /data
# Sun, 06 Jul 2025 16:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 06 Jul 2025 16:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 06 Jul 2025 16:51:58 GMT
EXPOSE map[6379/tcp:{}]
# Sun, 06 Jul 2025 16:51:58 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302c7f71e2643dd956dd5e36dd2da89d65cbf9081d8bf41b11137cff25e99da5`  
		Last Modified: Tue, 09 Sep 2025 00:21:54 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c252f5e914f7342632b731555ffb48b4217920a3165804125365c7b6e1e0bcc`  
		Last Modified: Tue, 09 Sep 2025 00:22:01 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d660a449f195f0a79ed0900fd103bf76b9be3c0c357bb40ea356c4ce5c2fdb06`  
		Last Modified: Tue, 09 Sep 2025 00:22:07 GMT  
		Size: 1.4 MB (1403222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f054c230fb35642e87fcfef5a05ec0da70de0dd7a7515b8458814931fdfd1a`  
		Last Modified: Tue, 09 Sep 2025 04:07:03 GMT  
		Size: 15.4 MB (15377323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699f24acfdfcef754525dda85a7134e459fc2c87ae7059427ca8c34305dd60a6`  
		Last Modified: Tue, 09 Sep 2025 00:45:00 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e201d6d52259cdac6bfbde31361677dc29e85181609300ebf743f87f3748fcb1`  
		Last Modified: Tue, 09 Sep 2025 00:45:00 GMT  
		Size: 568.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:062993e2d6c570a3d3901372b7103a65961a481a5ce26e1869cba4424a9bc2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2409184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc68f542195097956c20c5c1948c667caf7e95031325075d0ffdce8bf0fca470`

```dockerfile
```

-	Layers:
	-	`sha256:bfe08d1f899c31c9bc58522933fa57ab55d1abd917e6ce204511cca940f25c79`  
		Last Modified: Tue, 09 Sep 2025 04:05:13 GMT  
		Size: 2.4 MB (2373430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8e0c24c45f5829fb563371b0a79eff1f555a4cf3cfa78ea84fcb4b682231e7`  
		Last Modified: Tue, 09 Sep 2025 04:05:14 GMT  
		Size: 35.8 KB (35754 bytes)  
		MIME: application/vnd.in-toto+json
