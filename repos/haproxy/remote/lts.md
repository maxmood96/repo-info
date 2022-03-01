## `haproxy:lts`

```console
$ docker pull haproxy@sha256:20fc6249fcb04b8c022cd859a7e184cf9fc81f18fc4779147e55ccfcd020474a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:lts` - linux; amd64

```console
$ docker pull haproxy@sha256:3055525be465de82ca2f613232850a125667d54e5019a258c212a2295eaf26cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39165081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b96a5d979723add88eda0f1313bafa1e41f21a8c368040fd7f168c29a8333af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:25:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 01 Mar 2022 02:31:15 GMT
ENV HAPROXY_VERSION=2.4.14
# Tue, 01 Mar 2022 02:31:15 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.14.tar.gz
# Tue, 01 Mar 2022 02:31:15 GMT
ENV HAPROXY_SHA256=e6346b406b911b94c88eb05a5f622d53d49ffc247468fb03c12a4ffe3cc5ff04
# Tue, 01 Mar 2022 02:32:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 01 Mar 2022 02:32:56 GMT
STOPSIGNAL SIGUSR1
# Tue, 01 Mar 2022 02:32:56 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 01 Mar 2022 02:32:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:32:57 GMT
USER haproxy
# Tue, 01 Mar 2022 02:32:57 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa43762acc5d21214d1e5e903c018a9c0ee5409b0cf38fc2aff30a6ea454460b`  
		Last Modified: Tue, 01 Mar 2022 02:40:39 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a824c982c0b029eed68d4960c52a2c6a972227e5d2e2b206deb5a7f7c911441f`  
		Last Modified: Tue, 01 Mar 2022 02:41:50 GMT  
		Size: 7.8 MB (7796799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b1edea736d6e9eea02c3903e126b8ce22207c96419bf2b4ad1ec5fdade84bd`  
		Last Modified: Tue, 01 Mar 2022 02:41:48 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:91e82d1b7d676db6d3a9f251ab2bb25b3a8c59bd460b65a0f04c552ee08eeffe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36622479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40da54afc91fce25a414a435799a4e37353eae67c0b592d81c1b82d01450f05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:53 GMT
