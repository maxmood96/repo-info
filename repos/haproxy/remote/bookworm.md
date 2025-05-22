## `haproxy:bookworm`

```console
$ docker pull haproxy@sha256:e43b60f97e36df71aed0b79b60ac3f390ff72da796ab6f8fa47705a81d39224f
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
$ docker pull haproxy@sha256:0fc3d0d77163b52d1dfced4579af31de7e4aaff19b62eacae1854b10d89c599f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41780801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca815b98bc6fa2e237df274f16b7d587e6a8443e96580ec83df9ed8c6dbdd31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 17 Apr 2025 17:13:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7578d1b01d53f8b30efac62f510e006c369bb37c957b03852b85e868afde0f3`  
		Last Modified: Wed, 21 May 2025 23:13:02 GMT  
		Size: 3.5 MB (3500695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9223bc3fb19b4a9908fdaab437c8b03eeb39804a99aa674a9e8e393f834c6c3f`  
		Last Modified: Wed, 21 May 2025 23:13:01 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67321637817d7e845130cd1126cfdaf89ac0dbac395601f31bb8510db69d68c7`  
		Last Modified: Wed, 21 May 2025 23:13:02 GMT  
		Size: 10.1 MB (10053139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfc2b1f0e51b7447d51bb70e732efa8868c462542a1e544dd1373dcf7175efe`  
		Last Modified: Wed, 21 May 2025 23:13:01 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:4e77e4913aedbf17c96614c765c8316dcf9fe085be93f47728ccc176bcfb8c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2409631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0eddaeae67731306c2a5cfa32816f058711bbfaf44b33f488b8959940310dc1`

```dockerfile
```

-	Layers:
	-	`sha256:9509a44099350584bd30ed1a4fe087d17569a8a00b04621c49268856b415a51b`  
		Last Modified: Wed, 21 May 2025 23:13:02 GMT  
		Size: 2.4 MB (2387858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5e06eec1ff265579d59e4075bde30b2905b4410e8092c080eb503aa8e09464`  
		Last Modified: Wed, 21 May 2025 23:13:01 GMT  
		Size: 21.8 KB (21773 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:fe2cc04e9a7c47497d4ddfa89fd6fe0d1414ab5e9755b1db0641134c414864e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38939547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65a4ff8f190b5af9a89372ad48dee114f11f4cac0060959f6c706deb9104752`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 17 Apr 2025 17:13:29 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
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
	-	`sha256:c844192bd7daa2c88e3a02223e0a664557e2c8561ac23c4c4c61f7c64badbc0a`  
		Last Modified: Wed, 21 May 2025 23:15:33 GMT  
		Size: 10.1 MB (10106470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f26ade00489e86b343f1745b4a5db648711d7a52ef50d7f62abbd45f090fec`  
		Last Modified: Wed, 21 May 2025 23:15:32 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:91261f0e378b26ea0a3fa54fb80078538f37c4ba0004037f835fd00463790929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2413571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:673b677dce1aeee71bb7074cbc1e3f58a4ba3b1c78143e44de6015e89f81dc24`

```dockerfile
```

-	Layers:
	-	`sha256:30eb46e872fdfdd5ae6f995f11e92bdeb45fe7f6426d1a8eea30707f91cb42ef`  
		Last Modified: Wed, 21 May 2025 23:15:32 GMT  
		Size: 2.4 MB (2391680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa667a1ab85c0640c4a0869bf5f3e16623adb226f52c40fd921473734bceac81`  
		Last Modified: Wed, 21 May 2025 23:15:32 GMT  
		Size: 21.9 KB (21891 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:7b2cd3d5654a25fe1e902e53192095fe01e840bfd4fd95541eba5978fd0998cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36740996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1249b8cd7ce6d4c4bfe59e16ed7999264b2a6328dc9c361b19ce5f76a76f35c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 17 Apr 2025 17:13:29 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
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
	-	`sha256:81c3c3ac0187de4c467077b52842314c898beb4d808c606a510fbc862bb55368`  
		Last Modified: Wed, 21 May 2025 23:17:08 GMT  
		Size: 9.9 MB (9896232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb13aab6ca32ffbce64967e0954cf1306015563355750cb76eb87ef46bdf1c81`  
		Last Modified: Wed, 21 May 2025 23:17:07 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:617ef556a32666611e5b75ff3a75aa4d022b7b39b83344f9d56e4c29495b6b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2411988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275c3c1bc8da1c3ee828bfb09b3000baee90d0af2ab8be0dfa00bffabe2e615a`

```dockerfile
```

-	Layers:
	-	`sha256:85ff313e2c7319e382348f29cee8121f52ac4aaad4acccd8712d1d15eddee614`  
		Last Modified: Wed, 21 May 2025 23:17:08 GMT  
		Size: 2.4 MB (2390101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da5bc33875fd109c9bebd34f8e895b6d2e8f67e9d67ca74a3e1f649231ec6e44`  
		Last Modified: Wed, 21 May 2025 23:17:07 GMT  
		Size: 21.9 KB (21887 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:84d775abc9b3ddec68878f7797ea595ab3d9fca397139bfc932835e304dd6c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41407254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a834cdf35ab48bde62a686e4790d6dfe15c94c1e295f7084cc3391e70fcf399d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 17 Apr 2025 17:13:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd4fd474e07a8fbfb9f0c17f4bf095afca6ad25cb455ffa5586ef48224d0ff5`  
		Last Modified: Wed, 21 May 2025 23:15:54 GMT  
		Size: 3.3 MB (3324393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74952c534a8157841fa2bb92a773b87d89be798e02e8eefabc939e5988c31d92`  
		Last Modified: Wed, 21 May 2025 23:15:53 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e9794183d44821d35b69d83d3006740587fbab7d0248645b8bac91f10ad67`  
		Last Modified: Wed, 21 May 2025 23:16:40 GMT  
		Size: 10.0 MB (10015946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b72b5bdbacc4d9e6b16c3f466a1ea16be0cdd4a4b44479b499ad080b87c9b3`  
		Last Modified: Wed, 21 May 2025 23:16:40 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:6142217e6c5379034773c599a2d11ea8565e355d2b937ae9ae9470ab14c11325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2410072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a2aec0406a4040bdf2b9c320b288f2f10590b848e5b8f323ea0d37acf26909`

```dockerfile
```

-	Layers:
	-	`sha256:f2d9a640115f6ce019a6704a851a300e35b6301a7162092a946d4bd4c9652416`  
		Last Modified: Wed, 21 May 2025 23:16:40 GMT  
		Size: 2.4 MB (2388141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:105db7162892c99f238436af9237b54dc8b73a2e2508e018633b9e2da42f3582`  
		Last Modified: Wed, 21 May 2025 23:16:40 GMT  
		Size: 21.9 KB (21931 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; 386

```console
$ docker pull haproxy@sha256:f694050c2400764629574102fb2089620b38406d95ae80e5276fc0fad72eb8b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42440898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882cf928946a55d799390b844db889c794e2861a2109d5cc55e4c6b4ddb5f7c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 17 Apr 2025 17:13:29 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a99c625096b4756c0406c25967e62d0f59f95c9150367c761e40b27aa21db6`  
		Last Modified: Wed, 21 May 2025 23:13:01 GMT  
		Size: 3.5 MB (3506069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad3882c6e26b0a5ccf186b50b5d20b9d3a6f5d66ef83babe3584675c367e9f7`  
		Last Modified: Wed, 21 May 2025 23:13:01 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a62a3c85b149af9586310ad41af635ea2e3de3da1546a42556eb55abb188b3`  
		Last Modified: Wed, 21 May 2025 23:13:01 GMT  
		Size: 9.7 MB (9725704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e54c5d1b816cca53eb679055ced5fa6d8aa0f7d34cc924ba15ebaba2571347`  
		Last Modified: Wed, 21 May 2025 23:13:01 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:34ba5df97812362a53833748549bd62004fbc1d70304bfb86acd434193bdcaa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2406751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d34b633d5a4e4747d79853216f61ffe4a4b96c2feab9f7b7ec2e501f25eb1e`

```dockerfile
```

-	Layers:
	-	`sha256:a770c6b3832e1d4a680071055c7f73488aac0d34e54cf734d749f27da6c448e2`  
		Last Modified: Wed, 21 May 2025 23:13:01 GMT  
		Size: 2.4 MB (2385027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b8f689d78816f54efa63f6d8cc2da1af74d9e9dd7ef5f974ef183a8dd4a758`  
		Last Modified: Wed, 21 May 2025 23:13:00 GMT  
		Size: 21.7 KB (21724 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; mips64le

```console
$ docker pull haproxy@sha256:2700da12cc040facfb6c2f760eefa9dbc17a98deb79a7a20c74e3d360835c9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41593704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eef66e9bf9d4d1170b94dc81bea23ac136fc66c403bf7e9a75f5d4fc3fecf1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 17 Apr 2025 17:13:29 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:901060d913f9d0bbb82847b3b60c3a263ed0dac4f75aa29161be6ed89b57082a`  
		Last Modified: Mon, 28 Apr 2025 21:11:19 GMT  
		Size: 28.5 MB (28514138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e3738fdfb9b5496051b58acd79f288b004b1f351674ceee392730c95f7c3b6`  
		Last Modified: Mon, 28 Apr 2025 21:53:55 GMT  
		Size: 2.9 MB (2895397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3afbf086f9b0bb821168653aa19215551281384882ceb29aaf7bd052de04a8f`  
		Last Modified: Mon, 28 Apr 2025 21:53:54 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27725da04bb49645e1ba459b7c45c952981a75674eb9f7669c77a6b33020559b`  
		Last Modified: Mon, 28 Apr 2025 21:58:59 GMT  
		Size: 10.2 MB (10182526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f75db3679487d5f0eb0494353c3aaf44c33f1836d53c505fe79d4e2fde81960`  
		Last Modified: Mon, 28 Apr 2025 21:58:58 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:eeb8208440f2a2fe30292c7bd36fce75adca4ef1c9fd8321a8f19ffe48d7bf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fb1303c23682697a69ecda2836cab73e54f572e84fb7a47c6fb9c760739763`

```dockerfile
```

-	Layers:
	-	`sha256:424315cf389b439e0bd89f27485f9a1523d2d21abce30eacc8fbd506db2ac4cf`  
		Last Modified: Mon, 28 Apr 2025 21:58:58 GMT  
		Size: 21.6 KB (21648 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; ppc64le

```console
$ docker pull haproxy@sha256:680ea335cde3e4c092f1027394b041ac513a67d6b3707eadc06d7daa7f00bcb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46357495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55399e91d07692759ffc5a95ec29d55f1514e79b935e661eaf8250fe912fb896`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 17 Apr 2025 17:13:29 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
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
	-	`sha256:ea71b17e5fc164d50da9718d4dc5ca7cf2d0ee5e15120c2dffdae7e6e974e01d`  
		Last Modified: Wed, 21 May 2025 23:17:55 GMT  
		Size: 10.6 MB (10583845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c75fb9a8d905e2c7c904ade0b870d5366d18f2856987cfe5f40573ad0b0bc38`  
		Last Modified: Wed, 21 May 2025 23:17:54 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:5cbd11eb5b11cc4b0047eccebc310ac07c02a58da4a978f4deaa4e5f694b249d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2414099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547cbeadd7ce720ca5884cc6a8b86a11b446a0eeeab18204feb846fba2ada03b`

```dockerfile
```

-	Layers:
	-	`sha256:479340d6faec30bab26277d6fbbe706638620a2a27051264a648b563e30ed3ae`  
		Last Modified: Wed, 21 May 2025 23:17:55 GMT  
		Size: 2.4 MB (2392266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3656a0f06ff0f5651c0dd4d924a3062226cce8a12c82351cc2bac3c4e9262ea6`  
		Last Modified: Wed, 21 May 2025 23:17:54 GMT  
		Size: 21.8 KB (21833 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:bookworm` - linux; s390x

```console
$ docker pull haproxy@sha256:efcbf38f4e9e2bfcac7cba347b1eef6d4ea37e631a2081604e0386b0cc7a6e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (40022758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a23c91534c78c7eec76c000d59291c880a712bd499d1e8704a7100248b1fcc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 17 Apr 2025 17:13:29 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.1.7
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.1/src/haproxy-3.1.7.tar.gz
# Thu, 17 Apr 2025 17:13:29 GMT
ENV HAPROXY_SHA256=a3952644ef939b36260d91d81a335636aa9b44572b4cb8b6001272f88545c666
# Thu, 17 Apr 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Thu, 17 Apr 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 17 Apr 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Apr 2025 17:13:29 GMT
USER haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Thu, 17 Apr 2025 17:13:29 GMT
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
	-	`sha256:7e107db1658ea6fbead7d23dff64a19e222af195b83438b48baed33afad62d26`  
		Last Modified: Wed, 21 May 2025 23:16:29 GMT  
		Size: 10.0 MB (9973411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccf2d2f33a039970577149bdb18716a0788b4817120a0c1c10265d22a016bbf`  
		Last Modified: Wed, 21 May 2025 23:16:29 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:bookworm` - unknown; unknown

```console
$ docker pull haproxy@sha256:531cb7ecf9ccbd0272075fbdc316d2667da4830086791809dc6d0f8a2bfbdc49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2409350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000428d6b2f76ce2af456d26a18c039c78a177447b2801d996e7fbf1b26847d6`

```dockerfile
```

-	Layers:
	-	`sha256:a0c1dbac9603c92c7ef88c0198be3a983b883dc42ad1c3830a2440dff75d9865`  
		Last Modified: Wed, 21 May 2025 23:16:29 GMT  
		Size: 2.4 MB (2387580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a43082ff8b82479e975c645e626020c8039e1286e9a69e880a6215c468aa3d`  
		Last Modified: Wed, 21 May 2025 23:16:29 GMT  
		Size: 21.8 KB (21770 bytes)  
		MIME: application/vnd.in-toto+json
