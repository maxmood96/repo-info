## `redis:latest`

```console
$ docker pull redis@sha256:82d08ad50c181182ee5ce23dcefd754a12f946534af57959ba08490e1d0696a0
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

### `redis:latest` - linux; amd64

```console
$ docker pull redis@sha256:0b2216cb86345d3ece3696ded9ae59ddf1c65a9e8d48188db1784f1a1f95b448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45883627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e49ed81b42baf75651be228e537c5495ab66cf1633f89a3703fdfe5d2df779a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0249d9189da6b30b61d990460de543a0464927fe2e4b1b862a9824d3f51a7b`  
		Last Modified: Fri, 27 Sep 2024 06:04:50 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4825c5e958150faef3f35f8e908327605055610572417a2d82c7feea127e37c7`  
		Last Modified: Fri, 27 Sep 2024 06:04:50 GMT  
		Size: 872.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ce50685fa23fc9d10b032933f2ee373f61996c7549761ed2a01fec3b8a6911`  
		Last Modified: Fri, 27 Sep 2024 06:04:50 GMT  
		Size: 1.4 MB (1437796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455886c7d31bf1ee5a8ebaa9bfc23791a00bdaea4b70dc1a031eb274d6441ea2`  
		Last Modified: Fri, 27 Sep 2024 06:04:51 GMT  
		Size: 15.3 MB (15316881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96377887d47643fdedd9a451ea4114f2b6312d0de4d5a6f7c8bb62bedffbf0b1`  
		Last Modified: Fri, 27 Sep 2024 06:04:51 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fac73c23c9ba7b5ee2a1269891ee089dfb0c43dd3889e295cb3c76f5883a9a4`  
		Last Modified: Fri, 27 Sep 2024 06:04:51 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:8f9cb6a6a7f4bf1f8ef3d78d0aebf9dcde7c2a276bf1f6f2f6b035b5c66100c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2293689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087b7545883d273907c33cb029f0d40d14ba826a8b0b44f35efb85224095c2da`

```dockerfile
```

-	Layers:
	-	`sha256:9c04cb318d296d397cc11e51822a7cdcbe33af81433d9d90a3487ae8538aba1b`  
		Last Modified: Fri, 27 Sep 2024 06:04:51 GMT  
		Size: 2.3 MB (2257522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:211840385a1de59f47c4d8fe50da4a7471e776790d329c926573aed8500e68cc`  
		Last Modified: Fri, 27 Sep 2024 06:04:50 GMT  
		Size: 36.2 KB (36167 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm variant v5

```console
$ docker pull redis@sha256:fbfab65ed1646994ef8488669d407f6a63aa08b1621adf4c5014d03f26463661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43343739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42869c976fc72ae6397dc0cc16d99a98fca4b1c3e2d161f243e8292b7d5b7661`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e00e26c399758469504bc526b6228808d62d07f6a5d20d261a24fcdce1625f`  
		Last Modified: Thu, 05 Sep 2024 10:43:34 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074f6f1ac3b0206c316f8ce6e2666d671599a04e3cf74b5321292a0cd73f316c`  
		Last Modified: Thu, 05 Sep 2024 10:43:34 GMT  
		Size: 872.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcab59160d4b238a3f1ed46055a3fd873f706ed7613308bb9462c67995706bd`  
		Last Modified: Thu, 05 Sep 2024 10:43:34 GMT  
		Size: 1.4 MB (1414240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8d2cdc615fc72ea539e048b661612ea503b9db3fb5d03d96bf71bfb8807f02`  
		Last Modified: Thu, 05 Sep 2024 10:43:35 GMT  
		Size: 15.0 MB (15039413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4488b44ee8ed8c732927688db7a6d7d5fdf3cc2dc817a9a630948b2ee9de2dd`  
		Last Modified: Thu, 05 Sep 2024 10:43:35 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0504bb69ccdf52d4a3c9ea31fc84bf08c98c343fa68bf2344eeafbfb8aad86e`  
		Last Modified: Thu, 05 Sep 2024 10:43:35 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:9b7f22511cfc65c4bef922349e4db38aab876caa032644149cec35d38675657c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4449058f6077965ee4ad94d30ce9f0078b1add75df64def87be4ae7bff3921`

```dockerfile
```

-	Layers:
	-	`sha256:396fbd798e2a08b0443651099c55af9eb261b3cfa71e1767a14be9dd4103a849`  
		Last Modified: Thu, 05 Sep 2024 10:43:34 GMT  
		Size: 2.3 MB (2259843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61016d229ac60387b726f5575c3fde19ed2eece8488f53dc9ff1c243c426b27d`  
		Last Modified: Thu, 05 Sep 2024 10:43:34 GMT  
		Size: 36.3 KB (36322 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm variant v7

```console
$ docker pull redis@sha256:e01d38790c5e0ff34b3760a9dd0dc54a6508c4c746c0066b2252290497401c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40828702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb4f30b6b953a3b4ec900685977d1574ac0d036472564944d41a9eb0db700ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda9c52fe25861b8269e8b67ea3df32cdd87f557b1e4472e7e04d686f5b38553`  
		Last Modified: Thu, 05 Sep 2024 11:41:38 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036636061be413be106af0c286fecfb0cbce9b151c33f16958c588aa1fe4f232`  
		Last Modified: Thu, 05 Sep 2024 11:41:38 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a7d2433a8cd07a6328f8d110defe79122f74a7076ae94bbde88658374c4b0`  
		Last Modified: Thu, 05 Sep 2024 11:41:39 GMT  
		Size: 1.4 MB (1405380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a33048d9a1ee7311c1167947d03ba90cc4100952b619f111c3f4a9fdca29676`  
		Last Modified: Thu, 05 Sep 2024 11:41:39 GMT  
		Size: 14.7 MB (14702381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b91a5240a799b0419a0a851499e8d34e4dc5a38c9e87bb7d3253bf915ea2f28`  
		Last Modified: Thu, 05 Sep 2024 11:41:39 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9191e2229527205fe423e00b55e4bb05dae66217e07d1b50b0a5d0bed0eb216`  
		Last Modified: Thu, 05 Sep 2024 11:41:39 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:1638cddb34080ab5fa9fc9fcba0c91e8d401272857092b8f6f605c244086400a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa93081fb7b1dbe4858ea6499a61eb086c1bbb577e1010ef138b6425b023bb5`

```dockerfile
```

-	Layers:
	-	`sha256:8d5b0a46cd2618470089842a0a6ccaaceafbb5b66b37fc77d1a75e8f1c22e07c`  
		Last Modified: Thu, 05 Sep 2024 11:41:39 GMT  
		Size: 2.3 MB (2258674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c185d1eb1dcc94e3c6f64eb70c481b45143bed261cffc72b4171fdaf3081d9fe`  
		Last Modified: Thu, 05 Sep 2024 11:41:38 GMT  
		Size: 36.3 KB (36322 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:be82842d40189839724d2f9827b7cd1987bd26a07137466144a9a47ff968bec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45845568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fba7e5fadd5fc42b7aaf71b85f2b1de951fc870f97d0d64e5eb06243be7c79a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631720f833ee3e86218d50c6e7c3b28232cfcbda97a9f82064e83ad610df72aa`  
		Last Modified: Thu, 05 Sep 2024 19:18:49 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704a08909867fa18bd96eb65315c874647a380700717b7ebf31f7491f0ffbdd4`  
		Last Modified: Thu, 05 Sep 2024 19:18:49 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090311ee98f0cda0e26a98af3522b45fe00424377467ef6a355c5ca1843964a0`  
		Last Modified: Thu, 05 Sep 2024 19:18:49 GMT  
		Size: 1.4 MB (1369421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50eb2e3e87d65fde641db2a78c7890c01a3c45a8f3aaf908a1717130f6cbf33c`  
		Last Modified: Thu, 05 Sep 2024 19:18:50 GMT  
		Size: 15.3 MB (15316929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a05d8378bf09344ab2c10e58b896d3ca2d779bfc6f21cfb18932bedf8205fee`  
		Last Modified: Thu, 05 Sep 2024 19:18:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713e6192e133b403ef083cc509863bd80ff2b2811dacb30ad7a4a436b85ad84d`  
		Last Modified: Thu, 05 Sep 2024 19:18:50 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:28a57aa32e38050fb51e0096e608cb5fd91a701deb81480fe8687f73032694a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bf813b068f6d245ba0e122fe2dfa5f4d46de1d7972450a2973f2559b374431`

```dockerfile
```

-	Layers:
	-	`sha256:ca44f5ac94c8d6bcc1b966562d07c8a78c643cb3c58fd938338d26e8b4d1493e`  
		Last Modified: Thu, 05 Sep 2024 19:18:49 GMT  
		Size: 2.3 MB (2257813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8805ae6661cf55b88671860229e012136d94e9420d351f8d72492ff80a69522`  
		Last Modified: Thu, 05 Sep 2024 19:18:49 GMT  
		Size: 36.5 KB (36523 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; 386

```console
$ docker pull redis@sha256:94f521337b4630b519a4dbdf6c8f25fcd27a3508796e393738189f51da98d3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46400341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa07c36119d240d2f0ef4dddae5df05c9e7702b815e080f439ed0016cd8171a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1fe3f7e6a33b897b04d4f3598b7f4523b88a2c321e5de3e8d10265aa011e1c`  
		Last Modified: Fri, 27 Sep 2024 09:09:55 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446f5441f497b9c6cc007f3fa051dc6cf58f524e4e6ed50cc0d7722d30838bd5`  
		Last Modified: Fri, 27 Sep 2024 09:09:55 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db35cf68c2e3e3aedbe1d30267d932a1dbe1637cd29d71fa0b40d3a4b8771a1`  
		Last Modified: Fri, 27 Sep 2024 09:09:55 GMT  
		Size: 1.4 MB (1413160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5f68f3d65a13edbddd7b27100144abf56ed9a7f62751640b33244a1a230f0b`  
		Last Modified: Fri, 27 Sep 2024 09:09:55 GMT  
		Size: 14.8 MB (14840292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9555fa53d5ddff4838bd59514a72004377fb758cbf5ca39d1c78925a839c4fb3`  
		Last Modified: Fri, 27 Sep 2024 09:09:55 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149f5892486ef9aa4cc359a360ed90c6f22ea3b86cb21a4d98a9c1101ebb60f`  
		Last Modified: Fri, 27 Sep 2024 09:09:56 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:83be5b29663ead5224cfb93a90e3570a98daaae2fd50eee80f5f48d83b88b41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14733b6c470700e8bd151c49664e6d118aa04ef5da8e3e468efeb86c4817a6de`

```dockerfile
```

-	Layers:
	-	`sha256:a43df7a8b8a182f5ce6469553346c7e2ed23a04e81351826eec790af1d8eb9dc`  
		Last Modified: Fri, 27 Sep 2024 09:09:55 GMT  
		Size: 2.3 MB (2253557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d00076609fb19a6be5d659d772393bf37e8d1f6e0007feb1f334014591f8125`  
		Last Modified: Fri, 27 Sep 2024 09:09:55 GMT  
		Size: 36.1 KB (36111 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; mips64le

```console
$ docker pull redis@sha256:ba051adeff5724d1f09da0d0a1c42bb51f758ab997ce0a1eee866ee5ddc101af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45862605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8657dd2c8e1c0f4b2286a2a02d9f53d422167daab0ab5d8102545d70145826`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78ded6aacc18ba1e115ee4a957989a30bc1ff29324ae6cea4ea329b8f4cf32f`  
		Last Modified: Thu, 05 Sep 2024 22:04:18 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a2f49c8aff2cbacc720b8dc64c32f2f9e7e12062ceb2e5c1af4679f321ec24`  
		Last Modified: Thu, 05 Sep 2024 22:04:18 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bd0e997223e54e28eab87e64e1b810dad18c18be475ebdc5040dd0c128407f`  
		Last Modified: Thu, 05 Sep 2024 22:04:19 GMT  
		Size: 1.3 MB (1325350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ab946a486656145b455fb23dc78b4a54ab0fe2b09d54fc4e6817e35e2ba520`  
		Last Modified: Thu, 05 Sep 2024 22:04:20 GMT  
		Size: 15.4 MB (15409522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118a350c0c3f4cf9ecf8f7041acf84ba5d82bf873e3cc5c206be44cea6b0e5c3`  
		Last Modified: Thu, 05 Sep 2024 22:04:19 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fdfd6b1bdacf3d2ad6b5bb7ebbdab258bc18ffa3d6e5d44466a276f0a2c56a`  
		Last Modified: Thu, 05 Sep 2024 22:04:19 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:307059f2cdb910de6321db9f2a21fefdb18af3b121317e1a426991fbc9222c62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 KB (36054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e7027dd72cb8bcca079640085f99cd8b9563ed1dc606718af7a1fb5998616e`

```dockerfile
```

-	Layers:
	-	`sha256:44652d45b15c7dd5a718b4863cbf38c43400b1640da916866bb9284cf8696a42`  
		Last Modified: Thu, 05 Sep 2024 22:04:18 GMT  
		Size: 36.1 KB (36054 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; ppc64le

```console
$ docker pull redis@sha256:987714ab3e6d513dce560197c6f37ebcb6e2639c7c5ee56d4e176dcfa77f26a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50967712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df7d828cc799a278a0cb00a33fbba042dfb5f66b4e22d64eb7061ba1290e365`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43de23ba6070456e84887b4fab96ab4b17d0e9fc944080d16b066c58ed4c9675`  
		Last Modified: Thu, 05 Sep 2024 05:43:56 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c2632ef5aecfd0b1145b0cae265f9490d1754a12be0b88c9b1e1c7f81671ba`  
		Last Modified: Thu, 05 Sep 2024 05:43:56 GMT  
		Size: 872.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892e4c2993eb9a15d0d4ffd9d3bc484bc21a83be69f2ca466fb0bf7ec0f2fd2a`  
		Last Modified: Thu, 05 Sep 2024 05:43:56 GMT  
		Size: 1.4 MB (1360018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263403fce3c05fce6f992bc3fd99239ff8dfafaff3af63bb65dd383761a866ea`  
		Last Modified: Thu, 05 Sep 2024 05:43:57 GMT  
		Size: 16.5 MB (16482663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b942d8f0347b5654a54af52429eb79dd318524ec249e2693a226f683ef3971`  
		Last Modified: Thu, 05 Sep 2024 05:43:56 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b0140d0974da5748bce43f9b8e5440eba76bcee2af690cc769d5e820ca4afc`  
		Last Modified: Thu, 05 Sep 2024 05:43:57 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:5bda2914d56c4508ec10478e48c6411fde246f594c540e171ee87762810abc4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c26616808f52279df8612860fd566c1b3097169fbc380bce089533121e5ae6`

```dockerfile
```

-	Layers:
	-	`sha256:f391895cac8c74afadb78cef28697d3d6935ddacb0c0f7b1dc26181f4f578bd0`  
		Last Modified: Thu, 05 Sep 2024 05:43:56 GMT  
		Size: 2.3 MB (2261822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0c754d062dc916f8585fccb6a31c1a21b9edb061a006c7df62671dc987b5b86`  
		Last Modified: Thu, 05 Sep 2024 05:43:55 GMT  
		Size: 36.2 KB (36238 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; s390x

```console
$ docker pull redis@sha256:4cf747216bc56dfdd9dea7f4f57ea808168e1cef52d0636180fb754c97958113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44249416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f22fff765caea15bd505eac730eea0891ed51f897a29020eaa1d4299d2694e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["bash"]
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_VERSION=7.4.0
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.0.tar.gz
# Mon, 29 Jul 2024 07:59:06 GMT
ENV REDIS_DOWNLOAD_SHA=57b47c2c6682636d697dbf5d66d8d495b4e653afc9cd32b7adf9da3e433b8aaf
# Mon, 29 Jul 2024 07:59:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
VOLUME [/data]
# Mon, 29 Jul 2024 07:59:06 GMT
WORKDIR /data
# Mon, 29 Jul 2024 07:59:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Jul 2024 07:59:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jul 2024 07:59:06 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 29 Jul 2024 07:59:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22bf7237fb996f8a40ffec5c53d9a935ede86bc3a8bea62f64efe42159438e3`  
		Last Modified: Thu, 05 Sep 2024 06:42:09 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fc0f8bda0f03143a078161df9fe8c60bbfafb09b9b3467fbe123f42239ccf1`  
		Last Modified: Thu, 05 Sep 2024 06:42:09 GMT  
		Size: 871.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b27a885264a8ef4df2d1239e7f6afd1f011905b27a875eaf83c9e3bd71fb0c`  
		Last Modified: Thu, 05 Sep 2024 06:42:09 GMT  
		Size: 1.4 MB (1403051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3076d4bdd1b4a703481e9461d62aa0c7773e7c7ddeff15f323ccdd8eb03c130c`  
		Last Modified: Thu, 05 Sep 2024 06:42:10 GMT  
		Size: 15.4 MB (15353373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9538c0f6994230fb48435ad60afba85d036f405da02a7ea29c0433788864f9a0`  
		Last Modified: Thu, 05 Sep 2024 06:42:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82019d7d6a6743b9fefdf01c1f33af62913d7b475aad6fc7614a691439fa93c0`  
		Last Modified: Thu, 05 Sep 2024 06:42:10 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:f72a257459ea0c09daf6dfcdfd3312e38f8dea1cf0355826c82e3b4b83a863eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2293508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ccbd20af76be0340037cf51a85cd1c6f67ae0e8faf2689fce38a6f1267e4f31`

```dockerfile
```

-	Layers:
	-	`sha256:c2447fbfb4c05dd2d4727cd88da9b0e954c734ff2f1b0757ec03b1213f770e6b`  
		Last Modified: Thu, 05 Sep 2024 06:42:09 GMT  
		Size: 2.3 MB (2257340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff40fc811e18cc19c3f180e1994102025918f8e6c8d88b78fe0af565b5db964`  
		Last Modified: Thu, 05 Sep 2024 06:42:09 GMT  
		Size: 36.2 KB (36168 bytes)  
		MIME: application/vnd.in-toto+json
