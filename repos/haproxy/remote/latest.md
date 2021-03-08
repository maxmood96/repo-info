## `haproxy:latest`

```console
$ docker pull haproxy@sha256:3214ebf1267b178440a327cbb5c6167b65c22a6dd64a56f25fbace986757300f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `haproxy:latest` - linux; amd64

```console
$ docker pull haproxy@sha256:586ed760a5a2f7c662a0c0c6499ba4deee11caea609aaba3c5a381d75b3df61f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36767363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e151b1aac28b63489aae6e912ce76d98fef88f6573f88d548dd2d54f9ca5d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 21:37:25 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 21:39:38 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 21:39:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 21:39:38 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 21:40:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 21:40:39 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 21:40:40 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 21:40:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 21:40:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 21:40:41 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7bca45a971fe608786870ce75c9976f8e5a958f55e1287a6120048b897c63b6`  
		Last Modified: Mon, 08 Mar 2021 21:52:33 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9de78517be39f734e7e1882b46afaea8cdb7ce9a0b3f7665a3a0e33a658fbaa`  
		Last Modified: Mon, 08 Mar 2021 21:52:59 GMT  
		Size: 9.7 MB (9670271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4c22e4f7cc999fa3fefe75b56d996159c8b4190b98b7b36d80a0e5e24caad2`  
		Last Modified: Mon, 08 Mar 2021 21:52:57 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c239ac2f6da77003db0b8d9bee46a28e2ef72974b205d843b7de6411daef69`  
		Last Modified: Mon, 08 Mar 2021 21:52:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:fd160acb019b9cee4334606628c1835a3c2a55cdaf157b622cd772058f0b7663
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34126380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef626ed9cf808dab1b3f6f9fc89cc41094363728e62d88eceaa7c8bdd39ab4a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:50:10 GMT
ADD file:fbd00ef7871dc27d7ed5fa8c238cdc80652bd87b8033be7de9e54a799bbf10a4 in / 
# Tue, 09 Feb 2021 02:50:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:45:24 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:48:37 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:48:39 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:48:40 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:49:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:49:42 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:49:43 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:49:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:49:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:49:46 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8e683fcc73f4da7d69ce1d5f4e1d77510aa459490068f38db2d8663698b391a0`  
		Last Modified: Tue, 09 Feb 2021 02:59:07 GMT  
		Size: 24.8 MB (24839297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def565d52deae74587a55f60d168bd531ebe8095c594027b7057a8fc1be0e8af`  
		Last Modified: Tue, 09 Feb 2021 03:54:54 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fff3e31705a444ba58f6fedc10fd7e8509560df170ce2a6464e3c7c680f5512`  
		Last Modified: Wed, 03 Mar 2021 23:52:53 GMT  
		Size: 9.3 MB (9285141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:302d9907c27970d03ed0ac50d978a7ec92b9627bd8dfe895d0ce38c29ff8abae`  
		Last Modified: Wed, 03 Mar 2021 23:52:48 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9fe9f8f082ead91dcc43c0af3b0ce2eec1e43e565420891144646e2e66c0bc`  
		Last Modified: Wed, 03 Mar 2021 23:52:47 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:22739469108f3026eb1cc7566b171ad09e6baf29d82ecfe6971acb8b1d390ec6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31800938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24a61c6cff6c522f2e6dc8dc2eefb1283b754cef79e8fc718bc2e851d64dff4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:57 GMT
ADD file:e675d50366bde57173a75f9a29367d765e7da2b7254c5254b64e777cf6870502 in / 
# Tue, 09 Feb 2021 03:01:00 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:49:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:59:53 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:59:55 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:59:57 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Thu, 04 Mar 2021 00:00:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Mar 2021 00:00:45 GMT
STOPSIGNAL SIGUSR1
# Thu, 04 Mar 2021 00:00:48 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Thu, 04 Mar 2021 00:00:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 04 Mar 2021 00:00:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Mar 2021 00:00:56 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:db574d82360c3b60abadbef4f3daf8dee01f24741fc6ab3692aa543558d8b624`  
		Last Modified: Tue, 09 Feb 2021 03:09:46 GMT  
		Size: 22.7 MB (22703384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9978ebb1881387f11e025fb46dce2b3c715f705f6d240737574f8848c27fa0d7`  
		Last Modified: Tue, 09 Feb 2021 03:58:16 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b042e3b0a9b457749c8b6be38159bf336900ac0a449ef7837355b905d54513`  
		Last Modified: Thu, 04 Mar 2021 00:06:28 GMT  
		Size: 9.1 MB (9095610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb11dc12989b181df9b197123d5c719e0263ed7a7dd62a319b386a262407e5c`  
		Last Modified: Thu, 04 Mar 2021 00:06:22 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45586ab18fd80a8fca25174c46c6093922dcbd4130cd774955373136fb442bcc`  
		Last Modified: Thu, 04 Mar 2021 00:06:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:fb7ce8e18b0ce77f8541295869bf9addf4f39936e606fb2f95fd60f183820553
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35345046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:149902bcb92ba5cbb82706a611dfcee896c375e4d9ea66fe4d6a73359d1af05b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:59:41 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:40:11 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:40:12 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:40:13 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:40:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:40:54 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:40:55 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:40:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:40:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:40:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7f43dd52365bce2c2b75f29577aa39d2b5794e2561cddc0678422ffc1f7d15`  
		Last Modified: Tue, 09 Feb 2021 04:08:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab089d5e39e2bee9f1457db0064c673f2197022e4f35bd09866546237fcce328`  
		Last Modified: Wed, 03 Mar 2021 23:44:50 GMT  
		Size: 9.5 MB (9491653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bca2e6c325b028c12e42ea4e7d6d92b0db82199b38df988fcb4e62cefe820bb`  
		Last Modified: Wed, 03 Mar 2021 23:44:48 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48adef33c780445a2435d0b2c14556b53b34fc9ca5795864b6c3cbc7cc4b25d6`  
		Last Modified: Wed, 03 Mar 2021 23:44:48 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:08029dd29e3f4a419baf0ece22ad92d46b2f27ce01cec80f4859d2492f13c0b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37318546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1457ecba48f46c6e0909e9a34ff886af1fd3b5a35c05286c03d3f4da1456539b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Mon, 08 Mar 2021 22:02:40 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Mon, 08 Mar 2021 22:05:06 GMT
ENV HAPROXY_VERSION=2.3.6
# Mon, 08 Mar 2021 22:05:06 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Mon, 08 Mar 2021 22:05:06 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Mon, 08 Mar 2021 22:05:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Mon, 08 Mar 2021 22:05:57 GMT
STOPSIGNAL SIGUSR1
# Mon, 08 Mar 2021 22:05:57 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Mon, 08 Mar 2021 22:05:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 08 Mar 2021 22:05:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Mar 2021 22:05:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b6129a97a33727ea8a598d1e797bccce491920bf29d769880cf2fc6d3e0436`  
		Last Modified: Mon, 08 Mar 2021 22:17:48 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fc7f55bb52d577bb49216caae38e742ba182d2719615fd195125099570f183`  
		Last Modified: Mon, 08 Mar 2021 22:18:17 GMT  
		Size: 9.6 MB (9563873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91893e7877fd0573b74c92a13310c45ca6568bbfc3b61cadce60a54553812896`  
		Last Modified: Mon, 08 Mar 2021 22:18:14 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14935bdf9a0768984c33b8ba5f706939f3133106b3412589747e11f46a54221`  
		Last Modified: Mon, 08 Mar 2021 22:18:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; mips64le

```console
$ docker pull haproxy@sha256:f047f58d1b05f146259a460b5534d4f371a3bfd8a5adeb09a04276656fa00af0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35014317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7140e196cccbd6502dc6775c8fa25da1dea923c269c4fa57aec0831eb87b8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 03:09:26 GMT
ADD file:0222a151f4e5033d9eae98ce2b703a63f52d049dd72ac40bdd0dc2dafe619f0a in / 
# Tue, 09 Feb 2021 03:09:27 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:41:09 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:07:23 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:07:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:07:23 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:09:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:09:49 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:09:49 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:09:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:09:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:09:52 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfb81134097d874e01b495d1fba82e384056d0a3a45f01a69a2e86ae82af1e96`  
		Last Modified: Tue, 09 Feb 2021 03:15:55 GMT  
		Size: 25.8 MB (25764640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a549d56662447dd8cb15faf59ca0fc2eda7a877e9aee16aadd09fd46e4214a`  
		Last Modified: Tue, 09 Feb 2021 03:57:56 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd84d34b65468db17bc6bb2cb72cc70ef09422490d888737d7c029ec4d8e344`  
		Last Modified: Wed, 03 Mar 2021 23:13:19 GMT  
		Size: 9.2 MB (9247729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a561995add47ef6d0a089710e967ccabeaf9d9a416be3e03be23ef058b4834`  
		Last Modified: Wed, 03 Mar 2021 23:13:09 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0499d598e07691795e195c0d80a2dbf4807859d41722ba9689117269d2c452f4`  
		Last Modified: Wed, 03 Mar 2021 23:13:09 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:741a0dc67c8b115376f867d987bc1d9a4bc90619a4939074c94ce0cd1defbd89
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40679819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce2f4a27a4c4caea7672c616fe0801ca3902d1d571793e66f1158d9ace20952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:19:19 GMT
ADD file:9a8cfdf0eab394a693b5cde0700ad47b6e8506ef0b79fabb8a07874b96e6c394 in / 
# Tue, 09 Feb 2021 02:19:34 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 05:52:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:16:59 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:17:02 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:17:07 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:21:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:21:21 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:21:24 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:21:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:21:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:21:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9996b4fb6bc1c50f95ba30f8988c9c89526556fa320d3fda59d3d8359f7810d6`  
		Last Modified: Tue, 09 Feb 2021 02:27:59 GMT  
		Size: 30.5 MB (30519509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7f600bc4989eb9f12d5006a73f5958eb4fe85f86bc4008d7a899bb935b0f1c`  
		Last Modified: Tue, 09 Feb 2021 06:38:36 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f996cf993595d7dfaa53dd8b2756f38db1c17c7fd9711ac10dc4191cec786d60`  
		Last Modified: Wed, 03 Mar 2021 23:31:40 GMT  
		Size: 10.2 MB (10158363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7991881f420b992a3223335c3213fc329c88dffe0516c57bf925f34dd2783fe`  
		Last Modified: Wed, 03 Mar 2021 23:31:37 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f9d3ebe569638afe6c4bad4532d993022b91325ea88fafc3a593a4d0c8848d`  
		Last Modified: Wed, 03 Mar 2021 23:31:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:7caad1df1cc08ce7f758568a4a2fb426d700c62c3dc78d0041de32e5d57477bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35093083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cdecbc4babbecaa160b39e9ef4bd2cc182628cb8bce7bfdd24d2f91c10bd48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 09 Feb 2021 02:42:10 GMT
ADD file:0edb2de05df54191a141bd125f59d7e14eef0cc4576927a247b8dd7d6f255d04 in / 
# Tue, 09 Feb 2021 02:42:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:39:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy
# Wed, 03 Mar 2021 23:41:38 GMT
ENV HAPROXY_VERSION=2.3.6
# Wed, 03 Mar 2021 23:41:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.3/src/haproxy-2.3.6.tar.gz
# Wed, 03 Mar 2021 23:41:39 GMT
ENV HAPROXY_SHA256=6d4620e5da1d93ed75f229011216db81d5097b68bf175e309f2fab2890bba036
# Wed, 03 Mar 2021 23:42:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		gcc 		libc6-dev 		liblua5.3-dev 		libpcre2-dev 		libssl-dev 		make 		wget 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.3 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_ZLIB=1 				EXTRA_OBJS=" 			contrib/prometheus-exporter/service-prometheus.o 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 03 Mar 2021 23:42:19 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Mar 2021 23:42:19 GMT
COPY file:a7db5ef8dbcd831ff68d6ff2fb45bc340539ad6d7a58d54323fd7399d1520910 in /usr/local/bin/ 
# Wed, 03 Mar 2021 23:42:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 03 Mar 2021 23:42:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Mar 2021 23:42:21 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:032413a44cf56b097e48b8221bf475ca1bec26e7a27f35fe61d699366a335b79`  
		Last Modified: Tue, 09 Feb 2021 02:45:31 GMT  
		Size: 25.7 MB (25710021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e65f701864562492efa2c0035134b62d68efdb6e7241a0a2dcc3151e6d5775b`  
		Last Modified: Tue, 09 Feb 2021 03:44:28 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fc0238f1fd6fa72a0d48c70d25c0223d69ee003d98edc91896d34a78569752`  
		Last Modified: Wed, 03 Mar 2021 23:45:58 GMT  
		Size: 9.4 MB (9381115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a706369cf995e0ac6dc64e80d0aa1273c88faef770d5525485b9be6b982dafa`  
		Last Modified: Wed, 03 Mar 2021 23:45:54 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac4428d8a67f044ee63239ab25919c550a35aefffd9dcd18e8dea892fba0a42`  
		Last Modified: Wed, 03 Mar 2021 23:45:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
