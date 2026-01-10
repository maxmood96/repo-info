## `haproxy:lts-trixie`

```console
$ docker pull haproxy@sha256:f7c4770cb573796473ffbf2f18843376ecc9ca8e109bea48cadbd1b94e5e0c5d
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `haproxy:lts-trixie` - linux; amd64

```console
$ docker pull haproxy@sha256:63421f7bd3473b6559f29aef7b90501b0b32d896287a05299a58534ce88b7bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44468646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e22cdedb9012e2191df97026a295aca2fda44ef3f0b21f595410996b30c330dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Fri, 09 Jan 2026 18:02:54 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 09 Jan 2026 18:02:54 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:03:37 GMT
ENV HAPROXY_VERSION=3.2.10
# Fri, 09 Jan 2026 18:03:37 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Fri, 09 Jan 2026 18:03:37 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Fri, 09 Jan 2026 18:03:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:03:37 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:03:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:03:37 GMT
USER haproxy
# Fri, 09 Jan 2026 18:03:37 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:03:37 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a263f66e011a087dcf2bd63e1da2bf12d411e03626af3cd33d52b093d89d6a6`  
		Last Modified: Fri, 09 Jan 2026 18:03:53 GMT  
		Size: 1.6 MB (1580903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bed7cd9312087979b597031d69e23b17e88f749151f6d07979f64698bbe0b`  
		Last Modified: Fri, 09 Jan 2026 18:03:53 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23caac861f53e0fffb0df001ffa71bb4da2a04e73bf002160832483d6dce87fd`  
		Last Modified: Fri, 09 Jan 2026 18:03:56 GMT  
		Size: 13.1 MB (13109568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79efe4e80edda6a7b33631e217e390e81f3cba38c3690caaf2d0149240f64e6`  
		Last Modified: Fri, 09 Jan 2026 18:03:53 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:12aaac3e15807389444a3730c0c2993fa8743201696c8b2e1b796afbe8a041bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bf39d14a295c8356104602a9dfce6e6f561ce9176b5c18dd885e9638dd2ba8`

```dockerfile
```

-	Layers:
	-	`sha256:4714491571fa05e4caf4fd5664867be117ca1d1324f3df0b873732352a9689f1`  
		Last Modified: Fri, 09 Jan 2026 20:02:01 GMT  
		Size: 2.1 MB (2113708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c7653b2428b9fc89c22d0aab363ac5577804a58eed94b6a461cef817ba9b7a8`  
		Last Modified: Fri, 09 Jan 2026 20:02:02 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:5bdb336545a58b11822716bea2982febf2542ca7b34a32289428ca8bf2a2b8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42732307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc79367daa6cffbcb93a00375a6a0bf15e29824bfb13743534d13cd5e16d3673`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Fri, 09 Jan 2026 18:03:39 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 09 Jan 2026 18:03:39 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:04:35 GMT
ENV HAPROXY_VERSION=3.2.10
# Fri, 09 Jan 2026 18:04:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Fri, 09 Jan 2026 18:04:35 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Fri, 09 Jan 2026 18:04:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:04:35 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:04:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:04:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:04:35 GMT
USER haproxy
# Fri, 09 Jan 2026 18:04:35 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:04:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe2d29559591c117dbd4adc1b64087153d5c6e682fbb6d3155d7287711a89bf`  
		Last Modified: Fri, 09 Jan 2026 18:04:49 GMT  
		Size: 1.5 MB (1534778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4208ee7115d1b30cf235c835f9c277cea0071c16cfe161a44a0a0da5136e7f9`  
		Last Modified: Fri, 09 Jan 2026 18:04:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170ff5da070972d3dc02da8c7816a6f3445c35efc83b0dea3f3bdcdc67837d83`  
		Last Modified: Fri, 09 Jan 2026 18:04:50 GMT  
		Size: 13.3 MB (13251742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e3a0872e1cbd81adcd405553ec5e05dcd2e4da482f3cba85a9b60480505018`  
		Last Modified: Fri, 09 Jan 2026 18:04:49 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:d3e5342cfdfb4441709f372ab19ccf59e78ffba2cc965cd848ec9e57c4166735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a386d425cbf2274dc8fd013e133a09e8e5dce18de629311426eae6566f86bb`

```dockerfile
```

-	Layers:
	-	`sha256:5c99ca50b888d6e9646551767afd8c3e8fe47424269b7be6af4efd2e0e08b954`  
		Last Modified: Fri, 09 Jan 2026 20:02:06 GMT  
		Size: 2.1 MB (2116688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0e6e092e5deb7e0fbcb58a47f6c144b941b48d0ce775644e946e09bb5c6543c`  
		Last Modified: Fri, 09 Jan 2026 20:02:07 GMT  
		Size: 22.5 KB (22471 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:c9a69ac2c5bea59c1dc5f856a124c31f6ce2fd8dc883f26c2a951cc575a7f36f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40706201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41777eba77a762d338d6983d0c1efe21041680803380eade6c574f65f359cb40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Fri, 09 Jan 2026 18:04:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 09 Jan 2026 18:04:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:05:14 GMT
ENV HAPROXY_VERSION=3.2.10
# Fri, 09 Jan 2026 18:05:14 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Fri, 09 Jan 2026 18:05:14 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Fri, 09 Jan 2026 18:05:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:05:14 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:05:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:05:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:05:14 GMT
USER haproxy
# Fri, 09 Jan 2026 18:05:14 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:05:14 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8ad5969c6e35b2ac8d59cddf3c0a7b3b560c81bc0f8bb6337b4844b505fe98`  
		Last Modified: Fri, 09 Jan 2026 18:05:27 GMT  
		Size: 1.5 MB (1488832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d843745b9a38b2145f474c92dcc747ddbeba2d0007f53239b7c85395fade6ff0`  
		Last Modified: Fri, 09 Jan 2026 18:05:27 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1461a28b1fcbceef9e0c7e6fae8dabd7f829560213a457f05af922a4c6d5df92`  
		Last Modified: Fri, 09 Jan 2026 18:05:28 GMT  
		Size: 13.0 MB (13005726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2643b8ce311b734e100def13344bf62c7a06c14e254961df89cd36e5cf7c5d`  
		Last Modified: Fri, 09 Jan 2026 18:05:27 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:38ec2e904d6e4b567a5014574e7adf8e832af24339e49879052ddb3a615104fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1633e838c42ecfc28d39659a03d3a07610f75696cb8e15349db9e2a10b3239e9`

```dockerfile
```

-	Layers:
	-	`sha256:f88ffbb01604b10d8629b7108890be88da4d6f95ae79b37d2a33a7eea516c16b`  
		Last Modified: Fri, 09 Jan 2026 20:02:11 GMT  
		Size: 2.1 MB (2115131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec8b00aed984188db37818f29c98604d8e403704254ee510eea58b35bb27b5e`  
		Last Modified: Fri, 09 Jan 2026 20:02:12 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:619accb2d1b5bcb1048f9194c00bc4d630621794f3e3d8e901a6bcaf48d41fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44719921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec00f7d5425a9c80e78474c17d8f7c1f78733e512e159dc1e8785a335917caa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Fri, 09 Jan 2026 18:04:33 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 09 Jan 2026 18:04:34 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:05:16 GMT
ENV HAPROXY_VERSION=3.2.10
# Fri, 09 Jan 2026 18:05:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Fri, 09 Jan 2026 18:05:16 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Fri, 09 Jan 2026 18:05:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:05:16 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:05:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:05:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:05:16 GMT
USER haproxy
# Fri, 09 Jan 2026 18:05:17 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:05:17 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6971defb07e994b28da537ac6944698c033e8e5a91b24a02982a319795f08a81`  
		Last Modified: Fri, 09 Jan 2026 18:05:31 GMT  
		Size: 1.6 MB (1563671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9e9a025a4b482954deddddc601b9fe7420082ee2d6c1ad9f3ea1d36fd0121b`  
		Last Modified: Fri, 09 Jan 2026 18:05:30 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ae5064ac2f8313b0f2451a257e5657ec141b3148eb029efc590fdede148106`  
		Last Modified: Fri, 09 Jan 2026 18:05:31 GMT  
		Size: 13.0 MB (13015971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3466827a7e906a44166f861aefe35a2982783034e7224b9da3544632487ae9e0`  
		Last Modified: Fri, 09 Jan 2026 18:05:31 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:16fafb55d72f2fc4865c43173e7d2cf0f03bf74c96e35a3947f2225a730113f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bd69958f36a5d5d74616764a6e8280d8547bf77410038411e466f6d98e09a6`

```dockerfile
```

-	Layers:
	-	`sha256:6b6f98c6cea73bee0e26343976efb892fdf74bc42429bf0122f9a5e5eb346ba5`  
		Last Modified: Fri, 09 Jan 2026 20:02:16 GMT  
		Size: 2.1 MB (2113993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a264b03365610e80a721edcab6c98845aa66cc5c39c9f90984cfa69ff1227c`  
		Last Modified: Fri, 09 Jan 2026 20:02:17 GMT  
		Size: 22.5 KB (22508 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; 386

```console
$ docker pull haproxy@sha256:9e68eb6c140fc2191bd89bd39084152d6d73b02689e63a2eff05780d1d6beb37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45701681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec38dc6e2c1b60d44ea57be507c275550db528e487f7b8b88f52487a37814c6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Fri, 09 Jan 2026 18:04:10 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Fri, 09 Jan 2026 18:04:10 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:05:02 GMT
ENV HAPROXY_VERSION=3.2.10
# Fri, 09 Jan 2026 18:05:02 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Fri, 09 Jan 2026 18:05:02 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Fri, 09 Jan 2026 18:05:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:05:02 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:05:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:05:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:05:02 GMT
USER haproxy
# Fri, 09 Jan 2026 18:05:02 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:05:02 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bc90a614a178bfd53fcd433268ff658330105c793b78117d0e4803ca4e068e`  
		Last Modified: Fri, 09 Jan 2026 18:05:14 GMT  
		Size: 1.6 MB (1603071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cf319f98c93e27835f084709b2b9f8a1edff56f84acdfbc3c0939d00e2541b`  
		Last Modified: Fri, 09 Jan 2026 18:05:03 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ccc767c430bc18a443e2a1d3715cb7788abdbace79ba907d2ccd11ef059740`  
		Last Modified: Fri, 09 Jan 2026 18:05:15 GMT  
		Size: 12.8 MB (12803869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a5bd36bb0f541ea0b9cad5f17f083284972fd211662f9a80563560a48037cc`  
		Last Modified: Fri, 09 Jan 2026 18:05:13 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:879f7a1d34e5faf13391629bea585d36d68ae921780c68b643583f018b78ced1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410397c40cd986dd27f254fac341a60b0a8e42e4365987bee5c5084ac40f1ffc`

```dockerfile
```

-	Layers:
	-	`sha256:90096388c7dca9b50376f450c075e8e2b3967efe150e736690dc3a991f6968c8`  
		Last Modified: Fri, 09 Jan 2026 20:02:21 GMT  
		Size: 2.1 MB (2110889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:078ab87b94c2e5cfb4167da16ae3a8fbc105d7b0d956e1c62735724724df7672`  
		Last Modified: Fri, 09 Jan 2026 20:02:22 GMT  
		Size: 22.3 KB (22304 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:74cbbe15174339202ba348fdee47f183845f8e4e8b0080ff21e4b7d9a4e438c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49041299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4b751190d39d7e0f45abef6db6f72714a4b4d8cf935564170b96b7668e3524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 16:12:01 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 07 Jan 2026 18:24:59 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:06:15 GMT
ENV HAPROXY_VERSION=3.2.10
# Fri, 09 Jan 2026 18:06:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Fri, 09 Jan 2026 18:06:15 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Fri, 09 Jan 2026 18:06:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:06:15 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:06:16 GMT
USER haproxy
# Fri, 09 Jan 2026 18:06:17 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:06:17 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809f05bbafbf395501c9631726ea2b1e6a0670e50f85d034886473ac29795493`  
		Last Modified: Tue, 30 Dec 2025 16:13:56 GMT  
		Size: 1.6 MB (1638947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e0ee5e04d7241488d8e08a9188b542e5d81e69a99ae1cf95efd9f767b893bc`  
		Last Modified: Wed, 07 Jan 2026 18:26:45 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8a400b296c8e86158c3fdf35c6965ac7a32c8aef97615a714feb64c7c78d4c`  
		Last Modified: Fri, 09 Jan 2026 18:06:42 GMT  
		Size: 13.8 MB (13803817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd270ad2e5c581aa64f797f14bc602b1c7183873c1e3bc781220a86849661a`  
		Last Modified: Fri, 09 Jan 2026 18:06:40 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:a601f79846f9f7a3cfa768e023bfc5e25ace257c88086616c382cf7a880ff6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9c63164109ee4ea9b59cd989c53c1a190582d1818c29fc6367d0a7800d662e`

```dockerfile
```

-	Layers:
	-	`sha256:8028a71477282c4f3f974023a0f947c0c4c7be6b8c4514f84260016419a36f4e`  
		Last Modified: Fri, 09 Jan 2026 20:02:26 GMT  
		Size: 2.1 MB (2117254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:893e49c527fb9a9020c997795af366bf567c8737d93ea7fe853c81dd884d86aa`  
		Last Modified: Fri, 09 Jan 2026 20:02:27 GMT  
		Size: 22.4 KB (22410 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:5059235cb93d45ccc80e3a027ea0b16fffc6f6a33b704cb968a96b5e038a203c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42523120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153f618795b5ea353b8a7c0efc65b675498f2e2393e20e319428c4169ff1ae6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:30:07 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:30:08 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 19:25:00 GMT
ENV HAPROXY_VERSION=3.2.10
# Fri, 09 Jan 2026 19:25:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Fri, 09 Jan 2026 19:25:00 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Fri, 09 Jan 2026 19:25:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 19:25:00 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 19:25:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 19:25:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 19:25:00 GMT
USER haproxy
# Fri, 09 Jan 2026 19:25:01 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 19:25:01 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c306661d9ddb361973108b269c5a7a80f6657e752a63c49de5f7c724708b5cb7`  
		Last Modified: Tue, 30 Dec 2025 01:44:32 GMT  
		Size: 1.5 MB (1535079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0931f081a7c2f17b5783986400a9a24b12cba9370be682d4eb23cc8e328befc2`  
		Last Modified: Tue, 30 Dec 2025 01:44:31 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52ee522055ab68ac625b67b9896b40a60c207ed959474ceca03c103f7b49f30`  
		Last Modified: Fri, 09 Jan 2026 19:26:20 GMT  
		Size: 12.7 MB (12713271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c597527515dc974750396c2e16156a5a139aff4128be648308a2829fed8853ee`  
		Last Modified: Fri, 09 Jan 2026 19:26:19 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:cc476cd2d61023923fa6922de61f99e38c1887ab28de61bc67c444e9b7e396b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f200f663d1bc49d69e0e2b56aea6867384fb332025fe49cd097c40f5408bd12c`

```dockerfile
```

-	Layers:
	-	`sha256:55cfdc1791b6fe4ea9a411be23ff60161fdf67abdf173bc317fe51be05e8d5f0`  
		Last Modified: Fri, 09 Jan 2026 22:59:29 GMT  
		Size: 2.1 MB (2107645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd369834f4df5854a05bc58cc9316d5a589d838b50d078ac959a976634778d1c`  
		Last Modified: Fri, 09 Jan 2026 22:59:30 GMT  
		Size: 22.4 KB (22410 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:d5bc33d4595ab49bd10fe434cf5805dda8cfcf175246ced75f33e203f60f410d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44858190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15811b955c3d44c6b70d0f8f7d1f0428f2f2ab33df49da9bd273626bda742ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Wed, 07 Jan 2026 18:25:13 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 07 Jan 2026 18:25:13 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 09 Jan 2026 18:04:17 GMT
ENV HAPROXY_VERSION=3.2.10
# Fri, 09 Jan 2026 18:04:17 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.10.tar.gz
# Fri, 09 Jan 2026 18:04:17 GMT
ENV HAPROXY_SHA256=df9412eee0faf78147cd3f1bbec9582ea678c33535b1afec081036c5bbb8015b
# Fri, 09 Jan 2026 18:04:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 09 Jan 2026 18:04:17 GMT
STOPSIGNAL SIGUSR1
# Fri, 09 Jan 2026 18:04:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 18:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:04:17 GMT
USER haproxy
# Fri, 09 Jan 2026 18:04:18 GMT
WORKDIR /var/lib/haproxy
# Fri, 09 Jan 2026 18:04:18 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa458f4c2a525dde0e80a98372ae78350c1d899c29da667e62773328507ef4e`  
		Last Modified: Wed, 07 Jan 2026 18:26:18 GMT  
		Size: 1.6 MB (1599473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23457e9c46a1bf8f6b092177e2fb06ddf8a617fa96e7373d833d0b25240456b8`  
		Last Modified: Wed, 07 Jan 2026 18:26:18 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241b98e5547af25403d7afc7190cc50bca1f2a08ecfa80d0989996e62043bc00`  
		Last Modified: Fri, 09 Jan 2026 18:04:37 GMT  
		Size: 13.4 MB (13422656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e0298adbf352a15caff7852ead3ce488d3357a3790053b7e1186a26c12545a`  
		Last Modified: Fri, 09 Jan 2026 18:04:36 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:d7ccfc71daf7eb6aa06c876522a9116cc0a3249a0028b471044af60c31675040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6438e918c3839d58ee14a09c7db2748b4c96bcb48447a9ec54088fd106240555`

```dockerfile
```

-	Layers:
	-	`sha256:77c4cd4537c994de182b1c1f159aa6793bc5dbb7769d676c4d7f2071eb1fe552`  
		Last Modified: Fri, 09 Jan 2026 20:02:34 GMT  
		Size: 2.1 MB (2115152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:559d582af5a877cadfa845dbed9fe93ffdf39d10f2d3d27e6d8dee2c93dc1447`  
		Last Modified: Fri, 09 Jan 2026 20:02:35 GMT  
		Size: 22.4 KB (22350 bytes)  
		MIME: application/vnd.in-toto+json
