## `haproxy:bookworm`

```console
$ docker pull haproxy@sha256:b068b18fa6cef9cb46a6cfd609a428340c70be37dfd324506b51d19d3e8f96fe
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
$ docker pull haproxy@sha256:8d4b6239725ce469d4537885d870e1d2fcbc44bbd9f188d0017b9049d8521f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41813770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0632185672ee8d79fd16d2b15ab7b5e6d598aeac0959f28c5ed0fe06111733f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:47 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 04 Sep 2024 22:30:47 GMT
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
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f958bdd3a08732be0256370b83d6122be36ba2fec98ee3847e32071a68c705`  
		Last Modified: Thu, 19 Sep 2024 18:58:01 GMT  
		Size: 3.5 MB (3498996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f08e816132965e7b896a0eb45a37824eaf6cebbc1514f4a2087f583f9278f81`  
		Last Modified: Thu, 19 Sep 2024 18:58:01 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a6f8317a48b906420d311d7258cadd30c7b3256d401bee2312dbdf23ec07b0`  
		Last Modified: Thu, 19 Sep 2024 18:58:01 GMT  
		Size: 9.2 MB (9186645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9943ea4f028833c71edf47dc70d8d49b8235f274eba0bd93070f4331a8cc22f2`  
		Last Modified: Thu, 19 Sep 2024 18:58:01 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:481dc15a03739129e65b32b1c781e06b344f70b633b9409fd6d2100af041ff4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 KB (25655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0405d26ba0a02c732f752da2f6d0c95b2e59993a429553106fb78c589841b6a5`

```dockerfile
```

-	Layers:
	-	`sha256:91dfefe037829391fa0d60f7122b244a24a99c6e96df8ba16c04e3ff1e3bdb94`  
		Last Modified: Thu, 19 Sep 2024 18:58:01 GMT  
		Size: 3.5 KB (3473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d65e36eb8b9156812e8751cb7c902cfe9081312857e61d06250115094607823`  
		Last Modified: Thu, 19 Sep 2024 18:58:01 GMT  
		Size: 22.2 KB (22182 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:8b52ae56650d66aa0be8b99a0d9506952bdbb8d3a28c773a252ff1b3136cdf9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39090968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529b5ed193f0c6f344eef0eeb5e9038eef9cf7801ab76e12c7e6f64e47883319`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
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
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10da2a8092670417ce3a236da9617fb1607e6d2977cea4217d1412fedfc51997`  
		Last Modified: Thu, 05 Sep 2024 03:15:05 GMT  
		Size: 3.1 MB (3073135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d405e88f3f635b0a6018e515984ff75f49b19884d00287dbcc4f0d3aef535caf`  
		Last Modified: Thu, 05 Sep 2024 03:15:04 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c96f262c0ab53ea5b73fb7b49fbb837b642799c860bb62b2cfc7a6b58d0f061`  
		Last Modified: Thu, 19 Sep 2024 18:59:48 GMT  
		Size: 9.1 MB (9128780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c730d89b836a7dfd2f39c90d0b34f7892d31e92c11bd317a61061aa7ea913d2`  
		Last Modified: Thu, 19 Sep 2024 18:59:47 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:57e68d9fc6036c8d109dafd0568eeeac8fad4b581e7ce5e799817828367abbe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c1c634af0067a22c971c3acdd28871690e064b285fe9d170a5996a3989e580`

```dockerfile
```

-	Layers:
	-	`sha256:63607f6e8b32c43a786767c6228de29f961cb00c42a6d669fb875b5819cd0d90`  
		Last Modified: Thu, 19 Sep 2024 18:59:47 GMT  
		Size: 2.4 MB (2364115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc216ac689ad86d2e1d517d911e020f5387db5eda7e12f0dd62477c0517976a`  
		Last Modified: Thu, 19 Sep 2024 18:59:47 GMT  
		Size: 22.3 KB (22310 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:8a25646fccf75c60389f133cb579137f328d21d36dded0bba7d483ecf0fecc8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36588714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d670a440912bf786bc1411afd284f672248aa04bc1aaaea2d8b9543831afce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
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
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8075eb848fa904c0d02ebb20c4745fee8be54bdc634ff22d0a646f4fe3eb74d5`  
		Last Modified: Thu, 05 Sep 2024 04:13:53 GMT  
		Size: 2.9 MB (2907438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feeb91f7a335b39306394da2127faebb621a165bc6a7fa860bc7fddbaddd5e80`  
		Last Modified: Thu, 05 Sep 2024 04:13:53 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b3ab4e96fa3ec0fff4928a3efd4adf059c96bec28b02f82455b59e724d7bfa`  
		Last Modified: Thu, 19 Sep 2024 19:00:51 GMT  
		Size: 9.0 MB (8961375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa53ba5cb1f71979f301d0a0aad869fa6fe24f27417ce7f53a4ae9d0d8a19ab1`  
		Last Modified: Thu, 19 Sep 2024 19:00:51 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:b2a31247b778d0443437df64049741caecb30db3876515da09930015710e906c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d272f48511d0a32e819af85fea2367a528b48a8b4fa4e632433c0b8fa38bc922`

```dockerfile
```

-	Layers:
	-	`sha256:553c5eac592be17691460438b2414ab1eced55687b39f0a5e6c593adcebfeffd`  
		Last Modified: Thu, 19 Sep 2024 19:00:51 GMT  
		Size: 2.4 MB (2362950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4727388685771e44b0682f051bd582210e311c1c8dd940606934520eba08f32`  
		Last Modified: Thu, 19 Sep 2024 19:00:51 GMT  
		Size: 22.3 KB (22310 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:e0f285205ce64039b5ac77b5d714ceb4134507f470fe6926e5600e770ce5f2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41659846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d1ff3512e7b3082950794720151d440329c7efe9972bd9bfe9d0f4bcd9dc94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
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
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5549a1ccb130b702c1a3fd911e80f12853993b5c6ff6a701130d098482b31bd`  
		Last Modified: Thu, 19 Sep 2024 18:57:42 GMT  
		Size: 3.3 MB (3322464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a886bf09b0292ffa960c7fecd60877ef45ba648f80835e2ed5e65c3537cb45f`  
		Last Modified: Thu, 19 Sep 2024 18:57:41 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e37f62e0ad2eb5cfe0f37e673119b601e28a10fb318fa2ba78e77b311c42e9`  
		Last Modified: Thu, 19 Sep 2024 18:59:23 GMT  
		Size: 9.2 MB (9179192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1705865f03e84caad64566f07667584cd04c95a8040258cae81f90a28c1d5fbb`  
		Last Modified: Thu, 19 Sep 2024 18:59:22 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:61edb6eb9de7f6d296f0656867c339b7ba8dd20ea8ff6b440eb3df8e8bde2d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67838dc33150efa1d6e9ea90704376bcf85ebbd98a3fefe6c54bf822ea9abceb`

```dockerfile
```

-	Layers:
	-	`sha256:ac6540b68a338ca04cd227c9c124ce5da3202d7c627a6905f0876d545729dcf9`  
		Last Modified: Thu, 19 Sep 2024 18:59:22 GMT  
		Size: 2.4 MB (2360998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d90a8b4bfa7e7473ba51c5667adefec31ce69520b9700c8351d676bc3de400b`  
		Last Modified: Thu, 19 Sep 2024 18:59:22 GMT  
		Size: 22.5 KB (22539 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:a1801eb996d0316c950d92897ccec5ab5a45b1f0e6f29a68f4a2fc5682d6d96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42593909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782adbf4882c7ecdfda099de5b7f7151664336dad80995530286ee2855c52368`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
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
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51db934968c96b7a7d766c392ee506efe7d01ec87bb2809a0efaed8168193051`  
		Last Modified: Thu, 19 Sep 2024 18:58:06 GMT  
		Size: 3.5 MB (3502364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cecb4dab0a95aae9bfae098aea2507cf796d098526296ddcf46c6cddf3d4ec6`  
		Last Modified: Thu, 19 Sep 2024 18:58:00 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58634f14293264fac96ab5b2c60dfdf06bc1f5a4625ca339debe883d29c6750f`  
		Last Modified: Thu, 19 Sep 2024 18:58:06 GMT  
		Size: 8.9 MB (8945603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3685c2432e1b986ed58fd707f8776acb98ddf424fb7272f591a4eaaa5595b44a`  
		Last Modified: Thu, 19 Sep 2024 18:58:06 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:5f64275dbbbe5a282ec968f1a319a1341930995c7e38aa3164bb96aef0d2d09a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06dfb4d93aaf5372de489d6274514e89f658ed9cf4069c63b3763171925ec1ee`

```dockerfile
```

-	Layers:
	-	`sha256:b546ceeb9c6452de6a6da7b81e95533c21d4a0d36e15cca80ac0342dfc494f5d`  
		Last Modified: Thu, 19 Sep 2024 18:58:06 GMT  
		Size: 3.4 KB (3430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d91647c6804359293be64c4832cb17aed64da0f27e6a91166a02ce6ea79b173`  
		Last Modified: Thu, 19 Sep 2024 18:58:06 GMT  
		Size: 22.1 KB (22129 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:3d21bd1522ad7bc388516a0168d8caa1d8abf8093954a9f8f44bdbf3a6310ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41341504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869dcd3260c8323d4890f7fc2f377d01be24e3231fd93401921a4e310a04b14c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
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
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef73fedcab81f0b053a63007a18b27311e104bc8f6ff95790ccedc941cdd7944`  
		Last Modified: Thu, 05 Sep 2024 05:06:40 GMT  
		Size: 2.9 MB (2894500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb5773fd81c8673234b2076e42d44191a7c46a21b8749ce5980b4df02662af1`  
		Last Modified: Thu, 05 Sep 2024 05:06:39 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8896573227cfb4f866c10becb93290f2bd13838fe69ff444ba96d1c31b6974`  
		Last Modified: Thu, 19 Sep 2024 19:07:06 GMT  
		Size: 9.3 MB (9320304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b50f551003b495ebf7c0daf08a9148a72bb79354ca6216ab1a589a5dc84053`  
		Last Modified: Thu, 19 Sep 2024 19:07:05 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:101aee8e855f438a84d5a59d5e5b438b725593c09f56105556695cf52d4e4b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d90b151f4739d09268f9440416bc0f7a85ee50a11317712b3949620e9bce68`

```dockerfile
```

-	Layers:
	-	`sha256:e5522451df41c2cb89f7c0704a4e5f8ee745f8f89de748f273d765d3cf959858`  
		Last Modified: Thu, 19 Sep 2024 19:07:05 GMT  
		Size: 22.1 KB (22062 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:7de718fc8c919fe3cfa1706dcc5e7b90620852b7da82acfb565b32daff2d81bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46528803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6d0555f753313477118641c8f386f3c2dc3e284deb6434afb8ffb691eaf437`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
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
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2d1a5729ec07197ee9a1afbd7369785f25e4ab3024eab522f93d2466d31b9b`  
		Last Modified: Thu, 19 Sep 2024 18:58:15 GMT  
		Size: 3.7 MB (3701522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f08e816132965e7b896a0eb45a37824eaf6cebbc1514f4a2087f583f9278f81`  
		Last Modified: Thu, 19 Sep 2024 18:58:01 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d701dfc0980af871c4845bada2645cde97d197a518a01737aa77c0b1e5e048d3`  
		Last Modified: Thu, 19 Sep 2024 19:00:55 GMT  
		Size: 9.7 MB (9703278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8430a8630b3c33f65fd20dcf1b6011b4021a4c52f7ec2107a2d27ff2a1445c30`  
		Last Modified: Thu, 19 Sep 2024 19:00:55 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:6d5f3616185e46ebfb38a7f33b69f748cca639d840ee0beda3d48bb8affc972e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96aa09e3abdc37212431c838b3710715424eeb0d2b422b0a1ff32a7ec6a49c8`

```dockerfile
```

-	Layers:
	-	`sha256:a2a533d14c60de77c12048235f50e85e48445f75271296b03dc464d2dfba7f76`  
		Last Modified: Thu, 19 Sep 2024 19:00:55 GMT  
		Size: 2.4 MB (2365017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6987dda0b1e47dce297e648b489d8bd0f91060bcbef20dafb32c504a14f83cc`  
		Last Modified: Thu, 19 Sep 2024 19:00:54 GMT  
		Size: 22.2 KB (22248 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:12c3f2cecc112b8c9fd79370fb6aa42084b0ad816d7f036d7dbac17f48fe632b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39724823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd6fe4a0068ea78faec4fb558063b199462bcb37b283087bf7668d69931ba22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
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
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23f2457d002b3c1305a7275149b8ae34a1893e1b617f66abfee44aef929b4f`  
		Last Modified: Thu, 19 Sep 2024 18:58:00 GMT  
		Size: 3.2 MB (3162477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cecb4dab0a95aae9bfae098aea2507cf796d098526296ddcf46c6cddf3d4ec6`  
		Last Modified: Thu, 19 Sep 2024 18:58:00 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a61bd57f9a9107684c7c619099302b9896c7b636a624e7565114b594b9ca7fe`  
		Last Modified: Thu, 19 Sep 2024 19:00:58 GMT  
		Size: 9.1 MB (9070378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33868564859e85d7e918d08cbc7def443629055ef554b079bfa52c0c28794b88`  
		Last Modified: Thu, 19 Sep 2024 19:00:58 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:1b35394167bd26cc09ad7c65d84afced2f5a74a7f60cf4cf17923bbdd1328920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c96a6fee3a1f4a4882552c2e0b2d3b67c58cad1a28a5cf15c8453934c94693`

```dockerfile
```

-	Layers:
	-	`sha256:2f078b0c51ecad56705e2ae260b0f87e21d57f027a85015cbfdb1c5940189eff`  
		Last Modified: Thu, 19 Sep 2024 19:00:58 GMT  
		Size: 2.4 MB (2360521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3db93c3a25afc4abcb99217b983e0c87de98d5adb1802b4092ccdb57fc388d41`  
		Last Modified: Thu, 19 Sep 2024 19:00:58 GMT  
		Size: 22.2 KB (22182 bytes)  
		MIME: application/vnd.in-toto+json
