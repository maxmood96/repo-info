## `haproxy:lts`

```console
$ docker pull haproxy@sha256:9613befc23e726125547d44873d4918141dc7f367338f2e0b48d4322ba2ca94c
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
$ docker pull haproxy@sha256:d721ff8ac51b4dea8d40a69c774c9ed1ea9eafcbc05a697ebd427d4b3d16daa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42042650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50638eac51982d74b3ac12db7d5e278a6f68fd9a9154d9797bae753d3c97ff06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 13 Aug 2025 17:13:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039ada74b0c9094f8ba8a2331db1c5e395a061b571b459f85de43891c435efa0`  
		Last Modified: Mon, 08 Sep 2025 21:55:46 GMT  
		Size: 1.3 MB (1277831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5587fd693769b649478ec014986f19c7a36b64cdfbea311c29a74b489812f5`  
		Last Modified: Mon, 08 Sep 2025 21:55:46 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f530dc3474a1299b6871422a074334600e1e070911bf946a466cb5b0ead460e`  
		Last Modified: Mon, 08 Sep 2025 21:56:03 GMT  
		Size: 11.0 MB (10989688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8868c5ca7fa3b609c9a68a0f0b0043dd59dcb943a9182c732fb0d9bab9bbc5`  
		Last Modified: Mon, 08 Sep 2025 21:55:46 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:78799c9fc93790acd999c064b67a137fec947e2a3fd506001ea2df271490a603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d13c2aa0ef540402567e8f5dba0387b8aafc731d8d6c42d28c876c4d761da65`

```dockerfile
```

-	Layers:
	-	`sha256:12ae376414ca815b7a6b1e4eceb08c40cf909e905c9a2c5b80902745ec141aad`  
		Last Modified: Mon, 08 Sep 2025 21:58:53 GMT  
		Size: 2.1 MB (2099816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3d7c61ad15f897cc27b6f62516f296aa7c73230b7e65d352ce3b446b38b3ed8`  
		Last Modified: Mon, 08 Sep 2025 21:58:54 GMT  
		Size: 22.0 KB (22036 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; arm variant v5

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

### `haproxy:lts` - unknown; unknown

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

### `haproxy:lts` - linux; arm variant v7

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

### `haproxy:lts` - unknown; unknown

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

### `haproxy:lts` - linux; arm64 variant v8

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

### `haproxy:lts` - unknown; unknown

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

### `haproxy:lts` - linux; 386

```console
$ docker pull haproxy@sha256:9d25c3ab0f776d26b1f2205acc8c1c4e5b0de4d16960f559f356d5c07a6ff4fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43277200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae482ee3828da75feb5ba7e5d8107349aad56333bf8ab3e2f6022f60d9979072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 13 Aug 2025 17:13:28 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b98c06a51dd82a82763ab8e6a3bfb982f5810868ee4211fd5544b108bb5a16`  
		Last Modified: Mon, 08 Sep 2025 21:18:54 GMT  
		Size: 1.3 MB (1285589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd3d0da28508a1c1d85fdc2b31418ed0b74a1b92ab70f1771ea398eb3a28e77`  
		Last Modified: Mon, 08 Sep 2025 21:19:03 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35327d05f11787711f639f09e458c81d2a85d91cbf69649074f050635b4b1840`  
		Last Modified: Mon, 08 Sep 2025 21:19:11 GMT  
		Size: 10.7 MB (10700190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11989d4a33507d95ac8586a985ee3ee23e0bdc88efffa8b3033bee25ac3924a2`  
		Last Modified: Mon, 08 Sep 2025 21:19:15 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:ec2cbd8a1287194e51dfd295ec4b6582fb7178e8ba9912c4480d218cf2756c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3942edfa02925f4aa979062c8be1422d705253f745bc41882f538b5792b1e083`

```dockerfile
```

-	Layers:
	-	`sha256:21a456960979485c51fef0446f51bff9ada05d597a15b9dbef523664a70d3aa7`  
		Last Modified: Mon, 08 Sep 2025 21:59:13 GMT  
		Size: 2.1 MB (2096989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e25fd6174818b5f38c67dac54bcbc403878a5e55c3bfa61ea4b4866dd4cefdd5`  
		Last Modified: Mon, 08 Sep 2025 21:59:14 GMT  
		Size: 22.0 KB (21980 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; ppc64le

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

### `haproxy:lts` - unknown; unknown

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

### `haproxy:lts` - linux; riscv64

```console
$ docker pull haproxy@sha256:e92ba4ed4695083238709e891dd3adfd3af3029175ed5e0c9dd8289dd0ee75cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40156240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623d5c20e8ca2993076c9a5624d33a858da29d6c2ee27892bc9029b9b05cc26f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 13 Aug 2025 17:13:28 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
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
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd727ae25de0945557b6a8540322cb772fb3a8d2c86a2ef85ad17842ec3a767e`  
		Last Modified: Tue, 09 Sep 2025 15:40:33 GMT  
		Size: 1.2 MB (1246119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe193ac8557e2ff7440d014bf4bf38f227d0f5c09373e39143209e88ccc0b90`  
		Last Modified: Tue, 09 Sep 2025 15:40:46 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2176f4204c64ae5afc39bd45f2510512978958c1fab046a0e876ac6e1701f346`  
		Last Modified: Tue, 09 Sep 2025 15:49:41 GMT  
		Size: 10.6 MB (10637106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f00826a0cb8f37df9d51805526ee5d52d97f829489fbdac28cb4800a69071c`  
		Last Modified: Tue, 09 Sep 2025 15:49:41 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:70af3fdc6755e6c9adb12b4251b35c64d496868ceccf8101122a91c885168db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99efc62314b386ec7058381549cfb4fb4f4179ba39d452b3d6b902207f55d0b4`

```dockerfile
```

-	Layers:
	-	`sha256:144b53d3ca81bbd37aba50e622e240972520a6756844f87299e5d427837ea25c`  
		Last Modified: Tue, 09 Sep 2025 18:57:23 GMT  
		Size: 2.1 MB (2093760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4915af1e647cb1cbeafff4d401a761dbcb79605cb5a91f365e9baa038bf6bb8`  
		Last Modified: Tue, 09 Sep 2025 18:58:08 GMT  
		Size: 22.1 KB (22108 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts` - linux; s390x

```console
$ docker pull haproxy@sha256:b17cc63d2883f8f2c96b099fc92cbc0a221d8c6611967128ef4e216d022a2483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42411970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace9f853cd255d1a6326a2e7cf77dfaf988927592768557458fbb0a78a8f187a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 13 Aug 2025 17:13:28 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307fb7f4966f1d48604abeea53dc31cf0d4083c5a8be502d9d579c4c4dfc6fc2`  
		Last Modified: Mon, 08 Sep 2025 21:53:52 GMT  
		Size: 1.3 MB (1292967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcad8b9064876b58201eee23caa04b9792e730cdcb67f0a24e91158749476d78`  
		Last Modified: Mon, 08 Sep 2025 21:53:48 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab084030f2dde04f1597930aa34a9b7afa17199d183fc701d0f8b1fd8d999fa`  
		Last Modified: Mon, 08 Sep 2025 21:53:48 GMT  
		Size: 11.3 MB (11284465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822c899d1b232ae1ca024ba6f5ba1f6ed512c2224b9c701990b27233274bff98`  
		Last Modified: Mon, 08 Sep 2025 21:53:49 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts` - unknown; unknown

```console
$ docker pull haproxy@sha256:65d23a508775b05881907759bb1197c26c2ae33eeb07ddbd096c18502945e53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97c32cdb67cad212f4f6cf63222c3167938bcb585cad5a42e471808496619f8`

```dockerfile
```

-	Layers:
	-	`sha256:bac46d5d01316c8f603e6ddf8e7f8e5ba467ccf1ccae5f1438ddb41c711fe732`  
		Last Modified: Mon, 08 Sep 2025 21:59:28 GMT  
		Size: 2.1 MB (2101261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f24544af6c6c0711870d6c0049e416f46a65f40d0451754610fb2b34fc536204`  
		Last Modified: Mon, 08 Sep 2025 21:59:29 GMT  
		Size: 22.0 KB (22036 bytes)  
		MIME: application/vnd.in-toto+json
