## `redis:6-bookworm`

```console
$ docker pull redis@sha256:d74db717c8b8a7be8e3cc949b4ad7cf4b87276ff2a47bb487ef0f5f05430c0f9
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

### `redis:6-bookworm` - linux; amd64

```console
$ docker pull redis@sha256:537490804ee56e77352eef77e7bee11ce7a4ef99beb34ba270fa22029991edf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40159872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028a4debc996fa0e7f6d0818aacf6a7272e1826d4cc7b8a6259497cda68d9b7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 04 Oct 2024 09:56:40 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4737acb22223ebdf5189d999959090cb87f7e69f71dc450704addd6874a7d3`  
		Last Modified: Tue, 24 Dec 2024 22:16:06 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2057648791c69168fd496e90528eb55ecf03a3ca76143c9cf99494355853637`  
		Last Modified: Tue, 24 Dec 2024 22:16:06 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6a22d00bc827020fa015c48fabcf42ceafe065baae4aa16c57590cd8c3d246`  
		Last Modified: Tue, 24 Dec 2024 22:16:06 GMT  
		Size: 1.4 MB (1437778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89f4e4eb843231c24e5d7bdf0a42b0d986a9bba8942251807239dc9bdac76d0`  
		Last Modified: Tue, 24 Dec 2024 22:16:06 GMT  
		Size: 10.5 MB (10487842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befe6f4e7e525c61cde4e29d8835ff7ee7c24f6b4b186f9fdfbf1679c2a72b3a`  
		Last Modified: Tue, 24 Dec 2024 22:16:07 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc355ab4192fca5caaa40963fd5f96ff9cd0594f1de4bc39c2ed6eebe6ba3cd`  
		Last Modified: Tue, 24 Dec 2024 22:16:07 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:12160aa7616ac15f3b668641bc2a55863d4f6a04fd30215394792fe9d8405773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33884cea54c8aaeabf6b2273b70f6d820c4d1ac4f5f2facb7467d43c69cb68a5`

```dockerfile
```

-	Layers:
	-	`sha256:9959d473fb40c9886e68c5914f0a2469c05fab9c2ac02789deb09fe9716b80dc`  
		Last Modified: Tue, 24 Dec 2024 22:16:06 GMT  
		Size: 2.3 MB (2265770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40a9e24c9a858a8eae219f199f12a86bb10ef85c78167d13cad438ff748c55ef`  
		Last Modified: Tue, 24 Dec 2024 22:16:06 GMT  
		Size: 35.8 KB (35766 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; arm variant v5

```console
$ docker pull redis@sha256:4a0d4abc7348dd958ac73e1d6a242fc2abc4341c643e43ab8f4d0823a0a78d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37242681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca59ed0497ea1f4feaf06b8ebe398220a6b2679d7f09c2f1da75ff49d3cb864c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 04 Oct 2024 09:56:40 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a754f850492d0cd17f9ea00a27d704991bf15a674d30de284ac5300d326eae88`  
		Last Modified: Wed, 25 Dec 2024 01:25:45 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b435ae95ce69d1bba51ab7fca05fe15f3324de438a4919ecbeaef5d9b8bb95c0`  
		Last Modified: Wed, 25 Dec 2024 01:25:45 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99dc6648ccfc1cfd73395e89dfc22e715de8b797ac7c2625750d631231832801`  
		Last Modified: Wed, 25 Dec 2024 01:25:46 GMT  
		Size: 1.4 MB (1414228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b812432028fd2e80e6db1f7e6954eee1278cdb8ea85d4a4c0a7e81c0ad9cf9`  
		Last Modified: Wed, 25 Dec 2024 01:29:18 GMT  
		Size: 10.1 MB (10070872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4fe851ff59d19fd923292659bcf63d2a6aecf21fef977ed22e76a6a1248cb6`  
		Last Modified: Wed, 25 Dec 2024 01:29:18 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca656a762df67c99e4ac05cfe3cff0e816f407d7e8cf05571f4021ca3e9d77b`  
		Last Modified: Wed, 25 Dec 2024 01:29:18 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:99f71bf38730e116add8b559148305739fd78ee35b9a1878781c5a64615606a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75852475d29a64ccd11060056e40c9003c50933c85d6ded39552a0f0e0f4c407`

```dockerfile
```

-	Layers:
	-	`sha256:55a52130b4cb00e135c994a575a7b9c80c6285426bda9c8cc11a4c35bbca7909`  
		Last Modified: Wed, 25 Dec 2024 01:29:18 GMT  
		Size: 2.3 MB (2269282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6aabfca1679955b441e303aecfb95fb90b8bb9bf86b1c6ba88f1314891073a1`  
		Last Modified: Wed, 25 Dec 2024 01:29:18 GMT  
		Size: 35.9 KB (35910 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; arm variant v7

```console
$ docker pull redis@sha256:5388a9303b35e022325b530492a4173a251a71c6f590bced8f1984128c87858a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35130839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a8c3da80ace8b8e1f652e46df3e43a8f5ed0be26ff451750d510ff3834e0bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 04 Oct 2024 09:56:40 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a88ca8976df81c3661c6c180af8f5c36aa115f1b5f15905dc24e82e4c5dea0`  
		Last Modified: Wed, 25 Dec 2024 03:24:56 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f79d2ef9f412c5109c9a90317c110487d7d3dd89af601e1bda3c036cc515d1d`  
		Last Modified: Wed, 25 Dec 2024 03:24:56 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813ed6638d8de38fea9f96c095699ac56d473b731a5421c2d42d58327a817795`  
		Last Modified: Wed, 25 Dec 2024 03:24:56 GMT  
		Size: 1.4 MB (1405386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab42bdec35dee08267738bdd832e1437d42c6ab193a09d3e861174ef776ba843`  
		Last Modified: Wed, 25 Dec 2024 03:28:21 GMT  
		Size: 9.8 MB (9789256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1f72487cd79ccb0766f1b9e45b27ffba173c1ae25ae36d95d6be46ac387de3`  
		Last Modified: Wed, 25 Dec 2024 03:28:20 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5989c18fab70393550e3dda4fb790101cb7d060747d4563a3dd1a166f1800dbe`  
		Last Modified: Wed, 25 Dec 2024 03:28:20 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:5861bc888b0e50d7433e49ffb27c2fa05b9d573d05d82d1379a28b154554aa20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6991bb4ba00233662d9504c4881e05d2e8dfa0a3c7827aa0f205dbdc7bd2048`

```dockerfile
```

-	Layers:
	-	`sha256:94672e944ac1d27aaa11ee1b520a7f3bd65da8e72d37be2d44fb30bdc620e4e1`  
		Last Modified: Wed, 25 Dec 2024 03:28:20 GMT  
		Size: 2.3 MB (2268007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0634c620b4b882fe88b19ef15fe96ff53aa4f4c27229f41b2a153485e2950a0c`  
		Last Modified: Wed, 25 Dec 2024 03:28:20 GMT  
		Size: 35.9 KB (35905 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:b9a9582a4d451368e4f465c4478f9d68e2491b2eb500fd617f38cb20c2519040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39858123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2936bc32ae9523b93e665feec5afa9e63617cf28dcd689c36cf52a1f4b664e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 04 Oct 2024 09:56:40 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fc6d52d57a97f33e2bbbe5a4a7e48b9a7de6222180471056cf26b1ff3bfe85`  
		Last Modified: Wed, 25 Dec 2024 01:24:00 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b1f24592680924927057c8d6458779983a82b65c427f563deea3293e91a996`  
		Last Modified: Wed, 25 Dec 2024 01:24:00 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331d356ef102bae52d39e85c1f051de9d6d5f443e9f7fe3b0a457873dc3a2a13`  
		Last Modified: Wed, 25 Dec 2024 01:24:00 GMT  
		Size: 1.4 MB (1369381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f49c69ecf9f03c6b2e6a6fb435c0ba16567185f1226f1bc5e3fc4f3dcb31aa2`  
		Last Modified: Wed, 25 Dec 2024 01:27:03 GMT  
		Size: 10.4 MB (10427344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701df939969084ae804858c550362d8ed7a80d5b1708ab1384d2423bd07993bf`  
		Last Modified: Wed, 25 Dec 2024 01:27:02 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bdcf9b148902000f40d7732d5b7c9ae76855c72564e9f2a24920049651d791`  
		Last Modified: Wed, 25 Dec 2024 01:27:02 GMT  
		Size: 569.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:c2dd4e381649958efce188c91318ad191e49c1087d7205a2c4128a991f79604f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717ce9c0b7a4b3e8b5943e137a7c88ee20174d03c2e8b03c4dcb4cb9d4c92abe`

```dockerfile
```

-	Layers:
	-	`sha256:84623a0271af6f23ff1a9ac3d3f2111e6c02e73b89eac03a064234dbed08504d`  
		Last Modified: Wed, 25 Dec 2024 01:27:02 GMT  
		Size: 2.3 MB (2266051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407f407072838e40c7b1e18677d9312aa7aebbad5ade68c1976c53a38a5229e1`  
		Last Modified: Wed, 25 Dec 2024 01:27:02 GMT  
		Size: 36.0 KB (35954 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; 386

```console
$ docker pull redis@sha256:074f5de56effee6a080f653787e6a956073cf8727ebfd36324e7f3269be16e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40844404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0eade0d61f3c73f2f521cc7d3cbd9d1e5d7b6d12154df3dff12737975018fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 04 Oct 2024 09:56:40 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812664346ebeb6aa05ad57cf423363046c5d7843b708e919a559cc849c4e5996`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613c89f90a4026937b233d86e694453a0ca8553430fcfaa1430e80abe8a07fc5`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 871.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e93fe8fe6f0ece30f70c7a3ae450d3f880f762c57382774f99b1c99e445d64`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 1.4 MB (1413149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb78f764b58f1e7182e5f58aa3e6729c7894931ff9b95dcb97d20fab2d399059`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 10.2 MB (10223198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c83972f71bdcd222ce688ac34168992e65d15db4a4fd43c2bb4d14a5d2dcd1f`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cf5048f2cf58f30cd773fa5842e0089a663f3948e589ca3569bea325e868dc`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:cee72877ba9a75396cf7e1f19aa0b142d2c4affb34f33c56f2c6673b22952d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebea6988bd2bb424c82a5fc7dfeb310c329ed0b7f0e71107d7a2bdb0527004dc`

```dockerfile
```

-	Layers:
	-	`sha256:43dabbea2ed5633c6f4498846c511782f50fbfcba82fa42ce5618a9749c48cb9`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 2.3 MB (2262903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2278fe38d69895c8482a30c541c57d7f74f369ab05091cdcee0ead473bcba21`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 35.7 KB (35716 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; mips64le

```console
$ docker pull redis@sha256:d566ce7912877845843b13a70091fa4596a104e02687884a242c5871f00b3267
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40256533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:309e7835641ab89e25e8db94fa69e637a26a0337e7158dbde3122462cfa797a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 04 Oct 2024 09:56:40 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5e3a886ce0ac3bb044cde26c3d4a0c62e45c326bec3a754a1a695b1e55ee00`  
		Last Modified: Wed, 25 Dec 2024 11:24:06 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735b4f0bbfeb6ad150142dc0a4d6f24164299d5ff2f9e3731b6f55815d307bef`  
		Last Modified: Wed, 25 Dec 2024 11:24:06 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb270486ce13bd178b2d0db2a3cf5c551c44153a880c0848a01dfaee57c63fc7`  
		Last Modified: Wed, 25 Dec 2024 11:24:07 GMT  
		Size: 1.3 MB (1325339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f269f576389ef8b0178afa5c780a403bd3f1042718cc5c22160c7d4b2dfc476`  
		Last Modified: Wed, 25 Dec 2024 11:41:39 GMT  
		Size: 10.4 MB (10422645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26001b6a89c8a0d536fdea673131299f8d5a326d201a35404773c91a5d03e7be`  
		Last Modified: Wed, 25 Dec 2024 11:41:38 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8af5323e33a15068a89a90b3a744c31ab2a51056fb3a2d3a0aeee90da0351c6`  
		Last Modified: Wed, 25 Dec 2024 11:41:38 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:e736db7c75d22519adc9350da4900825a8d3a9262ca53d80df98c1d298d03c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a7a9928af5be1911e4474822ad40fc30a5a4ed50fca255c0f09488f0f156d5`

```dockerfile
```

-	Layers:
	-	`sha256:5e88c9459ce63e4d4786933b5a6cc75d465a081dbb7d5be5491c83a4c1ae0431`  
		Last Modified: Wed, 25 Dec 2024 11:41:38 GMT  
		Size: 35.6 KB (35647 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; ppc64le

```console
$ docker pull redis@sha256:63c7a49c8551bf12dd5090b3c44fceb8d0cfddb136a277621f506c395a077278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44761968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd45a007c61ce7ea8c04adf71d0b6ccae7d914244c59c630abadd5920b20f92d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 04 Oct 2024 09:56:40 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb4d7380c1abdc7fe203729740b41c9fa6d8ba63e9766d266988ec207271cbd`  
		Last Modified: Wed, 25 Dec 2024 05:52:54 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bc41aba6253aef79f551974f2b314954909dcb364bb93bce2f7d174711c69f`  
		Last Modified: Wed, 25 Dec 2024 05:52:54 GMT  
		Size: 872.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93c15d05e601ed33e33df871e002bb7d0dd3c60f99a48699a9a3de5730f3098`  
		Last Modified: Wed, 25 Dec 2024 05:52:55 GMT  
		Size: 1.4 MB (1360054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb85362f2e370c98d4dba573838230ee5322d03d80db898cab6dd6b6e3d5da1`  
		Last Modified: Wed, 25 Dec 2024 05:58:57 GMT  
		Size: 11.3 MB (11336001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c975d2aab9b2a58ed44150295ad099158a7cfb70abfd14b2b013a78eadae1a`  
		Last Modified: Wed, 25 Dec 2024 05:58:57 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76b0e980debe648ab7b83a7e3d9d51b43759ea14ea6d04e5cd6bbae0cec08e2`  
		Last Modified: Wed, 25 Dec 2024 05:58:57 GMT  
		Size: 570.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:17b56bf7c1768712b00be38d739ed6f13705de9978639e0a26d00fdf0bb2f459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bb71c5ab4a73f40445fd16c019b1831e6220b0ccc0b5a55a584e2f1d76ed0d`

```dockerfile
```

-	Layers:
	-	`sha256:6c798002496b586b72563a5676f0a6ec6584eeec767f3775a179e4c3d097a361`  
		Last Modified: Wed, 25 Dec 2024 05:58:57 GMT  
		Size: 2.3 MB (2270072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8202dbbfbc9e8d708398b460d124916a8a63b30b2178679e71555d2f2c1c0fd5`  
		Last Modified: Wed, 25 Dec 2024 05:58:56 GMT  
		Size: 35.8 KB (35830 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; s390x

```console
$ docker pull redis@sha256:db7d6e23d5a38b477b2d8635cc6ff3c1ec8916b6e7d464b56f1b017da50cf712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38739524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b217c0b9a192160de597aa24bb0307694aad728930bab8e25130d70fb6f5b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 04 Oct 2024 09:56:40 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV GOSU_VERSION=1.17
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_VERSION=6.2.16
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.16.tar.gz
# Fri, 04 Oct 2024 09:56:40 GMT
ENV REDIS_DOWNLOAD_SHA=846bff83c26d827d49f8cc8114ea9d1e72eea1169f7de36b8135ea2cec104e7d
# Fri, 04 Oct 2024 09:56:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
VOLUME [/data]
# Fri, 04 Oct 2024 09:56:40 GMT
WORKDIR /data
# Fri, 04 Oct 2024 09:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 09:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 09:56:40 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 04 Oct 2024 09:56:40 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2526727a4a6ebc6a348a2f4392140bb419e74bf72035304d73324444bbddf08a`  
		Last Modified: Tue, 24 Dec 2024 23:59:53 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a284305d05e26286175824a5cd911e394ad31c401399daa26b30a271ccfc897d`  
		Last Modified: Tue, 24 Dec 2024 23:59:53 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54350215ad6d9a5d53973f6a2baf9fe4ba58bb93cf25e433488b1a1b61eb37c`  
		Last Modified: Tue, 24 Dec 2024 23:59:53 GMT  
		Size: 1.4 MB (1403016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd00a016b85d6971c786009de428efda4a7f66fac304ad756ff4540184f594da`  
		Last Modified: Wed, 25 Dec 2024 00:04:42 GMT  
		Size: 10.5 MB (10454934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5113b767e16fdecc408f3de1aa88223e6ef86007601303f92175c8eda77f7ac2`  
		Last Modified: Wed, 25 Dec 2024 00:04:42 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281daa0f0f11334c026e4731e03d843e042fbbf0961e01b02ea5351b55be9577`  
		Last Modified: Wed, 25 Dec 2024 00:04:42 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:343a8e8cb3fc25d39e95311c5f4cc06d2529ddd7c56dbd1398817f8c9338f944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27eaa3cdd194c0eb2ab6102b08672a8bab9981ff6c07598c75bae226b4c9dc02`

```dockerfile
```

-	Layers:
	-	`sha256:e365d5482176e4890378bcca47947fe354612d826a02082df0bcb750c3daae36`  
		Last Modified: Wed, 25 Dec 2024 00:04:41 GMT  
		Size: 2.3 MB (2265494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd80f5c1a4c1c77ff115771a716b5184b4fd20de743307921430b3bdc60ed72f`  
		Last Modified: Wed, 25 Dec 2024 00:04:41 GMT  
		Size: 35.8 KB (35766 bytes)  
		MIME: application/vnd.in-toto+json
