## `haproxy:lts-bookworm`

```console
$ docker pull haproxy@sha256:7cb77fbf43c42aec2070c9bccc8b0fd1c70d9247e221153b92df7680a749417c
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

### `haproxy:lts-bookworm` - linux; amd64

```console
$ docker pull haproxy@sha256:d7699076320bd929293325e3950168d630a11c1af25b900ab28c7e10359b6f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41137958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f968998619ef8164b21a98848a2a8666a9fa98c0fc37b3a7267ee21a959555`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 22 Apr 2025 17:22:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_VERSION=3.0.10
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.10.tar.gz
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_SHA256=d1508670b6fd5839c669a0a916842f0d3d3d0b578bb351a2a74a1de3d929ce26
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
STOPSIGNAL SIGUSR1
# Tue, 22 Apr 2025 17:22:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 17:22:04 GMT
USER haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
WORKDIR /var/lib/haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c43fdade0fcc74e60c6bb35389155e6c50bdc14b10c8e9a04497c28179fc6f`  
		Last Modified: Wed, 21 May 2025 23:13:01 GMT  
		Size: 3.5 MB (3500683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f412ea5827377b31584872df03a5d2e9a92a03d41cd430a96714988f29c102f2`  
		Last Modified: Wed, 21 May 2025 23:13:00 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a326d6dac51502b63d0a7ef193d5e8b3d9b07146eecee5a69eae1093d3fe71d5`  
		Last Modified: Wed, 21 May 2025 23:13:01 GMT  
		Size: 9.4 MB (9410308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb54010662a818a38661578c65043696532b01fafb78aea3de4d051d4cdc8a5`  
		Last Modified: Wed, 21 May 2025 23:13:00 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:eae02aee7b5b4a0dd3a7b14704254808b5cb04017609c98e2622baf55dc74880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2409648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f6ccf8df410af5f33996b8f1f57c4f6f8a4a83fe8ee9abbb463ba85dc038a0`

```dockerfile
```

-	Layers:
	-	`sha256:62516a022bac0265a01665ba7afa05da07e95e1722d8733928f421a4431fffd7`  
		Last Modified: Wed, 21 May 2025 23:13:01 GMT  
		Size: 2.4 MB (2387866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b58fdb5ab828df90796b0d4111132c43f4ccb2b1d81d7b45e633bc74cbda40`  
		Last Modified: Wed, 21 May 2025 23:13:00 GMT  
		Size: 21.8 KB (21782 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:3d2dd9162476a16b4886a48f26c4bd51efe97fe5cb7503e4ba420e3f08555a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38211463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa51f80507551e0220683aaa9802ef552d1ab4e863cd979d2500a719411af20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 22 Apr 2025 17:22:04 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_VERSION=3.0.10
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.10.tar.gz
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_SHA256=d1508670b6fd5839c669a0a916842f0d3d3d0b578bb351a2a74a1de3d929ce26
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
STOPSIGNAL SIGUSR1
# Tue, 22 Apr 2025 17:22:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 17:22:04 GMT
USER haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
WORKDIR /var/lib/haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cec91862f6b0af3546519f4ea28af82d237d43022aaf48b743c0a50d31b1931`  
		Last Modified: Wed, 21 May 2025 23:14:35 GMT  
		Size: 3.1 MB (3074542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ca83a05b3cb93622aded85f3de8d18e78ff62c7fef4218608d087416f1dcc5`  
		Last Modified: Wed, 21 May 2025 23:14:35 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373680b7d23edc99b23aba068e7ea6dfd3bad2f0568395ccd3de5cdb9fe5ab40`  
		Last Modified: Wed, 21 May 2025 23:16:32 GMT  
		Size: 9.4 MB (9378384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642c3f7868d269c9b9b8a16b2523d89c191696483a716840c85b293b916f0bfe`  
		Last Modified: Wed, 21 May 2025 23:16:32 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:fd0d6e5de612d255d8b7ca0c07640f1a293aafdaad49c6fb5c853c59cb69b72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2413588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433e4b061b5024d8858123ba6cf819d2376387f1d292d9683deae16e14997799`

```dockerfile
```

-	Layers:
	-	`sha256:a5c9a8c39e2e33a216e8c76e762a9d73db0e9a5d1ae97f6959bc5b634b6378d7`  
		Last Modified: Wed, 21 May 2025 23:16:32 GMT  
		Size: 2.4 MB (2391688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f756f0bc60ed0b00edb0a404bda548a3514fde4c7bf4ee3326ce85dfd786429`  
		Last Modified: Wed, 21 May 2025 23:16:32 GMT  
		Size: 21.9 KB (21900 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:d8f4a5390933e1f8fd57bd893e81f06fad09913ac9d0fde4610be1f0eb6bb4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (36042077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00e602654970a570c60019bf0552fcdd3ab42a4cb6513e4de157ba8ccb091828`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 22 Apr 2025 17:22:04 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_VERSION=3.0.10
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.10.tar.gz
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_SHA256=d1508670b6fd5839c669a0a916842f0d3d3d0b578bb351a2a74a1de3d929ce26
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
STOPSIGNAL SIGUSR1
# Tue, 22 Apr 2025 17:22:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 17:22:04 GMT
USER haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
WORKDIR /var/lib/haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99f1fd0040c720090a4a658b14eddcebacfa8e9ceea1496ac57e2d4a4473ba6`  
		Last Modified: Wed, 21 May 2025 23:16:09 GMT  
		Size: 2.9 MB (2910204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49389a80416baa4290cafa447e8be5a444ed0af7ba0590671f07fd1fe15426a4`  
		Last Modified: Wed, 21 May 2025 23:16:09 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27adda23cebea2837fe1863c88525da779afc7bed3800f6de0d31f71a04c52b3`  
		Last Modified: Wed, 21 May 2025 23:18:04 GMT  
		Size: 9.2 MB (9197313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e107f2baae7824509a10235dd7cf19d0d95c00325034ac41737ccdc0e403097`  
		Last Modified: Wed, 21 May 2025 23:18:04 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:d493773894a09288a14fadda7440d3d7e2a4b47ce6b6401ba7604e64c99acebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2412009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c5e1313ce35cb642989881f1b85bcbe5cdb211fa5ddfe75fb8ee0edb72d0ba`

```dockerfile
```

-	Layers:
	-	`sha256:fb6881fdbffec79054b590708ea4f45f24b4abfecbdbeb89674047aa68aa421d`  
		Last Modified: Wed, 21 May 2025 23:18:04 GMT  
		Size: 2.4 MB (2390109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0607e5eb0d850e94e9df1170bf5a6043fdcd46ac56e30c9f574374d414473e60`  
		Last Modified: Wed, 21 May 2025 23:18:04 GMT  
		Size: 21.9 KB (21900 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:fba5838fc1912e98ba60e22c4c732d8fd0ef6e11ac4ea457d370fcd0505737fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40794712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fad51a1049014de1de99cde37c77510c4100b147c85f64163214f2d021ad6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 22 Apr 2025 17:22:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_VERSION=3.0.10
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.10.tar.gz
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_SHA256=d1508670b6fd5839c669a0a916842f0d3d3d0b578bb351a2a74a1de3d929ce26
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
STOPSIGNAL SIGUSR1
# Tue, 22 Apr 2025 17:22:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 17:22:04 GMT
USER haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
WORKDIR /var/lib/haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd4fd474e07a8fbfb9f0c17f4bf095afca6ad25cb455ffa5586ef48224d0ff5`  
		Last Modified: Wed, 21 May 2025 23:15:54 GMT  
		Size: 3.3 MB (3324393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74952c534a8157841fa2bb92a773b87d89be798e02e8eefabc939e5988c31d92`  
		Last Modified: Wed, 21 May 2025 23:15:53 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9685925a955b8c8d6f25b50abfe0e3aaf25f3bd33a4663810ad72bc5910626`  
		Last Modified: Wed, 21 May 2025 23:17:27 GMT  
		Size: 9.4 MB (9403405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe70d74ee8b49b7bc6b840b10f8cfff498ba3199747fc73a849b525f90e4373`  
		Last Modified: Wed, 21 May 2025 23:17:27 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:ffdc7cba8e133b20668f78c7c9ec841b59c6a12553e7c025f708ff3706fcc42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2410088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e756736f7cc31543666bc5ea0a34ee979af51c2e9440567bcacb8bdfe5e6270`

```dockerfile
```

-	Layers:
	-	`sha256:a7efda94d5f682d7f54932af9497ba9f1dfae98348db1c629b5c66b698211cd8`  
		Last Modified: Wed, 21 May 2025 23:17:27 GMT  
		Size: 2.4 MB (2388149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0ecc597c55c2762dc18dec5a53c618a1fd00b32aea253739f03035de7682098`  
		Last Modified: Wed, 21 May 2025 23:17:27 GMT  
		Size: 21.9 KB (21939 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:ab5ffc35c55ba4ca984f863bc8754d7eda0b9a489e64f88258838f65e245c6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41873079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe37b44aa6b991948047d51373821b19a04756168f9c0e05a3552a962cc54883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 22 Apr 2025 17:22:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_VERSION=3.0.10
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.10.tar.gz
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_SHA256=d1508670b6fd5839c669a0a916842f0d3d3d0b578bb351a2a74a1de3d929ce26
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
STOPSIGNAL SIGUSR1
# Tue, 22 Apr 2025 17:22:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 17:22:04 GMT
USER haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
WORKDIR /var/lib/haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356bc6bfc45a9dfc2370e3baa2c19d1d0e0d34fb0f5e0c932b23c2d03f56f704`  
		Last Modified: Wed, 21 May 2025 23:13:37 GMT  
		Size: 3.5 MB (3506033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e572fb9b44be0945a8ef9b7ae669bc3d9a2df5d8d4755949494283194f8845a`  
		Last Modified: Wed, 21 May 2025 23:13:37 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c369472805fa38ccae146e81e5b7cfadd221a39e7c245c5e603827edc391bb2e`  
		Last Modified: Wed, 21 May 2025 23:13:37 GMT  
		Size: 9.2 MB (9157917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edf84099020d30b2f91d7b9941c49370e8c9888e3b848b3740663d7af2c2225`  
		Last Modified: Wed, 21 May 2025 23:13:37 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:75bd7f5929a56b81da82db822207913ae1ae5b565b44ad25810b965a1d78a949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2406771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d46ce4ec9be686f6e2cd5dce7c0ce8b221cc8609dce7b38729dd12d633a32f`

```dockerfile
```

-	Layers:
	-	`sha256:5a37f149c9a351f5cd00563fae3423a109a1038d92bae28dc44549ea6a2970df`  
		Last Modified: Wed, 21 May 2025 23:13:37 GMT  
		Size: 2.4 MB (2385035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5eaae92eccf3e58ce2da68da51b9953a9de88a1f78d18a36435a934a555e890`  
		Last Modified: Wed, 21 May 2025 23:13:37 GMT  
		Size: 21.7 KB (21736 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:d346b30c69f3f88231e107327a649119c5c90458f1ed4b84c6e4db52a3a793be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40938115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671bc1c721c6e150bf4517903e0c4e7339148e566c7991a3003f6bf0dbbb495d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 22 Apr 2025 17:22:04 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_VERSION=3.0.10
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.10.tar.gz
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_SHA256=d1508670b6fd5839c669a0a916842f0d3d3d0b578bb351a2a74a1de3d929ce26
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
STOPSIGNAL SIGUSR1
# Tue, 22 Apr 2025 17:22:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 17:22:04 GMT
USER haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
WORKDIR /var/lib/haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65747dc904d40ad67cb8c68d41158cb757807a395c02b6056d6f2867999d7e7`  
		Last Modified: Wed, 21 May 2025 23:26:50 GMT  
		Size: 2.9 MB (2897333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47714184055b24aa5ffc9f1fd9442891a7266736121baf880538ac4450883b7`  
		Last Modified: Wed, 21 May 2025 23:26:49 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c67d807848c9b3171867a56253b37f3a47009a30460899258d3ed4bc6c50dfb`  
		Last Modified: Wed, 21 May 2025 23:31:46 GMT  
		Size: 9.5 MB (9527292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0289e3ffb32915483137e67469ddd3c4216838d15f78de1e7a4a757fd3dd05e9`  
		Last Modified: Wed, 21 May 2025 23:31:45 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:8b94344ff543d31ea217877004ae29117c9d7f124774a6a844357d5b8790a49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bcd5713847520910f790bb33c6154cf3a1636f58f01bff22486570da1584c2`

```dockerfile
```

-	Layers:
	-	`sha256:7fd0eacf57d748570d8c2ad4f872157a2a002b5098a7ca26d4438f97f2407d19`  
		Last Modified: Wed, 21 May 2025 23:31:44 GMT  
		Size: 21.7 KB (21657 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:c372998f19474cd7ce718bed348d49755ad55f17b7431f054ebbad493c01fa32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45673208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e9ebe3f2aed28cb09f5fada19d89b32471b1ca45f05e1c382122eae6794bcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 22 Apr 2025 17:22:04 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_VERSION=3.0.10
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.10.tar.gz
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_SHA256=d1508670b6fd5839c669a0a916842f0d3d3d0b578bb351a2a74a1de3d929ce26
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
STOPSIGNAL SIGUSR1
# Tue, 22 Apr 2025 17:22:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 17:22:04 GMT
USER haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
WORKDIR /var/lib/haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333c23e8b70b76b8ea0de8337d8ad3f29324110bfc586436fb95d2fb99913a45`  
		Last Modified: Wed, 21 May 2025 23:16:22 GMT  
		Size: 3.7 MB (3705099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaf42d45280fc5f18a64f8f5e033381ff53e2d578f85763c8a3d1b242bec66f`  
		Last Modified: Wed, 21 May 2025 23:16:21 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0430a49cee5c8fe8ddbf55a6691631cb0df41a14310c4d5034119c1888ef7b32`  
		Last Modified: Wed, 21 May 2025 23:19:16 GMT  
		Size: 9.9 MB (9899559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e18715fe016c70a99bca9508c1fbf6dd82870c1b35864aef51559c0d3f3a14`  
		Last Modified: Wed, 21 May 2025 23:19:16 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:3a5c3c20707d48a833c8d8b19b38aeba733efeea4c8821dac3b23258d2c7ec71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2414115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e0bde1e59ec406bf88d6e1d36186e6c6b68fdf18d572ce05ba7e8eebe18985`

```dockerfile
```

-	Layers:
	-	`sha256:2dd53a13db1ff168a52af31471c9f70c98665aeaba718375b51a9da6aea24591`  
		Last Modified: Wed, 21 May 2025 23:19:16 GMT  
		Size: 2.4 MB (2392274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f9ed93b5a79bbdb78666e3ee18367300d5dff9ae6833bd3f071169f9e71ab47`  
		Last Modified: Wed, 21 May 2025 23:19:16 GMT  
		Size: 21.8 KB (21841 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:9085c13fbbb3e9c5b1253b8b8978303ce670ca7ea1a0d7a78a7236e6935b3ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39323692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f5253bd714bfe862d3f0b01e7aec5e2dafa0bceb589004e00973028e30674d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 22 Apr 2025 17:22:04 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_VERSION=3.0.10
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.10.tar.gz
# Tue, 22 Apr 2025 17:22:04 GMT
ENV HAPROXY_SHA256=d1508670b6fd5839c669a0a916842f0d3d3d0b578bb351a2a74a1de3d929ce26
# Tue, 22 Apr 2025 17:22:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
STOPSIGNAL SIGUSR1
# Tue, 22 Apr 2025 17:22:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 22 Apr 2025 17:22:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Apr 2025 17:22:04 GMT
USER haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
WORKDIR /var/lib/haproxy
# Tue, 22 Apr 2025 17:22:04 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d7d5016f6fa7406fa5aee32e37a634f773eeeb24cb33a615911aafc2b4ea60`  
		Last Modified: Wed, 21 May 2025 23:15:27 GMT  
		Size: 3.2 MB (3164900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6a4656f73b2a30957e366bdca0a83d815be606b2edad650b7f7b994a7110cd`  
		Last Modified: Wed, 21 May 2025 23:15:27 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26092b60b21166ce7461d95f49c7fe6c0eb324c316c315304d04c7893733a3b3`  
		Last Modified: Wed, 21 May 2025 23:17:29 GMT  
		Size: 9.3 MB (9274345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0908488088614fcff99c29da9ab1e93fcd1526af6aa28ce0e6eb17be10a8d8e3`  
		Last Modified: Wed, 21 May 2025 23:17:29 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:e54de528d23c375a168797da0ccb4ce5b0b39294e2534e7cf7ed820bc9ad60e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2409369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82d5eb230f24f901a3549e20c4d36ee6d450d03fe37589375a5ea0e40062c0b`

```dockerfile
```

-	Layers:
	-	`sha256:eda0607f5d123bc562bf9c3aa060e85ddd971fda1c9f1bd540c3c12e645556b3`  
		Last Modified: Wed, 21 May 2025 23:17:28 GMT  
		Size: 2.4 MB (2387588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:255f5329d5524aff9e1e6ed25715bffcd99aef64d1134bf05a36c30af6aae166`  
		Last Modified: Wed, 21 May 2025 23:17:28 GMT  
		Size: 21.8 KB (21781 bytes)  
		MIME: application/vnd.in-toto+json
