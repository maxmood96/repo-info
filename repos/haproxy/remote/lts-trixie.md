## `haproxy:lts-trixie`

```console
$ docker pull haproxy@sha256:eecace6a981635206e12e8c43455e2a04ea05f0d30fde0fb0cb2c8dc9eaa27b9
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

### `haproxy:lts-trixie` - linux; amd64

```console
$ docker pull haproxy@sha256:6cb6affdbd9a0a3ba9135fb334c78eae42c1ef006569a16f4af784b26b3f76c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42051597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd82db43fba59b51114490ef44c2df53297fc8acd9903d00cc3f98b1ae8ba8e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.2.5
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.5.tar.gz
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_SHA256=77316a3e1b6c39245bc11ef58f4d6dadd063c014c1baec8f0d81798c519e072b
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 23 Sep 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
USER haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643f5ec399a03cdb1c1c52423aa47e8f5161dd5fe6dbd0169087c821d0350c68`  
		Last Modified: Tue, 23 Sep 2025 19:49:10 GMT  
		Size: 1.3 MB (1279319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a97f3636885ece44ba1b9cf7d1d8d918e93d444e030010380beb3bac511fc8`  
		Last Modified: Tue, 23 Sep 2025 19:49:10 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3caf9a450953f423633efa09be414899e9db34f95bccf2e57ddf90a1ebd61d6a`  
		Last Modified: Tue, 23 Sep 2025 19:49:11 GMT  
		Size: 11.0 MB (10997142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e937e592e640210d3488ddf7fa4e288f3bfe63d8a3ca7acd03b908ba923f43a`  
		Last Modified: Tue, 23 Sep 2025 19:49:11 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:3f947544199035b7c42f33e7b7d43f469673cbe1a3ff8b618ea685d9868b875e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633baea16d4a18e96153e35e109de27617d322d844ab5cf3876cae6f31b52eb1`

```dockerfile
```

-	Layers:
	-	`sha256:abbc64a44920208fccb7082b3781068d59172f908587173f09153bda440609f7`  
		Last Modified: Tue, 23 Sep 2025 21:56:18 GMT  
		Size: 2.1 MB (2099816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e7c407fe8e8921cc9ea5beed4494e012b7f91c63d1263e31e32806923c9ec60`  
		Last Modified: Tue, 23 Sep 2025 21:56:19 GMT  
		Size: 22.0 KB (22036 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:07bca6ab690a0d5b9b40b8912fce898a3d373d0bdc5a8d056387f9edda2d0313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40286638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d6a4920bb481890fe445aa46bde1336714fc38188ab6d8b7a731460741d139`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.2.5
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.5.tar.gz
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_SHA256=77316a3e1b6c39245bc11ef58f4d6dadd063c014c1baec8f0d81798c519e072b
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 23 Sep 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
USER haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:5d61fc20e756831552727f89a087e2b45b07dace604ad2cda0a2afa80ace388d`  
		Last Modified: Mon, 08 Sep 2025 21:13:29 GMT  
		Size: 27.9 MB (27941760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05278ef1c4be6d0f5528e5b76bb5ab6d0c4decf5c1ddb3419704cdad7b05023`  
		Last Modified: Tue, 23 Sep 2025 18:06:37 GMT  
		Size: 1.3 MB (1262741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7bcf83b84040dd2ef1c2d7bae8e995fd08af4e104073bb2f50ba1fd527f5f1`  
		Last Modified: Tue, 23 Sep 2025 18:06:37 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229ffae89866657895c84f7127d945cc5375e8f41bf7d314ec72685d56152191`  
		Last Modified: Tue, 23 Sep 2025 18:06:42 GMT  
		Size: 11.1 MB (11080494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38553fd60b33e020533ab8a1a33136ef4232d4e8f8e012446499fc92dfa8c21c`  
		Last Modified: Tue, 23 Sep 2025 18:06:37 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:ae7fe72cdfa90f6ce80b8fe98fe528ad52d920777b341646205b9539e58b48f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec17dc7d656fe89a9b4cc9533157e98862df726aee569803e0d64312f20b3331`

```dockerfile
```

-	Layers:
	-	`sha256:f2bea28c2e2d58d7f1a7850c6027e6f538511522e10151caf8ca9a1c6ca11787`  
		Last Modified: Tue, 23 Sep 2025 18:56:22 GMT  
		Size: 2.1 MB (2102811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:961a82a1cb259100af47540ff943bbdec7dabb9a2412f7a911130578c0d257be`  
		Last Modified: Tue, 23 Sep 2025 18:56:24 GMT  
		Size: 22.2 KB (22174 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b89cb92bc46ebecba02444974ec4ca27ec0a2fd9a77c603f89532658f8e2e191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38315269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd2ed1beeb97ebf3893d924e2ba05f1556ae1870fb7a6475cd11af002e0f72a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.2.5
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.5.tar.gz
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_SHA256=77316a3e1b6c39245bc11ef58f4d6dadd063c014c1baec8f0d81798c519e072b
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 23 Sep 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
USER haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbfd61c4b3a47c322fe690798bea2b5e4bf38d77edfb38f9e6a245b8999723`  
		Last Modified: Tue, 23 Sep 2025 18:15:13 GMT  
		Size: 1.2 MB (1235954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a415924fd61bd68b33536480a3fcce84ac22480314bec068c0b9c7a6bbaae356`  
		Last Modified: Tue, 23 Sep 2025 18:15:20 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd64c856744c0a4bb17c0565c17daac25cf344e3095d93adddc091fc3d15b109`  
		Last Modified: Tue, 23 Sep 2025 18:15:25 GMT  
		Size: 10.9 MB (10869824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd0ec43c8dc74c3c26161cf2871a84fa937f3fc2927ded58b6161543183091f`  
		Last Modified: Tue, 23 Sep 2025 18:15:36 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:f9a40d2e42f03964d5c01e532227cd09c8977cf313cafb64cf22d7e6e888e3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22e751419e718b7ff1185d6761c84cb79b5b2db04c01cfc704625ab0eba32f8`

```dockerfile
```

-	Layers:
	-	`sha256:b47469e88d4bf12271f879a8149aef58de195eb4d54e7ec6eb7e2f425c437872`  
		Last Modified: Tue, 23 Sep 2025 18:56:27 GMT  
		Size: 2.1 MB (2101252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2776a71e09506175af2578435f8cbd6b5e1f3b9f1b87542b289b063d107ba958`  
		Last Modified: Tue, 23 Sep 2025 18:56:28 GMT  
		Size: 22.2 KB (22174 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:f2df4916d24411fe59d65627660220c36c3a5c028513393821d9f60cd020e01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42329277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f681e034b92b3d9e8f73c48159e6207ef514fc00d7766c0ff53c61e78c80d2bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.2.5
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.5.tar.gz
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_SHA256=77316a3e1b6c39245bc11ef58f4d6dadd063c014c1baec8f0d81798c519e072b
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 23 Sep 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
USER haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9142e3f7a22492e1b1246f57b051cb95ed737183071ff7196263bb132d72d629`  
		Last Modified: Tue, 23 Sep 2025 18:05:54 GMT  
		Size: 1.3 MB (1260885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29929511cf7e620b4a79e1b0d3ac15084598e1f4fbd9bf494442f7a55e9ffbaf`  
		Last Modified: Tue, 23 Sep 2025 18:05:54 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1251b902138e842ad91742c0b6df4427b4bccf021d014246dfb0d3f245e039dd`  
		Last Modified: Tue, 23 Sep 2025 18:05:56 GMT  
		Size: 10.9 MB (10930121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ca2fef95722158cbad111a8d6c3eeab4bd092d8b54b996e7c0ebcff94a1164`  
		Last Modified: Tue, 23 Sep 2025 18:05:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:5b0a2093d46ad981d0f40d754d01d0a205afaa20d7d090bc73ecfb50f9c89f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d162ecd3650f8090736c72d188ba0c848710dc7cb3449cc54a4ddb4ed418ce`

```dockerfile
```

-	Layers:
	-	`sha256:67111074321f9db50205f3541e8c77a05e24111958b2d427a921037dceb76ddc`  
		Last Modified: Tue, 23 Sep 2025 18:56:32 GMT  
		Size: 2.1 MB (2100124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef1fd0687eecf2c0822ff0acd26d27d9200ad7fbb3941e55d4f0a1c13f0e4de`  
		Last Modified: Tue, 23 Sep 2025 18:56:33 GMT  
		Size: 22.2 KB (22217 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; 386

```console
$ docker pull haproxy@sha256:92ef3528ecda133758181c04fdc07e120f809281cf7a2855abc737d27843a8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43287260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e5213931eac3769d6fff019fd231c610762548879502a130b32ab88019e6b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.2.5
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.5.tar.gz
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_SHA256=77316a3e1b6c39245bc11ef58f4d6dadd063c014c1baec8f0d81798c519e072b
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 23 Sep 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
USER haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834d685284f9ca04ba37e2ea7e4b771753b0cf448335122129ebbce40f5273b9`  
		Last Modified: Tue, 23 Sep 2025 18:06:54 GMT  
		Size: 1.3 MB (1286819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65b11f3584be03f2d0aa37e7722a122fc43d9ed19847632be81571fb22d9505`  
		Last Modified: Tue, 23 Sep 2025 18:06:54 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d6c611b1c7d6974705f25a49bbbc5c019b951e70525d454a33ab72d2649b40`  
		Last Modified: Tue, 23 Sep 2025 18:06:55 GMT  
		Size: 10.7 MB (10709014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14922d9dfaf4bb6fe1c84f488d145d80340aa3065f7eedffb385d10f74852f9b`  
		Last Modified: Tue, 23 Sep 2025 18:06:54 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:ce7a01dca399e44e04f947943bc4dc3bd5545f984073be7f1cdd567dd3bdb6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b8582830e8dc1325e84fad484da4aad2262b89b02bf124ca9689a9cc2958ee`

```dockerfile
```

-	Layers:
	-	`sha256:fb6acd76954ed7780dfa3b2352bf14295ecc091c8dc1d798885fd37d2dbd78ca`  
		Last Modified: Tue, 23 Sep 2025 21:56:30 GMT  
		Size: 2.1 MB (2096989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a93be0a29388c3ec8575848b0e0b00ee30070f76224c2bca4e8b4bb87dbf48b1`  
		Last Modified: Tue, 23 Sep 2025 21:56:31 GMT  
		Size: 22.0 KB (21979 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; ppc64le

```console
$ docker pull haproxy@sha256:49c2d66bc721627977c626fc4d0f522064cc057f07b03138b0579d195dcb23c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46551349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf05e0062168c43ff1954a192ef028f66ef9893c9965c61acd656f695492210`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.2.5
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.5.tar.gz
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_SHA256=77316a3e1b6c39245bc11ef58f4d6dadd063c014c1baec8f0d81798c519e072b
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 23 Sep 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
USER haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954fb1925e4b457fa58518f37c30d87765cb47ba4bf9c6ae03bc6c92bf64fcee`  
		Last Modified: Tue, 23 Sep 2025 18:06:29 GMT  
		Size: 1.3 MB (1309728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0beda2e9498f147b4ca6d857a2434e0c3f36b1fd3a4b2f7eeca90b0194f63a`  
		Last Modified: Tue, 23 Sep 2025 18:06:29 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369c018715b66367cead9635da4807095b26e5d104e036b566dbe7486c62d0c9`  
		Last Modified: Tue, 23 Sep 2025 18:06:31 GMT  
		Size: 11.6 MB (11645629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ed13aa0318ae60a71c4367ac9ecaa247b3a768d582b1842bd29f5769566444`  
		Last Modified: Tue, 23 Sep 2025 18:06:29 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:0c9ac227c7c80c162f117ec612e061cff8921f15f04f6dd526cf8d46037d8c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2125473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab7246343168c78be568e97f40cf8dc29ee61ebc2a8a9f13cf6fb7fa641a8e4`

```dockerfile
```

-	Layers:
	-	`sha256:cf9a18b4ccdb7422d4028453de0ea730eaf19d562ba65a84044024c08b04300d`  
		Last Modified: Tue, 23 Sep 2025 18:56:40 GMT  
		Size: 2.1 MB (2103365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df2f24a747b9984a619b617d5f1265c194e676b1118b53a773e60bc9885d15b8`  
		Last Modified: Tue, 23 Sep 2025 18:56:40 GMT  
		Size: 22.1 KB (22108 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; riscv64

```console
$ docker pull haproxy@sha256:5c61e9292ee900bb9c4411a422c00414779d7f6bd9e9e1c7d79c6f0006110812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40168765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73af9799114a87d9b1de3cd8e14b5c2f1dba940c95bc2d0abb6eb275e71194e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.2.5
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.5.tar.gz
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_SHA256=77316a3e1b6c39245bc11ef58f4d6dadd063c014c1baec8f0d81798c519e072b
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 23 Sep 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
USER haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbfa6d289653e209600f08a3a0f15cdbd12ff5c8395414568eddff943ac44fe`  
		Last Modified: Tue, 23 Sep 2025 18:28:59 GMT  
		Size: 1.2 MB (1247471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc888516dbdcb5fe53bed57afdea881e337bf5eca4ee7533d57fb7542cdb7751`  
		Last Modified: Tue, 23 Sep 2025 18:29:00 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac0d6ca7cf40f5a32f8fb561ddeed11fa76c9bc4cbd1b8ae108d1524b62f802`  
		Last Modified: Tue, 23 Sep 2025 18:29:01 GMT  
		Size: 10.6 MB (10648279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b724df522f071c8421c912d9b2e93bb31fd942865158dfdd179800405c4d8b`  
		Last Modified: Tue, 23 Sep 2025 18:29:00 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:4ea8c24e17a606555cba0dffba9c4278f582c34e955f030e8dde80ce22c3946f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf5dce296eae3030c411cb1bbaa3a994b0b4b07a84d16514b240ef3b1493d13`

```dockerfile
```

-	Layers:
	-	`sha256:7139762ce38b4e09042a5d30f0360c8aa8330b40402ea1da5cd4417e46e5e681`  
		Last Modified: Tue, 23 Sep 2025 21:56:37 GMT  
		Size: 2.1 MB (2093760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b29579b94badad8f4b2e2aa6c9e07233b89f49686149d0cb9d0aec55ce0e1cbe`  
		Last Modified: Tue, 23 Sep 2025 21:56:38 GMT  
		Size: 22.1 KB (22108 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-trixie` - linux; s390x

```console
$ docker pull haproxy@sha256:fdfe282803916162ccf2fb89ec9da1c7db8c626e52f48cd6fc5af91b1fd7addf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42424070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae10c0acd2f0f7445178b6ca08d232183b624a31792e045b9ea9edca0cc0d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_VERSION=3.2.5
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.2/src/haproxy-3.2.5.tar.gz
# Tue, 23 Sep 2025 17:13:29 GMT
ENV HAPROXY_SHA256=77316a3e1b6c39245bc11ef58f4d6dadd063c014c1baec8f0d81798c519e072b
# Tue, 23 Sep 2025 17:13:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		haproxy -v # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
STOPSIGNAL SIGUSR1
# Tue, 23 Sep 2025 17:13:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 17:13:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 17:13:29 GMT
USER haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
WORKDIR /var/lib/haproxy
# Tue, 23 Sep 2025 17:13:29 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd4deac747c9dafb68aa34548c4af0c0382f787ecf8977da0f84503188bfaed`  
		Last Modified: Tue, 23 Sep 2025 18:07:17 GMT  
		Size: 1.3 MB (1294292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e976e9e07f53d11a652e1548299759b85d105ce12eebf27ec74e675ac21c94ce`  
		Last Modified: Tue, 23 Sep 2025 18:07:17 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724c3b2ad53614c649623282312bc06d3c8cd768c697f0706da84b5118d8ebbf`  
		Last Modified: Tue, 23 Sep 2025 18:07:20 GMT  
		Size: 11.3 MB (11295230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9024b4b28056cd802a6d9da1fce879816a137d6dc89b3944f5762f6c251490fb`  
		Last Modified: Tue, 23 Sep 2025 18:07:16 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-trixie` - unknown; unknown

```console
$ docker pull haproxy@sha256:fcd6912714e20d967290510d10d4df611840abe86d06c751d79fa350e652d6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d579f17c7ddf8edad8e74e4edebca1bf025046d35d71063511085e92e649ad`

```dockerfile
```

-	Layers:
	-	`sha256:fb644b5978f051eee69d5f0ae3ad0bc01593734ac79466fe278d70e205bedf02`  
		Last Modified: Tue, 23 Sep 2025 21:56:41 GMT  
		Size: 2.1 MB (2101261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa3fb72d38f39038efd6c5b382c46e3cba7b082c8a7f1c1cfdfa38e2b77a9afb`  
		Last Modified: Tue, 23 Sep 2025 21:56:42 GMT  
		Size: 22.0 KB (22036 bytes)  
		MIME: application/vnd.in-toto+json
