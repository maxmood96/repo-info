## `haproxy:lts`

```console
$ docker pull haproxy@sha256:554cce99b717c92c31cb3342a401235909c3b4b189a1411428d85d237b175a73
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

### `haproxy:lts` - linux; amd64

```console
$ docker pull haproxy@sha256:c50828e058d86093bae8e9f2652462fc2a138863e77d5f8e6ea71c37b71a3db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41101801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a32e1aeff8aee8ef797afa49f0f45b12bcb266acdf0a30270a727577bc9aa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebbcc63a98169da1b40115289702ed0c5767fe9143a2ba649a75e22b6758052`  
		Last Modified: Thu, 20 Mar 2025 17:53:37 GMT  
		Size: 3.5 MB (3499306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83732d6b3583faeaf8884a087b7a6e4269e53e60f3bb16b2431edb671f926f6`  
		Last Modified: Thu, 20 Mar 2025 17:53:36 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deb7fce41040fc0eaa38b981b4df242798b53d5c450a1846ac450884e8da83a`  
		Last Modified: Thu, 20 Mar 2025 17:53:37 GMT  
		Size: 9.4 MB (9395992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe5cd90448dd3b5c76513c52d9b042dfcd0722d516622722cc55c3b0f227d78`  
		Last Modified: Thu, 20 Mar 2025 17:53:37 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:9e25fa1abe52e4dd9d0e0d5069e15ed32fc0f4c088209a3d523b50961abc99b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535edd0e30a0ff48ae44b23856e909d68f615436bbd2eff4451ad0e0a3cd67ab`

```dockerfile
```

-	Layers:
	-	`sha256:5f195532ded0ef2a947f065696281f75f5855bf3704ded8fbcf7ddbcb1594984`  
		Last Modified: Thu, 20 Mar 2025 17:53:37 GMT  
		Size: 2.4 MB (2369073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ced8991b27a5b3ee1279187a150e2e66f5d16645105551aecabfe51056c01a4e`  
		Last Modified: Thu, 20 Mar 2025 17:53:37 GMT  
		Size: 21.8 KB (21772 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:d4f4e08af37be721a6ac381bbca7db050618c55934b6d6007020d4d459649c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38165482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0503ccf93ceddc151dcb894e3af1d4bcde1a1497c1393b54e7ef5cdd51829c17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a06bf00a22e98835898fabeb6f4b4e688d5e3dd40a63cf933c7a8f01f50907`  
		Last Modified: Mon, 17 Mar 2025 23:15:23 GMT  
		Size: 3.1 MB (3073487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159e989cc552c37f191008030afdd4b3a51980fe51d0d335aac5432300cdffb3`  
		Last Modified: Tue, 18 Mar 2025 02:24:19 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6575a3afe0e9eed819683fadac63a5dd8bd6e1fa7126223b933fdb1937c74a`  
		Last Modified: Thu, 20 Mar 2025 17:55:36 GMT  
		Size: 9.4 MB (9354503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1ab4277b672d432d8c192d0de9ba1a4786012d738f4e795b49178683aa9624`  
		Last Modified: Thu, 20 Mar 2025 17:55:35 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:8e349b6160c4d50c0d7bfabffcc43454b6263cb63cceaa17e363b984577dcdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2394476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf698438fe28dd699d8b9dcf0a5f2a44fdf4757285143c2703a6a9c95bd92f83`

```dockerfile
```

-	Layers:
	-	`sha256:1567c140cf4ffa7c8945ec12d6d3b8195344c4694fb51280c407c8d6d0a6a6f2`  
		Last Modified: Thu, 20 Mar 2025 17:55:36 GMT  
		Size: 2.4 MB (2372587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:292d92b74b586c675857f89fd3e3deb61963ce0b0c8834e0541250847abceaa9`  
		Last Modified: Thu, 20 Mar 2025 17:55:35 GMT  
		Size: 21.9 KB (21889 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:0910c9aeace8ad3aed6cfe77fc404c4e1526bd07d238d593bb950b44358116e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (36000511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d806a0a5622afdeebcbef1b89d81c9815499e9033f0086bcd79f303cf188745d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90de84afec6d4f313e7bf277c66cdcd6136876e4c4965613cc67e1980d1444fb`  
		Last Modified: Mon, 17 Mar 2025 23:43:15 GMT  
		Size: 2.9 MB (2907809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3765238d144b9228c5e898a9ec77dcc08b04f997fa12e4fc93987498a9d089f1`  
		Last Modified: Tue, 18 Mar 2025 07:08:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b926d47f234bde8855c67f886a3d9bc1e12892b3ff6ad4987a9c629c60213606`  
		Last Modified: Thu, 20 Mar 2025 17:56:24 GMT  
		Size: 9.2 MB (9175974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4a0aa4b9add24000e4fcbe4c54d8a546a2ab6470ccbd830db9c789de1073d8`  
		Last Modified: Thu, 20 Mar 2025 17:56:23 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:f7702de65c90ea8fd3fed488b206203eaa4adcbc7026cf76686b3a458fa674f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d37dae2968ebcd68cdac68af8156c0edcc89ee8eb96e094747e44b8dcdcbd0d`

```dockerfile
```

-	Layers:
	-	`sha256:a8172d95d453af2885e554911873f1be9b5c248a2e97f62260db737e30c6b7e1`  
		Last Modified: Thu, 20 Mar 2025 17:56:23 GMT  
		Size: 2.4 MB (2371316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc9f0de84ffcfc59eb8db04437492333dc52964e8df6b164b806ec8356b0bfd`  
		Last Modified: Thu, 20 Mar 2025 17:56:23 GMT  
		Size: 21.9 KB (21889 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:3697e2160adb1c0ac086183147fe681401030abb5c9c94528f550f814429560c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40748173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc557dd22c6dae4082ac172aaa83fe3fc54f030f6027800545f9d03253cd4f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f1f5b37bd6494f4c979734eddbf38ec3c9d650a090b347a2d957a8954d0749`  
		Last Modified: Tue, 18 Mar 2025 00:23:40 GMT  
		Size: 3.3 MB (3322905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c3da725bc9ab1211ba59e744f1a5fe5b4e9f2b38e18b7ea5c785fd180194a8`  
		Last Modified: Thu, 20 Mar 2025 17:53:10 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b387add951b88b3c35f7bfd1fd52f66f09e73f0c14480904fdb0a30c958481a`  
		Last Modified: Thu, 20 Mar 2025 17:54:43 GMT  
		Size: 9.4 MB (9379590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9c18ba2dba67611f74cc31c55c7967a8dacecafaf4fbb6e49cca6d4271b00b`  
		Last Modified: Thu, 20 Mar 2025 17:54:43 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:09e80ac9b192c094a64af6307ac1fb3b0311e22c447240a966b62b628285d7f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2391286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e837637248c28706b6a576ce90e015305684939428b78ee6e7423fb669033dab`

```dockerfile
```

-	Layers:
	-	`sha256:2c3eca4ead243b4915acaf168c95bc93a02a6f6b94d1816c5f98e9ddf1424400`  
		Last Modified: Thu, 20 Mar 2025 17:54:43 GMT  
		Size: 2.4 MB (2369356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f8304840f3c51a92fe46e493bf81490dda2ebd290eab73e09294acb67cc1773`  
		Last Modified: Thu, 20 Mar 2025 17:54:43 GMT  
		Size: 21.9 KB (21930 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:6217bff3b1b8f15b4de0e1a4676836be863efc244936434f398d6db962065b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41839295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd48562dda74c6d2f4eebf7785f80d3af6a533f0472b2e2f910b86bb983daa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a934e4fd2e0f4efb32b0933b619dcf646aa9ffe836110a032a61881fb1d37a5`  
		Last Modified: Thu, 20 Mar 2025 17:53:50 GMT  
		Size: 3.5 MB (3503437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ceecc53b36446d42ecf62c21b507deff81dc716830aab58d4aac4725cf96b6c`  
		Last Modified: Thu, 20 Mar 2025 17:53:50 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b842703f5e1f5b240727168b299adef8eaacff8864b085027e84205e5ffb4d30`  
		Last Modified: Thu, 20 Mar 2025 17:53:50 GMT  
		Size: 9.1 MB (9144689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e267ecf9ed0bce51dd5d2dfdc3c8226b693d0de9baf66c6d8ec377cd80f43b0e`  
		Last Modified: Thu, 20 Mar 2025 17:53:50 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:9a1fce9d5f318f887956a6dbc8dda2105842ac7477a79fd39cb59ddf4a8833f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f538972d91edf5d3768adf2dbcc5ead67214cced170b9fe3763e15ace0577d`

```dockerfile
```

-	Layers:
	-	`sha256:e7c179552e69ce3cda92bc8579185e7204e4cddc15d670593a0cfeadc9b973ab`  
		Last Modified: Thu, 20 Mar 2025 17:53:50 GMT  
		Size: 2.4 MB (2366201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9011c8b1ff179e9482bf2c4d2b0afbd528b617c811efc22c4ffac9730859c246`  
		Last Modified: Thu, 20 Mar 2025 17:53:50 GMT  
		Size: 21.7 KB (21726 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; mips64le

```console
$ docker pull haproxy@sha256:5ab600aa863cb5f013623bab5bdc03fdd2844aeac9a9d7601929ace3b877b92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40891792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901aaf44d3e6bbfdb4459e7302eb4a56a8089e32e837d9b946af27ce2f8b1f8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:18c44d6735d044d9bace3fdbe647c9b8187637683376f05d85dcb1185876721f`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 28.5 MB (28489456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b514658a4f48245596c09f7112cb0f6884c0b1fa96bda139a946ab70038e2fe0`  
		Last Modified: Mon, 17 Mar 2025 23:20:58 GMT  
		Size: 2.9 MB (2895399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0467b6da4ce332003153c6aee3f7184652dad841330e46d759b478e43848fea`  
		Last Modified: Mon, 17 Mar 2025 23:20:57 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba5f7f71938b38ef7188412b02a9975e11dc8483d9a2635f95baf738e8c545c`  
		Last Modified: Thu, 20 Mar 2025 18:02:19 GMT  
		Size: 9.5 MB (9505297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bd1f45cd56d87bbf53606125f12de3c4b7a53189f2997ba5ebdd26e3281f68`  
		Last Modified: Thu, 20 Mar 2025 18:02:18 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:df357eae948f43aecd91d2f8737cdddf36c867fa5b1ccad5d427621287c90c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ec6f6b0773a5756e7fa8f39ff5f6f5797b6a7bcd8d260f5accba5902710d1b`

```dockerfile
```

-	Layers:
	-	`sha256:b72043aeb3b47af4594f02018c7f79e827b24b25845f53cad37494fb7a64c88f`  
		Last Modified: Thu, 20 Mar 2025 18:02:17 GMT  
		Size: 21.6 KB (21647 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; ppc64le

```console
$ docker pull haproxy@sha256:e8ed1d89ffafd7ad9d10c8c6b8ee0b88e755fc74d48721de182c4790d844ccfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45637736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58e3304f64966f88bade4973f5d7809f43fda06e064cca926f69d3f17157111`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297f17f6db06f7ccb8ce850d74e9476f76be07c3d767a47f85269129c1aa3413`  
		Last Modified: Tue, 18 Mar 2025 00:05:31 GMT  
		Size: 3.7 MB (3703023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362219842806f48e93cf4a662cc0a59d3d9b5f9daf98f8205062caca3e15349d`  
		Last Modified: Tue, 18 Mar 2025 04:47:56 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66548ff22b233154848853bd38b182b0921224e00ce7ebf44e6dcee9e3449f5`  
		Last Modified: Thu, 20 Mar 2025 17:55:22 GMT  
		Size: 9.9 MB (9885259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ef605fe0399826ad60fb0ea1137778c8b44798269f88fb02f323cd6c93cc89`  
		Last Modified: Thu, 20 Mar 2025 17:55:22 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:a90319c946309ce97e6a0d2ac24224736ed3c8c1704855029f84a57d41911305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0a42401417248a4d9eb00a03c61b5f84feab0f7e11dfe4de5c72734d4edc2f`

```dockerfile
```

-	Layers:
	-	`sha256:c7bdb603065031c7376f71f36f567315fb7b116e9111990a7fa8314180b7c9a6`  
		Last Modified: Thu, 20 Mar 2025 17:55:22 GMT  
		Size: 2.4 MB (2373387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4af366eff1890b2c07404ac1a64a68dce9c76a65eb6e9527ffdd7c98964d893`  
		Last Modified: Thu, 20 Mar 2025 17:55:22 GMT  
		Size: 21.8 KB (21832 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:bd378bb825dfbfc7ee45a084a4517c1083276c118bc44d3fc1c829e8d380eb20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39283204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e8fb53a329a3743d657cf52105f3a88f342618d808d89cdf4594b935aa5725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_VERSION=3.0.9
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.9.tar.gz
# Thu, 20 Mar 2025 17:13:31 GMT
ENV HAPROXY_SHA256=7dc731b681b7aa93dc23aa36b85fa7b91bb1cf53faaca97404544ea454acecad
# Thu, 20 Mar 2025 17:13:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
STOPSIGNAL SIGUSR1
# Thu, 20 Mar 2025 17:13:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Mar 2025 17:13:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Mar 2025 17:13:31 GMT
USER haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
WORKDIR /var/lib/haproxy
# Thu, 20 Mar 2025 17:13:31 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ac3c278183a5f89567d212db7d1cf86cdf072aa72fbb0786fd4105c665de4a`  
		Last Modified: Mon, 17 Mar 2025 23:18:50 GMT  
		Size: 3.2 MB (3163408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9d273263b11bc640b62365d498bd5690e754578121542ede73f2b39a10ab0a`  
		Last Modified: Thu, 20 Mar 2025 17:54:16 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d2ee9e7bfec59203fbe4c99dba9815e10351664112af4c53c96adc615bcc56`  
		Last Modified: Thu, 20 Mar 2025 17:57:18 GMT  
		Size: 9.3 MB (9257097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa581d5e104ea4119710d20a1906f5ea40427c3192d748c5e6787a84dd858b8d`  
		Last Modified: Thu, 20 Mar 2025 17:57:18 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:40dedb3cd73060f067a63b3d4abae7c0e0908a78b119563952abe7c23bc3bb1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1c395eb495706e2311b24521d1e1f80e520c26e0c4c5fc2550548e4fbbb5ea`

```dockerfile
```

-	Layers:
	-	`sha256:124e2710c344dbd686b3d7a1b4f6038103535c2f493bc1f1cfa8f96581477ffc`  
		Last Modified: Thu, 20 Mar 2025 17:57:17 GMT  
		Size: 2.4 MB (2368795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0070bf18b78cc1ce8ab27d77f515879ccf2c94e2c84be94ea0f3e099f96c100f`  
		Last Modified: Thu, 20 Mar 2025 17:57:18 GMT  
		Size: 21.8 KB (21771 bytes)  
		MIME: application/vnd.in-toto+json
