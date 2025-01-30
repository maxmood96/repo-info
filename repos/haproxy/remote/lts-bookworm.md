## `haproxy:lts-bookworm`

```console
$ docker pull haproxy@sha256:e89d83675fb2e842f747ba7f73a779c34aad2632d22e70f24049ad52fa4f99d8
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

### `haproxy:lts-bookworm` - linux; amd64

```console
$ docker pull haproxy@sha256:fb32cfbb8cac3e247ea6bd9ccb4cd9171881d6fce0b85758c3bebd230dd2c34d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41015793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514a41a58eba3e780916c04c8bee092927a2505a63b0f3367520164b50b69194`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 12 Dec 2024 18:18:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 12 Dec 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
ENV HAPROXY_VERSION=3.0.7
# Thu, 12 Dec 2024 18:18:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Thu, 12 Dec 2024 18:18:23 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Thu, 12 Dec 2024 18:18:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
STOPSIGNAL SIGUSR1
# Thu, 12 Dec 2024 18:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Dec 2024 18:18:23 GMT
USER haproxy
# Thu, 12 Dec 2024 18:18:23 GMT
WORKDIR /var/lib/haproxy
# Thu, 12 Dec 2024 18:18:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d67b1065a98974f5655b0f3ffc7a7e5b39a71626c4bd47935e08710f285111`  
		Last Modified: Tue, 14 Jan 2025 02:16:44 GMT  
		Size: 3.5 MB (3499318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8855209f7173e2a7ed452eae44fee9daf2878a1f3ad14d3fc3b8b45602c76c98`  
		Last Modified: Tue, 14 Jan 2025 02:16:41 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444fc48b92cc4df557fb57bc795773a42900d713f54ab9e9219f23ba91fc6a49`  
		Last Modified: Tue, 14 Jan 2025 02:16:44 GMT  
		Size: 9.3 MB (9302419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4252e78e7e4a97ad84ad47e01a6180c7e2740dd3f8c61d4184b82606fdc1acd5`  
		Last Modified: Tue, 14 Jan 2025 02:16:44 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:384df854abe491046d37d3c3f2fe0aedd4c897a0ed4b46962344bcb7b6c8873f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7beab4b8f2282fb2273ba35e0737f8765ab810ce86ba4b9798f1cfdb64a6c41d`

```dockerfile
```

-	Layers:
	-	`sha256:211126b551142d75d01baea3732ca77653d97d253d1397909cd7d95a4ae56ed0`  
		Last Modified: Tue, 14 Jan 2025 02:16:44 GMT  
		Size: 2.4 MB (2369047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd799840d1cddde2feeb2048d258630799547803eec2c834d8fb151ee46addd7`  
		Last Modified: Tue, 14 Jan 2025 02:16:44 GMT  
		Size: 21.8 KB (21772 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:fb9b2c075daf9bfe32109e715c5565b89f239e722fe370b5d83f909220470984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38159968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada36b161ed11726fe00609d7c005b1943d815e471d320b832080409c42bdf3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 18:21:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Jan 2025 18:21:32 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:21:32 GMT
ENV HAPROXY_VERSION=3.0.8
# Wed, 29 Jan 2025 18:21:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.8.tar.gz
# Wed, 29 Jan 2025 18:21:32 GMT
ENV HAPROXY_SHA256=930ae2c33058e1f497fe62cdaacffab6cab6a91e31ba011a9a2f9fe6c5c4aebc
# Wed, 29 Jan 2025 18:21:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:21:32 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:21:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:21:32 GMT
USER haproxy
# Wed, 29 Jan 2025 18:21:32 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:21:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13cab84d28620a7a08021a20ad2ffc76f921f7e124b546f8caefddd64d8d572`  
		Last Modified: Tue, 14 Jan 2025 02:19:10 GMT  
		Size: 3.1 MB (3073438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347acb2bab2b92056a6d75c784e5cffb8e14a0a97a5f293450554d7152b652e2`  
		Last Modified: Tue, 14 Jan 2025 02:19:09 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cc2fbcab5f57674b22b107ef621de87c750914f7440f8ddadd87aae2fae2bf`  
		Last Modified: Wed, 29 Jan 2025 23:28:49 GMT  
		Size: 9.3 MB (9348224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c561d97b19fbe5dd486f91914cbd66f148c15d69d2a62eafb0052a02fa12cbbf`  
		Last Modified: Wed, 29 Jan 2025 23:28:48 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:d5ef0759fa9affdaa5b2a42e4a14945aeb4bb2dc422007d25d7c3e6449b0d423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2394451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3321d18c768c887f075bafc0c51b84fbf7e61baa998ccc37514628e97b15a575`

```dockerfile
```

-	Layers:
	-	`sha256:7afec61f1e5fe60e0c5f7d53cd1b87cbc3c25ac7be2567a14a2c3d4a6493f52f`  
		Last Modified: Wed, 29 Jan 2025 23:28:49 GMT  
		Size: 2.4 MB (2372561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f113847aeb8c6f7f7e40571244df92b931372c8dcf2e9d180ad06260412bfc4c`  
		Last Modified: Wed, 29 Jan 2025 23:28:48 GMT  
		Size: 21.9 KB (21890 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:a9cb3f220f6c1a661abdcd59eb79130937e77ec8c45c140b0a80a93829bb95c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35907923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e0271685b69c24596eb5d3f5f6cd8cd2c02fa98a6d8cd4a214310abe8e5069`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 12 Dec 2024 18:18:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 12 Dec 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
ENV HAPROXY_VERSION=3.0.7
# Thu, 12 Dec 2024 18:18:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Thu, 12 Dec 2024 18:18:23 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Thu, 12 Dec 2024 18:18:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
STOPSIGNAL SIGUSR1
# Thu, 12 Dec 2024 18:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Dec 2024 18:18:23 GMT
USER haproxy
# Thu, 12 Dec 2024 18:18:23 GMT
WORKDIR /var/lib/haproxy
# Thu, 12 Dec 2024 18:18:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b2605eec1dd682d8c37895db5b3efd941d9675d834c2c26917caf3dd8668a7`  
		Last Modified: Tue, 14 Jan 2025 02:21:35 GMT  
		Size: 2.9 MB (2907790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312571f07e47f0b85563d7245f56f68d3f119e36dbe459d1fa3d77f999f576de`  
		Last Modified: Tue, 14 Jan 2025 02:21:35 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5060997b1badcd48886c4ecee37a300f1d8bec1b162d8c4fcbd3cfb180b4cf`  
		Last Modified: Tue, 14 Jan 2025 02:23:57 GMT  
		Size: 9.1 MB (9083894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e8264cadd812b4aad7d0c42e475f66039e5aba90f53bfbc53e178cc19b2698`  
		Last Modified: Tue, 14 Jan 2025 02:23:57 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:32086fa6e8cc423b3e643ec97c8842abb99c164262703142c5d72bdda34f596b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8115ff9cdc730ad482cf0cfe945ce7da07c5e23b6203b679b6389b1eb0e912`

```dockerfile
```

-	Layers:
	-	`sha256:0fc356ded65fd63304d1fcb79ffbd7a2729986c434735b36f1e737d105ee7d93`  
		Last Modified: Tue, 14 Jan 2025 02:23:57 GMT  
		Size: 2.4 MB (2371290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1c339c60cf5c8cb1bce4e6fe8e9ea03c7f3de6b3835923745922664a560190f`  
		Last Modified: Tue, 14 Jan 2025 02:23:57 GMT  
		Size: 21.9 KB (21890 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:6257daffeaf18c3bf30f82c59814b5c8dd87540653d7484a71bb2b27fb57321a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40647468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf503b053ddd65991fab890dd3727d8a6f3ee1da1e80835b78778e8edd9011eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 12 Dec 2024 18:18:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 12 Dec 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
ENV HAPROXY_VERSION=3.0.7
# Thu, 12 Dec 2024 18:18:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Thu, 12 Dec 2024 18:18:23 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Thu, 12 Dec 2024 18:18:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
STOPSIGNAL SIGUSR1
# Thu, 12 Dec 2024 18:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Dec 2024 18:18:23 GMT
USER haproxy
# Thu, 12 Dec 2024 18:18:23 GMT
WORKDIR /var/lib/haproxy
# Thu, 12 Dec 2024 18:18:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7b0e6036e799ed5b09bd0cd29b73303adf595f85e5bcc329db7f53d3096c1a`  
		Last Modified: Tue, 14 Jan 2025 02:28:13 GMT  
		Size: 3.3 MB (3322877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3616c13f0ae03b4667ff114759560d5f2bf0f9ce7a42468a64f52fea448195`  
		Last Modified: Tue, 14 Jan 2025 02:28:12 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3e5b23cc3670fe8f971d362b535a8ac6116e9c052a3e0b5d096de663e29d3a`  
		Last Modified: Tue, 14 Jan 2025 02:29:55 GMT  
		Size: 9.3 MB (9281920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f9de17b1b07ae75ce95f1733bcf0c931379a56696dd3e5b431a99cd715263c`  
		Last Modified: Tue, 14 Jan 2025 02:29:54 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:91f4cc9e61b40819bb588678287eb46e805a1306e0a1df750527dd96d4586e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2391260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da11e4ba49be7e792d703e615fa7b870c409c31737c042a65769f5d0021a4539`

```dockerfile
```

-	Layers:
	-	`sha256:64b817056b9fa9e6b1052542cf2fd3ac113e3e81b1e3db9b3c6b24b76842cb70`  
		Last Modified: Tue, 14 Jan 2025 02:29:55 GMT  
		Size: 2.4 MB (2369330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a17408dde6cdc76bbd7397310636c0e24a8a9125233d7cf807e75c46f3b1bf`  
		Last Modified: Tue, 14 Jan 2025 02:29:54 GMT  
		Size: 21.9 KB (21930 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:cba22009ac9b5c576ecc605b6cd755014baaadcdb66b977059f0bbdf5b9c45be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41750173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a238543442391bf35c4dae1b4244dbfe2e87390316424e7467390c2774059d1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 12 Dec 2024 18:18:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 12 Dec 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
ENV HAPROXY_VERSION=3.0.7
# Thu, 12 Dec 2024 18:18:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Thu, 12 Dec 2024 18:18:23 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Thu, 12 Dec 2024 18:18:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
STOPSIGNAL SIGUSR1
# Thu, 12 Dec 2024 18:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Dec 2024 18:18:23 GMT
USER haproxy
# Thu, 12 Dec 2024 18:18:23 GMT
WORKDIR /var/lib/haproxy
# Thu, 12 Dec 2024 18:18:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40973c8c0fe0513ecc3090a549fca9fc3505ba13040f0027ef09ff2b38c7abc6`  
		Last Modified: Tue, 14 Jan 2025 02:16:48 GMT  
		Size: 3.5 MB (3503440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ca33c53d74f6463595c6c1f782b805241b3c4f85b23ce004481c5c8a326382`  
		Last Modified: Tue, 14 Jan 2025 02:16:48 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c608c33976c672ca41d33d86e2426f4f6d60b1535147e2e8f60280b06f0781`  
		Last Modified: Tue, 14 Jan 2025 02:16:49 GMT  
		Size: 9.1 MB (9057500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c68aa633b714d295a1551ace55e558d0487bfdba0da7a6ef3c9e945c5de7323`  
		Last Modified: Tue, 14 Jan 2025 02:16:48 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:258ffd37198a9c5b869532d6c06ed3f74edd7b72ff176b77f625b6b45a59ee24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f9f2e54164b32805fac63f9c15c264e63989170d759b2b748705509040d924`

```dockerfile
```

-	Layers:
	-	`sha256:2693efb72d85705ae1b5d0435a6447ef31dcfa1165d120fae917c32abaf5fd32`  
		Last Modified: Tue, 14 Jan 2025 02:16:48 GMT  
		Size: 2.4 MB (2366175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:171fb858a95c53f7a32ac42052edcc1c3f1f19c3e47de1afc726a166c0208548`  
		Last Modified: Tue, 14 Jan 2025 02:16:48 GMT  
		Size: 21.7 KB (21726 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:bbca0b4306a4bf600857ae1123b71ba9247c0cc54e5e2c1fa9784acd19623b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40878731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6964608699cf6d306dba4a0f8b4aa10acf91d6ef534432df4dfeb4614bbe6e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 18:21:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Jan 2025 18:21:32 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:21:32 GMT
ENV HAPROXY_VERSION=3.0.8
# Wed, 29 Jan 2025 18:21:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.8.tar.gz
# Wed, 29 Jan 2025 18:21:32 GMT
ENV HAPROXY_SHA256=930ae2c33058e1f497fe62cdaacffab6cab6a91e31ba011a9a2f9fe6c5c4aebc
# Wed, 29 Jan 2025 18:21:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:21:32 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:21:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:21:32 GMT
USER haproxy
# Wed, 29 Jan 2025 18:21:32 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:21:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee81822f69876da1e9c9b593b95f8643321ed94fb5b99c1066f245cab214fe9`  
		Last Modified: Tue, 14 Jan 2025 02:28:04 GMT  
		Size: 2.9 MB (2895367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6baa679cb4b900d271d63935f647962d397fb609bac90d5b455c09d82315cb1`  
		Last Modified: Tue, 14 Jan 2025 02:28:03 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60db59a4f1f540950c41548255d89953429e420bac356fde6332b81c7de18bb1`  
		Last Modified: Wed, 29 Jan 2025 23:36:35 GMT  
		Size: 9.5 MB (9495074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dcf73a3e4014a7522077d704efb38d13759e6f06579ac0752b0bf881cca48f`  
		Last Modified: Wed, 29 Jan 2025 23:36:34 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:ba12833c7ffe1fbb93a9383f77911fceb7c89c1ebf2bee1e827dc9f8d32f23c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75923e9da4d512e776115d9e02e335116dfb2f7ce393d374d4325ddebba7fdd2`

```dockerfile
```

-	Layers:
	-	`sha256:4206551c6c41cdfeb108cfe7787c888b482cc1b8cf26852724d1b42473ae5359`  
		Last Modified: Wed, 29 Jan 2025 23:36:33 GMT  
		Size: 21.6 KB (21647 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:c333e92aa590af2ca6e7ffbac9cd4531b8237e249836257bdcd687b8944831d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45629650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895566d5da8ad50cf446aa07f48da92c1ecab33392bf49f69ecab33617b3fc3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 18:21:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Jan 2025 18:21:32 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 29 Jan 2025 18:21:32 GMT
ENV HAPROXY_VERSION=3.0.8
# Wed, 29 Jan 2025 18:21:32 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.8.tar.gz
# Wed, 29 Jan 2025 18:21:32 GMT
ENV HAPROXY_SHA256=930ae2c33058e1f497fe62cdaacffab6cab6a91e31ba011a9a2f9fe6c5c4aebc
# Wed, 29 Jan 2025 18:21:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 29 Jan 2025 18:21:32 GMT
STOPSIGNAL SIGUSR1
# Wed, 29 Jan 2025 18:21:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 29 Jan 2025 18:21:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Jan 2025 18:21:32 GMT
USER haproxy
# Wed, 29 Jan 2025 18:21:32 GMT
WORKDIR /var/lib/haproxy
# Wed, 29 Jan 2025 18:21:32 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af6431e87310d9ff734faa158ee99941b74aa8629f2f87fcd4f4eeb65549cc7`  
		Last Modified: Tue, 14 Jan 2025 02:43:11 GMT  
		Size: 3.7 MB (3702910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab19ef049110189d6410acbf925b3c6ac46ff4264affba93cf10253cdd61c77`  
		Last Modified: Fri, 24 Jan 2025 19:29:07 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c83c7a49fcda991cd0ede80b3ad9f062983b05fff3f6429e20ada47abc1a382`  
		Last Modified: Wed, 29 Jan 2025 23:30:28 GMT  
		Size: 9.9 MB (9880252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb1fa28b9b27491553c9aaf76200c23a9ed5760a68db897c9248abec06d999`  
		Last Modified: Wed, 29 Jan 2025 23:30:27 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:6e4905c98f20a8dac99fc53790d716260d747b510cc970524056f5f071935c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39eab79ce903abcee7584c60ca2643f9c878212a267c5abab91b2b428ef7023b`

```dockerfile
```

-	Layers:
	-	`sha256:9e2fb97698f2e3fac788e5f58deadb84a3836af5162d023d12e8a89214b423c3`  
		Last Modified: Wed, 29 Jan 2025 23:30:28 GMT  
		Size: 2.4 MB (2373361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef728071f4cfcf17d75096bd4b87fb35be9a9383caabdb9c597dcc0b5f6ea74`  
		Last Modified: Wed, 29 Jan 2025 23:30:27 GMT  
		Size: 21.8 KB (21832 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:23f9ec4a2d077442aeb28b091ccbd0e152c7ac6d627d06bd45509ca39bbca9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39184218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102cd8b4d85eded53e9e1481a476835aaee89800cb612cfebade1c93b39f40ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 12 Dec 2024 18:18:23 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 12 Dec 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
ENV HAPROXY_VERSION=3.0.7
# Thu, 12 Dec 2024 18:18:23 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.7.tar.gz
# Thu, 12 Dec 2024 18:18:23 GMT
ENV HAPROXY_SHA256=5c5c6b66645278435a89cd6e2a0d39f8e7d2546212d847bd0d236511ff996f11
# Thu, 12 Dec 2024 18:18:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
STOPSIGNAL SIGUSR1
# Thu, 12 Dec 2024 18:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 18:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Dec 2024 18:18:23 GMT
USER haproxy
# Thu, 12 Dec 2024 18:18:23 GMT
WORKDIR /var/lib/haproxy
# Thu, 12 Dec 2024 18:18:23 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed175806a9965adb498bef3a953ad655c07286b45f574660a8685b6d96c01059`  
		Last Modified: Tue, 14 Jan 2025 02:33:53 GMT  
		Size: 3.2 MB (3163307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f309c1cf5d1c825591e3bfa7b759cc496b30d5c71dbc2f8f838946447cddcf2e`  
		Last Modified: Tue, 14 Jan 2025 02:33:53 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1518eb83bf5f5dcd838a560e52a7fc1579faeeb86ab0030a80a1f95167f176b8`  
		Last Modified: Tue, 14 Jan 2025 02:36:20 GMT  
		Size: 9.2 MB (9160533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5b6b49c99b125b7b6ea45ae820f3cfbfee4a642d6d49b2143b742590d4c2ab`  
		Last Modified: Tue, 14 Jan 2025 02:36:20 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:160ac7cd9ad4c6f055c829b12dd9c7e111e1d998126f3b4b829d1150b0107922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b1b2a3b220d3436febe205e06789d7656c4af19b4d9fde63b89ab5b6533cce`

```dockerfile
```

-	Layers:
	-	`sha256:fadd9e9b2c8895d8ae7fc6e0766c61a22d3d8ec2a8484e9441fed09c59f70efd`  
		Last Modified: Tue, 14 Jan 2025 02:36:20 GMT  
		Size: 2.4 MB (2368769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44ec66fe0e2c471482e7529d78c76c7dcfa92f5ebe9bfcebb0519641b40dff5`  
		Last Modified: Tue, 14 Jan 2025 02:36:20 GMT  
		Size: 21.8 KB (21772 bytes)  
		MIME: application/vnd.in-toto+json
