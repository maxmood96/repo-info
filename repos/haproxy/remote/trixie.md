## `haproxy:trixie`

```console
$ docker pull haproxy@sha256:7a5f2b4eac999e35d38b0c49040ec885ac2929c6b1a17fde0d1dc2fbcaf07c52
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
$ docker pull haproxy@sha256:c49f0d1084eac089d4c227738a81be083484cb12a163efe4f067651cebdad5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42070002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2679aefe0800d6438663d8734fce3914c385731de3df0b776e131f3b8380ca23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 03 Oct 2025 17:19:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
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
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6063bba9d0e3ddc1bd878ebc0da32e07cd6d294e91aeb1ceba03f07f401ae53`  
		Last Modified: Tue, 21 Oct 2025 01:17:33 GMT  
		Size: 1.3 MB (1279443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f8b444bea83e9b7337b192da696a43451f2a362263284e63f21a14f9d4e4e8`  
		Last Modified: Tue, 21 Oct 2025 01:17:33 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc962268af434d86f9477b7c906f772096ffebde2a42d9148d8d1a092561668`  
		Last Modified: Tue, 21 Oct 2025 01:17:34 GMT  
		Size: 11.0 MB (11011000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f3b13630a71ccc750bd546d86c9f3ea7a621855f3961253350a6b7ff2f085d`  
		Last Modified: Tue, 21 Oct 2025 01:17:33 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:f04e6ed0e632c4ac4dbd35a955ed258180eae5edc596012104f107118bfb2000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2041becf20a423a6fa4fe4a413d361a2eb294c507c6ee6445af4e8bfb38b11`

```dockerfile
```

-	Layers:
	-	`sha256:afb0086e69a8f229177ea6d76dea8b8dcf9232b8c16b7c5230169ad97539fce7`  
		Last Modified: Tue, 21 Oct 2025 09:57:37 GMT  
		Size: 2.1 MB (2099870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba33b86ed30f55ece76a0944f39b04c92a1f0ba100e0ac0e6cdbb3dec3edd4c`  
		Last Modified: Tue, 21 Oct 2025 09:57:38 GMT  
		Size: 22.0 KB (22035 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; arm variant v5

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

### `haproxy:trixie` - unknown; unknown

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

### `haproxy:trixie` - linux; arm variant v7

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

### `haproxy:trixie` - unknown; unknown

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

### `haproxy:trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:ff828e4f991114ccfbe8fbb4aa34c4a002911fa1cbb86abee7e02ad63ce7532e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42346220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2580b6b86dc4a5ffc5bc7b2576e8a294cbf5acce91c8187c6fea1a6586351c92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 03 Oct 2025 17:19:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
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
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d3dbd087a5df0d85720d22a334310199d37832cf204ac23a9ad2b42cd2ad56`  
		Last Modified: Tue, 21 Oct 2025 01:17:48 GMT  
		Size: 1.3 MB (1261054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13842ae8fe2e15ec292d009ab26a803a43ae817b422683549633cac69e471093`  
		Last Modified: Tue, 21 Oct 2025 01:17:47 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fed31af1f03e9eb2856a050a46926a617a5d5a51e80307b0678f263f0b58449`  
		Last Modified: Tue, 21 Oct 2025 01:17:48 GMT  
		Size: 10.9 MB (10941400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9d785e06607d00579eae000dd81fade395ff3bd3b49ce9359bfba839ce2d1f`  
		Last Modified: Tue, 21 Oct 2025 01:17:47 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:7cf2f634df5a99f76545d7169a9b32ef652a2175b083e56f9eb6f15383e664b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbcd274814e582332607ed03f93f8c12f1187e90c57732316965933533d71cdc`

```dockerfile
```

-	Layers:
	-	`sha256:2a8e293cf331631f325accc62abd21b7b3a44a9c85e01db83c3a3225b0b60d4a`  
		Last Modified: Tue, 21 Oct 2025 09:57:46 GMT  
		Size: 2.1 MB (2100178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ffe7536e20e12fe5c50871a302efda1105b2570979149e01874c7a7cc0b2e9`  
		Last Modified: Tue, 21 Oct 2025 09:57:47 GMT  
		Size: 22.2 KB (22218 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; 386

```console
$ docker pull haproxy@sha256:f07fe99cde85b2a72bb1a4a409d587e4557e0b616bff34de5eea79cba7b815e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43305216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68817ed4147e5553bde3e679b90659fb14d6ef056f63281b699356fc07b3e01f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 03 Oct 2025 17:19:43 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
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
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962eda37e55880b04b8114fdb1158042155c839d2eb542438dbee633f9ddd62a`  
		Last Modified: Tue, 21 Oct 2025 01:17:44 GMT  
		Size: 1.3 MB (1287005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b463fe7668b1f46544454a644ceaad04a7e6f70945666cf648065a79039fd018`  
		Last Modified: Tue, 21 Oct 2025 01:17:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d4513891e6ee704e1143cd6a574fad0e2bcef661d74588f888aa5f967de783`  
		Last Modified: Tue, 21 Oct 2025 01:17:45 GMT  
		Size: 10.7 MB (10721946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8373d29c8082b8c48c8ec97e1319adb06b2bc1b018549f07a2bb5551af8f4f`  
		Last Modified: Tue, 21 Oct 2025 01:17:44 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:c911f312fc9d3a296ea5e4032fd8edeb1023e4d5ec0f07fa2b4cbd14e2ec83c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa5e87bc7781e671258f7f5e52a0c4448cbfdde9be9e306e59c23955ad714b2`

```dockerfile
```

-	Layers:
	-	`sha256:7e199e64e404ce97911f3cc204e0557f8e04422a14d30bfe80d37c0f09ff4390`  
		Last Modified: Tue, 21 Oct 2025 09:57:51 GMT  
		Size: 2.1 MB (2097043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82ad7066790cf37c29366fefa22f30043c434f695642a5e68d5198000476ebc1`  
		Last Modified: Tue, 21 Oct 2025 09:57:51 GMT  
		Size: 22.0 KB (21980 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:trixie` - linux; ppc64le

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

### `haproxy:trixie` - unknown; unknown

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

### `haproxy:trixie` - linux; riscv64

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

### `haproxy:trixie` - unknown; unknown

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

### `haproxy:trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:1702c0fb5abafeb3b2832fc167e30ed491516b679cf42faa6baa3a457c562676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42439021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d44dc95121d1e25145151bcf878b2ad3f4d43492f881c4f528c0fcc3baf2eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Fri, 03 Oct 2025 17:19:43 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
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
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdbafedea5d5252d209f3230c0a782066a9adab715d650edf6456f1314148cf`  
		Last Modified: Tue, 21 Oct 2025 01:24:27 GMT  
		Size: 1.3 MB (1294444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2627b87008b67bae410024700ba44b608d1c45e0cff1e5f524ad9a054507fe`  
		Last Modified: Tue, 21 Oct 2025 01:24:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf60001d23c78629c597f97d30c196a8bc7984baa53ec80ff8211c4d46a7aa5c`  
		Last Modified: Tue, 21 Oct 2025 01:26:18 GMT  
		Size: 11.3 MB (11305685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47966b4317a8bf57984c432f518bd2460cd28a2dff0cbde75c6fcc3bb86aad67`  
		Last Modified: Tue, 21 Oct 2025 01:26:17 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:e6f2953523217a2394f06a8ca0aa5bc7543885a8c500df7ed0ea034dc7ec56c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ad622cb641d038a280267374f3e3587f1e743ddbc2b4102e5af497c9f2aede`

```dockerfile
```

-	Layers:
	-	`sha256:8f56dc1325e7e117410dd83d60a65d061d97aac5bdb781cf2021dd240fbc9030`  
		Last Modified: Tue, 21 Oct 2025 06:58:14 GMT  
		Size: 2.1 MB (2101315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ca17f24b2ee099d302f76b175c929f75fd51dc4351a40d12755a5b05e5cf965`  
		Last Modified: Tue, 21 Oct 2025 06:58:15 GMT  
		Size: 22.0 KB (22035 bytes)  
		MIME: application/vnd.in-toto+json
