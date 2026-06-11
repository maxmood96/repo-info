## `haproxy:latest`

```console
$ docker pull haproxy@sha256:3b075fbd3151b6187a548c6acb5602e0441417a87afee272a15d2e593de523a4
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `haproxy:latest` - linux; amd64

```console
$ docker pull haproxy@sha256:2403ac439f6a857d51135b948d273332831d91c767427c0f02d19dbea83574d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47061891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48377019caa02bb331e17ca502841fdcae901c22def06126a2d06730e8526fa9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:47 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:15:47 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jun 2026 00:17:44 GMT
ENV HAPROXY_VERSION=3.4.0
# Thu, 11 Jun 2026 00:17:44 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Thu, 11 Jun 2026 00:17:44 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Thu, 11 Jun 2026 00:17:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 11 Jun 2026 00:17:44 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jun 2026 00:17:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:17:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:17:45 GMT
USER haproxy
# Thu, 11 Jun 2026 00:17:45 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jun 2026 00:17:45 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39aba918f7a7d429d0c20c7858f338efdcf16f92ed75d36751d62a7fd4adc164`  
		Last Modified: Thu, 11 Jun 2026 00:17:52 GMT  
		Size: 1.6 MB (1581308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9310d2c1644d3d71f89a9432afa7d2e23f641aaf9a252faf852453c597db24`  
		Last Modified: Thu, 11 Jun 2026 00:17:52 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f839b6f976965040538d747e3724782cd57ee4624819a2f0e9154392017fb0`  
		Last Modified: Thu, 11 Jun 2026 00:17:53 GMT  
		Size: 15.7 MB (15693528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd764ba633a4cabf71d6fb8e27e63a324a268bd7051cb657985912cb77818b14`  
		Last Modified: Thu, 11 Jun 2026 00:17:52 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:eb438400dcacd8c786f0aa5affe59b82c11d1a66774577d9f8327a720f57321b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5e1663cdab28e058188a2949ecd4a441d315328fb8eb20e6cfd31e33ab14d5`

```dockerfile
```

-	Layers:
	-	`sha256:93f996e53fa0199993ba04cd4edfdb355ea6b0b90a323ee92d6448a1271b07bd`  
		Last Modified: Thu, 11 Jun 2026 00:17:53 GMT  
		Size: 2.1 MB (2114442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9d17ca86f5e04db7ab9ceced488c6fa09174e5592c8f9015b0ab227965541a`  
		Last Modified: Thu, 11 Jun 2026 00:17:52 GMT  
		Size: 22.9 KB (22940 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:459a945b73d51b59b23197443fdb44082a7b6eb50ca1be59bc25f58b52533c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45397260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876652434ece3b7aa801607e840ba5fc32dcbd296ab8fc2a9a11c5a25cabb199`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Wed, 03 Jun 2026 18:12:02 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 03 Jun 2026 18:12:03 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 03 Jun 2026 18:13:03 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 03 Jun 2026 18:13:03 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 03 Jun 2026 18:13:03 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 03 Jun 2026 18:13:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 03 Jun 2026 18:13:03 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Jun 2026 18:13:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jun 2026 18:13:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jun 2026 18:13:03 GMT
USER haproxy
# Wed, 03 Jun 2026 18:13:03 GMT
WORKDIR /var/lib/haproxy
# Wed, 03 Jun 2026 18:13:03 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b4f0a387c1b0ceb12d76ff30f8be132f0e560aa502bcb07cd6d9b16a44eb7b`  
		Last Modified: Wed, 03 Jun 2026 18:13:11 GMT  
		Size: 1.5 MB (1535852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6f987a59870efc12119e168dfb7f7d20e1e88908e6208b5e1eb1b0aaf36415`  
		Last Modified: Wed, 03 Jun 2026 18:13:11 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e702d0fe785891c664761fd3c756533e6f47ef7eb9f61c2361d9ad728191b773`  
		Last Modified: Wed, 03 Jun 2026 18:13:11 GMT  
		Size: 15.9 MB (15905892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1684114e203e90cf4944a4bfd73a07a4f78300dc4eaeebc5ba0d1f904e2f9bc`  
		Last Modified: Wed, 03 Jun 2026 18:13:11 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:a11a353b678f6b3a66e29bc005ec3d36b84e4138118e211ed7d042558ba58b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81bfcbacd4adfe7fa8119876d3c7c62728c18ac43b60eec6f7c2b4b729820220`

```dockerfile
```

-	Layers:
	-	`sha256:396ddff9193bf5690ef1b7e7e36d4694a4da04d7c4f006df9911dc1a1c25f4be`  
		Last Modified: Wed, 03 Jun 2026 18:13:11 GMT  
		Size: 2.1 MB (2117438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e60610d922f8f8d83d991a9a02d8d53703c7deaf28e0d8b7baee749afc21e5`  
		Last Modified: Wed, 03 Jun 2026 18:13:11 GMT  
		Size: 23.1 KB (23078 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:bf8d43402c4adeb54696663f8f67dbc8ae2b3d1f7484d5d2f5837e7ae358b6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43386166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b801abdb4431a7856c7c23a7a65b730ebad718f3415714c96f5f32f219ee7fdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 03 Jun 2026 18:10:39 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 03 Jun 2026 18:10:39 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 03 Jun 2026 18:11:32 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 03 Jun 2026 18:11:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 03 Jun 2026 18:11:32 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 03 Jun 2026 18:11:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 03 Jun 2026 18:11:32 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Jun 2026 18:11:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jun 2026 18:11:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jun 2026 18:11:32 GMT
USER haproxy
# Wed, 03 Jun 2026 18:11:32 GMT
WORKDIR /var/lib/haproxy
# Wed, 03 Jun 2026 18:11:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ba8e19d7aba841097a4d0c335ad84864c7710193a417a74a7dd4aa301c9187`  
		Last Modified: Wed, 03 Jun 2026 18:11:39 GMT  
		Size: 1.5 MB (1489590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34470ba44440f39dafbe3392a5ba83962f09d97f8de8cce32a05817f4b44f229`  
		Last Modified: Wed, 03 Jun 2026 18:11:39 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41c4e2780961fc4664e7f44d19154a26d185a87f836db5043035cf43b353595`  
		Last Modified: Wed, 03 Jun 2026 18:11:40 GMT  
		Size: 15.7 MB (15689103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d34dc4c2c9687512b55e901a2ddea1ad3aa9aaabde384a9c4652714cae77d5`  
		Last Modified: Wed, 03 Jun 2026 18:11:40 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:f9fd02b89edd160659d1a7d46dd82bcb14b19174af5df7b80bb76f9624092962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3191bbfe41719fe1a3153edb7d8f4b03a4377db304695b8624fe9ea41ece806c`

```dockerfile
```

-	Layers:
	-	`sha256:d916c0bb8ed3dc53839a54842065ee85bcf75af08944738553a20a297a54bda4`  
		Last Modified: Wed, 03 Jun 2026 18:11:40 GMT  
		Size: 2.1 MB (2115881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:821b792471f04df319c8cf1131fb6a6c548da7e4c53bc6a8c070a8cc9ccd1fd1`  
		Last Modified: Wed, 03 Jun 2026 18:11:39 GMT  
		Size: 23.1 KB (23078 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:cda99c2478c5a9dab5fe0f426f97a41551bfa681e0025ce3520d74d1362ecca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47277588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beec369cf938d0733bf73ded0b8c50ea696e7222cae872600de9050dbc7bd287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:16:06 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 00:16:06 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 11 Jun 2026 00:18:43 GMT
ENV HAPROXY_VERSION=3.4.0
# Thu, 11 Jun 2026 00:18:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Thu, 11 Jun 2026 00:18:43 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Thu, 11 Jun 2026 00:18:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Thu, 11 Jun 2026 00:18:43 GMT
STOPSIGNAL SIGUSR1
# Thu, 11 Jun 2026 00:18:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:18:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:18:43 GMT
USER haproxy
# Thu, 11 Jun 2026 00:18:43 GMT
WORKDIR /var/lib/haproxy
# Thu, 11 Jun 2026 00:18:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df01abe7b3188fe11763c740ea263cffdbb9292d6d8ffbbbf3fad457df8c28fa`  
		Last Modified: Thu, 11 Jun 2026 00:18:51 GMT  
		Size: 1.6 MB (1563995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379bdd440083ae7cb64443a5188c839473ddeb175261bd126e8000866ceb350a`  
		Last Modified: Thu, 11 Jun 2026 00:18:51 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b659ce08e77628557584b79ffaec2f8627cc250badd56dec7ff5d6ad0ec1314`  
		Last Modified: Thu, 11 Jun 2026 00:18:51 GMT  
		Size: 15.6 MB (15563427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f54f832fbe3118016779f4466a32e2aee913198ebfe048c26b0e57516e30e0c`  
		Last Modified: Thu, 11 Jun 2026 00:18:51 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:490eda34224052ad539106ac18ff0d2914109294f83c812303dfad1d3301cd26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ada536079cc3010a719ce3409ea49dfd3f6812dc66a34122c2b791ccccfee0`

```dockerfile
```

-	Layers:
	-	`sha256:f80496432203c1260b2f1c12e54afdcf91cd2faa47e7df5f9becc81968b27315`  
		Last Modified: Thu, 11 Jun 2026 00:18:51 GMT  
		Size: 2.1 MB (2114743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65c45442d147d23b91d6bcef628935ef394aad8cd664b8c1d3064aaf8b4036e2`  
		Last Modified: Thu, 11 Jun 2026 00:18:51 GMT  
		Size: 23.1 KB (23121 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:d7af8daa43bb362aed82a246f3e8be2f89853d8cc6be8acb37f0b5389373aa8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48355407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfeec7b5c2db18b0e9ed55f80545f57930c09b5638b7b2762da69837439f582`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Wed, 03 Jun 2026 18:10:49 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 03 Jun 2026 18:10:49 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 03 Jun 2026 18:11:43 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 03 Jun 2026 18:11:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 03 Jun 2026 18:11:43 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 03 Jun 2026 18:11:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 03 Jun 2026 18:11:43 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Jun 2026 18:11:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jun 2026 18:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jun 2026 18:11:43 GMT
USER haproxy
# Wed, 03 Jun 2026 18:11:43 GMT
WORKDIR /var/lib/haproxy
# Wed, 03 Jun 2026 18:11:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd65d8f5d687196ac14f36694b6c22235afc3d40c5edc6c8e0cc36a9162e5b65`  
		Last Modified: Wed, 03 Jun 2026 18:11:51 GMT  
		Size: 1.6 MB (1603835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02127b95885def7349c7b6639d9565fd7fb672e5fa4f5db171a9580c7ca9d76c`  
		Last Modified: Wed, 03 Jun 2026 18:11:50 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4e2bbd91b4c3825a23656575436b9baa772ceb5a994d301b766ac5d9b91613`  
		Last Modified: Wed, 03 Jun 2026 18:11:51 GMT  
		Size: 15.5 MB (15454596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac240e3aacc761f2c986fca5a648f4fa9962c5aa5955552999ce26aff6bf09ae`  
		Last Modified: Wed, 03 Jun 2026 18:11:51 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:52b030cd3da8f67e41a7e11d44dd339734345fa1e1df98a7f89be4ad55f8fd14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50d0e056ef6c2f9c2343a84bcdcc7af5d37afec8fe560f28dd573309b2d5f45`

```dockerfile
```

-	Layers:
	-	`sha256:1572425923dd4f7fa5fa07044476ff80c45f3935f349e8ca9a3787b989a7c23b`  
		Last Modified: Wed, 03 Jun 2026 18:11:51 GMT  
		Size: 2.1 MB (2111613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53dc856f2cf089e1078400d762dbc39f7c8be9474b231ada9b72283399368a43`  
		Last Modified: Wed, 03 Jun 2026 18:11:51 GMT  
		Size: 22.9 KB (22883 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:2c28214531195dbff20faf23004d0f7ee8c1f1ffc6d1cd3938b3b4e0711c8a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51710023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e68059ef37d137765b59a2a25120a8355964145e50f2568142ac20622e6196f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:57:35 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 22:57:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 03 Jun 2026 18:10:53 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 03 Jun 2026 18:10:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 03 Jun 2026 18:10:53 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 03 Jun 2026 18:10:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 03 Jun 2026 18:10:53 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Jun 2026 18:10:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jun 2026 18:10:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jun 2026 18:10:53 GMT
USER haproxy
# Wed, 03 Jun 2026 18:10:54 GMT
WORKDIR /var/lib/haproxy
# Wed, 03 Jun 2026 18:10:54 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2682f083b1ebf5bd4e4423d2b37efeb458f008ac7b2800f061f4abeb082ca07`  
		Last Modified: Tue, 19 May 2026 22:59:19 GMT  
		Size: 1.6 MB (1639553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada36dad28b45f88ff713f4189bbe40d949a14533ac18d07a0dff0cd73c3dc50`  
		Last Modified: Tue, 19 May 2026 22:59:19 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebee687f1c0d4cbdfae7bcac0ccb99eefbb208e968c5d73ec3a5fb4cce0bdb`  
		Last Modified: Wed, 03 Jun 2026 18:11:08 GMT  
		Size: 16.5 MB (16468377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7541eddadab687b92244d319bc8d301e780bd86e3dae41339ce2a29e576cdd`  
		Last Modified: Wed, 03 Jun 2026 18:11:07 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:b2fc2fdcbe0ffb306871b11b42aec9e6cd5dd20894ce4227c8a217b84a4158ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2141012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8e234e03af465da50829da738900ae9e227c37bc3ff302e7d0f77273cd79c3`

```dockerfile
```

-	Layers:
	-	`sha256:2c9dc26c3d4469cfe74ed550780e6bd323a3ef07da2effc88b7a6424ad1e7de2`  
		Last Modified: Wed, 03 Jun 2026 18:11:07 GMT  
		Size: 2.1 MB (2118000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52166337d623eacd342c76c742651d7bc91d150f5bdbe54e34f3d5f73447c33f`  
		Last Modified: Wed, 03 Jun 2026 18:11:07 GMT  
		Size: 23.0 KB (23012 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; riscv64

```console
$ docker pull haproxy@sha256:2e1647c2ba2671e8d257a8556123b80c94be03a24119462b011e7b5fdeff1882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44943471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699c6b5e50c7c0c5ed4684fc589161711833e58cc04abdfbb0ab1707633a9572`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:55:30 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:55:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 03 Jun 2026 21:45:30 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 03 Jun 2026 21:45:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 03 Jun 2026 21:45:30 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 03 Jun 2026 21:45:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 03 Jun 2026 21:45:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Jun 2026 21:45:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jun 2026 21:45:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jun 2026 21:45:31 GMT
USER haproxy
# Wed, 03 Jun 2026 21:45:31 GMT
WORKDIR /var/lib/haproxy
# Wed, 03 Jun 2026 21:45:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43ed4caffc37a4b22e17493e24339a19567e70a308fcaab3e7c52a7bc2def06`  
		Last Modified: Wed, 20 May 2026 02:15:51 GMT  
		Size: 1.5 MB (1535661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f5c3212984eab49401eba678332008a47c0de2e4433ba8519dc27c46dfe9e1`  
		Last Modified: Wed, 20 May 2026 02:15:51 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695e268d1b08331da2080285c03d41c2ce14897a40c4c14a2046e7be73d626f8`  
		Last Modified: Wed, 03 Jun 2026 21:46:41 GMT  
		Size: 15.1 MB (15128570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7474dc023ab7929c691ac2effc62c0885d036673944a5b2cce3a69f11a559a8c`  
		Last Modified: Wed, 03 Jun 2026 21:46:39 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:a9071711eecc1f4b2a8ba01dc8d3e3c34c22368e9f777f96d154952c883d6c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4418e97d13c4e724308f3b53d762a0a07058a53341af5662f66b00ca2ee98964`

```dockerfile
```

-	Layers:
	-	`sha256:21ed54eba8d846cbd6f2154e269a1021fe390bb36af62b5c4a7598be7d470344`  
		Last Modified: Wed, 03 Jun 2026 21:46:39 GMT  
		Size: 2.1 MB (2108391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4093098b3ef4653e2d6e08bacb5d30142cb805256625d0491d0019936b36e4cb`  
		Last Modified: Wed, 03 Jun 2026 21:46:39 GMT  
		Size: 23.0 KB (23012 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:94c6ddf716b08f5d7949e3b4eaac39e7a88f206284934528ad2c3a55ef1df5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47541394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4af4740388884daead54355782cdc97026b35c068fbdc06b471c8d76f39eac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 03 Jun 2026 18:09:52 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 03 Jun 2026 18:09:52 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 03 Jun 2026 18:10:44 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 03 Jun 2026 18:10:44 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 03 Jun 2026 18:10:44 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 03 Jun 2026 18:10:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 03 Jun 2026 18:10:44 GMT
STOPSIGNAL SIGUSR1
# Wed, 03 Jun 2026 18:10:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Jun 2026 18:10:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Jun 2026 18:10:44 GMT
USER haproxy
# Wed, 03 Jun 2026 18:10:44 GMT
WORKDIR /var/lib/haproxy
# Wed, 03 Jun 2026 18:10:44 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d5251243b10366472465b46ee3c7e1f399eed48090d7136a6e7de4a1c7d97e`  
		Last Modified: Wed, 03 Jun 2026 18:10:58 GMT  
		Size: 1.6 MB (1600060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c00214d4b4f7325d4e32fca6f6e05d05305dd668a3e1809fb437d0e217d18b`  
		Last Modified: Wed, 03 Jun 2026 18:10:57 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807946ff04043ec74bd8cc5d2f0aafdc0a0f7f009d484431a00eed39522c4502`  
		Last Modified: Wed, 03 Jun 2026 18:10:58 GMT  
		Size: 16.1 MB (16093768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a6962abe9616a52e96d65f8ae0864d51508475a62b841fbd445597d04b7b52`  
		Last Modified: Wed, 03 Jun 2026 18:10:57 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:d1947de2c6e8442d3608b8d27897608659eb76342f7ea341a9af6d6b8e563ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d937883d61d68165a4abdf3fe6c5e1e0de5702af80c19ae69a81c9dba01336`

```dockerfile
```

-	Layers:
	-	`sha256:1cbf596b302f70f537c011e692b99c91b8165df72df72da405a68ef9b50a8f75`  
		Last Modified: Wed, 03 Jun 2026 18:10:58 GMT  
		Size: 2.1 MB (2115886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e27a46f153512ff336fd057f693d4678dd2af43de7708fefdfcd7614c8814c8`  
		Last Modified: Wed, 03 Jun 2026 18:10:57 GMT  
		Size: 22.9 KB (22940 bytes)  
		MIME: application/vnd.in-toto+json
