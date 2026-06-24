## `haproxy:lts`

```console
$ docker pull haproxy@sha256:acaca248b45b4fec19914c2215789ecec6d629ab1d867ce65af83762ed781c2c
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

### `haproxy:lts` - linux; amd64

```console
$ docker pull haproxy@sha256:f33aa735d7a88d2c3dbb16a443f43bd50d6c3e3c2ec19b06b91c3dd35360bc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47061858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c355ec3fc9629617a21e9d9b50ce418a2b1bdf00e8c8c8166575604e29dd7c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:15:18 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:15:18 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 24 Jun 2026 01:16:08 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 24 Jun 2026 01:16:08 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 24 Jun 2026 01:16:08 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 24 Jun 2026 01:16:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 24 Jun 2026 01:16:08 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Jun 2026 01:16:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:16:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:16:08 GMT
USER haproxy
# Wed, 24 Jun 2026 01:16:08 GMT
WORKDIR /var/lib/haproxy
# Wed, 24 Jun 2026 01:16:08 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bbd11fc85ace5bcb653fd3d98a49ccf3774f57be6b71d501bdb3bd6b12f28a`  
		Last Modified: Wed, 24 Jun 2026 01:16:16 GMT  
		Size: 1.6 MB (1581257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8510c6e8abedf09b8a0330bcbc088eb0f951fb6a6d3c972bbfb2204902ec823f`  
		Last Modified: Wed, 24 Jun 2026 01:16:16 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12284231b1971ba5dbde9b3af36dbad7a81253550bbd51ea8da22d5e581c5902`  
		Last Modified: Wed, 24 Jun 2026 01:16:16 GMT  
		Size: 15.7 MB (15693546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94b95c9dcb73480026be40a882e9388688ec8d7b3503c154b8cf2a11d144ec2`  
		Last Modified: Wed, 24 Jun 2026 01:16:15 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:4920536457ad3676a3f71d8db87f366228efd20813b797d474b9262b458e8eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5f98112468a673cce3aef40e6c5c80019a71c428842343bc06ba5ac7bfabb0`

```dockerfile
```

-	Layers:
	-	`sha256:4ea7dda37114b9ab9999779bdd9e2c1f5ce6ba9bd3c5622f5324736e331f74a2`  
		Last Modified: Wed, 24 Jun 2026 01:16:16 GMT  
		Size: 2.1 MB (2114442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b193665336fe26ac7afcc20c4477214851b268d6fadf05bd73e5054d475bb2f7`  
		Last Modified: Wed, 24 Jun 2026 01:16:16 GMT  
		Size: 22.9 KB (22940 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:cb94fe2003065b095912c5eb05ddce233499c5936fda4c496a92412a5b2f3daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45402649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54b0b062ace64ec7996f87a17aab4cffb77bb732bf6fe61069e50532765280f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:14:48 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:14:48 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 24 Jun 2026 01:15:53 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 24 Jun 2026 01:15:53 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 24 Jun 2026 01:15:53 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 24 Jun 2026 01:15:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 24 Jun 2026 01:15:53 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Jun 2026 01:15:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:15:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:15:53 GMT
USER haproxy
# Wed, 24 Jun 2026 01:15:53 GMT
WORKDIR /var/lib/haproxy
# Wed, 24 Jun 2026 01:15:53 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:da43bc6a07a9cd7cc23faa538adc0797482747316b5a85b9f3f94ed17f6c1a2a`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 28.0 MB (27959221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279d54ac64349f0fdac05b76b5fd0d878568637ad8181bdec7eca3915277044a`  
		Last Modified: Wed, 24 Jun 2026 01:16:01 GMT  
		Size: 1.5 MB (1535895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a172502228448602d224ad081ea0173efdc060fa23ff6aab92cd26b7f49c8f7`  
		Last Modified: Wed, 24 Jun 2026 01:16:01 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22bb01ced3f405349daff01e538cf95a2ea883ca9fbfa27231b54a10df289ae`  
		Last Modified: Wed, 24 Jun 2026 01:16:02 GMT  
		Size: 15.9 MB (15905894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd9d09374acd94abfcc1d964ad719edd2ab54e3cbe1ee3c67ac98d434e73801`  
		Last Modified: Wed, 24 Jun 2026 01:16:01 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:bb3f38b329c923f75d7e69edae3333252c0775d9759c75ef0d935b96af522027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0a44cdb5462a505856673009808663a8284c9302e0de083b97882088f1001b`

```dockerfile
```

-	Layers:
	-	`sha256:051f2dd656b180e1279dc34b50c823097fd52668e21f4eb7c7d06804ce091dc2`  
		Last Modified: Wed, 24 Jun 2026 01:16:01 GMT  
		Size: 2.1 MB (2117438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:712a2b6f6c9b02bc284117b16331b384f1390c2486616d6ea1fc8c5c4c734b51`  
		Last Modified: Wed, 24 Jun 2026 01:16:01 GMT  
		Size: 23.1 KB (23078 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:9caa65079017ea4f375fe4d28244065364dbe7640d92d189b2fa7592b827f8d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43391460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3aa0a8a53c8fbbe43c0a5b9d15b1bd6ce81150455bd3c44d74e75fdc26a0db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:15:36 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:15:36 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 24 Jun 2026 01:16:29 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 24 Jun 2026 01:16:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 24 Jun 2026 01:16:29 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 24 Jun 2026 01:16:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 24 Jun 2026 01:16:29 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Jun 2026 01:16:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:16:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:16:29 GMT
USER haproxy
# Wed, 24 Jun 2026 01:16:29 GMT
WORKDIR /var/lib/haproxy
# Wed, 24 Jun 2026 01:16:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979f6941f8fae94ea57d0362b2809f1e12f6a6274b02b7a704d9344bc8b04696`  
		Last Modified: Wed, 24 Jun 2026 01:16:37 GMT  
		Size: 1.5 MB (1489619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40640a8fdce540de80e7924089b2170c972309250b04119b223a06700fd3226d`  
		Last Modified: Wed, 24 Jun 2026 01:16:37 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a969f4dadc8b8e01c8d59aa4231cefe87917b2bbc06347323b27f6b6cead68a8`  
		Last Modified: Wed, 24 Jun 2026 01:16:37 GMT  
		Size: 15.7 MB (15689154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b6e19f9a47a69f91e80180e3ae99719d38e2238dd995cb013a14f7f6b8304d`  
		Last Modified: Wed, 24 Jun 2026 01:16:37 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:646d0c2f6801da18c6adf1f3af99ecbbcd6a26c3628a9ef5824b7d87937f6b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f458c93d6553c1fc9c5257cd4ef102d7a355c61a3f9e69d002b03ee47f573b56`

```dockerfile
```

-	Layers:
	-	`sha256:ff80119628f3fd4d1a38a84c738842fbbcdeb6d63c54b8a7ca6e3abba51f1976`  
		Last Modified: Wed, 24 Jun 2026 01:16:37 GMT  
		Size: 2.1 MB (2115881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c74f718934a5d788438f6fe402b29487571c9bddd92806eb02884e4f2a19a86`  
		Last Modified: Wed, 24 Jun 2026 01:16:37 GMT  
		Size: 23.1 KB (23078 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:f1b3d66bf725c60cea37525f0db04826e8fdaf01cfe42bdd20536a85530dcbd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47277565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84414496716260766424d9aa60157f04d6c9ee81720a97f88b9b1efac4d5e4ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:15:31 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:15:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 24 Jun 2026 01:16:20 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 24 Jun 2026 01:16:20 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 24 Jun 2026 01:16:20 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 24 Jun 2026 01:16:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 24 Jun 2026 01:16:20 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Jun 2026 01:16:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:16:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:16:20 GMT
USER haproxy
# Wed, 24 Jun 2026 01:16:20 GMT
WORKDIR /var/lib/haproxy
# Wed, 24 Jun 2026 01:16:20 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6354740a92261e9d44345f38fc9e1fc0fc549e5fc93cfaf5ba09e7292a9962ac`  
		Last Modified: Wed, 24 Jun 2026 01:16:29 GMT  
		Size: 1.6 MB (1563939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502e1459d8b2d75c2b41526915b4c1100a0ca3fe74ecddc665f743c45613ff0f`  
		Last Modified: Wed, 24 Jun 2026 01:16:12 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771b9535f8a29a280cfd549c95a09290ccabddea356a5ccc98acf55379aae5b3`  
		Last Modified: Wed, 24 Jun 2026 01:16:29 GMT  
		Size: 15.6 MB (15563436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f63e2719f3307bbb183fe51bc4919b734993870b3bab81b0af384c630c72b5`  
		Last Modified: Wed, 24 Jun 2026 01:16:29 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:645490fac601dbdf1a6ff6a43bfc7d8d5b056b16c46558de11f2f06aa2cad607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2b091ef9d5d15d88c6face10d1a055dbb309259faeacc5f650c1a22203fca6`

```dockerfile
```

-	Layers:
	-	`sha256:48431aa12b13e26b6e0920fa88370c659f059da5a5a3a70bd58dbab4111fb057`  
		Last Modified: Wed, 24 Jun 2026 01:16:29 GMT  
		Size: 2.1 MB (2114743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4c9da6ac40bc86c41510ce41c57ce71e2fe071592d3e84fd66f0af019e46499`  
		Last Modified: Wed, 24 Jun 2026 01:16:29 GMT  
		Size: 23.1 KB (23122 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:eaae9021278c09cf9738ce3a6515f0575fde408512d084f212a63fde428609ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48361168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1816447eadbb3525fd297e214e140db72958f43be07bb84be3eb06ccc99daf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:16:05 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:16:05 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 24 Jun 2026 01:17:00 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 24 Jun 2026 01:17:00 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 24 Jun 2026 01:17:00 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 24 Jun 2026 01:17:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 24 Jun 2026 01:17:00 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Jun 2026 01:17:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:17:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:17:00 GMT
USER haproxy
# Wed, 24 Jun 2026 01:17:00 GMT
WORKDIR /var/lib/haproxy
# Wed, 24 Jun 2026 01:17:00 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6e148aa3e8df3dc6e131bb70ee8600bde5b59312f78d5b8d7da8840e20705f`  
		Last Modified: Wed, 24 Jun 2026 01:17:08 GMT  
		Size: 1.6 MB (1603756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14b50b005ff2e897fb8525be32839afd32093aa5d9a2ca20d90c310341d1f16`  
		Last Modified: Wed, 24 Jun 2026 01:17:08 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52b6156e13d9db83d5b3db6d66aa1cd3f228c90dbda6598bfc3e651ebb1427a`  
		Last Modified: Wed, 24 Jun 2026 01:17:09 GMT  
		Size: 15.5 MB (15454560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b47fa4f14269a9597e56520cf32dc6beccd9bdf6c7d0f07039a6f48395546ba`  
		Last Modified: Wed, 24 Jun 2026 01:17:08 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:563a99ec51380f9d5f031f7720562f6553443b0bdc1aa26c1ad898b227d09355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f4759c104455c3c2b9a57c605f6b41894084fe3a1410147030c948f83ca31a`

```dockerfile
```

-	Layers:
	-	`sha256:f82445f49068b1c4c8ee539562dcd66da71b7487b4d2236acbf407974d39f956`  
		Last Modified: Wed, 24 Jun 2026 01:17:08 GMT  
		Size: 2.1 MB (2111613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca7492c5717227799df5582c5faf1d53852dbb15ab08ec83ad81ee3211aa3320`  
		Last Modified: Wed, 24 Jun 2026 01:17:08 GMT  
		Size: 22.9 KB (22884 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:6906f352b68135b71aeb98b8c0b9f4af7fc0db68b81af3b59694b177407d9a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6c651b4d3009c0ffac20cd5fba1242b645e039504aff8d9fc7c27ec9a085dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:16:32 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:16:33 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 24 Jun 2026 01:18:28 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 24 Jun 2026 01:18:28 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 24 Jun 2026 01:18:28 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 24 Jun 2026 01:18:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 24 Jun 2026 01:18:28 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Jun 2026 01:18:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:18:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:18:28 GMT
USER haproxy
# Wed, 24 Jun 2026 01:18:28 GMT
WORKDIR /var/lib/haproxy
# Wed, 24 Jun 2026 01:18:28 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdf48770d2ce4f6d2ec7fdca2214c67bee013812202b7495a65f8975916b4cb`  
		Last Modified: Wed, 24 Jun 2026 01:18:45 GMT  
		Size: 1.6 MB (1639536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f20c5b6c932d79067aaf227b5db380011b0983b51497f83f05ba19c64c6c68`  
		Last Modified: Wed, 24 Jun 2026 01:18:44 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5223577ebc1ba03a41082b90856a195c7cc39389789671c0b9b38113f2858e7`  
		Last Modified: Wed, 24 Jun 2026 01:18:45 GMT  
		Size: 16.5 MB (16452373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6c9959cf6b0a62088ffd6b8ce799ff018b3a9c0367355360c8033e915ae77a`  
		Last Modified: Wed, 24 Jun 2026 01:18:45 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:c97d2d258ecbeefaee16f4cbe40b188c0f3d5861ada10efa14ad4018ac90971b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2141012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5254ab5cf3dad2487ccc2a130b90e133ba389297af6a3cdd4f848ac36e09cf`

```dockerfile
```

-	Layers:
	-	`sha256:94ca47b4c2357b6c841367eb6673a7bd12d9991d2b77e2c509f9518bed71a229`  
		Last Modified: Wed, 24 Jun 2026 01:18:45 GMT  
		Size: 2.1 MB (2118000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250c0329caff90dd1243dc48fb173ab4f07c8dcdca00ac16f355de54b2508d48`  
		Last Modified: Wed, 24 Jun 2026 01:18:45 GMT  
		Size: 23.0 KB (23012 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; riscv64

```console
$ docker pull haproxy@sha256:d31b31f2798fff52d1bacbe250dec8d9fd6677167c0b01652c2c9de64c21a45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44932279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7556da78888a6d2289c68da0c7dc53204604342d6fb1a65720d958ec434ce74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 18:43:54 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 18:43:54 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 24 Jun 2026 18:59:38 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 24 Jun 2026 18:59:38 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 24 Jun 2026 18:59:38 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 24 Jun 2026 18:59:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 24 Jun 2026 18:59:38 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Jun 2026 18:59:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 18:59:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 18:59:38 GMT
USER haproxy
# Wed, 24 Jun 2026 18:59:38 GMT
WORKDIR /var/lib/haproxy
# Wed, 24 Jun 2026 18:59:38 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37465baa1f8cdf556a89cc741727534d7616ce29ccd10dc3358664061d0bfa9a`  
		Last Modified: Wed, 24 Jun 2026 19:00:49 GMT  
		Size: 1.5 MB (1535641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c59c90bab2f81d28789abcfb722db18b66d9294f43e5afa2290cd87e1e4cab6`  
		Last Modified: Wed, 24 Jun 2026 19:00:48 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26032648d534b9f146126d99d32dc0e20ef5501d5f1e46478d5fb6084e1838c7`  
		Last Modified: Wed, 24 Jun 2026 19:00:51 GMT  
		Size: 15.1 MB (15112617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7460e74f5de4126030e28113059845dc55ad2eccd696c796486fe6cc693af095`  
		Last Modified: Wed, 24 Jun 2026 19:00:49 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:0e8e6ece0c26b83bc1a101e8c679b3afbd0b628248f29d8b31ca4698368b0a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2131403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92999d7308217356285f2fabdd4e30e9f2737c1a905a20acdde8f38527c1c1a`

```dockerfile
```

-	Layers:
	-	`sha256:b57d89263d34673bfb203795184552389c3d074e619d1fd35bedffca7e1d9578`  
		Last Modified: Wed, 24 Jun 2026 19:00:49 GMT  
		Size: 2.1 MB (2108391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91206db89814d44e084f4f94ed84139fb5457ba67c3e0c9c235df96e828d21a3`  
		Last Modified: Wed, 24 Jun 2026 19:00:49 GMT  
		Size: 23.0 KB (23012 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:e6db09b7246c84dba63a86e475c984ab458cd28e21f530efade3448e80b80084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47546842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466e12ba061897aae43211f521903dda3e3fbe44b14372ad76802770e976ee0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:14:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		socat 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:14:58 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 24 Jun 2026 01:16:22 GMT
ENV HAPROXY_VERSION=3.4.0
# Wed, 24 Jun 2026 01:16:22 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.4/src/haproxy-3.4.0.tar.gz
# Wed, 24 Jun 2026 01:16:22 GMT
ENV HAPROXY_SHA256=9298f565c2a9ba8a4e7f89c54be2c5d3fd960b5b304eb5515e15d29d2c15d4f7
# Wed, 24 Jun 2026 01:16:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 		USE_PTHREAD_EMULATION=1 		USE_QUIC=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Wed, 24 Jun 2026 01:16:22 GMT
STOPSIGNAL SIGUSR1
# Wed, 24 Jun 2026 01:16:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:16:22 GMT
USER haproxy
# Wed, 24 Jun 2026 01:16:22 GMT
WORKDIR /var/lib/haproxy
# Wed, 24 Jun 2026 01:16:22 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571fe387244ece97a67132849be88945ea722f7cf59012e29a90cfeb8be37cab`  
		Last Modified: Wed, 24 Jun 2026 01:16:32 GMT  
		Size: 1.6 MB (1600048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943b6aaf775d0d4d265485a3b1df8a681a624169b326101b832c46f2aeaf75e9`  
		Last Modified: Wed, 24 Jun 2026 01:16:32 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de283bc063e438a96d3d3be11afa03aa315876155af63b69e1ac447e954e21d`  
		Last Modified: Wed, 24 Jun 2026 01:16:35 GMT  
		Size: 16.1 MB (16093773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1ddfb9b194f588354671adc2c95e9fefec0836a11c03f2cbe4dda138c77136`  
		Last Modified: Wed, 24 Jun 2026 01:16:34 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:015e2bb6597b10c047951005fd75d9b0c16a097a28ce954ae218402a7597f8b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2f66dbf677270c69d73e9fbcecfba8949cd4ef1892da4e1fc42badaacd8e67`

```dockerfile
```

-	Layers:
	-	`sha256:22e99b3237e2b77c12ce113b3a85f6d24baacd49bf49276dae219d15b1014b99`  
		Last Modified: Wed, 24 Jun 2026 01:16:34 GMT  
		Size: 2.1 MB (2115886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:691ce93aa989bc6561ad9b057ab6cb1c2f11ea8ce3faff0a17698d212327a77c`  
		Last Modified: Wed, 24 Jun 2026 01:16:34 GMT  
		Size: 22.9 KB (22940 bytes)  
		MIME: application/vnd.in-toto+json
