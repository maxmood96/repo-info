## `haproxy:lts`

```console
$ docker pull haproxy@sha256:986a8103f4567650d741840d2e04ca496a71eff499e9ddd4c4651cee333d5903
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

### `haproxy:lts` - linux; amd64

```console
$ docker pull haproxy@sha256:b353c93a7bacbe9ef9c100ddf95a8f834c1dfcf501e653f5a1cee50c0ed271c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41794245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbe4a2d3f7c14125557bd0a4a73216ea3d3dfcc1bc7e3852798c97be0167260`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229cd65254c8d29e64420a80f0550f5bf7e26d3b9b1b00a6baa96d06b9feb0c2`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 3.5 MB (3495551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3e78690f452549b0e845935787ad2ba37424d3e4a5cdbf8e7d9b80a8f959d8`  
		Last Modified: Tue, 23 Jul 2024 07:15:13 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e3eb7719ee6ee432b7cb6c49c789165e0a63699ba9d3f3524846be0fba26d4`  
		Last Modified: Tue, 23 Jul 2024 07:15:20 GMT  
		Size: 9.2 MB (9170771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd0f6e5123f36b375aaefa6f925cbfab4e14e0a3fb6d837c25d635134970241`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:77fbf3f78e02c4ed60d462f68ee2e762790c13543f28f63eef9316d914e9acb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c08c2e6af07f2b831c594635e1c2808affe5ef1de8fe9b09be9574ad59be3b`

```dockerfile
```

-	Layers:
	-	`sha256:9348c501d2768a5df36cf25ed92d45f31c584cd3702aede70abb0448b580794d`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 2.4 MB (2360692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e503c4cd17071b13839f90b9617c2ccb1324024be8f058e27777e95863dd90f5`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 22.2 KB (22181 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:1daaf85bf6470c780c4ecd56512bbbe63ba7b927954b142a7d442077338b7f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39073648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83095605e7ad23c45a745bf625964dc6e1a6aaecd18d739169b228073a2b5898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:752589c0ca446e2e74ef0b8c412eabb01e2a8035cfec47b1d9630b9f704fbda7 in / 
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b695a3453560aacd42060f43ccf1cbd7d20412f50126ca6a469af38d3fe1e5b1`  
		Last Modified: Tue, 23 Jul 2024 00:01:19 GMT  
		Size: 26.9 MB (26887299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbdcc7ea3438c1cb10f3677e1d27d2e729f24896d15e18ddc8b11c73ce76788`  
		Last Modified: Tue, 23 Jul 2024 07:43:18 GMT  
		Size: 3.1 MB (3071471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b70f1fd4b164ab5d2f735b52cfa09bf1099705fa06ca3a79de73590be44240`  
		Last Modified: Tue, 23 Jul 2024 07:43:18 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8295099d5908489660d95e8df2fb53370ee351d3908124a11ba2837f18163a5`  
		Last Modified: Tue, 23 Jul 2024 07:44:44 GMT  
		Size: 9.1 MB (9113236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9ab3694d176598c8f6ce37361beb7d999aa8b7c377381b7b1cc74dc6266f3`  
		Last Modified: Tue, 23 Jul 2024 07:44:38 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:d08a65e079a5c5150b87d408be291501bfc20db0d3cc45eec23326072b4d6c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e122a853b5a9db63c5449bdd6ab07451145aabb901705f96bced14d1217fc25`

```dockerfile
```

-	Layers:
	-	`sha256:b58c6365eab2ddda6f1afc4df162ddd78ea4135e4bc0cb35a97ac5f2b9b251e0`  
		Last Modified: Tue, 23 Jul 2024 07:44:39 GMT  
		Size: 2.4 MB (2364115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce4deabd719f4364194cb21ba27fc417a8e4a8c7c9eb514793a3d38670fa7cf0`  
		Last Modified: Tue, 23 Jul 2024 07:44:38 GMT  
		Size: 22.3 KB (22310 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:702e40d70512c87a7392652864f07b5cf2457bd3c62b97c82ad087d00ba193ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36572856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcdc7af328bcfa29ffd11a30aa31cb9946d9e1db08ff40578ddb1161cdb2125`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:b3438b93a141bfac397342418c34c4fe554bd257eeee378da353577c3d2206ca in / 
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ec16b40bfa260bcfd3b351a12bda1032683bb7db1fc4a9630b03194691569e14`  
		Last Modified: Tue, 23 Jul 2024 03:06:55 GMT  
		Size: 24.7 MB (24718200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578321af5215cd54501fe4c4cf84286f40b41c7b6cee3c2f276720191b9e726b`  
		Last Modified: Tue, 23 Jul 2024 17:35:49 GMT  
		Size: 2.9 MB (2906302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b15e492026aab67d1cf4eb393cef17be680cdf971bf81a839003e6713d495b`  
		Last Modified: Tue, 23 Jul 2024 17:35:48 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b509a26b04db69ec13f5b30fd1256a93e8a534b1ba00b2720987132490848a93`  
		Last Modified: Tue, 23 Jul 2024 17:37:57 GMT  
		Size: 8.9 MB (8946713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b8fba7a24a5d3bafef4200d62bf89b8c89ed50b3a5397f124300e713dbe885`  
		Last Modified: Tue, 23 Jul 2024 17:37:56 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:0ded6c650c5f7815dab4240faa5e4fcfb7308a063d0e8a94b565cd840c790135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a2a40eac2405ee8cbaee5eac71b7eb990e209142a38f78c8e1488abf923a9c`

```dockerfile
```

-	Layers:
	-	`sha256:4bb41b6d2ab45402e78860c92458ea06c265badca59dbdb776e194e01fe91c41`  
		Last Modified: Tue, 23 Jul 2024 17:37:57 GMT  
		Size: 2.4 MB (2362950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d530a11971e73fb8ffc9fe90434bdb7225ae8392dd20a2db4363ca883ea3159c`  
		Last Modified: Tue, 23 Jul 2024 17:37:56 GMT  
		Size: 22.3 KB (22309 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:2cd021338def0d948ee7a8479d8c3ddb4aa4a04c16bae9ad3c0cae46127d7733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41639198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d2ba40e44f8337913118e112ec149d7cd1a6304115843b290165f8c70125b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6652c547cc81f93a744d1fd2d1e79d85326c60cd50215064e4b8aa72226ba7c0`  
		Last Modified: Fri, 12 Jul 2024 00:57:44 GMT  
		Size: 3.3 MB (3318940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8171de54bc15583c3905d9db008cd8cb12923a7b27832d135763c78dbd1780ab`  
		Last Modified: Fri, 12 Jul 2024 00:57:44 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b2990367f10f9ffb42d16b1257b13f150558bf228206a2459c2394fbd9fcb0`  
		Last Modified: Fri, 12 Jul 2024 00:57:44 GMT  
		Size: 9.2 MB (9162056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92482e0c2fcfced82fa7371a45d23984a7f831bd17e99a9e1bf3b913e83460a`  
		Last Modified: Fri, 12 Jul 2024 00:57:44 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:03aea2cc1cbccc85caaf72a5aa4849dc2f0b90ef05ff77b0596aedbd49357964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a91b9cb0ac8f37aaab6c3eaf6b0f38f15e2596aef356ab722de03039acb850a`

```dockerfile
```

-	Layers:
	-	`sha256:0098c3101e6c6e790d7f13c1451a57772c6664fd861d82fb755fc73affa985a0`  
		Last Modified: Fri, 12 Jul 2024 00:57:44 GMT  
		Size: 2.3 MB (2342037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b7ef4cdb05db7ff665494c23abc8607d29c6916c63a80aecb9c28b882598831`  
		Last Modified: Fri, 12 Jul 2024 00:57:44 GMT  
		Size: 22.5 KB (22539 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:3d066c5017b8ebec52b47159a20bb36884d19a3c0b3311d9d6cc62bdbe819803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42580661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31fb4f9b4d2b6908a4ce6768810acb8d16b42c5be20fa0cf17bd30db2a3f53d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:9b63a9d86a51a3d56d700d09e1152578d700ba4453d852325d8eb9896534f3ba in / 
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7fa64a47f35cb425a1275bff76c45df3b76d3ff6b07911737090b82e4f221e93`  
		Last Modified: Tue, 23 Jul 2024 03:57:51 GMT  
		Size: 30.1 MB (30144309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1694de207f5bd17d26dd7edc7bbe24f1e4719784d076cd3855c0639b44b0a5ef`  
		Last Modified: Tue, 23 Jul 2024 06:14:48 GMT  
		Size: 3.5 MB (3500279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78350e1ad452d67d6c5ec748cf668068c07a768f9cccb509d81fec4a55c1f20c`  
		Last Modified: Tue, 23 Jul 2024 06:14:48 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9725129355c68531b4041ed7b8b09783ede1696872269be92b2140051b59ed65`  
		Last Modified: Tue, 23 Jul 2024 06:14:48 GMT  
		Size: 8.9 MB (8934434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa464f8c15b13ba79a2168478dfca977d534a1430ebcb4f4b79beda3d4217c35`  
		Last Modified: Tue, 23 Jul 2024 06:14:48 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:007f7deb042380c9f40c2f7e1b10bcb6b7a2e4123ab60e85208735fa75c7918f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f398bccbe8097c4676a10cd46e33de9d6929016841761c92938d45336c5e9c7`

```dockerfile
```

-	Layers:
	-	`sha256:eb56231e1979518978b72f1265e7b4a224db3832a15cc02235217c2dcaa31fc6`  
		Last Modified: Tue, 23 Jul 2024 06:14:48 GMT  
		Size: 2.4 MB (2357809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:905ed80cae02bc4a3e31ab3e6462693fbd05659b92da91ae7ebc7f66aad559a9`  
		Last Modified: Tue, 23 Jul 2024 06:14:48 GMT  
		Size: 22.1 KB (22129 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; mips64le

```console
$ docker pull haproxy@sha256:79546924dc768c03f2c7666135c25d550eae06d71013f953ce886d69ef202a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41324788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e8bcc09b1a084f20d526809e82a9c01cd177c2f2fe34d90e1bb07fd8b04e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:23 GMT
ADD file:9a0f0c8ed27f6f2bb89272036da4d44a63dcaf43fb03528dd2d970fbe64ccc92 in / 
# Tue, 02 Jul 2024 01:18:27 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:cbefe199012545da86e0f461f1964dea0c9bab400e37766ee5f32b967423cf0b`  
		Last Modified: Tue, 02 Jul 2024 01:29:29 GMT  
		Size: 29.1 MB (29124929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1aa09befb1657b3197ac829db488481d15293f25c37f219f41fde4bc0dca78e`  
		Last Modified: Fri, 12 Jul 2024 01:00:42 GMT  
		Size: 2.9 MB (2892398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dad4977e891ea367fbf53890a2c9eb734cccd7b6938d176fbbb44cb77bcadf`  
		Last Modified: Fri, 12 Jul 2024 01:00:41 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb172235e5f26c46238073a39006b3195cebac8d4d1f99f4088370f6db098ecd`  
		Last Modified: Fri, 12 Jul 2024 01:00:43 GMT  
		Size: 9.3 MB (9305816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8796de9d8230090c5a9d791039fc3c7d72dfb66407567e61e2ea7dd2b6bdbb`  
		Last Modified: Fri, 12 Jul 2024 01:00:42 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:e21e663bf56810d0e56149bcf2ea1784fdcece506342a6cd8437c6842a3fd58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 KB (22025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9822714cfef7ae36d582062c734691e938983ee963ae6d9306bc48bb9882ea1`

```dockerfile
```

-	Layers:
	-	`sha256:a4b5a58041fb97828f604c1760d60ea9d9e93748aade1bf43d0c5c65272ed7fc`  
		Last Modified: Fri, 12 Jul 2024 01:00:41 GMT  
		Size: 22.0 KB (22025 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:0c504b8a053d40ee04e5de71001990d6541f2d0a90c4f70657e6e57d04a5fbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46508709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb89be86128f911c3b437a59c8f4a58e6357d7bdaa0410caa223ee5feb625ff5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:5cc77fc68bd67c95f4f51e07f554f0227244f40137fb23780dfc932a424e1b0b in / 
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4d94a6ac7a4136997b66aca74cb19ab0acecd94c24cada5ab7ab322f2467eb86`  
		Last Modified: Tue, 23 Jul 2024 01:31:12 GMT  
		Size: 33.1 MB (33122275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518b42bbe9382623778c38223fcb890ddc47c82077ad84ceb56f081e0a13fb80`  
		Last Modified: Tue, 23 Jul 2024 16:56:44 GMT  
		Size: 3.7 MB (3698357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaac5fc26399514413cc23851e2c7fb907d60c90e52136d69b861cc67914bfa`  
		Last Modified: Tue, 23 Jul 2024 16:56:43 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a23c3454fcb264d10af98683ea3424beee2054d0ff03b8587a0eaf1e877e6c`  
		Last Modified: Tue, 23 Jul 2024 16:59:08 GMT  
		Size: 9.7 MB (9686441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712a4881f3c7f64b2be6d4ae5011f727f76e1c6b90eff35c13b6c942d25270e3`  
		Last Modified: Tue, 23 Jul 2024 16:59:07 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:25b418fec154262419132f081764e9e6a76959b5e5010675479c381e21b8c972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5093259edc61d16e126816fdcd5adf886edc446322050b4805f485df710751de`

```dockerfile
```

-	Layers:
	-	`sha256:e956e6c44d70ff990312ad941a44eb958a096d19be6edf102eefe5b1db3825f3`  
		Last Modified: Tue, 23 Jul 2024 16:59:08 GMT  
		Size: 2.4 MB (2365017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88bd82618f51df1875ee723cb0f9cb48cd29cdba3d77d57f07e08a87b372272b`  
		Last Modified: Tue, 23 Jul 2024 16:59:07 GMT  
		Size: 22.2 KB (22248 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:e44c9d02265bcac94b8aec634ec50772f240175c9c041098e058b8bd5c553516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39709023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9a67366eb4ecfd39f0160697d85f20d41fe74925fff60b5d0476526182970a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jul 2024 17:13:29 GMT
ADD file:d8b037f30c0a2aeded43f72fe61531da3a0e449e034255bb0a7b2182e4e3ca8a in / 
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["bash"]
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_VERSION=3.0.3
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.3.tar.gz
# Thu, 11 Jul 2024 17:13:29 GMT
ENV HAPROXY_SHA256=39a73c187a0b00d2602cb3ffca52d1b59d90f09032734fe8c03eb2e29a7d19df
# Thu, 11 Jul 2024 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jul 2024 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jul 2024 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jul 2024 17:13:29 GMT
USER haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jul 2024 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:48319744c6dacda7d13413becf85a83639982e97ecf615295a1257ccc3082721`  
		Last Modified: Tue, 23 Jul 2024 02:32:44 GMT  
		Size: 27.5 MB (27490099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ee41ae5a3500650cabbbc0997c64f33eb8d9b4752a8511010719ad8b081839`  
		Last Modified: Tue, 23 Jul 2024 16:13:33 GMT  
		Size: 3.2 MB (3160226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f50db47e65b423f68540632572c47b42d9ce729b8ac0487b75b7ae23d78fc`  
		Last Modified: Tue, 23 Jul 2024 16:13:32 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8bd6ae64bf0661f2d3190a5817a861229f3f7bbee924aba8116b4b793b7601`  
		Last Modified: Tue, 23 Jul 2024 16:16:00 GMT  
		Size: 9.1 MB (9057061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b589cf958f09dbe0eef016dd5fc69d17b639f29f9cc887ad3a281e947ccf8d86`  
		Last Modified: Tue, 23 Jul 2024 16:16:00 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:566b521e99875d59c1e1528b01899816d89751b32e522482ca4ff0bbd859055e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994c9b71dafc30214ed521227408d44b1cae42238cdc61d531bc58cb0e407a7b`

```dockerfile
```

-	Layers:
	-	`sha256:fb361a4cd1e4f6f1900bd0ac3a4fc24ac27c17b5425cd07b223528fb48bd02a3`  
		Last Modified: Tue, 23 Jul 2024 16:16:00 GMT  
		Size: 2.4 MB (2360521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d561453caa6ec3c57a7137f5362918e913c3e95593eb6a9fc23d859d72cdebe`  
		Last Modified: Tue, 23 Jul 2024 16:16:00 GMT  
		Size: 22.2 KB (22182 bytes)  
		MIME: application/vnd.in-toto+json
