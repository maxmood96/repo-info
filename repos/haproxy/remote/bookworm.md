## `haproxy:bookworm`

```console
$ docker pull haproxy@sha256:c6fb2ced2fe69243bcaf39251ffea5fce215256b07a25aa235c1eac966fa3c5b
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
$ docker pull haproxy@sha256:fe54da647b73880b2f048c954b7c681ff6e69989162a42d12395447db176631f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42581488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9e97eeebdcbe63fb7574157ccc35e608bbd5bfdf8abf1066be464f27d69892`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b7dee627c615685c2303a2dbc10b2afd1739b59831de6371ede912c4ca45c7`  
		Last Modified: Thu, 29 May 2025 22:29:03 GMT  
		Size: 3.5 MB (3500658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d292c112a9108fb846cc33d8ac8a0b8eacc1cede4540350db08fc6b39ddfa612`  
		Last Modified: Thu, 29 May 2025 22:29:02 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5c161f870a30b1d3ab8392e93d196cd6c712192a284a71fffcec146af7260d`  
		Last Modified: Thu, 29 May 2025 22:29:03 GMT  
		Size: 10.9 MB (10853862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80381871fb297258a9dc21e01df1648d1feba3f326aaa9878e556cfcfae9aa27`  
		Last Modified: Thu, 29 May 2025 22:29:03 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:257e6fb7c885509d81a41f0627884ce3dee6d6969eef0f66016e006e51c58cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2410658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6864cd43879b8be2420d85a7a0710fd2e652990beffe098c57cb5dbb7b901c13`

```dockerfile
```

-	Layers:
	-	`sha256:45f4465be2ad73455c38b1c6c13c3f309ebcce7cbd5fe4e5503e8d7c493d77c3`  
		Last Modified: Thu, 29 May 2025 22:29:03 GMT  
		Size: 2.4 MB (2388464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d790788dd86f1e13ae28a2f0b59dc7394f607fd5045b12068f9365fbfe8f85`  
		Last Modified: Thu, 29 May 2025 22:29:02 GMT  
		Size: 22.2 KB (22194 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:94eafe2ff353cf82d94388e15c9b523c1a875af7d95548c8a154936fd2a6a038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39747329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312f59f6fb01461483fa6272e6fd1584afaa7614925e5221bfc76442116e9de0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cec91862f6b0af3546519f4ea28af82d237d43022aaf48b743c0a50d31b1931`  
		Last Modified: Wed, 21 May 2025 23:14:35 GMT  
		Size: 3.1 MB (3074542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ca83a05b3cb93622aded85f3de8d18e78ff62c7fef4218608d087416f1dcc5`  
		Last Modified: Wed, 21 May 2025 23:14:35 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8808c1ee24a6de71541a13830096251365f7c328ec04a8e4a2505087fab7d00b`  
		Last Modified: Thu, 29 May 2025 22:31:11 GMT  
		Size: 10.9 MB (10914250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d71a3950c6c24396f028fe581ad60f1bc6d3f68aaef8d713e1574906292bd45`  
		Last Modified: Thu, 29 May 2025 22:31:11 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:de044146376feb171995c0930667363e16bda8c9cc70c370316d3d2ce0561c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2414629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f937d4d0823aadd125f816611b5ff6ded0985e0d59002e6a429072ab8b112e11`

```dockerfile
```

-	Layers:
	-	`sha256:25a328dd693ea61ee7a4b3aac238feacc9877af2e43ac68d6a536c2ae3c78b44`  
		Last Modified: Thu, 29 May 2025 22:31:11 GMT  
		Size: 2.4 MB (2392302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8d3c4ba3425bc08e0581581a5b8408cc98111fa1a90c5c1a7af33321f0ae4a`  
		Last Modified: Thu, 29 May 2025 22:31:10 GMT  
		Size: 22.3 KB (22327 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:0da06742987e7a0ffdee5c51ccf7e6295415b37f3978592ade7027d3956d59a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37555939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2faab3a4ff4a0d3ef6724150ef7c5a74ede08361785320df71711c63676f238`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99f1fd0040c720090a4a658b14eddcebacfa8e9ceea1496ac57e2d4a4473ba6`  
		Last Modified: Wed, 21 May 2025 23:16:09 GMT  
		Size: 2.9 MB (2910204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49389a80416baa4290cafa447e8be5a444ed0af7ba0590671f07fd1fe15426a4`  
		Last Modified: Wed, 21 May 2025 23:16:09 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4763160e68030f39bd1669f19b10dfe08b545ca78067233c2d0f9e3848742c48`  
		Last Modified: Thu, 29 May 2025 22:32:42 GMT  
		Size: 10.7 MB (10711175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ee4aed9f61c1cff1541737b1068896b71a0da8525bab6b1f7c3e3a14f7677d`  
		Last Modified: Thu, 29 May 2025 22:32:42 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:0bd3f3ccf349e8540ffe2cad5c58b3942d62fdf28d7e95427087ffb792815fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2413051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6bf209c7624227a47c88e070e125ce6a22a2110e18516b98a414830d565293`

```dockerfile
```

-	Layers:
	-	`sha256:678e69e5893c3cb69ec2273af3ffcbafd3afc3a19860c3f003a4eb00da9e99bf`  
		Last Modified: Thu, 29 May 2025 22:32:42 GMT  
		Size: 2.4 MB (2390723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e4aa598f8b3b155debc6977d34ee901e2b30e5358860fd7a21991c2916ac13`  
		Last Modified: Thu, 29 May 2025 22:32:42 GMT  
		Size: 22.3 KB (22328 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:a830b782da9938ed806d1bdc18d8c8ae3f5f29dd86b4ccd5e00add9d59da5ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42220888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747694591fa61a715904672e73b4eac349895cd7f02184ffa6ee488960ed933e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df13b6fc4e7c655d787518b0b76699521ecd89de0249007f51ee7386310c9ccf`  
		Last Modified: Wed, 28 May 2025 17:24:34 GMT  
		Size: 3.3 MB (3324336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278f774c5688e381f585dd1aff7c2af815ffbe405aa7eab1e9e8c037870b3223`  
		Last Modified: Wed, 28 May 2025 17:24:33 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c577509648430b3cdb26730ccf9810209e4bad0b8a249298ba8601fca24063ad`  
		Last Modified: Thu, 29 May 2025 22:30:28 GMT  
		Size: 10.8 MB (10829632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1d5db07886378bec4af9b35e8be232d883c82fbb335f78afe0425667870db3`  
		Last Modified: Thu, 29 May 2025 22:30:27 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:b35a5ddaf07b30efcc8c916b83a73513978caef6100daca4310c4547ede81e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2411147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67a09d89b3283a3682151d5b37b615249c279c676277f93a95317892d465155`

```dockerfile
```

-	Layers:
	-	`sha256:5a9eef6bd535ce4f31297e8e8d436eee41d2abaa6fd4a792e69ba90010c8e2fa`  
		Last Modified: Thu, 29 May 2025 22:30:28 GMT  
		Size: 2.4 MB (2388771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9510280d7edaa403f501b715d3bd8b8d6a981a63145628b10be214bf24c484f7`  
		Last Modified: Thu, 29 May 2025 22:30:27 GMT  
		Size: 22.4 KB (22376 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:4555439defcb8a4af0808b4fdef57b9b399e2cd5ccda2a9c0cd3200ca224e5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43213571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8907d9f133de102787cad2c59b85bd71c0f90f14a0da226d06cd1b57a7495241`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de85962b35e469267cc5f6052d0791228104d49161848756139dd17448aa617`  
		Last Modified: Thu, 29 May 2025 22:29:15 GMT  
		Size: 3.5 MB (3506046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2330469f2f0d5221d7a3f1658cfb198f12e47f6ccc2387c501e0ad6cd1f30b2`  
		Last Modified: Thu, 29 May 2025 22:28:55 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c2348c3bdbd81e8762b2bf105a143803a21cc48dbd89b165921c281e8a79fa`  
		Last Modified: Thu, 29 May 2025 22:29:15 GMT  
		Size: 10.5 MB (10498397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3bd3c222c2f08c7e18ff2e156f7bbb453de5f10661c08d62de11deee9a5b83`  
		Last Modified: Thu, 29 May 2025 22:29:15 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:818139a7d66e7fc03226085cb797d21b2e348d067e743cd448622d471f800bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2407761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e14e6e7391d61601e03a4a4cafcbd1de2b45e2f459707f351087a6dd9511c8c`

```dockerfile
```

-	Layers:
	-	`sha256:af87c328c940d9cd26b6862ea7026e3fc65d9cb79eff7dd8637eaf15aaa76058`  
		Last Modified: Thu, 29 May 2025 22:29:15 GMT  
		Size: 2.4 MB (2385623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fe321f4503726a30122dc5956e784fa55bd8eb9383d815baa0e0b59cd418021`  
		Last Modified: Thu, 29 May 2025 22:29:15 GMT  
		Size: 22.1 KB (22138 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:e4e63193bc88a07b797a20e2d27fdf5302ea38c208ba7bf81b096a8d9db85532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42443360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57eddc098a02fc155e066f51ecd281f6d6a2d71e5ec720d98c559ee07d316432`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Wed, 21 May 2025 22:28:22 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65747dc904d40ad67cb8c68d41158cb757807a395c02b6056d6f2867999d7e7`  
		Last Modified: Wed, 21 May 2025 23:26:50 GMT  
		Size: 2.9 MB (2897333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47714184055b24aa5ffc9f1fd9442891a7266736121baf880538ac4450883b7`  
		Last Modified: Wed, 21 May 2025 23:26:49 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd4fa19c816eaeaed3e1efaf57d35bf4f6413ea343cb63f67d8346e8f1775be`  
		Last Modified: Thu, 29 May 2025 22:38:24 GMT  
		Size: 11.0 MB (11032539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605e5b8d58346fa8ff73d6b0988232f59e7a136e674b4faa9752f5835f61a055`  
		Last Modified: Thu, 29 May 2025 22:38:23 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:336f8f04c4f3dc961e997ed24fc223dcfebbef8f9f3fe9a6de88d115fa53ef4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 KB (22087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296d35c9032d906dacdc055a4545861914e26ba2309e3eaa516136da1dc53409`

```dockerfile
```

-	Layers:
	-	`sha256:95bbb8ba618b573be4cac89d004de0f724cf5395824e92e8a6c42221a93e34eb`  
		Last Modified: Thu, 29 May 2025 22:38:23 GMT  
		Size: 22.1 KB (22087 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:a23b123a9b1b29d1a4442e0b638b3ee4e1bea5e7bf54d099bc85bec9dadbf0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47222598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ae2399cb0b6fb0e0f1dd40fa140c4a2d5d6c0fa5cca89847a25a138312447d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333c23e8b70b76b8ea0de8337d8ad3f29324110bfc586436fb95d2fb99913a45`  
		Last Modified: Wed, 21 May 2025 23:16:22 GMT  
		Size: 3.7 MB (3705099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaf42d45280fc5f18a64f8f5e033381ff53e2d578f85763c8a3d1b242bec66f`  
		Last Modified: Wed, 21 May 2025 23:16:21 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f4520e8c8a817c1276864874a0caa9cfb4660fce6649dc5f9598ecaa906803`  
		Last Modified: Thu, 29 May 2025 22:30:20 GMT  
		Size: 11.4 MB (11448950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd06a125e758c04f882784be82e4d340ba74fd4f90e1390b1579d24d5767f2e2`  
		Last Modified: Thu, 29 May 2025 22:30:19 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:4f6bc5c1bac5e46bb03cda50d11b8f8d054ca03157009b9737b544b74048d835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f52afc6561df83313d7cccb8183cecdb2b7da0310dc936796efc75e5794acc`

```dockerfile
```

-	Layers:
	-	`sha256:2975ae802b3c26e771eefe8a9f71783081904ffb11a47f788ffeb6b715762fd8`  
		Last Modified: Thu, 29 May 2025 22:30:20 GMT  
		Size: 2.4 MB (2392884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30192d02e5047938f3bb74fb71bb5ee7672ecf9d515966a0df1186a1962eb316`  
		Last Modified: Thu, 29 May 2025 22:30:19 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:da75facad212fd0c6f9d3204024122e0830f27e9ccc261d39921e6fa0ac02050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40865017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a507c4cd7179757af2baa1b830e894031e3cf7d318b4a1f6bea18998e01c7fe3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_VERSION=3.2.0
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.0.tar.gz
# Thu, 29 May 2025 11:26:38 GMT
ENV HAPROXY_SHA256=f762ae31bca1b51feb89e4395e36e17f867c25372a10853c70d292c3dd17b7b0
# Thu, 29 May 2025 11:26:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 29 May 2025 11:26:38 GMT
STOPSIGNAL SIGUSR1
# Thu, 29 May 2025 11:26:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 May 2025 11:26:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 May 2025 11:26:38 GMT
USER haproxy
# Thu, 29 May 2025 11:26:38 GMT
WORKDIR /var/lib/haproxy
# Thu, 29 May 2025 11:26:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d7d5016f6fa7406fa5aee32e37a634f773eeeb24cb33a615911aafc2b4ea60`  
		Last Modified: Wed, 21 May 2025 23:15:27 GMT  
		Size: 3.2 MB (3164900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6a4656f73b2a30957e366bdca0a83d815be606b2edad650b7f7b994a7110cd`  
		Last Modified: Wed, 21 May 2025 23:15:27 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72afe95e632183ba2023d8a36664b4493664bf601379c63265a6015dbca2fec2`  
		Last Modified: Thu, 29 May 2025 22:30:27 GMT  
		Size: 10.8 MB (10815671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3364e446b9a889fcd4e2b86bd70214c2fde3b4d0baf96eba72757cfe3df953`  
		Last Modified: Thu, 29 May 2025 22:30:26 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:208ff78170380763f9f9dee2683b7a2e69851fff23be71ddfac55133c85d7829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2410380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ff1473ce4d8a924e62d3b634e966fb71c5d208f20e54ace089e862c6558aa5`

```dockerfile
```

-	Layers:
	-	`sha256:023b5da2c8b092e4a9937243654fbe43f1898ce0ec5ea8aa38ff91413441ff11`  
		Last Modified: Thu, 29 May 2025 22:30:27 GMT  
		Size: 2.4 MB (2388186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf972c83c89b8ec579286752e719732d24684d95a11fabc63236b636926a769a`  
		Last Modified: Thu, 29 May 2025 22:30:26 GMT  
		Size: 22.2 KB (22194 bytes)  
		MIME: application/vnd.in-toto+json
