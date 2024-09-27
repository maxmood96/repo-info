## `redis:7-bookworm`

```console
$ docker pull redis@sha256:c584cf188f7cef85b96a93241d12419bc0476dbff3a27360a92bb9ade336f560
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

### `redis:7-bookworm` - unknown; unknown

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

### `redis:7-bookworm` - linux; arm variant v5

```console
$ docker pull redis@sha256:5f066da015ff80ff747c5e70b51b53acf98ada783caed0cde90f212903bb4c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43343661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4fdeedd9a25796b6f361233c4a435858e25bf46580309c72afed5ae9d4995e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
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
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cb3ebc81b94bd5bb52e3e7856da76f5497649037d61b7b437f59ecf2d2eee5`  
		Last Modified: Fri, 27 Sep 2024 16:04:33 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a52ee9a4bef6029e51d9831ed8fc8128f166c932281d1e93b50941abd3bd80f`  
		Last Modified: Fri, 27 Sep 2024 16:04:33 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1260e29e3a198bc8bb9a2a738ef1e65dbd8958aeecd2c188f4b20320a53635`  
		Last Modified: Fri, 27 Sep 2024 16:04:34 GMT  
		Size: 1.4 MB (1414250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262e4e1180866e910f46a883cf6e28feab7d0a9e618c74ebc619aca3d4155ff6`  
		Last Modified: Fri, 27 Sep 2024 16:05:57 GMT  
		Size: 15.0 MB (15039434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6ecffbe1d5d3d4ba429fc29fac43b5b536508861f1eb48a8f5c2dae582f373`  
		Last Modified: Fri, 27 Sep 2024 16:05:57 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cdba17b3aafee29913fdce160ec53fbea7204d35b262373d59b154f8f27b48`  
		Last Modified: Fri, 27 Sep 2024 16:05:57 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:33373ec2f75ff24cdb9a76b413c539706971b416230fe6c346e5fa537d3bf467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f28fdeecfde2c7f925f87975908a4ec8af63a66625cfb15c82c305f3f4b1d4`

```dockerfile
```

-	Layers:
	-	`sha256:dffd7db64c80287c2b6e666f56a8713ba9e022f33712e4583717c177b6b05133`  
		Last Modified: Fri, 27 Sep 2024 16:05:57 GMT  
		Size: 2.3 MB (2259856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cae8501c79c2ebac647f8b8e6f1c1f34adbd77b895f6ecb9af1669c7c100b634`  
		Last Modified: Fri, 27 Sep 2024 16:05:56 GMT  
		Size: 36.3 KB (36322 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; arm variant v7

```console
$ docker pull redis@sha256:e1951829e4a3f81966685d5024be6cdb3643b906822903cc2f39431f045992cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40828566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae022b900b95d8f010466d1ea0e41794c20f820fe1085568a575c9bd80266d8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59dbdc3c8ce4afb1df6a8958641fe3ddc3d2f2bad4c2bc546988abcb142626f7`  
		Last Modified: Fri, 27 Sep 2024 18:11:09 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bb0320eac2ab8a8cb5925ce27303157f445f9057c92364fc2f0f2e0f2a1838`  
		Last Modified: Fri, 27 Sep 2024 18:11:09 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014853e78292929f9cb901fec90cdb7c8ee749753025a242a41e36ecb4c7185a`  
		Last Modified: Fri, 27 Sep 2024 18:11:10 GMT  
		Size: 1.4 MB (1405365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362ac3d389073b836b8fa5feffb60f97a9a0bad301c9cba96bba6024233b273b`  
		Last Modified: Fri, 27 Sep 2024 18:12:28 GMT  
		Size: 14.7 MB (14702383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93d363ffde545460d85f2cbe4616d7357f596a697f5aab68fa356c69fdfb5c`  
		Last Modified: Fri, 27 Sep 2024 18:12:28 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a97acb07a0c0d258106da0c04930a51455994c42bcfbeb1d87093e7262d262`  
		Last Modified: Fri, 27 Sep 2024 18:12:28 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:ab172e7aa3a7142b6a8fdff971c97853a5b3ceff0c7e83d9ddc93d13c1ed41db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e43be130a730f97f17f12eb274f1ecfd3f2a4b72670a508e53f4011ec562745`

```dockerfile
```

-	Layers:
	-	`sha256:835ab6955404c2bb2fb28c938558215dcfc0ab8ac3422e5fd6e22448bd6bac3b`  
		Last Modified: Fri, 27 Sep 2024 18:12:28 GMT  
		Size: 2.3 MB (2258687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc6b41facc46e458f2aeff442851d2f09f7429ca1ea5c136e9144472cb14eeaf`  
		Last Modified: Fri, 27 Sep 2024 18:12:27 GMT  
		Size: 36.3 KB (36322 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:7-bookworm` - linux; arm64 variant v8

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

### `redis:7-bookworm` - unknown; unknown

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

### `redis:7-bookworm` - linux; 386

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

### `redis:7-bookworm` - unknown; unknown

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

### `redis:7-bookworm` - linux; mips64le

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

### `redis:7-bookworm` - unknown; unknown

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

### `redis:7-bookworm` - linux; ppc64le

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

### `redis:7-bookworm` - unknown; unknown

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

### `redis:7-bookworm` - linux; s390x

```console
$ docker pull redis@sha256:25727e0c8c09a3788b7a851100dda97021a42a9a94e121d739c81ebb1cf0d9a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44249048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c823cd918a8822e00de44b26991357b926cd3474be2bafcc66968fc6b71a8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 29 Jul 2024 07:59:06 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae8b5f63d4b2d87b49cc68d7cb56160f0c12ac26c58ba75afa80ebb50034847`  
		Last Modified: Fri, 27 Sep 2024 17:09:27 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b3e623750b2ddfd8ed24328a0a927afbb479d58ba0626783d07dcb6fca063`  
		Last Modified: Fri, 27 Sep 2024 17:09:27 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b885f0b76bb3cda2f1dbaaee2969e5610dce066e71eec2756ef0c49e76ec8d`  
		Last Modified: Fri, 27 Sep 2024 17:09:28 GMT  
		Size: 1.4 MB (1403032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f52f41f8bfee9d7b942da2b6775bd4c3ca634fc81a593f68b864c215dbe524`  
		Last Modified: Fri, 27 Sep 2024 17:10:55 GMT  
		Size: 15.4 MB (15353317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3199f43edf30dca71ae05193535bbbd935cc08820056fbc19737903e9edb80`  
		Last Modified: Fri, 27 Sep 2024 17:10:55 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9709dd1c3915fb19c657c0ebc5f0c95de28cff3e74e45d996e20c4e1072df52a`  
		Last Modified: Fri, 27 Sep 2024 17:10:55 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:7-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:75ca2f988a5612db472a4284933cea52d92783deed169a137f3c74e7b4c6bd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2293521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3781e0b849e90c6e4bebe0b7250901fe0a85de5bd6de826886e6b95582bc763`

```dockerfile
```

-	Layers:
	-	`sha256:420bad20146f93fc41aed68b281da5e695d20f97f107ce2683f948cbe5215aee`  
		Last Modified: Fri, 27 Sep 2024 17:10:55 GMT  
		Size: 2.3 MB (2257353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916a4291c4857a43c81f1c1ba85ae3783595d350d5c854355409d26434e6c77b`  
		Last Modified: Fri, 27 Sep 2024 17:10:55 GMT  
		Size: 36.2 KB (36168 bytes)  
		MIME: application/vnd.in-toto+json
