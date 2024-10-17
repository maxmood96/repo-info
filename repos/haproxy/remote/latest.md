## `haproxy:latest`

```console
$ docker pull haproxy@sha256:a1a9b8a602ba37b08da728e42f3ae0e1a9ab5bba8273471aa78006843a6021a5
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

### `haproxy:latest` - unknown; unknown

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

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:05ddd21db7c283069e79735d607f650669ccb7e890dd6a747bac7059d8ab8095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39090739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb2ede169879154c259c98ed4735400f8c4fcd39c9adbd0a4d084b2fda7c02e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 19 Sep 2024 17:21:03 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
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
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8901e76f43bd68a94c27283bb1de3353a11838cf517ba8517aa674b676242268`  
		Last Modified: Fri, 27 Sep 2024 10:31:20 GMT  
		Size: 3.1 MB (3073079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151bf25eb027fff8657942435f036ef10889fbb7ed721a623b0cf8ee040dec8a`  
		Last Modified: Fri, 27 Sep 2024 10:31:19 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbe67a7fe4acdf6c120df5f83a33facaacc71e41fa1da29f44155e27b59a651`  
		Last Modified: Fri, 27 Sep 2024 10:32:32 GMT  
		Size: 9.1 MB (9128718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466ab0c6a957655c1ecc9c86ae3739611cc94214b9dcbc1f1bbb472167593b77`  
		Last Modified: Fri, 27 Sep 2024 10:32:32 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:37227553c1bb67848c8fe8912284592fa41c2115323f62c0105dcc5082a32ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727562f4c83847cbee530c6b0f5daa98167f7b4dad214790d026a6c6088d9040`

```dockerfile
```

-	Layers:
	-	`sha256:35320a6e704762693b8e86dd0837bf45dd179b2b317acee70ff5e6d763f47cb1`  
		Last Modified: Fri, 27 Sep 2024 10:32:32 GMT  
		Size: 2.4 MB (2364128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7b1380c706aff0fe035624cd6519812badeb5a977f736f9657ae19d6fe264c`  
		Last Modified: Fri, 27 Sep 2024 10:32:31 GMT  
		Size: 22.3 KB (22310 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:5b862668a2707a206c5696228da49d3ce02bec31501f45bb902b9cf3d1051429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36588509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da83d01d04130e7ab9987739173e70f8b10b3e37646c0b9a8862a288e6fa2e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 19 Sep 2024 17:21:03 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7a1afdfa31a72964c2e3cfbb6cacb6c72a202a79e57de334fa6b16fb3b2b`  
		Last Modified: Fri, 27 Sep 2024 10:52:26 GMT  
		Size: 2.9 MB (2907401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cae2ef777126baf02342f29142bd3c3c5fdf56aa43f719b9e0cf2cc24152b5`  
		Last Modified: Fri, 27 Sep 2024 10:52:25 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be8815f497c615632f4f39fb681cf571b67fd285e09bb81ae25889292f2d6d0`  
		Last Modified: Fri, 27 Sep 2024 10:53:34 GMT  
		Size: 9.0 MB (8961322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3839e49deb7aa4cb7589ab06df002a917de3e8dac0bf0a4a0a1fb50f650331aa`  
		Last Modified: Fri, 27 Sep 2024 10:53:34 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:6ba3abad1398595996b7f19c4144370e941b38a2cedff0bffecfd3c141415484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4485099fb01e43ccccbda82357a71fd842912277bc7df5158e41b4758e379418`

```dockerfile
```

-	Layers:
	-	`sha256:0794c8c80b08dca0961df6dc3cd8f6054f342f88e870ca2449d123565817f5f4`  
		Last Modified: Fri, 27 Sep 2024 10:53:34 GMT  
		Size: 2.4 MB (2362963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eff13f67a516ffc7336eca41904ed7799f53af210476fd902892b37ac77ad77`  
		Last Modified: Fri, 27 Sep 2024 10:53:33 GMT  
		Size: 22.3 KB (22310 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:b25364c010f68eee8a9b3edaa27618d15174f596fbc3706e46e29746a37220bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41659592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3e14e3cdf7c22b4ee247f4b920417343d53a80b74c93bfcaf65d7ce52dcd7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 19 Sep 2024 17:21:03 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957709b782514c0eb3986f703384cee9e374c24047faca8646af08e790b49540`  
		Last Modified: Fri, 27 Sep 2024 14:33:32 GMT  
		Size: 3.3 MB (3322430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455cca654f6db7169816550de8458fb3ecebfee6f5338df120f062c5f61594e4`  
		Last Modified: Fri, 27 Sep 2024 14:33:32 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f679ae72934fba44a2a145250d913a38fdd4018567b3a82b5ac0584ef0e748e1`  
		Last Modified: Fri, 27 Sep 2024 14:34:27 GMT  
		Size: 9.2 MB (9179157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e525526d6b7a4cf59a136d4c8973e100ba06df212617a32ab38fd30e43c3dcb7`  
		Last Modified: Fri, 27 Sep 2024 14:34:27 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:10a2b90a5df8b85bbdf69ead81cc8fafc2b4f1892ff0c6fa65e588a3a42ab1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8861b7838e68eedf2439203fa062a081c15e1a9b4e1ebe8d0979c49b15930900`

```dockerfile
```

-	Layers:
	-	`sha256:8868b3f5bbddb44bcf638427f28d57fa08499b207ab4bf9b93f7ac7e92af1220`  
		Last Modified: Fri, 27 Sep 2024 14:34:27 GMT  
		Size: 2.4 MB (2361011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01a2cdc0cb3ef9a78ea44f0a87d350248aa6552e16787634460e730a3b02b10`  
		Last Modified: Fri, 27 Sep 2024 14:34:27 GMT  
		Size: 22.5 KB (22538 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

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

### `haproxy:latest` - unknown; unknown

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

### `haproxy:latest` - linux; mips64le

```console
$ docker pull haproxy@sha256:92195d020fb16e938df538fab2500c94e4e3b5673a0865829aaf901b0e3e82ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41341335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4a886e83b14e45fb81114fce763daab9efc1850340482d43061de6b8d4b73c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 19 Sep 2024 17:21:03 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
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
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd734f28a73fb12f1107a82ba37af8bb8174cfbe80f4b02820eed124a961a1d`  
		Last Modified: Fri, 27 Sep 2024 22:41:49 GMT  
		Size: 2.9 MB (2894513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f841b0ba5a9ea3efbdf77074e138a5d1142d168214f2ef5a19ea8eac4dca9b3`  
		Last Modified: Fri, 27 Sep 2024 22:41:48 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099bf848cc92f9126d485eb014a74c47e942a0a1b419bbde85babae29dd2e3e4`  
		Last Modified: Fri, 27 Sep 2024 22:47:15 GMT  
		Size: 9.3 MB (9320320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f190bba05b7732291b17d6c9689f0e204ecefcfbe7c79cafc79fbc0d0afe96bc`  
		Last Modified: Fri, 27 Sep 2024 22:47:14 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:57d271432978c162092f089b47630aa793387e91a9111830bdb32e66dd78652f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5f8827fa6b53557134ff2d9dc5ca02b4d36781777ecdc79345af70130ca5fd`

```dockerfile
```

-	Layers:
	-	`sha256:bd0e3c463e73e6d60cd76f3c9306901a54d3f1db5af93b755cbdd587b4448239`  
		Last Modified: Fri, 27 Sep 2024 22:47:14 GMT  
		Size: 22.1 KB (22061 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:281e8afc6674f85d429567a665d76e93a39582ec7b95d8f68d2dc4ae9a314d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46528556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f08f51d41c70cb5622c9aa186b47959a9cc5ffcd9bd1e1b9628181016f4a33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 19 Sep 2024 17:21:03 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
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
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd981b7018425234aa7d290a027983d5ee640abd38e047fe085e617a85c20a91`  
		Last Modified: Fri, 27 Sep 2024 19:45:36 GMT  
		Size: 3.7 MB (3701565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cc5f5795cbfd6fee609992a6f374073f51d587c2fdc7bb094df82937f0006a`  
		Last Modified: Fri, 27 Sep 2024 19:45:35 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3870ad45082645038b22d8c3a0dab9b51fb277262c0437cb0641c915d3c96e24`  
		Last Modified: Fri, 27 Sep 2024 19:47:15 GMT  
		Size: 9.7 MB (9703189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d5d056d8cc8dff88d3a579bf06664263de0181311065b62110dd8448dc3638`  
		Last Modified: Fri, 27 Sep 2024 19:47:15 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:f5eab5eafe28b1bff9ad9ccdf41e7d30a52a5258ccd462652b75af9440926651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4395c4a784256b487ef730a1e680c0e7ff0b1795bc1c155411ea72584f90905`

```dockerfile
```

-	Layers:
	-	`sha256:62585ac4a141d2062985ffd60837f9c7794986ff81bd771cdb6d0aef7b3989af`  
		Last Modified: Fri, 27 Sep 2024 19:47:15 GMT  
		Size: 2.4 MB (2365030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fc9ca6bac5aef19e86e28920363bf20afa3f01c69a71f6c12e63b034e1812e1`  
		Last Modified: Fri, 27 Sep 2024 19:47:15 GMT  
		Size: 22.2 KB (22248 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:6dfa6c3b9956a4184a358593d1e3d047f17936ba40fb7dae4355b98fbbfa8bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39724590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bb1189f5d6724bbeb477216bb3de9781a64f2613344ed30ec03a712803e13d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 19 Sep 2024 17:21:03 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3780a35f2ed88fb36b1e757851a1a2705df8c8b341a76764b08b9a2a1b0aed`  
		Last Modified: Fri, 27 Sep 2024 13:01:25 GMT  
		Size: 3.2 MB (3162522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b40da6d3e02a52789a9cf4070c7611c2901363f3add806083b6c7956dc26916`  
		Last Modified: Fri, 27 Sep 2024 13:01:25 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54b6b36c94a983f89aa52e657b6db532ed28bfbdaaf0d8bf5003554af27331e`  
		Last Modified: Fri, 27 Sep 2024 13:02:35 GMT  
		Size: 9.1 MB (9070407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e230ffc4f44e2bf01e175f2ad9182e57a75a9a3310cb23d8646626a2fa9aca9e`  
		Last Modified: Fri, 27 Sep 2024 13:02:35 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:588728f38b36a95b31956c3ce223a870699bb6566c59479756a817ae9c796790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dec7db9b744299d361721f58a45195fd3339a0e8f99396317c7ace472954f0e`

```dockerfile
```

-	Layers:
	-	`sha256:b2ba63dd602b46a6f59f60d8a60c484c8b88c43f726711a71c22bdc03ab089a0`  
		Last Modified: Fri, 27 Sep 2024 13:02:35 GMT  
		Size: 2.4 MB (2360534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d3ed10cdc2873dbadb59695c7d716e09ed975be5438cd60a41a5ec662f69848`  
		Last Modified: Fri, 27 Sep 2024 13:02:35 GMT  
		Size: 22.2 KB (22181 bytes)  
		MIME: application/vnd.in-toto+json
