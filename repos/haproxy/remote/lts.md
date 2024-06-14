## `haproxy:lts`

```console
$ docker pull haproxy@sha256:4c16f7c3d6e822381b37edffdab4bdd85d8951360e3cd0167d2833e7fe54e048
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
$ docker pull haproxy@sha256:93234acd44f710155854af33408ab237ff6c9ee5f1de90e93327df2191d7269f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41619236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d100039854cde7e952b83d12093378c97d0bc3b6d0b4bdeaaf94ee0b9ddd50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 10 Jun 2024 14:42:35 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
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
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d2f0fc3b6a45898fb88062236c443fa988193e980752f2ebf3e5a780b86277`  
		Last Modified: Thu, 13 Jun 2024 18:28:42 GMT  
		Size: 3.3 MB (3299423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd7f78dc5824394ea362a6b1b17415e59b5c61f2eef5dd36375410bb77f7e0d`  
		Last Modified: Thu, 13 Jun 2024 18:28:41 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c0f3693c613ff56a6a7a0f321c2d8896eec89ac0c4d5ac0cdcbbb91ef02d76`  
		Last Modified: Thu, 13 Jun 2024 18:28:42 GMT  
		Size: 9.2 MB (9167739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e9b0057276ab849aa903c68fe1c5e6e7cf95c73cad05dc02c624715580b805`  
		Last Modified: Thu, 13 Jun 2024 18:28:42 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:1630a21e21f43b72ae6a583e265b6e58dc091582232a2238de4f29365e77b538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2363847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3342febb19366d606c94344b6ed39415f845ab4858b7686bc998f960967c30`

```dockerfile
```

-	Layers:
	-	`sha256:7a5d55e505c55b0ed6396fe135fc4d66f05c7320f502d13302c3c388c54b63e7`  
		Last Modified: Thu, 13 Jun 2024 18:28:42 GMT  
		Size: 2.3 MB (2341666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a20225c138a3e07e3f59bf20a8dccfc72e70723a06b3754208732393de157bb`  
		Last Modified: Thu, 13 Jun 2024 18:28:41 GMT  
		Size: 22.2 KB (22181 bytes)  
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
$ docker pull haproxy@sha256:1470e0f7a3d16cce055867cac994da6c35f065b1e5b6206f34cab5043b8b7ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36397155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca8bd2bb29ba70bc44d5bb9d78d0fa67c69899e3b4ab709da18140e298b66a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 10 Jun 2024 14:42:35 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
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
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc72096e0874162a64de2ac67a48a63a826d5fa3fc4e0696e52da68e59aaf34`  
		Last Modified: Thu, 13 Jun 2024 19:32:52 GMT  
		Size: 2.7 MB (2711040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eeefec6ce70e221b37c51b077547faff5e15542c9c1dbb18804308b34841b2b`  
		Last Modified: Thu, 13 Jun 2024 19:32:52 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125f16f5bd29d3b5366d70ab2f50f4b16b62d45570fb6b0468f9671e911f7ee9`  
		Last Modified: Thu, 13 Jun 2024 19:33:50 GMT  
		Size: 8.9 MB (8944256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbf3409c18e89f48c5cb752b8c47e4f64f79175bd89f3b5f06e15aebd68abaa`  
		Last Modified: Thu, 13 Jun 2024 19:33:50 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:94cee1458841eb85043fca5b64f5606e399cd417a7e2d60e64fa67a9f3a14b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7011800a77614a4bbec63695f246e2b7bf2690afecf84436d3db8fdcd6952612`

```dockerfile
```

-	Layers:
	-	`sha256:b459f7f1f9274434eb5675a597138ab119f73cad1b71f7bc41eaf2bb6fcdebde`  
		Last Modified: Thu, 13 Jun 2024 19:33:50 GMT  
		Size: 2.3 MB (2343924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d9f6a542b0fc432303bd223499e437aa507aed63cc4cd58df2e06da29712ba5`  
		Last Modified: Thu, 13 Jun 2024 19:33:50 GMT  
		Size: 22.3 KB (22310 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:688889e694a4093d6c21f5880f0fb59a8bf7901abf1ffd1d8a1720b3a9d33da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41460595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426f7d14c26ddd3c427d7af44fe16fc9e57577922fd981ad18e6df87bd7faee4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 10 Jun 2024 14:42:35 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dead496f6c8d35ea1c4bf8790353ff6a1883e220cfccc51aa9fbd2e735e62bd`  
		Last Modified: Thu, 13 Jun 2024 18:06:14 GMT  
		Size: 3.1 MB (3122237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8481e04c8af4c1f8825312eaf98e3fe23fb71c26e351cacf45a8f983d14cf7b`  
		Last Modified: Thu, 13 Jun 2024 18:06:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6159b8db2dbb3761de308db94129950dc420ca657836395034774702681ff67c`  
		Last Modified: Thu, 13 Jun 2024 18:07:06 GMT  
		Size: 9.2 MB (9157047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c890054cc4a5a3c1be6b8c578295d6a61113affc5c2bacd05793558c333e6598`  
		Last Modified: Thu, 13 Jun 2024 18:07:06 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:f3053edcd5a4a4528381646b87fc93acec1c2f0d1543285105290099335a2510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2364511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c668dc5a70acc0eeb8f3909b94e34f257ae20b9b71c011c6cca53ec2125339e4`

```dockerfile
```

-	Layers:
	-	`sha256:b3ffbfa3655ae4ea2abc72f4e8817844be052f24756dd08779f39e1db871753a`  
		Last Modified: Thu, 13 Jun 2024 18:07:05 GMT  
		Size: 2.3 MB (2341972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab8d17ea19f5c5806114a072eb49e23325aeb57fc6ada05ea5e42e7906197be`  
		Last Modified: Thu, 13 Jun 2024 18:07:05 GMT  
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
$ docker pull haproxy@sha256:8ed64d813874e8400356059bae1e1f1815ae92cc2fa4fe94e28c849b7acbb306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41146737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105468154be1b8d2f959b2554ce83fc3f591e82bc031f945c5678867e10be150`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 10 Jun 2024 14:42:35 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce14e5c0b553499082c1d565688f457d68916c3c0b7e713db02a098701eb607`  
		Last Modified: Thu, 13 Jun 2024 23:23:34 GMT  
		Size: 2.7 MB (2699018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5b1b4c2e825d3758784454c05256adfa09c495a2dd6565344210f2653919e6`  
		Last Modified: Thu, 13 Jun 2024 23:23:33 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cabb1136d2c1bfb5a05f69fd883a7aebb25c8bb8107d156e87664f5b500c67`  
		Last Modified: Thu, 13 Jun 2024 23:28:43 GMT  
		Size: 9.3 MB (9302257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e55aaf6c72d0c8d2a0bcb9f554d6d683ec7714f5d06f1285cd8d6e389bdadd`  
		Last Modified: Thu, 13 Jun 2024 23:28:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:8bdc0ff090f0f369ed2db91056abd6c74e740ad5468560e634f284a13402201b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179026f41951d03225ce0b4f092c6c0501fe70ef437ae6241b9ae772ab8aa575`

```dockerfile
```

-	Layers:
	-	`sha256:f63c3690255dc8b1f164a668ba7d25150af229fd2dbdf220eb8077626e382406`  
		Last Modified: Thu, 13 Jun 2024 23:28:41 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:f74d4bcacbbb9b9eee53ef721dfea08a322ae9c56c350440de3329f41b1d24c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46330013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939588d80965d59ba10769701f26c3c1e4037c688452c107806cf527e0fb0f43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 10 Jun 2024 14:42:35 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
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
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779fc550baf2dc27749971fe960182aca7cb33b10af56e574beb5fbf337e241a`  
		Last Modified: Fri, 14 Jun 2024 00:24:27 GMT  
		Size: 3.5 MB (3501596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31942f152cc8362666a8f47d482d233e655b01422e898b1662469084b36615b5`  
		Last Modified: Fri, 14 Jun 2024 00:24:26 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cff8aa09d3eb80db090a9b870e742ce4c0041315b167872408b2d720f5c649e`  
		Last Modified: Fri, 14 Jun 2024 00:25:55 GMT  
		Size: 9.7 MB (9685583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db70bb7a288c6567889fbdc1aa7fee8105b250a801f217436151102056771fe`  
		Last Modified: Fri, 14 Jun 2024 00:25:54 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:c796e4c69f271f8951fb9f0b4ede9c2497ac760c5d7259c11075a3f9ec93d860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2368239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dc83755dd8aa2309e68ebaa8da18c65694789168bf003fc836bddbbed871ba`

```dockerfile
```

-	Layers:
	-	`sha256:3c5c4e67d087efe0d18c610df7b801823e943b1831f211c2e92d3e9b5beb8a4d`  
		Last Modified: Fri, 14 Jun 2024 00:25:54 GMT  
		Size: 2.3 MB (2345991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7196564d40aef6ee3158f46eb670cce374ab3a1d5d22b66a05b6a1d0ed8cb86`  
		Last Modified: Fri, 14 Jun 2024 00:25:54 GMT  
		Size: 22.2 KB (22248 bytes)  
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
