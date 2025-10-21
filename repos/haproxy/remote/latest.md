## `haproxy:latest`

```console
$ docker pull haproxy@sha256:a0a4c92a650c9f6ee9d05720e11388eb7dc1f7766a5dc8d09652e4463b8f18de
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
$ docker pull haproxy@sha256:dc60a7cafe54783e857f93775e428ddb6b27333d8c8222417169cac02dac96a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45029295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ca014edb614bf45ce57bb71ce2c182f4d1cf357fef90d5f3ae1e6b8fbb212a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30862e038e9113afbd549f1e5af209e7225da75cb13debc5b8c0b4c64d2e3fb9`  
		Last Modified: Fri, 03 Oct 2025 18:31:07 GMT  
		Size: 4.2 MB (4238695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc9e592cadb87ab7e3a07a5b7e9ef457ab404e753c524f178918652d45e2840`  
		Last Modified: Fri, 03 Oct 2025 18:31:05 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5223d15135d1e9a41bab8eb00704a34566919551d4377e04e9759f4d53c5b7a`  
		Last Modified: Fri, 03 Oct 2025 18:31:11 GMT  
		Size: 11.0 MB (11011191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f3668e4cd0f2e3580ae6bb2308f62b2b821e78006caf7b64ad108e449dbe57`  
		Last Modified: Fri, 03 Oct 2025 18:31:07 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:e9c3c428ac06d8468b929bb4efb9e9d3a61a63d7358392a4834d853b598d5c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d2788a11c54cff0e1922c84837e8023b5b94e430f02afc4c92188260108b48`

```dockerfile
```

-	Layers:
	-	`sha256:36bf74b2917964b60ba66b22c4595f0fd36db1a30d93c63952044dc47f1f1eb1`  
		Last Modified: Fri, 03 Oct 2025 22:01:30 GMT  
		Size: 2.1 MB (2099870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08bd0bc4107ffc6efed5337568604d108f143b6a69fc5455dfefd3b16ee8c684`  
		Last Modified: Fri, 03 Oct 2025 22:01:31 GMT  
		Size: 22.0 KB (22035 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:1c9ab3d0492253df71ca6616b1e097e0fdb363469fa67ece0d1a910c02440f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40305349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d83f37fad8ffaba8c32e20cad6efc674c93af1a937e1a70f5154715ff38c9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 03 Oct 2025 17:19:43 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32743eb2bbd74941947b3e523ae5def0852dc70e35072978f4124510235bce8`  
		Last Modified: Tue, 21 Oct 2025 01:18:30 GMT  
		Size: 1.3 MB (1262884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f83e197cb64fefbf5e228e20877725b4abe6560d33ec1d29d6e1f2d404da82`  
		Last Modified: Tue, 21 Oct 2025 01:18:30 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02eb335bfcfd438be661a171d05331ad407d5eacb76016bfbb605837093fcb08`  
		Last Modified: Tue, 21 Oct 2025 01:18:34 GMT  
		Size: 11.1 MB (11094543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3d9f0c3edde3fc9788685363ee9aab708edecbf8fc37c3a63ef60d78946f49`  
		Last Modified: Tue, 21 Oct 2025 01:18:32 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:b70c9e60321d571af3b6ff33c70fa527ddad362eab981327c06411efb0d1b106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2125039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72642bf1dc9ccbd6c26930934acf4465e84686d73b360043e675aee5f9ad99d`

```dockerfile
```

-	Layers:
	-	`sha256:911d7617fa499c6dfd2193d47011ff8c309414496592116d8b85d5f5210abc12`  
		Last Modified: Tue, 21 Oct 2025 06:57:48 GMT  
		Size: 2.1 MB (2102865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1db168f48370d46dba087bf41ba6082d6f57ad6634cc9d389b7239e860d0324c`  
		Last Modified: Tue, 21 Oct 2025 06:57:49 GMT  
		Size: 22.2 KB (22174 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:1f0404d62fefb87050dbdfc2dcddc2b95f8138d75af6fed807fe2649143031a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38333505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad266947003875f7478ee5f5d826526a2a5b1ad369bf12d7a0dc1ff276fb8d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 03 Oct 2025 17:19:43 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d265cd32883dc3cd07573fe4fd8d94c3782c08af7828499b571e1afe8658142`  
		Last Modified: Tue, 21 Oct 2025 01:19:34 GMT  
		Size: 1.2 MB (1236049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6f535952a646b6e95485c5060e78428b17430d09a1aa0c80806b411c5e97b8`  
		Last Modified: Tue, 21 Oct 2025 01:19:34 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67209ca1630ff45d5f7dedefc55ce2258c75f4c84af8dd23b67c2bd7525d2721`  
		Last Modified: Tue, 21 Oct 2025 01:19:35 GMT  
		Size: 10.9 MB (10882926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205c3a9cc66e3fb23aed8ca5c88fee952c7d3c73faf88131c2a9bbac453910b7`  
		Last Modified: Tue, 21 Oct 2025 01:19:34 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:d8f5505736bb785c700d9b024bf390c69da66f2b01e50efbabf041746d0e8b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca8ce08b8c8ef173dca6703e6e3fd01243a1bb0ecf92a1fd6fe507ccd9af19f`

```dockerfile
```

-	Layers:
	-	`sha256:92f919265fef42d7b03b1b8141d03191de78266fd3b2c5197270bd0ceffb5841`  
		Last Modified: Tue, 21 Oct 2025 06:57:52 GMT  
		Size: 2.1 MB (2101306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed3d8cf20655bc9d2712a607a065c51d7c66bf3a0a4005459f7559cfc5f6125`  
		Last Modified: Tue, 21 Oct 2025 06:57:53 GMT  
		Size: 22.2 KB (22174 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:e3901bcff72ccde6651c4687ca06a56459e94a39ffe7cf81f1a2b9fefb053196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45664568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe79e85940b5ae0d28526a4519ccc8964b1082173247d65bb09f5e6a042bb6ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fff96dc6ab6a9e31f6b32aed2b0b7c2c5e5552b37ec2b66b97f64455af491bd`  
		Last Modified: Fri, 03 Oct 2025 18:31:03 GMT  
		Size: 4.6 MB (4580426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87208700d19361eb085ecad38d9d29d7c4d7a4f68cf574cbe194fbe02976c36`  
		Last Modified: Fri, 03 Oct 2025 18:31:03 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b570c5a1bd3bd680b5c05486be4fc2aede373d713201417be427f7e2b56f5f7f`  
		Last Modified: Fri, 03 Oct 2025 18:31:04 GMT  
		Size: 10.9 MB (10941657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7a3126fad2f5d9fad803070f653a26c002dab0885f2e14ff5eb21862ec27f3`  
		Last Modified: Fri, 03 Oct 2025 18:31:03 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:ea5cc7a00756ef31072be3af9995fd449508a1de4a4e0caf57c8487f1683e564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070850eed09d133dbd718bd224bb9d0d924693db28ad420d883cde0cb1019286`

```dockerfile
```

-	Layers:
	-	`sha256:3038d5157ed71c0b96785405df45196e299c9b2a7f4e04d16899ae91bd706e51`  
		Last Modified: Fri, 03 Oct 2025 22:01:44 GMT  
		Size: 2.1 MB (2100178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58ef4b9592e7cbb850587297f7ca9c43e694e5a2be4b46e1159db58e221aa33`  
		Last Modified: Fri, 03 Oct 2025 22:01:45 GMT  
		Size: 22.2 KB (22218 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:410d3d911ecd9e2a5091eead2a7cf288c8b19f6adf8cf211c649dcdfe5c368a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46195186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a37ef0ca030e46e414fa4fee59f851ad543c8998cf796289d9e8f864f156b3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7cc2e9b4384fe7ee374710004bacef1c9a39a9ecf0425cb7c2b7b261a37325`  
		Last Modified: Fri, 03 Oct 2025 18:33:26 GMT  
		Size: 4.2 MB (4176810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ea9491344486e833ed885d77995bbdacf724d8bff5bc9457c681cc39864b55`  
		Last Modified: Fri, 03 Oct 2025 18:33:26 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea43c3a5ebbefbae633f9d95d92428eea9df09998c74522744f8c979c831b8d`  
		Last Modified: Fri, 03 Oct 2025 18:33:27 GMT  
		Size: 10.7 MB (10722198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e9616a9ff2c678e2ebbc7dd5f58007f335ae01c8c8d7f1668015609975a0bb`  
		Last Modified: Fri, 03 Oct 2025 18:33:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:29585f9eef90b2cfe2bdc3beae931a43b5cf6d64bf6fedaa1383989894118b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f9ec179b703071e4f9d623047c72850a964216c801a6de4fed15d79b1eedfe`

```dockerfile
```

-	Layers:
	-	`sha256:4f1e300d0526e27b7bf70fd38cdb0ac489933de8d57b005170e4900e91b75d80`  
		Last Modified: Fri, 03 Oct 2025 22:01:49 GMT  
		Size: 2.1 MB (2097043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adae37ab0514c65ad220ac22ae935c585028a45e379d0203f43f3311904231ad`  
		Last Modified: Fri, 03 Oct 2025 22:01:50 GMT  
		Size: 22.0 KB (21979 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:faa36c8c2fc66b7f1f3588c2139d7465ea00c0dda1e3d3f21321a2846cc0ebaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46567805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e94105ea1c27eae95272b9450e943a04e2fca6387fee135f4ccd2acda60d4f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 03 Oct 2025 17:19:43 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa480cd28c6d83024f0956dd0a6069d31ced439970222c630288cc6a8b49304`  
		Last Modified: Tue, 21 Oct 2025 01:24:17 GMT  
		Size: 1.3 MB (1309951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51ae4de58a89a04bf56cab7ffd8d3594d5efe269445274257939ca966029ac4`  
		Last Modified: Tue, 21 Oct 2025 01:24:17 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ec6cbcd6933611a028856d802f97d97d8a8829a1a186e1010221bfd5271df5`  
		Last Modified: Tue, 21 Oct 2025 02:10:36 GMT  
		Size: 11.7 MB (11657699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06260a5bdf538e4ec104b1c1446bca903894461d56b3f8d4a848dacec549e75`  
		Last Modified: Tue, 21 Oct 2025 02:10:35 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:375ac7248f20d2d12e81c3d83b1fba1364e4f6c8173ec549ecf8c44f730a4230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2125527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628fbc9b97ba2b5d8a19edfb38fca75f566e31d5b1c62534995e81258dcdc860`

```dockerfile
```

-	Layers:
	-	`sha256:39aa9713c142e5afadbe53640d870024d94cb9005ccdde3e2036bf86298b616b`  
		Last Modified: Tue, 21 Oct 2025 03:57:24 GMT  
		Size: 2.1 MB (2103419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06fc3c29c081e1e651ada22f34193662a36270c7ad063007bd8ff62184c1928e`  
		Last Modified: Tue, 21 Oct 2025 03:57:25 GMT  
		Size: 22.1 KB (22108 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; riscv64

```console
$ docker pull haproxy@sha256:4560b417d3eb2c06c133c64b9a6f89b1f2441c9a6ced1dd5c63073af1405c745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40190354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a33b8cadf57e0b429dccf3efc36380018690c8fe5addbfe283f05de9b205eab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 03 Oct 2025 17:19:43 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6db63d23977902cd61a5493af040699a9fa228b1e2639aa68d1114198a15a66`  
		Last Modified: Tue, 21 Oct 2025 01:42:20 GMT  
		Size: 1.2 MB (1247717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4342c56fad4b640a1ddfad5baa6ea747ca74d5b7b300c2c7530c1dbb13684d41`  
		Last Modified: Tue, 21 Oct 2025 01:42:20 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ec0c5f3f6fc87d5c45f376f5b47883237f75f9f226ac9684e7ccc443068a44`  
		Last Modified: Tue, 21 Oct 2025 01:56:22 GMT  
		Size: 10.7 MB (10665347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db09dadc618df541d4f324f56af4e83a8aee5d5799c92e516523c0309ed62706`  
		Last Modified: Tue, 21 Oct 2025 01:56:20 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:b401c51eac0434e4e8a8b6bc070e6b4ea85dd9d83303ea0b9b515b65b19fce74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99850aef9ce6b2901348c4787f70aa6fcd4497bc7288b6e3361476cfdf4ba82`

```dockerfile
```

-	Layers:
	-	`sha256:ac0773c3f5967383b9d5fce47fd65792a453a85c2d2049728592db5ea68a7e27`  
		Last Modified: Tue, 21 Oct 2025 03:57:28 GMT  
		Size: 2.1 MB (2093814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:046749f284c6b5323e9f8319a4b4134d172dba44512d59db96edfdd73b763d45`  
		Last Modified: Tue, 21 Oct 2025 03:57:28 GMT  
		Size: 22.1 KB (22108 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:2bbecfb87c1f1968fad7228e733dbd1e96332eab9b6c81c6bb8645fab5e69780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45042408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1ae2ef08c0adb184484ec6b0ca9385f6efb508b9c7e56c5d60d0c7b4ca573a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_VERSION=3.2.6
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.6.tar.gz
# Fri, 03 Oct 2025 17:19:43 GMT
ENV HAPROXY_SHA256=ad630b6b0b73e1d118acce458fec1bf1e7d0e429530f2668ec582f4f8bb78e65
# Fri, 03 Oct 2025 17:19:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
STOPSIGNAL SIGUSR1
# Fri, 03 Oct 2025 17:19:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 Oct 2025 17:19:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Oct 2025 17:19:43 GMT
USER haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
WORKDIR /var/lib/haproxy
# Fri, 03 Oct 2025 17:19:43 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72581a4a19f0dc4fd43a19aadf233d784c89bb312e4438493b97a806d8155e3c`  
		Last Modified: Fri, 03 Oct 2025 18:31:58 GMT  
		Size: 3.9 MB (3897569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fd5f64e59f0e01bf9d675150dd47bd79b34f55042a8360c35ce4d68a859605`  
		Last Modified: Fri, 03 Oct 2025 18:31:58 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e7f8689224f111c5d43f00d0d63f33da2ef1887bba58251cd4f147bfd96638`  
		Last Modified: Fri, 03 Oct 2025 18:32:01 GMT  
		Size: 11.3 MB (11305968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4a69e9860c4f00e645f19ffd00eb11fbc63a7f8498a9813183da9682e0bcd2`  
		Last Modified: Fri, 03 Oct 2025 18:31:58 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:77371ed08a5965fce9d079c5a8037a62c45fea2d2ae302894b0316ff45ff101c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad8416359add9986e9be6ac3c8cd59adb9d422ed468b731eb11e9b180d92708`

```dockerfile
```

-	Layers:
	-	`sha256:740f309fb13d44e04cb5fbd4493d3dbe7e45b2b6817e9b37940ee5c2e7324aaa`  
		Last Modified: Fri, 03 Oct 2025 22:02:00 GMT  
		Size: 2.1 MB (2101315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb70f7e3043f347b00be26241abf0f2b32133585bceea843ed95d1816778d30b`  
		Last Modified: Fri, 03 Oct 2025 22:02:01 GMT  
		Size: 22.0 KB (22036 bytes)  
		MIME: application/vnd.in-toto+json
