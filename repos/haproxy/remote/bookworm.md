## `haproxy:bookworm`

```console
$ docker pull haproxy@sha256:9f0435e9cfce4fa2cb13ddfb6ac47134c3581ef669ce799d64107c3ac9d58e02
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
$ docker pull haproxy@sha256:8dcb77860e2ad09b96afeca07cc94f207a4db85847155c8a0812d304ac3dd966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47078225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b88892a0aea09bec3c654872d7aa24114c21c236b6b082b98da5ba408d4409`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 31 Jan 2024 18:13:30 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb311fd72fec8d4a0ff33a058f6e6c7089699e27146b5dc5806771ee3e9438e`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 3.5 MB (3491102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3000fcbb9645d390e0eda1724a224bc7e97014f621d1a5739948ef1f49007853`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432c01694a9843788cde1e2c18da9b66aa79b38707681b771eff6be0362fefb1`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 14.5 MB (14461393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecde544d88045d1719cfb0854884f384742a1050d8d666e9bcda5c3d7318d25a`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:360346287b1c2a489ba14122591dfb4674008f7656062f613152b634e3358598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3143756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0595045d5e70c1e742151f77ca69331e349135ae510735d6b7917e44d9220fee`

```dockerfile
```

-	Layers:
	-	`sha256:c2d04636c865e6fdc9d7420e495e3d8634ac9d9deda724db92899d3411398dfa`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 3.1 MB (3122088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c1696065b2c2600f8d976ba42f9a46fbf562538c2710f47f6760f2deda93cd4`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 21.7 KB (21668 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:def84e70b4d7d5cae0916fcfc1282c357d99f366f3a03cfcd5f0ed7b5fa37f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42935154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8210062681e68d432fc4c96ce818e6fe8d42182bba89c2c805bba9b8572dac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 31 Jan 2024 18:13:30 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93250c55b4e76ea7df49c4f3d33908606f353b792be0a7b579571482fb6d4730`  
		Last Modified: Tue, 13 Feb 2024 13:08:25 GMT  
		Size: 3.1 MB (3066716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd191230532aee92f6b2f05ee877c37201168254a79072e26e6715cd8d4e5812`  
		Last Modified: Tue, 13 Feb 2024 13:08:24 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e02411de8f9421194c753b6896f18922bcc2d539d163c104342119061d2d98e`  
		Last Modified: Tue, 13 Feb 2024 13:35:49 GMT  
		Size: 13.0 MB (12982897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daafdcee73bd608ee76d6308225f184ffcaa2f4b6b389c8a22dd39c333f2eaaa`  
		Last Modified: Tue, 13 Feb 2024 13:35:49 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:6bf050a8ff49ade59f866f92951a65ac2da1655341b2e95327e91692d8d61a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3118409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4b87b41abeb4854ecb90bb3c91cce50272abb39f5651957b7799dfa3614c8a`

```dockerfile
```

-	Layers:
	-	`sha256:e895c75ec9e8c27916776a29b0b793b054bf21075a4a33fbd51f9ad92c89a9fd`  
		Last Modified: Tue, 13 Feb 2024 13:35:49 GMT  
		Size: 3.1 MB (3096796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab4c2d91b2b58d0169ee79456cfc159178f4843d9492b8a15bb891898e27e31`  
		Last Modified: Tue, 13 Feb 2024 13:35:49 GMT  
		Size: 21.6 KB (21613 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b6764e310eedbd2fa9dab58c149cb507efa67960450dc706fca04c2fd7c3ce74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (40029726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37bc83301fd00c9cf3efed612cacca1ce1911d112bc0f2eb8b7a9db1c315feb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 31 Jan 2024 18:13:30 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4a97c94e1c1d1908b71a332076b6a8eee59e83f0c6856a747f67fc523fba1c`  
		Last Modified: Sat, 03 Feb 2024 09:03:33 GMT  
		Size: 2.7 MB (2710915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3df935c7795e25ddc2afb799b0d6476073a8db3f66529d21634d71463bf671c`  
		Last Modified: Sat, 03 Feb 2024 09:03:33 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44adfc587080af0273fae3aa6749d7f9bb812a806b41a11f2bbaad96cfc4426`  
		Last Modified: Sat, 03 Feb 2024 10:00:18 GMT  
		Size: 12.6 MB (12575606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305ac343fcafbfc8381e170909b46d87b3d7ecb820f943761a6fff5879a9c11e`  
		Last Modified: Sat, 03 Feb 2024 10:00:18 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:e51ef010d15e67158d36e1381f0a53449bcecbe32a5d4ce613189c12ce34381c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3118211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f7648648f3608dce1e4c1ef935ad15999241070823d49b7c7220f3e551d988`

```dockerfile
```

-	Layers:
	-	`sha256:a15c34385adb0b26d7b8240a1e4316ba78bffbc902c01b702b8f5b1d72f7b8fd`  
		Last Modified: Sat, 03 Feb 2024 10:00:18 GMT  
		Size: 3.1 MB (3096598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85cadea5c3839f13526cd282b0e54e12babe12f63eb5b4659faed80667d4c140`  
		Last Modified: Sat, 03 Feb 2024 10:00:18 GMT  
		Size: 21.6 KB (21613 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:4f594410438dcb595b0f9ce2c80ce7f06db134faefa58782e08a380a6c52952d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45919424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b40811f51510c209d9a5378a8b1babd6e55a64a3d0c20bc7dcfde39e000fa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 31 Jan 2024 18:13:30 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415e9b063990eee029df7b6c394a1b21265a48c7e4af8491e730783834270e6c`  
		Last Modified: Wed, 14 Feb 2024 00:00:42 GMT  
		Size: 3.3 MB (3314250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c590571812615054febadef038f8df80f006f94650ae6e99535701a0f6cc57d`  
		Last Modified: Wed, 14 Feb 2024 00:00:42 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d1374fbdd22262fe5ce98e62c16e329953e9bcd2780cffbb0d7ffd900e47f0`  
		Last Modified: Wed, 14 Feb 2024 00:29:58 GMT  
		Size: 13.4 MB (13447174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f668bdb38950029a384ae8d644d0a28eecc671cb57b08855af6cf1dadea545f0`  
		Last Modified: Wed, 14 Feb 2024 00:29:58 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:f6dbf04560f57931b7791d281cb94911726e596018edb31eaa5def8cf4d3ebe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3118782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe9b2d1586db55a1f00b1b9083ad3a3547374e01b73a16233818a84b774007e`

```dockerfile
```

-	Layers:
	-	`sha256:84476a6e92835e2321f17480c3a1cbc06e1257744c0661e7605e7621e92476bc`  
		Last Modified: Wed, 14 Feb 2024 00:29:58 GMT  
		Size: 3.1 MB (3097267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7be9623434772af92a3d3b8ee01c3e5400e09e0837c4f1e7e361c3bccb9127c`  
		Last Modified: Wed, 14 Feb 2024 00:29:58 GMT  
		Size: 21.5 KB (21515 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:afbb7adc75a8d3f671c43ffc9b24865fca43875ce49be16481a9ed2dcabe4cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47331189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2957525de7327c903766fe15302682c29d2d23c60b183b44fc19d13388f594f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 31 Jan 2024 18:13:30 GMT
ADD file:d071fabb8bc92134fff788fc6f2e518f1291bbb7813cb5b41180aed4a50e654c in / 
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:beff29d65c5c5787a278dcce32970cc3af7110d5c13ae23f5a08898a2015b4c3`  
		Last Modified: Tue, 13 Feb 2024 00:43:46 GMT  
		Size: 30.1 MB (30141809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652780e07258a81fef5500fa4ce709a9e45bbd2923cf34add22a999adceb7cfb`  
		Last Modified: Tue, 13 Feb 2024 01:54:04 GMT  
		Size: 3.5 MB (3496195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10273027f89d609ac0ebed3c131da7334253c3b0e7894878ee040781bcb32285`  
		Last Modified: Tue, 13 Feb 2024 01:54:03 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b12c0356b4fa59e054182b0aee991ba5e02be405b1741f24ea751d5975cd3b6`  
		Last Modified: Tue, 13 Feb 2024 01:54:04 GMT  
		Size: 13.7 MB (13691550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c307521bf23d1b23d0ac8be4c6e8ec086aa4f4c70cf1c61ac7dade59fcb5016e`  
		Last Modified: Tue, 13 Feb 2024 01:54:03 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:d1c3b2e69b668048c9e094a8ee8665d3e9e7a2a12ac763de29c5a5285e4673c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6434b8acc9a76460cf6e3cd18ed9bf92ef499749efc99172c5209c4f44bade55`

```dockerfile
```

-	Layers:
	-	`sha256:b0e8dda4ae15eea8bfe476b0dc07d48c54bf06604d5b6106ec3d55c9d5ba2256`  
		Last Modified: Tue, 13 Feb 2024 01:54:03 GMT  
		Size: 3.1 MB (3116420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:450e29a4a3dccc75f0ec49a9ff4b2ac607c6d5f448e552a9e35882e0f7ede2ed`  
		Last Modified: Tue, 13 Feb 2024 01:54:03 GMT  
		Size: 21.6 KB (21625 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:ad79485f8c36d8de1be9ce446bf202f6c7b86fc4a76b2e2df567ab1e846d7dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45687998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176f9fc82e1aa782cb2a83ff78ec5fa38f5a18219d1a0d3f9777a3f65a3f7c94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 31 Jan 2024 18:13:30 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8956b6f23121167181118fba218bf9c7c47d13ac029aecca429fed0949d2869`  
		Last Modified: Thu, 01 Feb 2024 19:27:10 GMT  
		Size: 2.7 MB (2698803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274dd577b7c1ec37395744f1d64fb2bb7f0f1b7842402dbe25fdd70cae83171f`  
		Last Modified: Thu, 01 Feb 2024 19:27:09 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a3db5261afb95a224ecdea4526dc6b32d755b0dd00e8edcf401b0a0f1de5e2`  
		Last Modified: Thu, 01 Feb 2024 19:31:48 GMT  
		Size: 13.8 MB (13845114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50dbd9135ba0ccc72596ad39717a16e07825cb7e633d2cb15ae6a366b6fcf62`  
		Last Modified: Thu, 01 Feb 2024 19:31:46 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:9aebcc4cccbabf8619d9b8c2e3142d33de779319fab02a69efceec35a16400c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03453338fd55f6f75649e94a5af3fd95c4085e168ce36149db2fafb5b5aabd6`

```dockerfile
```

-	Layers:
	-	`sha256:bc6d47fdf9100ea708bd2820af4e45b8215c821957902365f206e54371f38f33`  
		Last Modified: Thu, 01 Feb 2024 19:31:46 GMT  
		Size: 21.4 KB (21367 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:80ab18c1ddcce1eb4a8e8e9b8624e4aebd86132ffbb9591bf41e026cf1e6e0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51634712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e81979a8124e628ec9ae85ad44637a8b4adbe498a62ac83f5a892775961fdcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 31 Jan 2024 18:13:30 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2244971bdeb0ffe951c062c7305fa9f47c0d38c610142a1024bc3988905d6c`  
		Last Modified: Tue, 13 Feb 2024 21:36:07 GMT  
		Size: 3.7 MB (3694014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c7dc76a82910bb57427f3f317178bd4c8307985fa6afb03a7cdae20b661a58`  
		Last Modified: Tue, 13 Feb 2024 21:36:06 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe0c00abb1b2b57e73e4e89dc665a9e45ab3fb12dc8014855f983c753ed3993`  
		Last Modified: Tue, 13 Feb 2024 21:37:33 GMT  
		Size: 14.8 MB (14820155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad3eb7f49184ad154ea0f38554b47e1c76fe1b110fd3192fe055bd214a3497f`  
		Last Modified: Tue, 13 Feb 2024 21:37:32 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:89c097d4e4b1ceee662969c1eae9c30a0c48f68fe5e7c2419d1564a2dae1c799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2e53019fc36b1a507bd6497dfd44b664320f3760b41248e76448c657e07a24`

```dockerfile
```

-	Layers:
	-	`sha256:bdd3a0d0bca024c649dbc386523ee5b88dab3d28a105c5ee4e58bf446d2df1b6`  
		Last Modified: Tue, 13 Feb 2024 21:37:33 GMT  
		Size: 3.1 MB (3110616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6d8064ea6d078f849d83a3fd68f87d20cc52425013112c8780ad2b011e020f`  
		Last Modified: Tue, 13 Feb 2024 21:37:32 GMT  
		Size: 21.6 KB (21554 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:f355f4d2377ea3a6b85ab8339a22188736c926632976f44d947f29f526d4649e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43738140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d7b83626b8bceeee2275abb5f4fed482b95089c0594a148484becd9b3436b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 31 Jan 2024 18:13:30 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a29f6b1bc2c42a19b9e7cefdbab822c717baed532cd10dfc76ede842431fe78`  
		Last Modified: Tue, 06 Feb 2024 10:18:26 GMT  
		Size: 3.0 MB (2964718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab54fd76279508ede5adca23c9d06f11b85a26c5f9e32f9403651eba4bb022b`  
		Last Modified: Tue, 06 Feb 2024 10:18:25 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9e0633eef490dc1456d5c579d31672524f45d77776935b1282af0c402aed84`  
		Last Modified: Tue, 06 Feb 2024 10:21:51 GMT  
		Size: 13.3 MB (13258298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d9462c8dbbbdac866f39bec06f3894cb6696920f7970c448fb2e0771618485`  
		Last Modified: Tue, 06 Feb 2024 10:21:50 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:62d4a442467cd852899117ccc30e993a17584b9b4cb89f7c2e45d09dffe33fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e56b52acce62756c2ee42307a5145469cb585246b0032b87e1ea086854df216`

```dockerfile
```

-	Layers:
	-	`sha256:07a8c648fc5b74cd5ffdc375e64df2f0558b2cd72641c6056d22a424266f76c5`  
		Last Modified: Tue, 06 Feb 2024 10:21:50 GMT  
		Size: 3.1 MB (3111589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:312cb90fe5c268e8434bb12ab9908f948ccbf903ec9bdebc3e74ce1b70286d5c`  
		Last Modified: Tue, 06 Feb 2024 10:21:50 GMT  
		Size: 21.5 KB (21501 bytes)  
		MIME: application/vnd.in-toto+json
