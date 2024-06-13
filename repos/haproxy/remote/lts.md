## `haproxy:lts`

```console
$ docker pull haproxy@sha256:5439222328c60ad818b9d9f9f24989daf33344fe0033da62505a903174fd27b1
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
$ docker pull haproxy@sha256:2367d6dbf3d1fac21c77bfd6c1f6d56813271b529629e98b7a9a03b53942fa1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41619218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a0eca74264e3ead34b5953d869b03165d78e7f58ebab7d71b1093b1db7c997`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08500fa7cd4148f5ee07adc2edbc582a2327b41f7f74bb5a93bd078006df30ca`  
		Last Modified: Mon, 10 Jun 2024 22:33:31 GMT  
		Size: 3.3 MB (3299427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6359bba6adc0c43dbd207c72cfcf1619bb11be8e64ae93a78775de58a6926707`  
		Last Modified: Mon, 10 Jun 2024 22:33:31 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80314bf42844cba36df0be715e78f330ba23a4f726fac073bbddec763200e48e`  
		Last Modified: Mon, 10 Jun 2024 22:33:31 GMT  
		Size: 9.2 MB (9167737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e988fd07b81d1e3f511637b67b128ab082ac80985acf587993e0da5aef33eeb`  
		Last Modified: Mon, 10 Jun 2024 22:33:31 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:7bf0ce3ba1bb9c6e8777fb059b2959c3d6d9bbb2d50cfb9faf993ae1b3c659bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1e91720dc96862005249cb9c9594fe0032accfdb44f0fbeed00b29fcca4b7f`

```dockerfile
```

-	Layers:
	-	`sha256:f51bdd094f52ee003b3e7b0cea9ba6edff8f29bbcad4a22d69811414750c1b2d`  
		Last Modified: Mon, 10 Jun 2024 22:33:31 GMT  
		Size: 2.3 MB (2341666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7933c028b04dc0fad5c0079fa446ef67f243b1392632411125e876c4043368c`  
		Last Modified: Mon, 10 Jun 2024 22:33:31 GMT  
		Size: 22.2 KB (22182 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:d56d7470824755644627745e009b73a27427bcfa0e69d68953aa3c0b89700047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38896953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24285fdd20aafc64963a100ae143eb52237de31491e49e09842e26de8e450e4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 10 Jun 2024 14:42:35 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b8c1197d561f22b5e451aca5bdd4aafabb05b04a45d0e6e5aaa9792e13e694`  
		Last Modified: Thu, 13 Jun 2024 15:12:10 GMT  
		Size: 2.9 MB (2874825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a6de1a9d32aeae2e347285d0b2395d752dc5c013453b94c04755e92564a998`  
		Last Modified: Thu, 13 Jun 2024 15:12:09 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab09cbb2535d6292aa9de497c60d2b3870b26b1be6af2c103130c9532c8b0ccf`  
		Last Modified: Thu, 13 Jun 2024 15:13:43 GMT  
		Size: 9.1 MB (9110505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e778c412c02c77a625cd12b2ff73e31b5573b02cca95ecb874623024a2407ff3`  
		Last Modified: Thu, 13 Jun 2024 15:13:43 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:63a05d49806e17c960d027d60d676b5c58e71bdc3831740cd5cddeef6748d0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196b3f4d3bc745396972e961f8c24906ee310790baa630e60f308fb8f439bd21`

```dockerfile
```

-	Layers:
	-	`sha256:ebf5811b1590bdf1896213c2557249e79bdb0818d436dd71957ddcfa6807d72f`  
		Last Modified: Thu, 13 Jun 2024 15:13:43 GMT  
		Size: 2.3 MB (2344946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df08593d8736e2df97c577270256c40e8ce51dea8e4d3809144093a3a798e831`  
		Last Modified: Thu, 13 Jun 2024 15:13:43 GMT  
		Size: 22.3 KB (22310 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:a0821f22cc197e8558914b3bf6ca03de6d4f48de9a481de10efd136f8fc41e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36397133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadf7eab789180df9b28c988997908786115a4f7fe12e3422711aeadcfab501e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4894614abaac161cd23e0cadace9c30e6a547a8ca2a41957bc8a4d9178cad285`  
		Last Modified: Tue, 11 Jun 2024 03:07:58 GMT  
		Size: 2.7 MB (2711051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a231bfb8df0ce6ba66a42b37f9baa8ffd920789067f76ffcd019889a0b814a`  
		Last Modified: Tue, 11 Jun 2024 03:07:58 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5e7fa3bb850657eb2269599d018c4acc00afb1ad21b5990fac8099d6308fb9`  
		Last Modified: Tue, 11 Jun 2024 03:07:58 GMT  
		Size: 8.9 MB (8944231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c356e4e1223c26b84807eec4cf7059949ec8de17d66d40da0108c1c875b682c2`  
		Last Modified: Tue, 11 Jun 2024 03:07:58 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:1be40c9c69d19641bb25f4c23076185d4e8318736ec857f9641e0e3fb52f336e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d734b9ba409b6c8430e4e14361094edd5a4c5e595b991f93825a954d0e7ce4c4`

```dockerfile
```

-	Layers:
	-	`sha256:5eea97d751a2f51d46fd7b49f968a86a5d8b0362ab6e8d770e70aade888fcf8a`  
		Last Modified: Tue, 11 Jun 2024 03:07:58 GMT  
		Size: 2.3 MB (2343924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b523882f6631e1dfe107b87b0d97aefdb2cfb7ca624021b6d7001e65b649f0e`  
		Last Modified: Tue, 11 Jun 2024 03:07:58 GMT  
		Size: 22.3 KB (22309 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:aa6b478fbc150ee77e6106e3126b50e6c3991161c05b8fe071efb0a1a5905db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41460315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5486df871700d539611483ce75ca1fa5e8853489f41ee5d454c7e08fb68f989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a318f1988768cfb671a164b7a4c1cd76272152cb1ab3c64e2b9f5dc0a4bf5d09`  
		Last Modified: Tue, 11 Jun 2024 03:34:35 GMT  
		Size: 3.1 MB (3122185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f0f594bb8bbfa6f0653d3a4e1aa82b9012f0b35e5107e4b87beaa474fddb83`  
		Last Modified: Tue, 11 Jun 2024 03:34:35 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9a6edc851061b9d24c23f30ee372f6e64ba4a2032b5af60fb5e59f11a79eec`  
		Last Modified: Tue, 11 Jun 2024 03:34:36 GMT  
		Size: 9.2 MB (9156978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f567ec354fe55f27e3e24f01db03a8c8eb5186bdf3b585fd762461190109e0b`  
		Last Modified: Tue, 11 Jun 2024 03:34:35 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:9c0b8efc3424c3c9126030e1cbe87697d617fe6b18f53b37f43e94c382b3a00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82b007515adbb0cd9a1728e13661a404776fc95265abd60f6390e5f56a565fd`

```dockerfile
```

-	Layers:
	-	`sha256:e3e327f24c88ec74ddba76f549ea6020c5bb55030ee49cda8be6beb0e6ecccf5`  
		Last Modified: Tue, 11 Jun 2024 03:34:35 GMT  
		Size: 2.3 MB (2341972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0625281787f9444681bccc03de66a65dcce89e6826ff7c33ba160428f51082f4`  
		Last Modified: Tue, 11 Jun 2024 03:34:35 GMT  
		Size: 22.5 KB (22539 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:972c13abd5f2dc6453d9743b4b58474a89b8c754552432f415f297ea0f1aebfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42398451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1c97b5b5e689cf6f6114dec0d712df1c3d24c2aa219f08f858a40196955e84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 10 Jun 2024 14:42:35 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbf31a4640b81c754a22a3dbfe4eb9ce27155153fd3ffa5d5e8e210d3afb671`  
		Last Modified: Thu, 13 Jun 2024 01:59:59 GMT  
		Size: 3.3 MB (3304843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1a5793c2400b4b892d99c4eef786507e72c0232b3ecf5565eac91307937400`  
		Last Modified: Thu, 13 Jun 2024 01:59:58 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d914798ffe13df7062923894b9fb7fc8e72451fcf26566512d45209ef1986447`  
		Last Modified: Thu, 13 Jun 2024 01:59:59 GMT  
		Size: 8.9 MB (8929307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a99aa5bc761736841448822a16977b76a7b52e7e6223e531a5177f282880cba`  
		Last Modified: Thu, 13 Jun 2024 01:59:59 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:8fd1c565ebe4c34096d2ce86db5659bcd60a3f9204112004c372d2e70ab13700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2360912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1605ba915264f8898c57dc5b29953d0406eb656a226352082dd5404422bdf4ee`

```dockerfile
```

-	Layers:
	-	`sha256:76d0e3b87aff977cf7faf3c0558592e65ecc30d718f3313b4c15987810723cb9`  
		Last Modified: Thu, 13 Jun 2024 01:59:59 GMT  
		Size: 2.3 MB (2338783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78af77b326467b0729d21b6b0cddaef8ccd0d4173fb8e979bc2ca047539bfb5e`  
		Last Modified: Thu, 13 Jun 2024 01:59:59 GMT  
		Size: 22.1 KB (22129 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; mips64le

```console
$ docker pull haproxy@sha256:8cad1d0992767d1704797d0b43aa1dc9a96b857a791aa832a6d91da7abc2546c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41146484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2a2cca7b22a263ecd3585cdc7e110088e4e94c2bfc54155b14c9920449594d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2905ff4ef2a27ce599e3715fd6a29801bd64f63f937c41b94086162739754824`  
		Last Modified: Tue, 11 Jun 2024 11:40:21 GMT  
		Size: 2.7 MB (2698985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25980722ed4d9b9bf7457da650a99049cc20778b2e74ee0545a52290eb69f1e`  
		Last Modified: Tue, 11 Jun 2024 11:40:21 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28784cd088a68f30ccc47cd6bd71eea48f9f569dc1e229d6d773c022c727a07`  
		Last Modified: Tue, 11 Jun 2024 11:40:22 GMT  
		Size: 9.3 MB (9302166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fd491a06341f1c0cbda342f98698f6c12b1529687c54412fda74b77b03d3ea`  
		Last Modified: Tue, 11 Jun 2024 11:40:21 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:09e08af1192451ee8a44321a0c2997e6a2141614ae01d6ca9a4c17b318343a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7568e5ddcd64fb2be178d1d9acf16c400796e3ce445999da91186ca392a999b1`

```dockerfile
```

-	Layers:
	-	`sha256:1d82fdd699bcf5d6a70427f02dbadcd03256ea6a3a957456cd3888b888a0c133`  
		Last Modified: Tue, 11 Jun 2024 11:40:21 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:b4341c916d898676853726b91086bdc9ed5cfcc32b380803ed846d9d4eb53fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46329900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1da177977e1b32626e3fa989221265c7c7e67708e54f4b105866c6d2148473`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d700353873cf75fe548b359ac5570afeaeb8040cfbb4b12ee67cd9f48c4bb7`  
		Last Modified: Tue, 11 Jun 2024 07:59:02 GMT  
		Size: 3.5 MB (3501588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcfcff75422dfe7f577a495b895c9e76075bd30ae5c7520473f78fb56ebcc21`  
		Last Modified: Tue, 11 Jun 2024 07:59:02 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a495446a9fd2739c3888875861a34f581ee8d2e1396c0c5c812c826459e6ecc1`  
		Last Modified: Tue, 11 Jun 2024 07:59:03 GMT  
		Size: 9.7 MB (9685507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e002e6ece366d7b8f263811c4a04e615daecafdf7eaa06dc6476bcc74a7c931`  
		Last Modified: Tue, 11 Jun 2024 07:59:02 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:c97fe9e54374f4897c5a1d07ac665eb95b63c93eef9482757b802eccfc51dcae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2368238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9e6e6c2a9be4e404475fd4f56613ae2944d95c554cbf09e066586f1394f37e`

```dockerfile
```

-	Layers:
	-	`sha256:68e88c5de0ab3580a860bd9ae2c79156ccaed437e6701567bdac5eb45154456d`  
		Last Modified: Tue, 11 Jun 2024 07:59:02 GMT  
		Size: 2.3 MB (2345991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0df958938756d6e0036996d46cede1f643b0b8dc7c26adf44e29e886a42d258c`  
		Last Modified: Tue, 11 Jun 2024 07:59:02 GMT  
		Size: 22.2 KB (22247 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:b5c14b4112753fa160bdeaf1e181570002a00217737901ece18b1e6e2e3c3c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39532689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539be0717b2d6c2bebdfeeab5cb7ca270d70edfcf7e6dca5c2a5d4dbe31ba938`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 10 Jun 2024 14:42:35 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["bash"]
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_VERSION=3.0.1
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.1.tar.gz
# Mon, 10 Jun 2024 14:42:35 GMT
ENV HAPROXY_SHA256=fef923c51ddc0ffb3c73b9b95e31e98c82cb9521c64754c5e95c42907406a670
# Mon, 10 Jun 2024 14:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
STOPSIGNAL SIGUSR1
# Mon, 10 Jun 2024 14:42:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Jun 2024 14:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Jun 2024 14:42:35 GMT
USER haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
WORKDIR /var/lib/haproxy
# Mon, 10 Jun 2024 14:42:35 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c00277acd09dcbdc73149364da7e9a54fbd3dff8a5c1af5a71d6e9e2007e4a6`  
		Last Modified: Thu, 13 Jun 2024 09:25:36 GMT  
		Size: 3.0 MB (2964940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c9487453956f5f801d576e7d7fef683eaba516beaba12c66b5476d9a11b8a7`  
		Last Modified: Thu, 13 Jun 2024 09:25:35 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1b403e46d0815745a8edd609e4b122c71fea3caaa44e3e6826f64e28b25e9d`  
		Last Modified: Thu, 13 Jun 2024 09:26:48 GMT  
		Size: 9.1 MB (9053648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5000e582c73dfb5275b8d66859dd20b656d576fcdf02a9a5e6c087b37ea32b`  
		Last Modified: Thu, 13 Jun 2024 09:26:48 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:a11d86a235225dcf543dc30bc772cd1a30afb12d15490fc4ecff04c891598849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4253040452c7754328d8387adc5cdfccc599604341bdd1dc3f443404f0a6361e`

```dockerfile
```

-	Layers:
	-	`sha256:d5cbf76475e740b678b9de649c27202857b65ad6c4c72cc7ef0498fc2d940179`  
		Last Modified: Thu, 13 Jun 2024 09:26:48 GMT  
		Size: 2.3 MB (2341495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d726528e82a46516cad32ea405bb9d266d1541170da7c5a820ef24b6cafa292`  
		Last Modified: Thu, 13 Jun 2024 09:26:48 GMT  
		Size: 22.2 KB (22182 bytes)  
		MIME: application/vnd.in-toto+json
