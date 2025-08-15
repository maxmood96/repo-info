## `haproxy:trixie`

```console
$ docker pull haproxy@sha256:5459c3870279663086d25360eec293a4464145fbc3bdb2943e2cdd7f6a68006a
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

### `haproxy:trixie` - linux; amd64

```console
$ docker pull haproxy@sha256:bd3b3b3d451cf6587bb64e100a47a68186fd2c24510bc06d8f394c09b14276a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42041271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41884b63cbb888411025552dcb6e38bcf4a9dce89328b1ea8f85ab8eda8c095f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6903a7ce3522badad8b9a73574aa44ff6f5d358ca867ea5cefe402fc678d6877`  
		Last Modified: Wed, 13 Aug 2025 21:16:39 GMT  
		Size: 1.3 MB (1276766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aba6b25e174e05b79d23ba7cbe3cf5b9c8f166690858c8ec96c47322ac0b27`  
		Last Modified: Wed, 13 Aug 2025 21:16:39 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d14b773f9b175ad9b3062c9ca6df3ca0c3f059d10b7471ba1f0fdedabeb78d`  
		Last Modified: Wed, 13 Aug 2025 21:16:42 GMT  
		Size: 11.0 MB (10989578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8834b00bdc0eaf26cc565d4434b4f7a1f92b630cfb588740d843f1b25d6a96b`  
		Last Modified: Wed, 13 Aug 2025 21:16:39 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:1ed89a7fa4e95d59500ffe6e7c8fb7cfb7016ef3ce3fe3c775fd7a4107313d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd96d65addcebd9db7ede7733fe7dc8943dea6e243ef429daebcbf3498d0071`

```dockerfile
```

-	Layers:
	-	`sha256:4545e589c8735d3f4e4699ff3cbfc624ecf50df6a914fd8f5ad85a2a82015b9e`  
		Last Modified: Thu, 14 Aug 2025 00:56:20 GMT  
		Size: 2.1 MB (2098968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45d9e6f70cb4f7787774aa0e9bfbd6b7d4409f77a4f4f8d80211200d488f0a89`  
		Last Modified: Thu, 14 Aug 2025 00:56:22 GMT  
		Size: 22.0 KB (22036 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:e10473c91519b5ea6d5d1adc83245e27e0ed58d6f573a14c8629e4d7df195f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40292193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412175191d7b5cfba3fc288ae95063ef8b968d215aaf4ed30f83d51d4a582c69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df03617ca2748b9aa1852c84952cfc3e336e91bdc9c6a976458a1a64ae06bea`  
		Last Modified: Wed, 13 Aug 2025 02:01:40 GMT  
		Size: 1.3 MB (1260195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494249a16e399bd97f300fe2d049aa632432a3be763a8e589155e7db439f8fa9`  
		Last Modified: Wed, 13 Aug 2025 02:01:38 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0828bd250a3c6c82ea0a3903bc7225db718caea49c9c8c06f69466048e4f44e6`  
		Last Modified: Wed, 13 Aug 2025 22:26:54 GMT  
		Size: 11.1 MB (11088650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cbeadd044f49aafacfd184cf8eaa897b91522f337542520ffdfd35f7650995`  
		Last Modified: Wed, 13 Aug 2025 22:26:53 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:1c6f274a8ad5210a73c0bf0135160a90ba349549d6d3006219d4a57912c1e30d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d807e7ad3a21d94d7302b8c8a02e7022a1f09b1391e6a8fb477828bd302cb629`

```dockerfile
```

-	Layers:
	-	`sha256:9a40dec214de4772b969f251194326540099956390e2d43c2db84c6fe327d09f`  
		Last Modified: Thu, 14 Aug 2025 00:56:26 GMT  
		Size: 2.1 MB (2101963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab0a58ede64158131a6013cd2581ef8fbbad5e362901f1c2be8e5bb216f0089a`  
		Last Modified: Thu, 14 Aug 2025 00:56:27 GMT  
		Size: 22.2 KB (22170 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b2ab6138bc8f77b67d6e4c6b1e1c8d795aff88227b481a9e1df49788e197e934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38315940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdbaf14c78d42ad83e19ab9d9c51c3c82e87cafd2e2c97687de192ac3941481`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd903ff72be6c438418b82ef7efcef0cd153d6c009d18165d7e4ac22432c3f24`  
		Last Modified: Wed, 13 Aug 2025 02:42:44 GMT  
		Size: 1.2 MB (1234018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6dc532d85fbc1afaf7f7f8886dcbc8d1a36fcc1a17109bfd9d7f59872cef40`  
		Last Modified: Wed, 13 Aug 2025 02:42:44 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8654f28b4fec083f3b9f6c5216055b9a3137d86d4e0c0486f1e3e8689cc2cbf2`  
		Last Modified: Thu, 14 Aug 2025 03:03:13 GMT  
		Size: 10.9 MB (10872795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0848020711dc918f7cb25f947943e69a1f8082e36a94786bf20889ba7733ce`  
		Last Modified: Thu, 14 Aug 2025 03:03:09 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:28752f29b90b5417c4753916157c998fc60048c026f5402089136962a9cfbe87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf74f690c20d2bf3db592ae6b8526b999b5c18e397c30a0db2819ad960d434e`

```dockerfile
```

-	Layers:
	-	`sha256:5f3683d6e57a2422c1d7375cb6dd4d510d0a3f294e22c5392771b76863a341d9`  
		Last Modified: Thu, 14 Aug 2025 03:56:25 GMT  
		Size: 2.1 MB (2100404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90e32a075468fa7c2a9172481ec2636b42001a576c0d4e41f312ae3c60c74aea`  
		Last Modified: Thu, 14 Aug 2025 03:56:26 GMT  
		Size: 22.2 KB (22170 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:427ab6f02a5745e194415d76d5ce4ff565f73e554e6d9c195aba9bff68deaea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42331885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dafe22f24bdc8d8a1f40b79a5dc4aae42a58a0bfb6fce3c739b3a582c7a540`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891da654b1e0819d89c064c6c39045ad3034bbdbf38993c24cbcc80bec9ff614`  
		Last Modified: Wed, 13 Aug 2025 01:54:56 GMT  
		Size: 1.3 MB (1258911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6ec86f4c8a99fd081d12023139141087aae12a90fc1ea2cd1607e8e69786f7`  
		Last Modified: Wed, 13 Aug 2025 01:54:47 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7cc532ed7404da5d174ab9e269c4400caba62be06cfa7f51b3edc2762c944e`  
		Last Modified: Wed, 13 Aug 2025 22:58:29 GMT  
		Size: 10.9 MB (10935297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7efd75f673c4f54c779c31e319abb954f9c9e1e3a5fb273c76b1f54fe042fa`  
		Last Modified: Wed, 13 Aug 2025 22:58:28 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:c0b81e4aca0abea0db9c7eeec938d6c49467242bf2b48e7655c07340094ee42e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ea46c69ef533e8acfddb2155589dfacdd42f48c9afb5a11e1ee0cb4a8b5180`

```dockerfile
```

-	Layers:
	-	`sha256:d297ac5e76f6ff2c171b7ec935d5fb37e4d4ed9c355f11cb73e14298307eacfb`  
		Last Modified: Thu, 14 Aug 2025 00:56:33 GMT  
		Size: 2.1 MB (2099276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b3ee3e0fe8548d583afc668b0a01fb2d1e7fec1bc15c7a69dddc1e87ddcdcf`  
		Last Modified: Thu, 14 Aug 2025 00:56:34 GMT  
		Size: 22.2 KB (22218 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; 386

```console
$ docker pull haproxy@sha256:4a4c1f2e07a10c1607021c2a61c95a3834648910d54f159b52834467f7c406e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43275860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f06f484789806a188e2a04270d98f10fad8f03b9f2264650319e6f1c1d92a90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af8d48772d64cfd59a3e1420bcf6d0125fac625fe8767130e2608f7e91db809`  
		Last Modified: Wed, 13 Aug 2025 21:17:32 GMT  
		Size: 1.3 MB (1284736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9819bb44f932c9baa185b2c0b888325fbb562482d21eaf732d4380738625d7cd`  
		Last Modified: Wed, 13 Aug 2025 21:17:32 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48af9981e905e6df68e7a342f15eb8e9ed8063cece8c80f85dfbdace08be7fa9`  
		Last Modified: Wed, 13 Aug 2025 21:17:35 GMT  
		Size: 10.7 MB (10700106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65da55d4f25cef904953ba5ac6fc5264c54cb49702d0a8e0faa62c1bf95dfd0f`  
		Last Modified: Wed, 13 Aug 2025 21:17:33 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:2b871ccfed807b4025a14da574c23dd932c8eed39a4b8bf51a1350f4c51ec0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f706aee054812037e91c5d3772b4ab90c872edb7af933003f9076eef4f68a5f3`

```dockerfile
```

-	Layers:
	-	`sha256:cebb3c7b9218a29b8176c717ae0b67ac684d2ec7d8229f33da11988fb5a49784`  
		Last Modified: Thu, 14 Aug 2025 00:56:38 GMT  
		Size: 2.1 MB (2096141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92cbdc11068ba8d3390c27117a2defaac7d00cff34aa86ee25c07c37dccaa360`  
		Last Modified: Thu, 14 Aug 2025 00:56:38 GMT  
		Size: 22.0 KB (21980 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:bc30e7f528a70b3c2c92a27fa234fa85f1cdeedc259cecc09d744532b5a66edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46551668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bbf3190bf1883fa34a745bae7a061ec12951a364142e0a11eeedee6c063557`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08cf3336548be15e9a272752cbf4aa834fff4755d4cd8907e6b67a6c04990b0`  
		Last Modified: Wed, 13 Aug 2025 04:47:02 GMT  
		Size: 1.3 MB (1307336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b874481c0dc085f1f373fbf03fc410d4db8c76218d068ceecffb4ace7649ed96`  
		Last Modified: Wed, 13 Aug 2025 04:47:11 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078721fe719a3999c871e97f9379f2bd72734914bb62bd4b282e129835a66b22`  
		Last Modified: Thu, 14 Aug 2025 02:27:41 GMT  
		Size: 11.6 MB (11648476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67eedf9d9504da9d4f4e7bc8acaaf599b85b68eb430e1b6233dd901f58ac5d29`  
		Last Modified: Thu, 14 Aug 2025 02:27:41 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:f789a6c13c0404a70371487d98ae060f5c732d52b16df8217657462eb55043e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9ab22ba39dcfcc372052ab31c7b14d61623d122cc6c30e880d1fc82c567437`

```dockerfile
```

-	Layers:
	-	`sha256:2d4358ca689287d1910257db0e5a38dacff34446133b5af395b919cc52d45d58`  
		Last Modified: Thu, 14 Aug 2025 03:56:35 GMT  
		Size: 2.1 MB (2102517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6032029593cd81faa36c494936abf3a94781f70a1502c7abd0e82f6f4256ecd8`  
		Last Modified: Thu, 14 Aug 2025 03:56:36 GMT  
		Size: 22.1 KB (22108 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:e425b5f924bcb6dd610ba8dccb91e186fecc798ea5685e90879614cca72afae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40169169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cda4862bc2d8c9285db4762d6659b4731e1bf416c842f662dca8dca3216f145`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311997e7d313b262fb90a639c3470f7f75355644de3ad48a51c6291339fa813e`  
		Last Modified: Wed, 13 Aug 2025 08:02:36 GMT  
		Size: 1.2 MB (1245287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca61b8b42954da27ebbbea9ddcf76e632bad4a77f5a1e536d221667706c007a`  
		Last Modified: Wed, 13 Aug 2025 08:02:36 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b720e51bf1acd8ba5f78b8aea506a27065ec178e502d61e340854360db4df58e`  
		Last Modified: Fri, 15 Aug 2025 08:56:30 GMT  
		Size: 10.7 MB (10650616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba85ed3d7c3ada13d40e5d6de38d7bb7d0a947a385ec654a3ab96721142d89eb`  
		Last Modified: Fri, 15 Aug 2025 08:56:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:3768839364b07d157e6ae6363b36d08453a5015ddb100f73b2e5bec19cfd948d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55b369a81e0b90bbb7c97e2e7d45c86564f0f4fb722a0149cace9224099d453`

```dockerfile
```

-	Layers:
	-	`sha256:fd1d824f2bb51e49e23f1f286481ab523406159e3e24dfbe0e846735119eedec`  
		Last Modified: Fri, 15 Aug 2025 09:56:23 GMT  
		Size: 2.1 MB (2092912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ee3e3f762006b9c22a8f6db47f937e4cdf671a4c5e7fc5be655896d92ee54cb`  
		Last Modified: Fri, 15 Aug 2025 09:56:24 GMT  
		Size: 22.1 KB (22108 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:ebe8d786ae2a23b43465783a595c1756acd316adb4027741a3a8d3d5eaefc778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42424917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93be80d476b200a3e0b5a6500a451c72ab202b58cd6186afc65fc0ac60359541`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_VERSION=3.2.4
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.4.tar.gz
# Wed, 13 Aug 2025 17:13:28 GMT
ENV HAPROXY_SHA256=5d4b2ee6fe56b8098ebb9c91a899d728f87d64cd7be8804d2ddcc5f937498c1d
# Wed, 13 Aug 2025 17:13:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 13 Aug 2025 17:13:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 Aug 2025 17:13:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Aug 2025 17:13:28 GMT
USER haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 13 Aug 2025 17:13:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56db9a2bc47e183d36acaa6b3f5d2b8660451625c86023d3edbbdda75b9cc31c`  
		Last Modified: Tue, 12 Aug 2025 23:20:50 GMT  
		Size: 1.3 MB (1292025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98c51551f038e27cd889bb8f0650573a451fd3821f06708378c6c103da06269`  
		Last Modified: Tue, 12 Aug 2025 23:20:48 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9259a665fa25b31904b87d7e8a3b687d760bb1afa4e1a210e492d13e317438`  
		Last Modified: Thu, 14 Aug 2025 02:52:12 GMT  
		Size: 11.3 MB (11298196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd1c650d98ad4fe0ca1283d389363598d9eb03d606d8fff7f327ab426659b00`  
		Last Modified: Thu, 14 Aug 2025 02:52:11 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:5f8aa69a01c677332ec3403ed572b66f1629d7552e20a0a46baf6cfc76e5cc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e55a540c2b1b64db145989fc60ba0baa88963f7c1b20a35c07e32caf206f02`

```dockerfile
```

-	Layers:
	-	`sha256:560ffb3012bea4cffc27ed3116a269fa407a4debb8e4658787b703a67afdb41a`  
		Last Modified: Thu, 14 Aug 2025 03:56:42 GMT  
		Size: 2.1 MB (2100413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b2118289c307811cd845eb13e08b68fb2664b0234d6f016a5d354f415b8ed7`  
		Last Modified: Thu, 14 Aug 2025 03:56:42 GMT  
		Size: 22.0 KB (22036 bytes)  
		MIME: application/vnd.in-toto+json
