## `haproxy:latest`

```console
$ docker pull haproxy@sha256:c2f13cec3d772feb8c0b6d5908cda1335e0482fd633e66b4a318014657919eeb
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

### `haproxy:latest` - linux; amd64

```console
$ docker pull haproxy@sha256:88b6bd01eead751cda50906dd0aed360cc6afadf09c6fbe7153b2be65f958ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41024118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66382c5479fcd5e844573ec7a10df30b4a08a18018e7642966450139d643a9b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2ff6ac4d30f12ab741cae9fde0da1a89f6041c801863b2a066230a2a237f5f`  
		Last Modified: Tue, 14 May 2024 02:56:34 GMT  
		Size: 3.3 MB (3299449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a21a823a84b3585ae04a9791c5f2c0affefbbdb3c85ef9642aebf006737360`  
		Last Modified: Tue, 14 May 2024 02:56:34 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61beaf23006585b8e6c8a26456d3aa8ea099cdf7990f92e23f0fd99da2ab427e`  
		Last Modified: Tue, 14 May 2024 02:56:34 GMT  
		Size: 8.6 MB (8572623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa80c60c3b09d03222ce80bbdcff1339506c6f1b70e29315f3db7f9dbba7c8a`  
		Last Modified: Tue, 14 May 2024 02:56:34 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:994d394c730d610ab183d4be1ab7e35f3126a2da8ce9c3e84a92aa3162421904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2362755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f31a002a3eb7eede9d463f852a7a9797b64ab87ed23dbbeed5e4f5b8d38b0d9`

```dockerfile
```

-	Layers:
	-	`sha256:5874921eebb2aefb76ef3f63a8f5d3e5de35029c24b3ce4ac91eec906cdab49f`  
		Last Modified: Tue, 14 May 2024 02:56:34 GMT  
		Size: 2.3 MB (2341061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:550b76c8063f15d36d74c920e949333eafba7ca72b511050ab7c222492e69357`  
		Last Modified: Tue, 14 May 2024 02:56:34 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:734120b738540165b697101064672eb162672a5de31b7eb5a39c6033cbad8754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38321728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5360ee7116af2a3deac8cf13e0288e10e4d222c31d2860543f7aa774d7b6bd5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad7a8b59059ac6b791e12f96d1f000402174d26d4a9e11593614afd5e7013f5`  
		Last Modified: Tue, 14 May 2024 14:37:22 GMT  
		Size: 2.9 MB (2874720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c6911c10e85084c7139f4489b77686397dce315c5f413b581e67ad30eaa8ea`  
		Last Modified: Tue, 14 May 2024 14:37:22 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b998c50797a03950a5ee2ee82bc67905fbca7dbfc4ba573d901a169eb6e729f`  
		Last Modified: Tue, 14 May 2024 14:38:41 GMT  
		Size: 8.5 MB (8535448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf9d68cab93225511da37ed163da782f15975d748ef2c4600509f5f98de651a`  
		Last Modified: Tue, 14 May 2024 14:38:41 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:bda0409ac56eda57ac5d066401da1d3404a6861fd674c010a7dd8f080360cc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7487487a9ace26c1ba284e5127c69c26dfcc9ad335f2a5384726365655cba82b`

```dockerfile
```

-	Layers:
	-	`sha256:ae3b83628db1f47459185fdc3e15dd0243898dc6d5fe9201d9656d1c032fd1ba`  
		Last Modified: Tue, 14 May 2024 14:38:41 GMT  
		Size: 2.3 MB (2344325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b5b795f7b021909aef59734558609c85efe2ccb2db2b763829a44e5f94fbfd9`  
		Last Modified: Tue, 14 May 2024 14:38:41 GMT  
		Size: 21.6 KB (21639 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:5bbce48a9da4dff1c703d75ebf73d90e4c50541dd54442d2bea6f2fa10ba8957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35825228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07fae352840bf7395161ba89734e47dd56b6b89aa45c262061f9f367dce808f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c85cb7a9d243082fd284f3dc187c29d67b4405813394768e776a8743e0bccef`  
		Last Modified: Tue, 14 May 2024 13:39:18 GMT  
		Size: 2.7 MB (2711051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0939c658e183b4ddce40c360c13cf44bed1481ba5c63bd6df0120e7c90a17aba`  
		Last Modified: Tue, 14 May 2024 13:39:17 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7559b00f0a58542da4873f178d50652228a8ec2b35cabb537633d51cc05fa7dd`  
		Last Modified: Tue, 14 May 2024 13:40:21 GMT  
		Size: 8.4 MB (8372333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c60ee8184aab828969da1ea139a3c951beb650c7dc16800e07f9032809d2eb`  
		Last Modified: Tue, 14 May 2024 13:40:20 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:e68820ee2f62bf7c97e91784e67ae0216a0396607b4a0e4706b57e6de4fc57be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06139ac260af4a9f605d0b36c662ae3b979965075b0d066a865c9858c71cad93`

```dockerfile
```

-	Layers:
	-	`sha256:63c5b1cf15b0baba6fbe5deb4d3e6ffb1dc516c3ca3ede5070fd8b59af89c129`  
		Last Modified: Tue, 14 May 2024 13:40:21 GMT  
		Size: 2.3 MB (2343303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4169257d885eee944f20604936f7ba89b944149427fa50261c2d6a84ac946b92`  
		Last Modified: Tue, 14 May 2024 13:40:20 GMT  
		Size: 21.6 KB (21639 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:0e19054616e09d187fe162b5e630002989827830c45cc285fcae2ce24b3436f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40867327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92c8fb69a0f8891ea85909f566e52576c792521278a58a63d8cb27f2ce9345b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab917124a9bee3e090f10916ad050a1869ab5f0aebddad4b68c56d47556a16a`  
		Last Modified: Tue, 14 May 2024 17:21:13 GMT  
		Size: 3.1 MB (3122254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeaf2855ceb38cc33a8fc3dd2a140c0749157b53349f04b8a241fb27f15eb65`  
		Last Modified: Tue, 14 May 2024 17:21:12 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619c8a534bd91d76bd1e7af33d30fd882c6c32267c2af132f230b2034f3d584a`  
		Last Modified: Tue, 14 May 2024 17:22:00 GMT  
		Size: 8.6 MB (8563938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfa8338c65f6e9db8f957183019a3c7f39f123886d63434c249f9efedab358c`  
		Last Modified: Tue, 14 May 2024 17:21:59 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:aa8e5a42acf9fe37c6f07c7fa29743a10eba78df6b8c0e6a679b4351a5ad73d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2362819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4dbf90823dc99f08c6981c3888da8a30fd3bc7b25ddc0fae552d5674dfafc5`

```dockerfile
```

-	Layers:
	-	`sha256:4d527c918000be2368c8fb641b12ccf1ff47b265203136f55b6ee0351b4e3b56`  
		Last Modified: Tue, 14 May 2024 17:21:59 GMT  
		Size: 2.3 MB (2341278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c99447854e4441180f316c4df09fcac9960a10e51b852e4cda1894919b08667`  
		Last Modified: Tue, 14 May 2024 17:21:59 GMT  
		Size: 21.5 KB (21541 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:a023358b8be5101a26b38715da8a19bcde912a222306361468c4a2e7f2f8a9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41808233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e519c56396b124dd309af756ef5d88db32fbe1b28e11e4b0b584f45339afcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315005b6802b231117e91bcfefe04666059d04052130cc5df1501e7162c38ec0`  
		Last Modified: Tue, 14 May 2024 01:54:20 GMT  
		Size: 3.3 MB (3304866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981006db2738ee956db413422e5c9e2a028cdcff93cb70d1c766a3c6cdd7cdd3`  
		Last Modified: Tue, 14 May 2024 01:54:20 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79949a119f9314073ef312363990b8a3a00e7ef54ad22ea42b1f4b6612a325d`  
		Last Modified: Tue, 14 May 2024 01:54:21 GMT  
		Size: 8.3 MB (8339090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbfee82db69da5365d1ed284f828a598b873ede150dcca76269c0d5165cc6e7`  
		Last Modified: Tue, 14 May 2024 01:54:20 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:e777c13b5ce0123d4f1cf0420d5cd6a0887862ee0d309e46f9059b4ff48dea2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2359838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0c8212abd0c4f501988f967a44a138d5a7551aa45badd0d5d57758f9ddb9f7`

```dockerfile
```

-	Layers:
	-	`sha256:d176291909f9e04566694d006f252f57d5a0784f6d69d2308eaf0a722bf61e1d`  
		Last Modified: Tue, 14 May 2024 01:54:20 GMT  
		Size: 2.3 MB (2338188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c8dac0307863b1b3af231a31017618024b1e8cc6b9e2e3500f55ef5fdac5db0`  
		Last Modified: Tue, 14 May 2024 01:54:20 GMT  
		Size: 21.6 KB (21650 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; mips64le

```console
$ docker pull haproxy@sha256:a4b9cafdfc3b652755556e26d4c5c9727e6b2b361285e48dcbd44274f37f316a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40541850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ff95cdb5d47d5b8d70eb74d0b946dac87b0fa45fc6f04e3a2124587aa0238c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a56d0ae70acaae011bc8fd7fa85f2723fb403a766882cfcb4601fe28c58d9fb`  
		Last Modified: Tue, 14 May 2024 17:17:44 GMT  
		Size: 2.7 MB (2699019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecc6cbe8271fb0a86b7d6977de37d03d64cc7932f524486713482a75936455d`  
		Last Modified: Tue, 14 May 2024 17:17:43 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07683a4c0de2a1268a59a9db2dbc74d818669f55a53053583e14a8d3e0a020a8`  
		Last Modified: Tue, 14 May 2024 17:17:44 GMT  
		Size: 8.7 MB (8697500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858f0527a16a273c8fc4920bddcc77d26d5825e00aa31fe73ef051290afd46db`  
		Last Modified: Tue, 14 May 2024 17:17:44 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:d0c9b073698af1cbae38366c6a54dce5ca3e5cd1d5ed69e826f9d6bd740cbd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c0c22f44ea8b5d51810091ef31d97eb180eae7b9d174e92bfe53a6f2425373`

```dockerfile
```

-	Layers:
	-	`sha256:f86586253ebf5ac7c8384077bdbb4ed260726c9b79e74d1c80bd561232208ce0`  
		Last Modified: Tue, 14 May 2024 17:17:43 GMT  
		Size: 21.6 KB (21556 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:2bbc198fda2b34d541bb52615ee59ce476ccbca8b74333b728a7f55a611e56ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45703443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2922fc0088c3a53c7f1e36db595bbb39a51eefc8cd71b4e482c8551e9b1c9113`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184770d6dda8f9121c2c17ada19fab3442e0d14650efa483572f7dcd530e5a07`  
		Last Modified: Tue, 14 May 2024 09:43:35 GMT  
		Size: 3.5 MB (3501543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159b4553c3a4f829bfd9ee66c9764b915071fafa08c8319c77818cb65bf215cc`  
		Last Modified: Tue, 14 May 2024 09:43:34 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba1fedf872184407fefeb5fe767052065fd476996a2b63761a1b31ffb815929`  
		Last Modified: Tue, 14 May 2024 12:48:31 GMT  
		Size: 9.1 MB (9059104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a95a9028fd36b5d20acc33647842386414920526ce316b35fff1ada558e38b`  
		Last Modified: Tue, 14 May 2024 12:48:31 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:87273c7087d251022dc6dddc15d3adb70bd0dc531de47918f5dd79d37f3324f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ccf7eb7afe0e3519cf7001668cb487a2295d7cff262f10cdd5278f888f4135`

```dockerfile
```

-	Layers:
	-	`sha256:b9378129df0a95cf8d5d64666378b1084447814d958467cf7252faa6dbf425c5`  
		Last Modified: Tue, 14 May 2024 12:48:31 GMT  
		Size: 2.3 MB (2345374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a26aff70d78a81e9f52bfc5a6dd088b76755a56aa1a6e5ff717fdb4a679ddec2`  
		Last Modified: Tue, 14 May 2024 12:48:30 GMT  
		Size: 21.6 KB (21581 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:b51b1429e23feb941693d95786230553b052c072f8ea551826819d24acfc574b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38946027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee7c40337add0e8955b0a6b18ffdefca1c4f45e68f6a2cea6638e55bfa7a4f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Apr 2024 16:48:36 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["bash"]
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_VERSION=2.9.7
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.7.tar.gz
# Mon, 08 Apr 2024 16:48:36 GMT
ENV HAPROXY_SHA256=d1a0a56f008a8d2f007bc0c37df6b2952520d1f4dde33b8d3802710e5158c131
# Mon, 08 Apr 2024 16:48:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Apr 2024 16:48:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Apr 2024 16:48:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Apr 2024 16:48:36 GMT
USER haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
WORKDIR /var/lib/haproxy
# Mon, 08 Apr 2024 16:48:36 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e108db9f99f6f0369e68c975399e1f316088f453dd7fdac8702a5870b0ba9b`  
		Last Modified: Tue, 14 May 2024 17:41:39 GMT  
		Size: 3.0 MB (2964905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ad45e58fdd24e9c1d14cf3e40fe76484d0681c44be0ab6b7be31e281ec068d`  
		Last Modified: Tue, 14 May 2024 17:41:38 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856493647b3d790382086ec42edc19f205d51338e4bac946d30738f1e5f1912e`  
		Last Modified: Tue, 14 May 2024 17:44:45 GMT  
		Size: 8.5 MB (8467087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed0beb5fcd07d012abd7e58dcdded270b7d0fce8f08c662585968aacfc1a242`  
		Last Modified: Tue, 14 May 2024 17:44:45 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:c858eb2850a7ef95f55ba41395c708ef8d8b73d19f62ffa840d1a351b42cc64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2362417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d653e1cc41dc3847b1cf15f784ac23ccf72362c3a233bd3fb0129a2727ffe56b`

```dockerfile
```

-	Layers:
	-	`sha256:73d8e66d7e4cb969ab7dfea53a492beb7183efea7c2f79b188ba24bb74baacfb`  
		Last Modified: Tue, 14 May 2024 17:44:44 GMT  
		Size: 2.3 MB (2340890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10b91360f1d14f409992bd254448878dcf28b795ab7455fab59c71cc93294852`  
		Last Modified: Tue, 14 May 2024 17:44:44 GMT  
		Size: 21.5 KB (21527 bytes)  
		MIME: application/vnd.in-toto+json
