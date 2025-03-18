## `haproxy:latest`

```console
$ docker pull haproxy@sha256:e51765f5a135cab0906c4ad52b37c384515af807fdd7bf827ce921c48af8825b
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
$ docker pull haproxy@sha256:ab1e6457b94b2cb09d287aff2fd7199e0964ae333fe1c4d93adaaf0a4e06b400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41721984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbacdc4037c50dc81ad518b420417efb74e70b23a827cabc05db7e59c611360`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c0049f1195b0577f6707bd5efa4895831db8d76c0e0aff66890fde0b1004a1`  
		Last Modified: Mon, 17 Mar 2025 23:13:19 GMT  
		Size: 3.5 MB (3499359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11136e79dbfa2ea9985a6aac4878a50e805b0cafc38e8e6f84ea551bd90a7a86`  
		Last Modified: Mon, 17 Mar 2025 23:13:11 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090d07d7aa5811c5335aed9d3bdae59c01938a5aaf9aa7503797f15cd0027949`  
		Last Modified: Mon, 17 Mar 2025 23:13:19 GMT  
		Size: 10.0 MB (10016123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a0e5f066f7bbf1761dbd289b50e14917d0c97f74cd5ca2189ee4517cfa8a26`  
		Last Modified: Mon, 17 Mar 2025 23:13:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:fc336803932e86bf5869a7d86ec3e9ac9fba43485bab9ec46a40ad60817290d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545e37b309057fef6c221d641ccbd41bf4cc9bf2e46f4885862483a4ec5a10f5`

```dockerfile
```

-	Layers:
	-	`sha256:0250df2f27e4575df1ada0b840abb4a6022c91dc499780933eb9b5d177327345`  
		Last Modified: Mon, 17 Mar 2025 23:13:19 GMT  
		Size: 2.4 MB (2369071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cee3c21f60f3bfb648ae893a7894cada33be0415b69068ecdcfd458be5a7c46`  
		Last Modified: Mon, 17 Mar 2025 23:13:19 GMT  
		Size: 21.8 KB (21773 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:4a5fd691b8b74cdef78c9179a84b6bf3067867480023bd48f065cb3378a0f38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38819232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964249dba15a0e3fc1245695c4b15088d705f3e6bfab5b30092042895c2c92a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a06bf00a22e98835898fabeb6f4b4e688d5e3dd40a63cf933c7a8f01f50907`  
		Last Modified: Mon, 17 Mar 2025 23:15:23 GMT  
		Size: 3.1 MB (3073487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159e989cc552c37f191008030afdd4b3a51980fe51d0d335aac5432300cdffb3`  
		Last Modified: Tue, 18 Mar 2025 02:24:19 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee39fa3e56964bc222d59625bf9e184b8da06e1bb7d8c6dc846e37b17592807`  
		Last Modified: Tue, 18 Mar 2025 02:25:39 GMT  
		Size: 10.0 MB (10008253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f264488c531641bd9d9357e881e931fe55b9ede3787d904c5d876715bdf9ebef`  
		Last Modified: Tue, 18 Mar 2025 02:25:38 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:5145cdf1d733d13fc81efe75a871a3f0bb3d942196d00ae323dbbdbae7113e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2394476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a69f9f0a7fe599e86aa552ac2e21bf9a0717d40d35af89e32e657ef843ff4b8`

```dockerfile
```

-	Layers:
	-	`sha256:71555d98bb73d9b00c86e812bb27d2dffc4b5c062f06d864a5b83d0858832de7`  
		Last Modified: Tue, 18 Mar 2025 02:25:38 GMT  
		Size: 2.4 MB (2372585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:853d70f04c76bea32a455f3826436ba5d67ba69b6f967bb4c78f9600c510a0c0`  
		Last Modified: Tue, 18 Mar 2025 02:25:38 GMT  
		Size: 21.9 KB (21891 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:487e136076ed52a878cb90588f3c58df489224d65ad92f77a07ae6694de26762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36641863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4102aa654069b66714520c6beb715c9496d2c0869bf4006bf3574bc3d196fb5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9c2cf1db117d5893aa91007c3b5be476fdffd36f19c82f0cb4e8aebf9d64d3`  
		Last Modified: Tue, 25 Feb 2025 02:18:20 GMT  
		Size: 2.9 MB (2907796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404fdc0fb57d39a8e26e53fce5df0d8735e863f965a6f0adb560d70a9cb5e793`  
		Last Modified: Tue, 25 Feb 2025 02:18:20 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8952bff13ffb8acf33f0841d7fa8293820556d9084205ad6d23f7eefdc1da58`  
		Last Modified: Tue, 25 Feb 2025 02:19:13 GMT  
		Size: 9.8 MB (9812693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51cb1bca945b9f19da8d0a8a774a16deff37ec0c9791ee6dc4d8af6d9ffd373`  
		Last Modified: Tue, 25 Feb 2025 02:19:12 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:004387e7eab4799e06e061a2d63310a8ab37e0395e89310cdbf8e0a5b931f988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd731e1f9de26526cd71270e5511508d01e956dd9a570871221af79630b36ce1`

```dockerfile
```

-	Layers:
	-	`sha256:a8a6831deade886ed3b41a63982284e33af95ed4a555a0e1bbf47e28d5862f61`  
		Last Modified: Tue, 25 Feb 2025 02:19:12 GMT  
		Size: 2.4 MB (2371306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfa7786a21c4799a0fb9b8c1039eeb1f09ce566b39a50d81eca5471b08629962`  
		Last Modified: Tue, 25 Feb 2025 02:19:12 GMT  
		Size: 21.9 KB (21888 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:f71049073870c7facd9ad8495bd3b02d655f0cc1ddeb7a2cd527cd40f6fb87d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41360105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4584d972ae771f5054c18199109eb03cc22172b75e978952907c0171d3ed2dff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b5a9c7e92ea9bae5a7a0483f146d25b0a03f857b6684921f286acf0e6777ea`  
		Last Modified: Tue, 25 Feb 2025 02:20:01 GMT  
		Size: 3.3 MB (3322885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7b4ee7e951b37043152ade0847099b1f46f92e07b958859030ae0f10fb4e9b`  
		Last Modified: Tue, 25 Feb 2025 02:20:00 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ed0f2753c8f1c99271ce1642d4a8d155dcd489e0a4102ee1bd09c63fc4967d`  
		Last Modified: Tue, 25 Feb 2025 02:20:49 GMT  
		Size: 10.0 MB (9987155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafecde205479d1ebb01ddcec3cb9393fcc385a48ed08f22a6095e62c6ce0717`  
		Last Modified: Tue, 25 Feb 2025 02:20:49 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:38e6f7db7f2ac6cb80662c24b2639fba8e8e2f3b5c19f352b16e289d630be1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2391274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36adbc453da45054cdea0e2efbdc52a5af7c794ce8e292de36d0c3e187da4f6c`

```dockerfile
```

-	Layers:
	-	`sha256:896781d59317d77bb4d5974122ef0ae7a064eaa5d96707022c72f907c1668d90`  
		Last Modified: Tue, 25 Feb 2025 02:20:49 GMT  
		Size: 2.4 MB (2369346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ed52e1ba5576e3d0259b9de206d292d04088af1f718ee05f9a79efed93a0782`  
		Last Modified: Tue, 25 Feb 2025 02:20:49 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:020a23c6edd60f421de4b36fe32caa21fceaf6d98d10c31115730aea04e66a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42443075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ec514e3a4a7f1a6761e08bfcab4dcfd6db6cc61bf95d15e19a0006adda57e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cadead52749063b96e13dd2a889ff0d752c169ebf517085465bcd00763460f7`  
		Last Modified: Mon, 17 Mar 2025 23:26:07 GMT  
		Size: 3.5 MB (3503408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b27197f6d64b5ed020420080dab2741a3218e77347640f955bbdd82f06e91d`  
		Last Modified: Mon, 17 Mar 2025 23:26:06 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd36bd5f66c14c5c25ee40e08e22e1c24c275fd91be421a719a3f5e8ff3aac0b`  
		Last Modified: Mon, 17 Mar 2025 23:26:07 GMT  
		Size: 9.7 MB (9748499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a782d14963a13621987c53de7f6fc0119589d647c26a6badaa8be4771e086b`  
		Last Modified: Mon, 17 Mar 2025 23:26:06 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:343936e5ace5e020f90d651d4b6f787b6c307fc31f6b00417e10a758da401798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152986681ddffa2a195c7b6a631cf344345d2aa3d01d0022d984a5d0104b5b74`

```dockerfile
```

-	Layers:
	-	`sha256:17687d261b14c10690c735efaa4a8be82416b4c840e192642364dbd0d904135b`  
		Last Modified: Mon, 17 Mar 2025 23:26:07 GMT  
		Size: 2.4 MB (2366199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d76b3d3101112bff878b789130b7598bacc17d507674d3d071c7cc114bd44d7`  
		Last Modified: Mon, 17 Mar 2025 23:26:06 GMT  
		Size: 21.7 KB (21723 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; mips64le

```console
$ docker pull haproxy@sha256:e2553890a6593771a39d1c4d562d84b8b5a91433d9dc0f9530c2199fa1730b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41509321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4b60d948de552e03fb9b27aa7651c06e343e0575b138e9fc5e3c0e783bd12`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c82bfc1c2f5e4b0dc4b532714b8582fae92d04a9d4c6e432252fb2e247fc44`  
		Last Modified: Tue, 25 Feb 2025 02:24:09 GMT  
		Size: 2.9 MB (2895386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d134d9bfb627f1719193c98a83137b618b72692f2b807ec8b91ad1507959f317`  
		Last Modified: Tue, 25 Feb 2025 02:24:08 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f168b861087b1b2a2c03f310fbd49ac0e75a6a89936860f6a0f2863778567860`  
		Last Modified: Tue, 25 Feb 2025 02:29:04 GMT  
		Size: 10.1 MB (10118607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7f4ebb43b12fbbc6d5643e518fbd11072ac9a954d204ba438fecbf4965109d`  
		Last Modified: Tue, 25 Feb 2025 02:29:03 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:0ebea310c156e07c3d68c33246d876a42c2ec2cd4ad233c7b301b66bfa0a181e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa1fcdb5b0571500c693cc3c525d581930214dfc2abc86fd5b8c1a74f666569`

```dockerfile
```

-	Layers:
	-	`sha256:8546480388ca37acd62249f8a4515d23d7586c0b96b4f9822731e206ce73d58f`  
		Last Modified: Tue, 25 Feb 2025 02:29:03 GMT  
		Size: 21.6 KB (21648 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:1792f02dcbcc34de6458dadb5e39199f3965c4408aaff6f45745a59d8f507162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46262142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413668c3df1aba4a1f3d3cc591373b984d056698f576cf46224a25d457f741a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ba39fe77c93589e1f3815ca27890f913cbf8ffe9ae54836f9455f556522221`  
		Last Modified: Tue, 25 Feb 2025 02:18:32 GMT  
		Size: 3.7 MB (3702978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bc6f29027769d00b506a51e73aa8c38c1b8573e422dbeec27479d1dfca9308`  
		Last Modified: Tue, 25 Feb 2025 02:18:31 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad995f48b4827fb8c2b9a18b10d730e429960a4d94d72776a49085676c5f2f12`  
		Last Modified: Tue, 25 Feb 2025 02:19:46 GMT  
		Size: 10.5 MB (10505208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbd4a91ddc96b9f0e28a0e755001d1620bc707cf2fbab1b3bb18b800980148b`  
		Last Modified: Tue, 25 Feb 2025 02:19:45 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:110f3f1b1d7914da7abc3c524747ad312db261fe734ead0025d28febfa97f7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f7335c854c46f282f0d306ad99e83d789cc5ac72abb6e7ae5a02dc42ca2875`

```dockerfile
```

-	Layers:
	-	`sha256:b7d11ece7b28e5aa2a6934a9a935a6c8fc35709dcdd9c155059a8e207f131523`  
		Last Modified: Tue, 25 Feb 2025 02:19:46 GMT  
		Size: 2.4 MB (2373377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea21f774fb82101e5e78be05a4504a680befc3f700b9126f5ae50e859c2295fb`  
		Last Modified: Tue, 25 Feb 2025 02:19:45 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:8491465dcd065d8c4284e966a9c00f2d63b643b1aefbbc79a833dfd7ccb35b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39921946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74df609b612636c6d888847f10b52a62587a038a2964787fcdce0f600e3021a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 20 Feb 2025 18:13:33 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_VERSION=3.1.5
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.5.tar.gz
# Thu, 20 Feb 2025 18:13:33 GMT
ENV HAPROXY_SHA256=36e2816f697f389233137dc7ec9559faa7703243395ad129af091b63f4f099cf
# Thu, 20 Feb 2025 18:13:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Feb 2025 18:13:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 18:13:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 18:13:33 GMT
USER haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Feb 2025 18:13:33 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1ac92efe54bfe6c889fb070cf9414a009a5bd1d6879252ec25cb105cf7038d`  
		Last Modified: Tue, 25 Feb 2025 02:17:47 GMT  
		Size: 3.2 MB (3163397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec25f4589ffdbb577c0bcfd5ad87b05e2df25d8b5ef48bf8767cdfc6d5ad8f4`  
		Last Modified: Tue, 25 Feb 2025 02:17:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535f5c181709b7dadd1424615ca8fe7ec29bc2ba93007c40a1db551ed750c44e`  
		Last Modified: Tue, 25 Feb 2025 02:19:08 GMT  
		Size: 9.9 MB (9892070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d22c44d1e43c1b10c91fb4e34070d09a242ffdd0d389b3ef9e011c79ac4f646`  
		Last Modified: Tue, 25 Feb 2025 02:19:08 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:6d29910aff021cfbf311685b50038ca7063e95aba2cdc3f573efa9798b74851e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7507deb1d9db7a7837f07c2ef04bbd7286ef72fff3c172f0af9f0009dad4fb11`

```dockerfile
```

-	Layers:
	-	`sha256:538a16c55e0dcf2e853cc6e2fa6a010f473ac1c5bfc90609dad6569c66814b07`  
		Last Modified: Tue, 25 Feb 2025 02:19:08 GMT  
		Size: 2.4 MB (2368785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9048839e1388dd1381ef0739023b2470da17abe4f99949fc7f4ce8747b4a7328`  
		Last Modified: Tue, 25 Feb 2025 02:19:08 GMT  
		Size: 21.8 KB (21770 bytes)  
		MIME: application/vnd.in-toto+json
