## `redis:latest`

```console
$ docker pull redis@sha256:ca65ea36ae16e709b0f1c7534bc7e5b5ac2e5bb3c97236e4fec00e3625eb678d
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
$ docker pull redis@sha256:45d8466617d62a19dabdd131d074c034450f2c674e759021c0623c85533d57b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44985388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4075a3f8c3f8e3878d1041c5019e4af445e3b79cf3b55e03063f9813cd49e3f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b95e092fd04b9ee860e2f1e3f9d5380df3e4a91a23fc7a11348a3b784860cd`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c111ca53a74317e5277376c3d486e9502e74a3493e03db6a91e7a566189a6df5`  
		Last Modified: Tue, 14 Jan 2025 02:18:52 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d6cf14046e227c5d483b39ed183a3cde6b11f9aff48a3fdead486872477f3b`  
		Last Modified: Tue, 14 Jan 2025 02:18:52 GMT  
		Size: 1.4 MB (1437822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589f36d317d9df03660b8ffdc795e30079ade277d9b10fda1ad7b6f7d8c14888`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 15.3 MB (15332475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94041d0cae8f070bddc89a3b3a5125705489002e74b339d0c19b9633c4f88637`  
		Last Modified: Tue, 14 Jan 2025 02:18:53 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5f785c970301c21c433db3e3e6ec176d550953b1d7a317577d3195ed465bff`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:b6fc582974fbd5024041e262e46d7896ac8c9a639ba46540ed30f7909a7bbee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57dba632e815fa3de4f807fbfb9e5384f19f13ba6ef13257920b84168ae89538`

```dockerfile
```

-	Layers:
	-	`sha256:b08b6683922f0eebeb141c0cc80a3bca7328faac46b01994caf92d08720b230a`  
		Last Modified: Tue, 14 Jan 2025 21:15:47 GMT  
		Size: 2.3 MB (2266360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a546afcabeff1e04628fd458d1382beb8e47991b27907c14a2ae164fe99a42b`  
		Last Modified: Tue, 14 Jan 2025 02:18:52 GMT  
		Size: 36.4 KB (36350 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm variant v5

```console
$ docker pull redis@sha256:19eb0b225c2efa5d2ea73bc2ebc04bc33048a2ea8dfd00b37103c9a709aa7a7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42208988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46054892831e13cde6b4b20cb550269eb22d61ac6f642650b2b2fe2e1003077d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 20:33:17 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b317a84a5ffa308c57175306020696c952df099c56779647a8852dccb2e928f4`  
		Last Modified: Tue, 14 Jan 2025 06:03:27 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17e033997c297993686589d3798e5467b72f35d3bc7f1357074082efa68343c`  
		Last Modified: Tue, 14 Jan 2025 06:03:27 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef4c635a71f98e4e03fba12868cf590621d23b6579791ee3e547e87349c424a`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 1.4 MB (1414250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29d33fd194b8b5f69ca99723459873485fb225d03b218a16236054b41e6582c`  
		Last Modified: Tue, 14 Jan 2025 06:04:46 GMT  
		Size: 15.1 MB (15055396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6366d9da701c1e8197e7e743f819f45e2522b8cbe8ee9726945aa4030bc1d1b`  
		Last Modified: Tue, 14 Jan 2025 20:33:17 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6d2c84316d476797cc1b7c307a344fa4325e7febb13aa0dfe8f0caeea9e703`  
		Last Modified: Tue, 14 Jan 2025 20:33:18 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:a56e56a03b827537448f814abbcc00305ffd0dc283f144648ed74ff8621cbe30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0623321e3be72115d62241e5818cc6e8b47a7c3db8f6d4184e4de6d6d8df2f7c`

```dockerfile
```

-	Layers:
	-	`sha256:2c78974ee52d5c56bb4cf00afca5e112733bc774782ab2a03f5c14c6c8ef82b0`  
		Last Modified: Tue, 14 Jan 2025 21:16:00 GMT  
		Size: 2.3 MB (2269888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03219024f76eacfcf23dd6f1dcf359754168bf5b84a2515e5b0a7951370e3d8e`  
		Last Modified: Tue, 14 Jan 2025 21:16:00 GMT  
		Size: 36.5 KB (36510 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm variant v7

```console
$ docker pull redis@sha256:37b64d4a9ec4ba7cda3bc58c11b1fd734630539b9a3be33d432f49fe1ce40b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (40039339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0c96c610c16b55c18425eb84b73c6fc1d788ba4684aefb401e63b706190d3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8851c8f378728d50f386447c584d7bbd74049eabfe43f81e40e4ab788436fcc`  
		Last Modified: Tue, 14 Jan 2025 08:38:15 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3ca11f8403646ec88da32dd4e2932053422db65eaacc23df5f52c1a7216a8a`  
		Last Modified: Tue, 14 Jan 2025 21:15:59 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd618ac58474b1849549df137009cfd90f9c24419aec47cf24a01d3638c9563c`  
		Last Modified: Tue, 14 Jan 2025 21:15:59 GMT  
		Size: 1.4 MB (1405349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8ba061202f7ae3cc802b03d2c990dbeeee0145543f262ce785a12f5c9e0aeb`  
		Last Modified: Tue, 14 Jan 2025 08:39:30 GMT  
		Size: 14.7 MB (14716714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0374494047168cdd638d64950d65811952a69bf654620066c798cd494bd91d15`  
		Last Modified: Tue, 14 Jan 2025 08:39:29 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad93913ae1cf2b8877c3927802f84ec34c7e7d8155fe665d129c94a003125b29`  
		Last Modified: Tue, 14 Jan 2025 21:16:06 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:53b2a66ad656c67a6640fd07e06c99b7afb8c18172e5819f006104764caa4876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0363aada3777f43d3cd2850e150d463e7db900a7abb09395babbe272eb55d003`

```dockerfile
```

-	Layers:
	-	`sha256:7cd165a64475c3fb7abd4824f3c3b587b1de35034f67ef2ec8376bc7588f14c6`  
		Last Modified: Tue, 14 Jan 2025 21:16:19 GMT  
		Size: 2.3 MB (2268613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c097a3062b19f984e720c9602cb83753a55f98b00a8dd65b12b66f851fe75cb`  
		Last Modified: Tue, 14 Jan 2025 08:39:29 GMT  
		Size: 36.5 KB (36510 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:b6cd4942c1a19ad21dc6703440a6cd324e3cba3cfcf676c4cbcf01ce20ada884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44739471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0043b23d6023a816605f785a6af2177a27cfbb44114af36742bacb5072b98dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc82b694f0127550ed145ca92bcefd210e83df8bf08f6bb661078a6916476303`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95871a2f28d8980bb35529c19424e8e1fbdbcc933bc0bf10234f5640c33b3e1`  
		Last Modified: Tue, 14 Jan 2025 06:34:28 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194ef0d9d22c60f7a7935e5fc03c9e19f886c021c94c74239ba445f202cf3edb`  
		Last Modified: Tue, 14 Jan 2025 06:34:28 GMT  
		Size: 1.4 MB (1369333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99cf812907808b844b9024e8af9001ea8557d3e53c98dd012b04c74f942d1ca`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 15.3 MB (15326433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0505c4e376ef0a451ef5afa9431178436b16a297be856551545f59825b0898ce`  
		Last Modified: Tue, 14 Jan 2025 06:35:39 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8829b28bc63865f15a8cb653369977a42d6790cd56cf8737d1e73842235e04a5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 571.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:087efa911f88de373c6ec2d7ebf69879370fe22c617d63d0537696b6b6fca313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a830e7fca79418b3cc5f1e95daa325c652bd6f220d04e345e3b92a9377fa5b2`

```dockerfile
```

-	Layers:
	-	`sha256:c5c9dfe2fa6a390638f9ef1cb36bc99de0de984975144d6b1c92f426749034e1`  
		Last Modified: Tue, 14 Jan 2025 06:35:39 GMT  
		Size: 2.3 MB (2266665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e0badec75a30455f9f1a318939e319606e7a49ca1a92ebc6b5a6486964066af`  
		Last Modified: Tue, 14 Jan 2025 21:16:38 GMT  
		Size: 36.6 KB (36562 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; 386

```console
$ docker pull redis@sha256:1ca4363476d871957b4be474d5af74047a2af2f561c9bf9ae2736372ec1a8761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45456180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a070df3a5c7ee2aa010200cfa37b3835933ec075c9535c5de5ca8fdc44ff00ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed072a923df8085e67e8fb64d9323c63ff68b04fe7d55b7b91e7956741d6431`  
		Last Modified: Tue, 14 Jan 2025 21:16:43 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c679f3caf7ba0b1b30dcc57a3abcef131fb64a1658baa202adc434f19a4913`  
		Last Modified: Tue, 14 Jan 2025 21:16:43 GMT  
		Size: 871.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d60bcf9426ea0c1659df6b96b070cfd3722f46b93efea255a870dcc418ad5e5`  
		Last Modified: Tue, 14 Jan 2025 02:18:15 GMT  
		Size: 1.4 MB (1413140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983a0dd666c29fa92207df518dee2f10feddfbac08a878e3048d9bb9921c9fa3`  
		Last Modified: Tue, 14 Jan 2025 21:16:48 GMT  
		Size: 14.9 MB (14852775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91595999328af42a3bc1730777ad7f1ff2a286a919d2ebb8d23d4c682faf41f`  
		Last Modified: Tue, 14 Jan 2025 02:18:16 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d812308f776bd596cc1d1107343b3158bb4b8d11f04f9df119ef7d4cf22836e`  
		Last Modified: Tue, 14 Jan 2025 21:16:45 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:8b6897d98153fc6c7d91e1e2136e0fa920dd19ba436d533c4ae3a1a9a4e319b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816072f002cf8bff5ec6c5a1fff106258274fd37a125e481165cc02e222bd6e9`

```dockerfile
```

-	Layers:
	-	`sha256:890e209c4ae10fa2ed053592a2ccb9ac8f258c626b5d52192c869ce0218d627d`  
		Last Modified: Tue, 14 Jan 2025 21:16:57 GMT  
		Size: 2.3 MB (2263483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3e80423afd5a1f1cd2074108498845aba061a585403fa0cabd5ef7d1eab66a`  
		Last Modified: Tue, 14 Jan 2025 21:16:56 GMT  
		Size: 36.3 KB (36289 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; mips64le

```console
$ docker pull redis@sha256:4c83e0ca2cf571c9a558e1c237a4185b86b6558194c7f9512a6e1cefb8331d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45238176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f04324d7ff79e7880cebb44d66136cef902f7749dd41a48e1b5fe992fc9d9b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a1ea2cfba4ec5af6f0861a10016319e343577c830f21f7e819a7672e63d68e`  
		Last Modified: Tue, 14 Jan 2025 17:48:10 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f57aad5e183954e5d00e4e6568216f9481526d0d4ed9cb5f8c6f7834814c83`  
		Last Modified: Tue, 14 Jan 2025 20:49:22 GMT  
		Size: 873.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74441a45cea6dd7311481fb76f43971ebe3232768f764b7b0d16950c83340a3b`  
		Last Modified: Tue, 14 Jan 2025 20:49:24 GMT  
		Size: 1.3 MB (1325371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993adb8ea05002e30472fd8b277ad7c2dabaafe8b560c6077dfeeac6b8096053`  
		Last Modified: Tue, 14 Jan 2025 17:54:32 GMT  
		Size: 15.4 MB (15423481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bd4979f2e9cf08f1ec3a49115c83375369691e5a07d11e8a3294d229dc258e`  
		Last Modified: Tue, 14 Jan 2025 20:49:30 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24479b0794b9ecdfb236c5b6b442c279a7c17eff35aeed32f6dad6907680e389`  
		Last Modified: Tue, 14 Jan 2025 20:49:35 GMT  
		Size: 573.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:db31edf6f0c29e68239b2e9a4960df804ffc62a8a148133992309ed0c040bca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 KB (36249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f9a3a11dd218ef8f2c9010d934cebd992ff24e533ba3805ec2d5fa707cdf3c`

```dockerfile
```

-	Layers:
	-	`sha256:d4259043dd56a54136c37d54b19515685b97adc95c9d2fc2e02b690ca58515c6`  
		Last Modified: Tue, 14 Jan 2025 20:49:38 GMT  
		Size: 36.2 KB (36249 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; ppc64le

```console
$ docker pull redis@sha256:0f8e18ee222aa13fd7d72460135a3eb30ccb089907d05379aac1a39ecd921697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49901210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071ea74b19cf0be94ade1d21b4364c38029b7673c943b583a92f4976f79c62de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97da7c42a55330a6da651b296e754891b2b2092a9c62d5615867cca851c8995d`  
		Last Modified: Tue, 14 Jan 2025 21:17:18 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744af93abb4d41145cbf42cdef9b2ff94c1fe38331c2a38b989636da302e47b`  
		Last Modified: Tue, 14 Jan 2025 21:31:03 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fcfa71c5570dd243aa0f6578b141fdff708ccec39fd57621798ac9bab8f662`  
		Last Modified: Tue, 14 Jan 2025 05:06:42 GMT  
		Size: 1.4 MB (1360052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e96faad908521ea42603721da0eadafd045dd260042dd5b7b4b850fa7ca1ad9`  
		Last Modified: Tue, 14 Jan 2025 05:08:33 GMT  
		Size: 16.5 MB (16493635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296ecab81cd1596efcda3cea797374d3f5b6b7fc5bc3dd28b1c926f53cb1ebf3`  
		Last Modified: Tue, 14 Jan 2025 21:17:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec7430c81d009586de5a1c5365645453308703cf11a211559d83c992b9502b`  
		Last Modified: Tue, 14 Jan 2025 05:08:32 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:8e7557de4e4294dd8da790e4b7a58efe14d12f1534cd039b52fb325c84b97ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361c7b83059bd141649ea5567e74c92dc67c0bfad127d2523fa3e9ffde3e45a4`

```dockerfile
```

-	Layers:
	-	`sha256:cf14cca08c77311bca461f330512083e9495fb54adaeee42589da8f1baec4ab1`  
		Last Modified: Tue, 14 Jan 2025 21:17:38 GMT  
		Size: 2.3 MB (2270674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:055e5ed4bc85ee018ded609f047043746a6f76dd05af925ea71f1c7966f8d746`  
		Last Modified: Tue, 14 Jan 2025 21:17:37 GMT  
		Size: 36.4 KB (36426 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:latest` - linux; s390x

```console
$ docker pull redis@sha256:8b06bc6b5ddadb0c39e6e3f261314fea5281d79b5d50b6cf25880ec04c2be4f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43631693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe83f34dcf9680def2f81a2150a6c40994885f55db1b90da9863f4e747c676fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 06 Jan 2025 16:14:31 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV GOSU_VERSION=1.17
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_VERSION=7.4.2
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-7.4.2.tar.gz
# Mon, 06 Jan 2025 16:14:31 GMT
ENV REDIS_DOWNLOAD_SHA=4ddebbf09061cbb589011786febdb34f29767dd7f89dbe712d2b68e808af6a1f
# Mon, 06 Jan 2025 16:14:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
VOLUME [/data]
# Mon, 06 Jan 2025 16:14:31 GMT
WORKDIR /data
# Mon, 06 Jan 2025 16:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Jan 2025 16:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Jan 2025 16:14:31 GMT
EXPOSE map[6379/tcp:{}]
# Mon, 06 Jan 2025 16:14:31 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 20:36:29 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6398545cfaea4fbe64e3c712edecff4f5ec3a5eb3f5267a560b84a5b0d44018d`  
		Last Modified: Tue, 14 Jan 2025 21:31:06 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3a309343d201b7a67fe08780851d3b03eddd26347a00398466205732158592`  
		Last Modified: Tue, 14 Jan 2025 21:48:43 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8e600569f6bef7b108d97d787511a0f5dafe5f30ed7afc85d6cbca687b89cd`  
		Last Modified: Tue, 14 Jan 2025 21:31:07 GMT  
		Size: 1.4 MB (1403015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31da60d4ccee676736356f89d19150b65ed6b322d992913beafaeb158e61ed8`  
		Last Modified: Tue, 14 Jan 2025 21:17:47 GMT  
		Size: 15.4 MB (15367263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4be648d92c30d96d8e77f4e57121811c08b71971ec73a288aaa6feb575e7971`  
		Last Modified: Tue, 14 Jan 2025 21:17:43 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2e2f1345f64c0b8c526f7c091f370b95ab71c0e52f46ccf22a9f43d31f4047`  
		Last Modified: Tue, 14 Jan 2025 04:44:26 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:latest` - unknown; unknown

```console
$ docker pull redis@sha256:e4eac9b796554723b97846f83d479291982e2ced587dafcfbc43876365e074aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c8134848c701d68b82c9fb7a075e7ff7eb9fcdbcc67303cbfd0cafb4d8beb1`

```dockerfile
```

-	Layers:
	-	`sha256:c17cc73047d00298aa75b03e62e0de700a32752c8935c511b6fc3b2deae48bb9`  
		Last Modified: Tue, 14 Jan 2025 21:17:57 GMT  
		Size: 2.3 MB (2266084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ee77f9a49a250122dee3a8209d269d46a579b4bbe6b322b40374abed0786583`  
		Last Modified: Tue, 14 Jan 2025 04:44:26 GMT  
		Size: 36.4 KB (36350 bytes)  
		MIME: application/vnd.in-toto+json
