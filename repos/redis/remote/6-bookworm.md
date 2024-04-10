## `redis:6-bookworm`

```console
$ docker pull redis@sha256:d4dadd22d075fa18b262fc1e9a4b1b9ce2db9fdacfe51046cccb05b2e921cb36
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
$ docker pull redis@sha256:060f8a0188a2b34c58172318b5000ffbace63201a4973155842ae38cdadf0865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41058757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80270b811a553bf3662cf4679e01f12c7f3f431542b138db36f47dbb26a37212`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 05 Apr 2024 21:53:10 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Fri, 05 Apr 2024 21:53:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=debian&os_version=bookworm"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
VOLUME [/data]
# Fri, 05 Apr 2024 21:53:10 GMT
WORKDIR /data
# Fri, 05 Apr 2024 21:53:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:53:10 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 05 Apr 2024 21:53:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a239622e6d75d409ea794c8b0f367d6081a2e1f8a1d0e0779e5a643a5d2c692`  
		Last Modified: Wed, 10 Apr 2024 02:56:13 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcc89d07207ef8edd5d9633bcaa632a54c20f8ddca6563445fe444a83495b93`  
		Last Modified: Wed, 10 Apr 2024 02:56:13 GMT  
		Size: 871.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9709e7565b05172b3eb2e5a2a0882d3a0236d2f8eb3dc4d190b82be39b90838a`  
		Last Modified: Wed, 10 Apr 2024 02:56:13 GMT  
		Size: 1.4 MB (1437812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c6fc4576a56adb9e34ec1f0ef194564c91eaac76c3bb275929051717bae3a0`  
		Last Modified: Wed, 10 Apr 2024 02:56:13 GMT  
		Size: 10.5 MB (10486914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49207c06519069f6a19ad67a7dcece6090edba87558a8fc0178078ccf1f1a7b`  
		Last Modified: Wed, 10 Apr 2024 02:56:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9228f9aa22eeb7f5e3a65d7f6549a6b7c1624dc24a09c54c4e53b05bdfc874e5`  
		Last Modified: Wed, 10 Apr 2024 02:56:14 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:3e037cf070bd1d1e07e35676fa235193a59d0d8c20fab7a7c0800d85d796b226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2275377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a59ca22eb28f9468db9780bdf2865a5d1908535e1e20de78d0c1d8d0d372196`

```dockerfile
```

-	Layers:
	-	`sha256:836bf774055d8dcb3d2831416b90c1ef01697f928207e5e1f9f691ea103a946c`  
		Last Modified: Wed, 10 Apr 2024 02:56:13 GMT  
		Size: 2.2 MB (2238584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1737cf9585473a900003780554cd0da4a2efc96261200cce205017fd4a213ca6`  
		Last Modified: Wed, 10 Apr 2024 02:56:13 GMT  
		Size: 36.8 KB (36793 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; arm variant v5

```console
$ docker pull redis@sha256:9621960100f5e2ee8bedb4edbe75ee476a65ed164f985f7321ff78e14841bf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38366753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ee180bead9b618c20f31c0ec309a2ea97ae9985955af7acb84c89a7dab1a11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:31 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 12 Mar 2024 00:48:31 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=debian&os_version=bookworm"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
VOLUME [/data]
# Fri, 05 Apr 2024 21:53:10 GMT
WORKDIR /data
# Fri, 05 Apr 2024 21:53:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:53:10 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 05 Apr 2024 21:53:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10184e7b6c29df87e2ad70153fe4c74f2d97b32f802cfab00e9246a12ce4d699`  
		Last Modified: Tue, 12 Mar 2024 21:12:16 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945d1b4e78cc28bd7fec631950b5b7b5685bcfa77d37147d7a4532c99de86b38`  
		Last Modified: Tue, 12 Mar 2024 21:12:16 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32b625d95b49c627d328a2fecbf7c5804292378ab5531a7c216892463599ae0`  
		Last Modified: Tue, 12 Mar 2024 21:12:16 GMT  
		Size: 1.4 MB (1414259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e5cf07c6434a7d7bb2995071e39af9dc15eb05109f615e3c7e21fdd465bf5`  
		Last Modified: Tue, 09 Apr 2024 05:13:19 GMT  
		Size: 10.1 MB (10065794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4cfc09de9234407c58c80cc2cd143dd7a0614f7881d2d89f1a999506727aff`  
		Last Modified: Tue, 09 Apr 2024 05:13:18 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409e08eb62970c55b4ad02e024d96f4b7e84c5421c687dcc4d4c9a34c5b7014a`  
		Last Modified: Tue, 09 Apr 2024 05:13:18 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:dabdeb61bde607f8e9c77b626f61c23d1808964fcb33c58e27e09ff46c4e8441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33fa08e7215b9bbed927d36bd4dd17a4658319ac3c760f1d2fd3da55b712f24`

```dockerfile
```

-	Layers:
	-	`sha256:3184b8f2e90f2b8397d9baf24dc2bb741518f8de5f7adbc8f834f7c673dbe623`  
		Last Modified: Tue, 09 Apr 2024 05:13:19 GMT  
		Size: 2.2 MB (2243130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:110a50e73519fbcffc6c1a81113c6cc7e3229ba833a1c5a079bf4f35d8cf5035`  
		Last Modified: Tue, 09 Apr 2024 05:13:19 GMT  
		Size: 36.8 KB (36763 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; arm variant v7

```console
$ docker pull redis@sha256:5822d961a3c604ea3dbd66e8fea7791c9c9eb295508d60e1749b607cf8a3dc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35909916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:473d88f11406896ea0a03133e67ea71fb7cf99c961e024f8e9d0a62d7fb645dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=debian&os_version=bookworm"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
VOLUME [/data]
# Fri, 05 Apr 2024 21:53:10 GMT
WORKDIR /data
# Fri, 05 Apr 2024 21:53:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:53:10 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 05 Apr 2024 21:53:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161f8b05dc168b62a9b0a51d7ffb539c5d4ba8c645360cfee50eddad5a59e945`  
		Last Modified: Tue, 09 Apr 2024 07:12:18 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9592a0e861480aa155581668783e600be46afff80d600366c688c7db0361f476`  
		Last Modified: Tue, 09 Apr 2024 07:12:18 GMT  
		Size: 874.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcbea9b4e9901eb8278159bb52049e1c9a9101263420c44ea8e5b23a6f74649`  
		Last Modified: Tue, 09 Apr 2024 07:12:19 GMT  
		Size: 1.4 MB (1405421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f61af67db8d92d23bbc8f9083fbfc72a571fb2265e822549016b8a2dac4f6f`  
		Last Modified: Tue, 09 Apr 2024 07:14:34 GMT  
		Size: 9.8 MB (9785083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bcaed9f98252b7f850d28323c6bc59bccf3cb44765597740ec9e43db0fa505`  
		Last Modified: Tue, 09 Apr 2024 07:14:32 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106da07e7ff7db758d15e8e2acfe496e10eccdc275043d2441ebfdffb66f889f`  
		Last Modified: Tue, 09 Apr 2024 07:14:32 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:2be3e17da61f156b55721fd73415ceb014b12c81d83ecc29852d459a960862c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2278864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84653c4161a1b63f259abf5ede8a5315310e20ca3ba8657375093fe5be039bad`

```dockerfile
```

-	Layers:
	-	`sha256:779b22008c620cf56e688f9bf33bdbff2c386cbc2cb8e51d4bfee11344961133`  
		Last Modified: Tue, 09 Apr 2024 07:14:35 GMT  
		Size: 2.2 MB (2242104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d93e19dcc829f1885f24f6de14b1c5315fe4daa46a97ed750ec5cd11271c188b`  
		Last Modified: Tue, 09 Apr 2024 07:14:32 GMT  
		Size: 36.8 KB (36760 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:1a63b95af4aa41d4e7e055b8ccf29eed1754a51f120d4d08d4142bdcb07efa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40942904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd99e533b6bf074a1382714f0fc55961c7f3c42cbc096812c0b126d8254f870f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=debian&os_version=bookworm"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
VOLUME [/data]
# Fri, 05 Apr 2024 21:53:10 GMT
WORKDIR /data
# Fri, 05 Apr 2024 21:53:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:53:10 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 05 Apr 2024 21:53:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba83bc46bf34377ca8f060583ee276dc004eacf89bcc390c1e0888ac476c191`  
		Last Modified: Tue, 09 Apr 2024 06:59:49 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8adbc896fb1d6c4b08188efcd2b4193baa5f94378ba605cc2e71d056a96c6bb`  
		Last Modified: Tue, 09 Apr 2024 06:59:49 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ee79a8cb2d23a0e8782f04cbed146e3b710be056d41fbc7628dfc313432d2`  
		Last Modified: Tue, 09 Apr 2024 06:59:49 GMT  
		Size: 1.4 MB (1369362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195bee6c961aa48a29acc79164d903461e1687cfe28031f73ed4ed7661385b92`  
		Last Modified: Tue, 09 Apr 2024 07:01:51 GMT  
		Size: 10.4 MB (10414424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1da02c40a8844e29f319214c3a76384265f608ad6894901f1bd24f36b321e9b`  
		Last Modified: Tue, 09 Apr 2024 07:01:50 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca09c86e874ae002f5df488f2313ac8e09eef2d1f4473d69cdbf440d8859a9d1`  
		Last Modified: Tue, 09 Apr 2024 07:01:50 GMT  
		Size: 574.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:a079ccc41b267ce213c4d58bde26f5fd5ecfe926bd238e5c5934b0ddd4a67585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2276723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e04b6ac5ac7a759023cf7232650afc9e5ba4b4580aed71d514dcfdc0410625`

```dockerfile
```

-	Layers:
	-	`sha256:c8aee92869f5e751d3c49d5eee21e9aa0c13f42f9f62ce7f7d2f55b402a9a8cf`  
		Last Modified: Tue, 09 Apr 2024 07:01:50 GMT  
		Size: 2.2 MB (2240083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fed0734917b65de2b8bf92afdb77c877b01f3fcf7bb4f83820ba2fb7db48007`  
		Last Modified: Tue, 09 Apr 2024 07:01:50 GMT  
		Size: 36.6 KB (36640 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; 386

```console
$ docker pull redis@sha256:61ea0063bffc777abf0c32510fa13af06f92ada4647854e41a223167aea3caa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41773551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02a300670c41b4165d2260e60a6842d9e806a7250ad4f73e5227234eda9cd21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=debian&os_version=bookworm"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
VOLUME [/data]
# Fri, 05 Apr 2024 21:53:10 GMT
WORKDIR /data
# Fri, 05 Apr 2024 21:53:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:53:10 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 05 Apr 2024 21:53:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dc1b104cb740dbf1c0bf9b1f9b0a457b8ade4628ebd27247654642cda8959e`  
		Last Modified: Mon, 08 Apr 2024 21:57:30 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a97789bdbfb9117b8a22f786eeaa0cc47cebe585e12de9ac4ca0a410b158b6d`  
		Last Modified: Mon, 08 Apr 2024 21:57:33 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39eadbd485b6b0857675c85b26a2589d7b46a011a83a42b735eb81d803ad544`  
		Last Modified: Mon, 08 Apr 2024 21:57:33 GMT  
		Size: 1.4 MB (1413106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57effb5de6a394857890c9749fa967f62e4d2034c2dbf7c7a128355fb999655b`  
		Last Modified: Mon, 08 Apr 2024 21:57:33 GMT  
		Size: 10.2 MB (10215888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621f5cc93897012848d9b776257834cb3fbf11335038d61e63e244d8d690d228`  
		Last Modified: Mon, 08 Apr 2024 21:57:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95355ef162fa1a7fa8f6413c02e55f8d7d74e617163cee134632199cfc4a47d7`  
		Last Modified: Mon, 08 Apr 2024 21:57:33 GMT  
		Size: 575.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:98e44c61aa62aa9901e48b6e66a472d75ec30268930ec8c86d98906b6f33b291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2273746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfbcf29e7e6bc32468139bd6a8a706a6c29832672e9cfd61e0c31a783931760`

```dockerfile
```

-	Layers:
	-	`sha256:2a9cdec20da17f9aff6fd88c12ce1b95e6224a3ab04504eeb3a58a5176a5f28d`  
		Last Modified: Mon, 08 Apr 2024 21:57:33 GMT  
		Size: 2.2 MB (2237000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c0aba7aadb39b2918c9d07a9189ebf51c6bc1982d463036ece0b7542b4548b4`  
		Last Modified: Mon, 08 Apr 2024 21:57:33 GMT  
		Size: 36.7 KB (36746 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; mips64le

```console
$ docker pull redis@sha256:b55e7d51ceea38110321b143397b5341fb676b40f7a119737db3156f1b91d4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40866371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1757b70244450f42b760ddf8680824a425dd421a7a731cdc4c667f98b712d931`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=debian&os_version=bookworm"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
VOLUME [/data]
# Fri, 05 Apr 2024 21:53:10 GMT
WORKDIR /data
# Fri, 05 Apr 2024 21:53:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:53:10 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 05 Apr 2024 21:53:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f725c52d0ecb77ff408ccb2b8ca7d71d9399f38f0425e0daf4c019babee0d6`  
		Last Modified: Tue, 09 Apr 2024 15:32:47 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ec6adf806872dc4dcbecc793d4dc0df8f152963ff60c77a948d118db959cda`  
		Last Modified: Tue, 09 Apr 2024 15:32:47 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce09eb63a8fb48785c4384aa6efa1f6cb21089fc559f6fe4eff43d5268799`  
		Last Modified: Tue, 09 Apr 2024 15:32:47 GMT  
		Size: 1.3 MB (1325294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98908c7c47c6fe42154309ca7cb09c4ece65e33ebe8b2981d6b3b7696eb0cd1d`  
		Last Modified: Tue, 09 Apr 2024 15:48:47 GMT  
		Size: 10.4 MB (10419183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698b56f66b1e8b8f1b57e08bc3a842d6e6b4feee72587cc30aa120c97ee857b8`  
		Last Modified: Tue, 09 Apr 2024 15:48:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce84352ff589c69d3ff288897532b2b1285ef32aa7dfac9d48f4541e3bc3f8f`  
		Last Modified: Tue, 09 Apr 2024 15:48:46 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:f59dfa2dbe6ac0c2d37570cbe5e46d3263f209cc3c7d0a10ff883336213721e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b7f39e25cd5756f7bbe816a1d24d10da418316d62dce2f4c8dde500797d60a`

```dockerfile
```

-	Layers:
	-	`sha256:01e3beeaf0fbfe9908910504261145cd69ac067dca3e69731f84b60873629978`  
		Last Modified: Tue, 09 Apr 2024 15:48:45 GMT  
		Size: 36.5 KB (36497 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; ppc64le

```console
$ docker pull redis@sha256:9577071c377da21ae337e64665061610c042620d094f1551a37ee4ead15d44e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45812486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae28a19cb63a92547651bea3bca4783f246d997882707b5a75b7e6b38fdabec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=debian&os_version=bookworm"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
VOLUME [/data]
# Fri, 05 Apr 2024 21:53:10 GMT
WORKDIR /data
# Fri, 05 Apr 2024 21:53:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:53:10 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 05 Apr 2024 21:53:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aabffec47310001cabaa99593bdc66c1dab0f4e5bb57aa681d919602d5f186`  
		Last Modified: Tue, 09 Apr 2024 05:09:01 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ca8e0a498fdc412f8ed1190ae702500af0f9b7411a525e10db20a1af17e161`  
		Last Modified: Tue, 09 Apr 2024 05:09:01 GMT  
		Size: 875.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526170dfd2927a6084a2126dfc7dd1f1259d53e9d4be4a3626008c92f9c5b106`  
		Last Modified: Tue, 09 Apr 2024 05:09:01 GMT  
		Size: 1.4 MB (1360022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f967628807d12573b24ddc167ecc78b484b30f578c7ec17f52867895aaceb8e`  
		Last Modified: Tue, 09 Apr 2024 05:12:29 GMT  
		Size: 11.3 MB (11330755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea84d59272f73c69efa8075710ab8daa17bfdd5b297a5814e6ffd12bbfd9104`  
		Last Modified: Tue, 09 Apr 2024 05:12:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2931cf0a471ca9cacc87a62f34dd99fa4d6a23d1b021be36eb9d76f08b50a8`  
		Last Modified: Tue, 09 Apr 2024 05:12:29 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:b767fb1231300367338ef2a3b95e1d69a78cd9179a38d4d202ab28060e663bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2280853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595444fcda1c3375cd080c450024de2e17c0b22de84a6b3c767e8a1d3e325b3a`

```dockerfile
```

-	Layers:
	-	`sha256:965aa929695569e7bb39e735af92d88716596573f3450dfa896818faff6b7bfb`  
		Last Modified: Tue, 09 Apr 2024 05:12:29 GMT  
		Size: 2.2 MB (2244169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d9035ea4002a82eba68538dd2127856d7f1e61574743b8d95e4ce90e885db4`  
		Last Modified: Tue, 09 Apr 2024 05:12:28 GMT  
		Size: 36.7 KB (36684 bytes)  
		MIME: application/vnd.in-toto+json

### `redis:6-bookworm` - linux; s390x

```console
$ docker pull redis@sha256:5997d994c5cb584f6c709fdd83bdf5569ee057ff8a8165fd308462dde1802d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39347469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1084ffad51766288c879002af8f2817c53fe1960b1159fb4a9ceb39e773f887e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	groupadd -r -g 999 redis; 	useradd -r -g redis -u 999 redis # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates gnupg wget; 	rm -rf /var/lib/apt/lists/*; 	arch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	case "$arch" in 		'amd64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-amd64'; sha256='bbc4136d03ab138b1ad66fa4fc051bafc6cc7ffae632b069a53657279a450de3' ;; 		'arm64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-arm64'; sha256='c3805a85d17f4454c23d7059bcb97e1ec1af272b90126e79ed002342de08389b' ;; 		'armel') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armel'; sha256='f9969910fa141140438c998cfa02f603bf213b11afd466dcde8fa940e700945d' ;; 		'i386') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-i386'; sha256='087dbb8fe479537e64f9c86fa49ff3b41dee1cbd28739a19aaef83dc8186b1ca' ;; 		'mips64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-mips64el'; sha256='87140029d792595e660be0015341dfa1c02d1181459ae40df9f093e471d75b70' ;; 		'ppc64el') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-ppc64el'; sha256='1891acdcfa70046818ab6ed3c52b9d42fa10fbb7b340eb429c8c7849691dbd76' ;; 		'riscv64') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-riscv64'; sha256='38a6444b57adce135c42d5a3689f616fc7803ddc7a07ff6f946f2ebc67a26ba6' ;; 		's390x') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-s390x'; sha256='69873bab588192f760547ca1f75b27cfcf106e9f7403fee6fd0600bc914979d0' ;; 		'armhf') url='https://github.com/tianon/gosu/releases/download/1.17/gosu-armhf'; sha256='e5866286277ff2a2159fb9196fea13e0a59d3f1091ea46ddb985160b94b6841b' ;; 		*) echo >&2 "error: unsupported gosu architecture: '$arch'"; exit 1 ;; 	esac; 	wget -O /usr/local/bin/gosu.asc "$url.asc"; 	wget -O /usr/local/bin/gosu "$url"; 	echo "$sha256 */usr/local/bin/gosu" | sha256sum -c -; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_VERSION=6.2.14
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-6.2.14.tar.gz
# Fri, 05 Apr 2024 21:53:10 GMT
ENV REDIS_DOWNLOAD_SHA=34e74856cbd66fdb3a684fb349d93961d8c7aa668b06f81fd93ff267d09bc277
# Fri, 05 Apr 2024 21:53:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		wget 				dpkg-dev 		gcc 		libc6-dev 		libssl-dev 		make 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -E '^ *createBoolConfig[(]"protected-mode",.*, *1 *,.*[)],$' /usr/src/redis/src/config.c; 	sed -ri 's!^( *createBoolConfig[(]"protected-mode",.*, *)1( *,.*[)],)$!\10\2!' /usr/src/redis/src/config.c; 	grep -E '^ *createBoolConfig[(]"protected-mode",.*, *0 *,.*[)],$' /usr/src/redis/src/config.c; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	extraJemallocConfigureFlags="--build=$gnuArch"; 	dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64 | i386 | x32) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=12" ;; 		*) extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-page=16" ;; 	esac; 	extraJemallocConfigureFlags="$extraJemallocConfigureFlags --with-lg-hugepage=21"; 	grep -F 'cd jemalloc && ./configure ' /usr/src/redis/deps/Makefile; 	sed -ri 's!cd jemalloc && ./configure !&'"$extraJemallocConfigureFlags"' !' /usr/src/redis/deps/Makefile; 	grep -F "cd jemalloc && ./configure $extraJemallocConfigureFlags " /usr/src/redis/deps/Makefile; 		export BUILD_TLS=yes; 	make -C /usr/src/redis -j "$(nproc)" all; 	make -C /usr/src/redis install; 		serverMd5="$(md5sum /usr/local/bin/redis-server | cut -d' ' -f1)"; export serverMd5; 	find /usr/local/bin/redis* -maxdepth 0 		-type f -not -name redis-server 		-exec sh -eux -c ' 			md5="$(md5sum "$1" | cut -d" " -f1)"; 			test "$md5" = "$serverMd5"; 		' -- '{}' ';' 		-exec ln -svfT 'redis-server' '{}' ';' 	; 		rm -r /usr/src/redis; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		redis-cli --version; 	redis-server --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"redis-server-sbom","packages":[{"name":"redis-server","versionInfo":"6.2.14","SPDXID":"SPDXRef-Package--redis-server","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/redis-server@6.2.14?os_name=debian&os_version=bookworm"}],"licenseDeclared":"BSD-3-Clause"}]}' > /usr/local/redis.spdx.json # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
RUN mkdir /data && chown redis:redis /data # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
VOLUME [/data]
# Fri, 05 Apr 2024 21:53:10 GMT
WORKDIR /data
# Fri, 05 Apr 2024 21:53:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Apr 2024 21:53:10 GMT
EXPOSE map[6379/tcp:{}]
# Fri, 05 Apr 2024 21:53:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1076c801a878edaff940bad7799813fe5cf569c2156cf21202f5cb915300c5b8`  
		Last Modified: Tue, 09 Apr 2024 15:26:23 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef0970f3a340d39b8e3fec1014c5cd01a604cc7331939a94a7d8cf836aec2b6`  
		Last Modified: Tue, 09 Apr 2024 15:26:23 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb55cfe2c9421883f4a6f960ad2af7674a2be278c51ba6b62af9526311d5a84`  
		Last Modified: Tue, 09 Apr 2024 15:26:23 GMT  
		Size: 1.4 MB (1403022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c563e80e75bc89727f3299882c74a25c162c5d8f6abaca490625831a84c7cd7`  
		Last Modified: Tue, 09 Apr 2024 16:03:37 GMT  
		Size: 10.5 MB (10453081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46e5b22c248f8f1f4e21d8380f94f8e063d4afb26173a656f98265911e9847c`  
		Last Modified: Tue, 09 Apr 2024 16:03:36 GMT  
		Size: 97.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3f344b764d32a5d8bc8155d90c8702a42024e34082363db1455cd16f063fef`  
		Last Modified: Tue, 09 Apr 2024 16:03:36 GMT  
		Size: 572.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `redis:6-bookworm` - unknown; unknown

```console
$ docker pull redis@sha256:c56bd2bdbccdaf6c53d66ab96685c490919c36bb4cdaf00f97669bf9b691912d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2276276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837f79b966064d1b4dc6b71bc4e2132bd71bf558f53af503feaca26ab71e3bc0`

```dockerfile
```

-	Layers:
	-	`sha256:180b570d9e4eedfe3a221429dfb78ba1088a6f56445b769c563f708d18219587`  
		Last Modified: Tue, 09 Apr 2024 16:03:36 GMT  
		Size: 2.2 MB (2239699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:129183320eba1580e564a430933b50508adcb6a1a08339699bb5b2fc9545ab02`  
		Last Modified: Tue, 09 Apr 2024 16:03:36 GMT  
		Size: 36.6 KB (36577 bytes)  
		MIME: application/vnd.in-toto+json