ADD file:eb61ee802e5118b26e1fec2c7fc58e34de0de54a5fd47dc6318c11a039ef528f in / 
# Tue, 01 Mar 2022 02:02:53 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:29:50 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 01 Mar 2022 02:32:16 GMT
ENV HAPROXY_VERSION=2.4.14
# Tue, 01 Mar 2022 02:32:17 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.14.tar.gz
# Tue, 01 Mar 2022 02:32:17 GMT
ENV HAPROXY_SHA256=e6346b406b911b94c88eb05a5f622d53d49ffc247468fb03c12a4ffe3cc5ff04
# Tue, 01 Mar 2022 02:33:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 01 Mar 2022 02:33:16 GMT
STOPSIGNAL SIGUSR1
# Tue, 01 Mar 2022 02:33:17 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 01 Mar 2022 02:33:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:33:17 GMT
USER haproxy
# Tue, 01 Mar 2022 02:33:18 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4aa6e26b4dfdac27e5b5e15b7ebf4366149755a79dd653a5b68d9d93dd94c695`  
		Last Modified: Tue, 01 Mar 2022 02:18:33 GMT  
		Size: 28.9 MB (28909528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05732a886770ec0de4b1aa78577ca0073356df80dfab3865952c1ad46cd9b5bc`  
		Last Modified: Tue, 01 Mar 2022 02:40:45 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9946d651ab3d70b2a67f279db5bb22c6c9cc700b7095f1a7603d83aba4e4d3c`  
		Last Modified: Tue, 01 Mar 2022 02:41:47 GMT  
		Size: 7.7 MB (7711067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da448e994d8560d2ababc5ca6bf8f238edfee3e96752a716afbdaf2a1fea44da`  
		Last Modified: Tue, 01 Mar 2022 02:41:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:761c39acb9b6a1d72febca6d9f1c1f857e2536ac7b98bfcd2428a4a379f0a022
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34137602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2366cd9d4e015770bd45f5321f7d9f1e8a9851b872a50e0d89a240360e9bab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:08 GMT
ADD file:7f27f5b43b7cb04e509fe145266d9bdeacfcacb024cafac32e57ef1c831d5ea7 in / 
# Wed, 26 Jan 2022 01:42:09 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:31:48 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Fri, 18 Feb 2022 05:43:23 GMT
ENV HAPROXY_VERSION=2.4.13
# Fri, 18 Feb 2022 05:43:24 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.13.tar.gz
# Fri, 18 Feb 2022 05:43:24 GMT
ENV HAPROXY_SHA256=4788fe975fe7e521746f826c25e80bc95cd15983e2bafa33e43bff23a3fe5ba1
# Fri, 18 Feb 2022 05:44:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Fri, 18 Feb 2022 05:44:16 GMT
STOPSIGNAL SIGUSR1
# Fri, 18 Feb 2022 05:44:16 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Fri, 18 Feb 2022 05:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 05:44:17 GMT
USER haproxy
# Fri, 18 Feb 2022 05:44:18 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:aaef1f1162ec03e01b5b955d41da400544ec2374093ae3dbc330ab2bb36df3e1`  
		Last Modified: Wed, 26 Jan 2022 01:57:59 GMT  
		Size: 26.6 MB (26564933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0602ad1ae7f3b207731c569c474289181c2bb551e22622129c2329f200c597ba`  
		Last Modified: Wed, 26 Jan 2022 02:46:07 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd4b8d92aec321cc0082203504e137fe092964105835521dac97d4e5369f7b8`  
		Last Modified: Fri, 18 Feb 2022 05:52:45 GMT  
		Size: 7.6 MB (7570783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275bd8efbe5ba7402f89d40253c8670e025bea508e1d3a0f14b2b5bfcd6f215d`  
		Last Modified: Fri, 18 Feb 2022 05:52:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:d44028fb3b5ced2558c69e4a5fd34e700c4fd2bb4a1d8997844fd93fba7222e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37918613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76df090c10c4afeb6beab6aa20be914915fd0551946e2344939a69802a25e8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:34:00 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 01 Mar 2022 02:36:53 GMT
ENV HAPROXY_VERSION=2.4.14
# Tue, 01 Mar 2022 02:36:54 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.14.tar.gz
# Tue, 01 Mar 2022 02:36:55 GMT
ENV HAPROXY_SHA256=e6346b406b911b94c88eb05a5f622d53d49ffc247468fb03c12a4ffe3cc5ff04
# Tue, 01 Mar 2022 02:37:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 01 Mar 2022 02:37:25 GMT
STOPSIGNAL SIGUSR1
# Tue, 01 Mar 2022 02:37:27 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 01 Mar 2022 02:37:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:37:28 GMT
USER haproxy
# Tue, 01 Mar 2022 02:37:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde6f55d0af53e214f76de75d5e1d156d20e066fff91b337abd9b0b15e1910bd`  
		Last Modified: Tue, 01 Mar 2022 02:43:13 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e5c0ead2df533a34f695cb50ba79a533e8716654e9a281ffb0bc76029febe9`  
		Last Modified: Tue, 01 Mar 2022 02:44:36 GMT  
		Size: 7.9 MB (7859865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8664d9ff29dcfd314e94682d717cae2bf9ab58ab8b7d81ad7a20bbba9e651f94`  
		Last Modified: Tue, 01 Mar 2022 02:44:34 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:be581926b0c46c66396ad6719acc05c81ca0ab96b7b78a61337fe9b20c72c5b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (39952426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea486be9d5dfcab3a6df3d249a913392832e399c1d6c83565850dbed3be13a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 01 Mar 2022 02:07:32 GMT
ADD file:e92ab504d4c0d3bd63da83254e6ca400b607c32e0f5037039648559b91770870 in / 
# Tue, 01 Mar 2022 02:07:33 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:23:00 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 01 Mar 2022 02:29:16 GMT
ENV HAPROXY_VERSION=2.4.14
# Tue, 01 Mar 2022 02:29:16 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.14.tar.gz
# Tue, 01 Mar 2022 02:29:16 GMT
ENV HAPROXY_SHA256=e6346b406b911b94c88eb05a5f622d53d49ffc247468fb03c12a4ffe3cc5ff04
# Tue, 01 Mar 2022 02:30:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 01 Mar 2022 02:30:51 GMT
STOPSIGNAL SIGUSR1
# Tue, 01 Mar 2022 02:30:52 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 01 Mar 2022 02:30:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:30:52 GMT
USER haproxy
# Tue, 01 Mar 2022 02:30:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:04a87e821be7e4b29d48011b7aa4ff884ca57fd36995cb3b99fd2fc24ac562d8`  
		Last Modified: Tue, 01 Mar 2022 02:15:51 GMT  
		Size: 32.4 MB (32377389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514f540124afe58aa18bee373fb65b9cd70a34342f3053efc503206e95898899`  
		Last Modified: Tue, 01 Mar 2022 02:41:34 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde2f0ce2cf621066b4a07a06e6c36d271c7dc5626e3260cf478411ca6b582e6`  
		Last Modified: Tue, 01 Mar 2022 02:43:09 GMT  
		Size: 7.6 MB (7573156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea5be3f6a76125ceed7c747b17ccc8161ed9e12f5be91c42dc059627c48223d`  
		Last Modified: Tue, 01 Mar 2022 02:43:07 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; mips64le

```console
$ docker pull haproxy@sha256:b028c2ac8c0b98c7135afcc5f47b0b79cca4899782f24dab1812d44934105fa8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37571241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486faf8397e47ee38a72e86c2ce8a10dc058bd9edbad3098d260bd28e2215005`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:49 GMT
ADD file:1901e1e1292cbfcd557262ec5d08551cecd0070b24928414d220472664fe3fdf in / 
# Tue, 01 Mar 2022 02:02:49 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:20:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 01 Mar 2022 02:25:58 GMT
ENV HAPROXY_VERSION=2.4.14
# Tue, 01 Mar 2022 02:25:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.14.tar.gz
# Tue, 01 Mar 2022 02:25:59 GMT
ENV HAPROXY_SHA256=e6346b406b911b94c88eb05a5f622d53d49ffc247468fb03c12a4ffe3cc5ff04
# Tue, 01 Mar 2022 02:28:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 01 Mar 2022 02:28:33 GMT
STOPSIGNAL SIGUSR1
# Tue, 01 Mar 2022 02:28:33 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 01 Mar 2022 02:28:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:28:34 GMT
USER haproxy
# Tue, 01 Mar 2022 02:28:34 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3baeb8c34a522fc616f97412d47dc1f665e93552c57aa8237ee1d673f9757cba`  
		Last Modified: Tue, 01 Mar 2022 02:12:25 GMT  
		Size: 29.6 MB (29632966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f57642e5ec1100e314835cf14332d08079daf8fce6780ab2112ae24c6fc09f`  
		Last Modified: Tue, 01 Mar 2022 02:38:34 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efae3e0e67eab7f9f6ebea82866d9e0e78f28f1a007a359bff97b052204a439c`  
		Last Modified: Tue, 01 Mar 2022 02:39:22 GMT  
		Size: 7.9 MB (7936417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d084351f1faedd325a56a7f30ee45a89c2541536695ebe8ec758fc697d50064`  
		Last Modified: Tue, 01 Mar 2022 02:39:17 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:12cf4cf3907ae23b8e506b7bd98c5c491f3bc7bf53868b298f7f0937fb5f265d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43465722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b00f0394fd97ebcca517a6513e0387e86fc1dee8a07febbb21fc0e4f877691`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 01 Mar 2022 02:05:07 GMT
ADD file:fc0989685aecf50ec36795d73893c30d9ddd4f946f8c5f4a6d10963f8ab41168 in / 
# Tue, 01 Mar 2022 02:05:12 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:44:12 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 01 Mar 2022 02:51:51 GMT
ENV HAPROXY_VERSION=2.4.14
# Tue, 01 Mar 2022 02:51:54 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.14.tar.gz
# Tue, 01 Mar 2022 02:51:58 GMT
ENV HAPROXY_SHA256=e6346b406b911b94c88eb05a5f622d53d49ffc247468fb03c12a4ffe3cc5ff04
# Tue, 01 Mar 2022 02:54:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 01 Mar 2022 02:54:45 GMT
STOPSIGNAL SIGUSR1
# Tue, 01 Mar 2022 02:54:46 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 01 Mar 2022 02:54:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:54:50 GMT
USER haproxy
# Tue, 01 Mar 2022 02:54:54 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1dde9239ed493e1fe68971baa3f162c734ef0f461ad109e48aeb5b56daa55cc2`  
		Last Modified: Tue, 01 Mar 2022 02:15:19 GMT  
		Size: 35.3 MB (35272910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f237603e0f675a585c0ef20973793bd1d558498997f4628b082817fe337d2ba`  
		Last Modified: Tue, 01 Mar 2022 03:10:12 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e21a1bda5c6a3992f5c978dcc8cf9c51d484b63c3897ba6d24024cc16a13e29`  
		Last Modified: Tue, 01 Mar 2022 03:11:53 GMT  
		Size: 8.2 MB (8190922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa8172a3c0e4f4d921c71b7603871c4fca3f02f38b6a03f45beb67bb372b9a3`  
		Last Modified: Tue, 01 Mar 2022 03:11:51 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:0ad2c5f6e65fdeafaa52954f49c4468fed5503e5a9a1980ab4ed9bf18a5ffd8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37489603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973bb54aedf16859e10200e9be5a7581d832cccc4275faec56ad89944d681f3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:56 GMT
ADD file:d869ad3392a4e752c2f73d08a4cc13594c94bfc050bd037db0ca9827a0207072 in / 
# Tue, 01 Mar 2022 02:01:58 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:14:59 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy
# Tue, 01 Mar 2022 02:17:51 GMT
ENV HAPROXY_VERSION=2.4.14
# Tue, 01 Mar 2022 02:17:51 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.4/src/haproxy-2.4.14.tar.gz
# Tue, 01 Mar 2022 02:17:51 GMT
ENV HAPROXY_SHA256=e6346b406b911b94c88eb05a5f622d53d49ffc247468fb03c12a4ffe3cc5ff04
# Tue, 01 Mar 2022 02:18:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v
# Tue, 01 Mar 2022 02:18:23 GMT
STOPSIGNAL SIGUSR1
# Tue, 01 Mar 2022 02:18:23 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Tue, 01 Mar 2022 02:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:18:23 GMT
USER haproxy
# Tue, 01 Mar 2022 02:18:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f81abce72636770dac4258df46a31beeb6ad81dfddd5b7c9c3fa6942ea074922`  
		Last Modified: Tue, 01 Mar 2022 02:07:33 GMT  
		Size: 29.6 MB (29647132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55aa058ef4dabe0cfc223438d40c61fa9af92e9be710236deab79310d4533f3a`  
		Last Modified: Tue, 01 Mar 2022 02:24:10 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b9f512afda8a1fb35a1e49a435427e2d5d99678aba5a8a9aa052c9380bb2e0`  
		Last Modified: Tue, 01 Mar 2022 02:25:13 GMT  
		Size: 7.8 MB (7840589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86caedd644f4c1ad23e607af0d1ce0f2f4e4b46e3c709454d108e8850aac818d`  
		Last Modified: Tue, 01 Mar 2022 02:25:11 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
