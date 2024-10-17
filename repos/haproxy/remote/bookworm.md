## `haproxy:bookworm`

```console
$ docker pull haproxy@sha256:abeaa648191a9acc8962136435c7b2920191a77376da898555c895738e23fe60
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

### `haproxy:bookworm` - linux; amd64

```console
$ docker pull haproxy@sha256:ae9eae084b25d9d6b8cb5c1876b6d6a8b61f7baadd92a42efba829e3755e7c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41813534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5cd2e6f7c97f475796bbaaf54ffcfca9462007125a9474ca15b286549131ffb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 19 Sep 2024 17:21:03 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["bash"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b3efb1a2dd1f243becf7a4fcf73dde5a51ce33bc59c76833c6d1ab27863aea`  
		Last Modified: Thu, 17 Oct 2024 01:18:24 GMT  
		Size: 3.5 MB (3498982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbdc2b66490b8e3dd67dc92ee844abf84fd8334f9c7d1ff5957a4f748622608`  
		Last Modified: Thu, 17 Oct 2024 01:18:24 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79b6a981f970230bb2ebbf11b7b5ef713e9b0f4ba07f6b7fefb0f5bdb4e13f7`  
		Last Modified: Thu, 17 Oct 2024 01:18:24 GMT  
		Size: 9.2 MB (9186628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d014fe376d58e92db5f439b3798417fa09118576afc6458503fa525bf7b220b6`  
		Last Modified: Thu, 17 Oct 2024 01:18:24 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:3e7ee15cd47cc5971a71fd194d5721b5a8c62ffac078fa52f1e6f8ac643439ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8788a1c3b934f46f655ff7220aa94b0efffaa3b3a7188bab96cc155c7b086844`

```dockerfile
```

-	Layers:
	-	`sha256:024d2e10f8380e40f3090789ee2ab6d9ddd8536c3220db6d5efe8b9de8c9c6ef`  
		Last Modified: Thu, 17 Oct 2024 01:18:24 GMT  
		Size: 2.4 MB (2360705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff76bb49cd3fa64e3584bba3c06226be21ec608eb12060c5ca904c4c6695d971`  
		Last Modified: Thu, 17 Oct 2024 01:18:24 GMT  
		Size: 22.2 KB (22220 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:ed993b25538b2fa1c5464949a3630aa08ea1729a9b27d682b04f8d4713a44fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39090807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb142e8fbd1c19f594dc6c0e2b6d17b5479c04d2ffa97c639f2bf37b6a959cf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 19 Sep 2024 17:21:03 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["bash"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6612936db4c2df3cbb250619be5b5ca4599afefe5aa0606b8f34dcf44e1ee107`  
		Last Modified: Thu, 17 Oct 2024 04:01:15 GMT  
		Size: 3.1 MB (3073119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d177f8968d4e7ebe30aab7d00bec30f2139752a53290ccc4fbfb85d8a67d18a0`  
		Last Modified: Thu, 17 Oct 2024 04:01:14 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857e3e0ead7762059f53349ae91ba42e82448955ef0f7868a3bd95b1e20bc92d`  
		Last Modified: Thu, 17 Oct 2024 04:02:27 GMT  
		Size: 9.1 MB (9128739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6b07c0e9d30def1f29c205eada8590ba8c34339f83b54d67b34d58b833bfdf`  
		Last Modified: Thu, 17 Oct 2024 04:02:26 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:6d772e0d02e0419190564971d56299a0e26934520728f78451c8e100ec1c74cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e044856934495007e00f625e450ae106c30e64f744f14883aa50959c4e49d01f`

```dockerfile
```

-	Layers:
	-	`sha256:a78577d155d5ba903a979833ead0f20906bdec5e797574655c805b10c32f6f1e`  
		Last Modified: Thu, 17 Oct 2024 04:02:26 GMT  
		Size: 2.4 MB (2364128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d35c6f050daf4caafd10af1cdce0b7b91e2d61edb6d33a70b2e551affdfa501`  
		Last Modified: Thu, 17 Oct 2024 04:02:26 GMT  
		Size: 22.3 KB (22348 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:1b2c04c48a787537bef82d0d69497e9efc309f622d32590a4ac7b862b1b98ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36588626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba5148b74fd9d562b254947e9d360f6c832c7c2da602ed12fb2e2de9426853d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 19 Sep 2024 17:21:03 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["bash"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b508b0a2f2f833fc13e49cf6d3fbde6f84f2d61753ee83562ec831ecd44094ac`  
		Last Modified: Thu, 17 Oct 2024 13:20:00 GMT  
		Size: 2.9 MB (2907436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acff7892b4f4f113a63579215e449dc6151660f5f41289d2fa7fafac2619898`  
		Last Modified: Thu, 17 Oct 2024 13:19:59 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489c1b50dbc21d99001d1b549061edca286d27a561dae3632f7f2a06b29da011`  
		Last Modified: Thu, 17 Oct 2024 13:22:03 GMT  
		Size: 9.0 MB (8961359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae549147373b51a97060924af936f644f2f7525013e0452961320cb19e85282a`  
		Last Modified: Thu, 17 Oct 2024 13:22:02 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:97f6b8cc6a716af6f35fe29d797ffaf4eb392caa1fdae792c3522e11a3b357a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d19c0243d53d8e64da472455152ecdf83c9c8ae692bd074c08e630846c2b06c`

```dockerfile
```

-	Layers:
	-	`sha256:6091ccd209762fd8282878a7e930076a79379069eaa3e718d478575953a9ce08`  
		Last Modified: Thu, 17 Oct 2024 13:22:02 GMT  
		Size: 2.4 MB (2362963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a6329426a4cb921f3be41779468f56507e1e47229fdcbf93094802a36e43c1a`  
		Last Modified: Thu, 17 Oct 2024 13:22:02 GMT  
		Size: 22.3 KB (22348 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:50af7df0fa394b59c3b22164318070abf28763ca2c9e65c474f60a11808b5adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41659576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a687a9c22afde341576caf0cb1080a1047ddd584ca84e12c15e37cb5b39cd71e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 19 Sep 2024 17:21:03 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["bash"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac73647c8904e50577771cc62b4fff969f2b0270d476bf12d93c8032da1c6278`  
		Last Modified: Thu, 17 Oct 2024 12:33:55 GMT  
		Size: 3.3 MB (3322424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb92beeee67c924c83067e8437b11005e52f67f6c3ca9667770774f50b5434b`  
		Last Modified: Thu, 17 Oct 2024 12:33:54 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9cce3014d026ba3c6f70d4675f8c636b033d4b3c4f701dbd3092bf04248acc`  
		Last Modified: Thu, 17 Oct 2024 12:35:03 GMT  
		Size: 9.2 MB (9179174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a4633e516d9a724eb4ec5e43f0281881aed86dc1846da2a84ade73e64d5dc2`  
		Last Modified: Thu, 17 Oct 2024 12:35:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:74db09229ee3f20651fc3bdd87bcd1e8587f58bdf087686050159dfd892d44f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c0c86e8e7006d46650070420be842597e2c782c98c0ed52f9541a6796ba0cf`

```dockerfile
```

-	Layers:
	-	`sha256:6fff70bc8c43c3feeb830de29bfd23744772df60cb9f9b3d9926734bd9bd908c`  
		Last Modified: Thu, 17 Oct 2024 12:35:03 GMT  
		Size: 2.4 MB (2361011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81250719c6f169c276879c6b31af281444ce1ced6e7197ec2e143eae47c53d4`  
		Last Modified: Thu, 17 Oct 2024 12:35:02 GMT  
		Size: 22.4 KB (22396 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:cf2d3750853470baad3034b5b135ff854b5f32916db9a86ef309bc108e47c3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42593897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446014a3f0393edbee0d6f96d5cfb1cd4879dc468826a167436569d2aedaca81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 19 Sep 2024 17:21:03 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["bash"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745c0e345716bc5ee4dfe4dc68ccb2b36ec2462a47dce36ee879a69ab26ca1a6`  
		Last Modified: Thu, 17 Oct 2024 01:18:50 GMT  
		Size: 3.5 MB (3502388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0aa370e142ad8ec4b54c27bb7a751f781f916f2b2d85477b7dde41f04a3794`  
		Last Modified: Thu, 17 Oct 2024 01:18:50 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9608ae0e20743947022bbe450872bdbf5c00e93bc32cd6beb3c96daaaebf992f`  
		Last Modified: Thu, 17 Oct 2024 01:18:51 GMT  
		Size: 8.9 MB (8945601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa595520e42357ef91be9608cb6e5a84befd9ad3893f47c70080d31d0ca30e1`  
		Last Modified: Thu, 17 Oct 2024 01:18:50 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:e4c705714e4bd7b90c1d868b5a7d62a57e836a7e9170e15879a265be95690063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61417e5b6f6a54ca87ced297bc54c840fc5b900026919654318125f080174221`

```dockerfile
```

-	Layers:
	-	`sha256:d885122210cca6a8ddf533b8f7b2577a37b65878af75b79531e488cf2ed3915d`  
		Last Modified: Thu, 17 Oct 2024 01:18:50 GMT  
		Size: 2.4 MB (2357822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b6c1d811ed4d2aa11a353f6edf915fba5ecb9a6b035429dcad6fa54e27476a`  
		Last Modified: Thu, 17 Oct 2024 01:18:50 GMT  
		Size: 22.2 KB (22167 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:f9ccf1050bb1f6b75fc102e8ed20fe6cadc55019ac654dab44707a6aa75421cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41341260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f8162bbe216912dbec5c438feb72f70ac1816228d2bd603debe90afcc5672c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 19 Sep 2024 17:21:03 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["bash"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbe4629f9c394b6740a6a015fc86abac83ccea83034434b9c8e674899e1bdb5`  
		Last Modified: Thu, 17 Oct 2024 16:56:27 GMT  
		Size: 2.9 MB (2894506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995942aeafb1f183607226eb0ee59302a14057971dbdf96a6f6e9fb2ce2d909d`  
		Last Modified: Thu, 17 Oct 2024 16:56:27 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9350dd10c3fe424648c3dc1833ef842d1ff5fad6993d0421c0821a26876119c`  
		Last Modified: Thu, 17 Oct 2024 17:02:04 GMT  
		Size: 9.3 MB (9320334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e07c053e1b91ffc4b0e4417fc3a71a7e3581bddc31e404941f39d8a0c24a89`  
		Last Modified: Thu, 17 Oct 2024 17:02:03 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:6d6134e8bb38b541456d639724b5a8940f3754eb780d97b069395813a1b8bf36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc36a32f83c9e819fc884d9d1b405e688bf083a317c9fdc9b298635f912b3d7`

```dockerfile
```

-	Layers:
	-	`sha256:24d081004ec88bec72f1e8ec9a813838393afb12f7aeb9ed515860d4f2c86656`  
		Last Modified: Thu, 17 Oct 2024 17:02:03 GMT  
		Size: 22.1 KB (22100 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:5ea1bb714c864f3b37ee186a47b4f269d5abbd044fc355ec724f1178e6333f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46528583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71df8e609d645fd03dcb129a71f06c2b1678c81c209cc6e3f3fe851e43dc1ca6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 19 Sep 2024 17:21:03 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["bash"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38713e34abe7afb308ec0015a994e7d444f8a9825a56e05dbb5968bac9f09f3e`  
		Last Modified: Thu, 17 Oct 2024 08:27:51 GMT  
		Size: 3.7 MB (3701565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c358b24578b3c4bfa39c35300c9517f9bdc57c2cb3bced79f974fc9e8f3f1e6a`  
		Last Modified: Thu, 17 Oct 2024 08:27:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a4568f38d305c7b3bfb402b099cb9bd155ba918987a9bcf8ed68d5cb4dc163`  
		Last Modified: Thu, 17 Oct 2024 08:29:24 GMT  
		Size: 9.7 MB (9703176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce88aff29030c2fbe8d20e2babad93e38073f9b233bd8e89adfe470f675cc796`  
		Last Modified: Thu, 17 Oct 2024 08:29:24 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:9a79fedf9cd81fb310ea6a89a3ede2e4468fe77d7c07ebc350e533072055042f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02086c6b7e7c7282704662b35a56a2db33bec450b6b1ee95d63d85676a13e128`

```dockerfile
```

-	Layers:
	-	`sha256:19c23c17e36a1545f26d37df683af4f63c42139563ff81b8968a77870c51ac69`  
		Last Modified: Thu, 17 Oct 2024 08:29:24 GMT  
		Size: 2.4 MB (2365030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9a23d82957688efe3a5f9d0582c72eb61691aa579221907d71045088487e9d6`  
		Last Modified: Thu, 17 Oct 2024 08:29:24 GMT  
		Size: 22.3 KB (22285 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:76fdbec9284c64cf59ff5d1a49ff54dd6a1a8823200fdbcc6aa88174ecc3b4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39724558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02de85b12b963a7809b82b8e40ffefa72825c35419457edee98f5873b6a16cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 19 Sep 2024 17:21:03 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["bash"]
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_VERSION=3.0.5
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.5.tar.gz
# Thu, 19 Sep 2024 17:21:03 GMT
ENV HAPROXY_SHA256=ae38221e85aeba038a725efbef5bfe5e76671ba7959e5eb74c39fd079e5d002e
# Thu, 19 Sep 2024 17:21:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
STOPSIGNAL SIGUSR1
# Thu, 19 Sep 2024 17:21:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 17:21:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 17:21:03 GMT
USER haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
WORKDIR /var/lib/haproxy
# Thu, 19 Sep 2024 17:21:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a412cbe356f754224c707cf0b43190beb406e2aaf995e9ef9ebe479ff7374c`  
		Last Modified: Thu, 17 Oct 2024 13:04:24 GMT  
		Size: 3.2 MB (3162467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cd77044314ab1ffb7abed88c1e962478418ba9eaf92784de655ac8a7360581`  
		Last Modified: Thu, 17 Oct 2024 13:04:24 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9859006f7e4f7d5b14ee7a0c66005081e840e7b10424341e1027d4062fc136ca`  
		Last Modified: Thu, 17 Oct 2024 13:06:56 GMT  
		Size: 9.1 MB (9070371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ba0ff50b2babd616f70320fb5c28a310d6a2ed0d184d6fa42216200f9e27f0`  
		Last Modified: Thu, 17 Oct 2024 13:06:56 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:001a03793d1ea8e33be8df2ab1ef915b28c9a1669f3a289d890db2b18b0d3115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f214725915f1d366525c4cf16d3f326f530ee86e919453d215ca47ad172936ef`

```dockerfile
```

-	Layers:
	-	`sha256:e5e2afce348a7f35a72bc5eb6d3f01e115c7dc797b1fe164469d81bf171b49ff`  
		Last Modified: Thu, 17 Oct 2024 13:06:56 GMT  
		Size: 2.4 MB (2360534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b73522ca97c6b838bd4a1f6e006350421484d4430a9aa11e74c3baf0879bb2c`  
		Last Modified: Thu, 17 Oct 2024 13:06:56 GMT  
		Size: 22.2 KB (22220 bytes)  
		MIME: application/vnd.in-toto+json
