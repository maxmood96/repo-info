## `haproxy:latest`

```console
$ docker pull haproxy@sha256:fe334a7bfe18a5ed8bc81a52d93a49edf323469beb3acae1952f2fa5a19e4ca0
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
$ docker pull haproxy@sha256:55cba2c6cb85229d0760ef3776023cd4bdd372eca649b55e0499bb27aa3ec5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42055870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7599b2eac895b7dd959c9fdd8e0d00f87101375fda5f47fc072cf353c73d6d76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Sep 2025 17:13:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba904ad1b6b0d55b1f18a2363038c5c2a8873d97f1aab2d49055c705c72ed32e`  
		Last Modified: Tue, 30 Sep 2025 00:25:13 GMT  
		Size: 1.3 MB (1279298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cb4c3d3c7fea46412cfbb997d75ed3ee34eda6607f9e818a95d7b403719519`  
		Last Modified: Tue, 30 Sep 2025 00:25:21 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b37ff6db26fa9c57397ed5782d4241dcfd877870db17fc615ee6733222f058`  
		Last Modified: Tue, 30 Sep 2025 00:25:28 GMT  
		Size: 11.0 MB (10997168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c123f1579d0a31c24dc1635a32449fab25423428623ea10ad2f2a2d252044a5e`  
		Last Modified: Tue, 30 Sep 2025 00:25:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:6bc0d325845a58425c1db5d1c5e58c716680a26901dfee7e2025433f8bad6c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2121850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929bb93c48253236ae96db3b35ae2b6d42633db9ad5e39ce1ed287754b4abf48`

```dockerfile
```

-	Layers:
	-	`sha256:c31ccb0f950c78e641bb728e4a6342b08df4e8e32fd47df9188a911767d958fe`  
		Last Modified: Tue, 30 Sep 2025 00:58:06 GMT  
		Size: 2.1 MB (2099816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:343ac1f6bb4bb6250e2727dbe6fefff5f5115c4f34838e8ae3a848fb42885f2d`  
		Last Modified: Tue, 30 Sep 2025 00:58:07 GMT  
		Size: 22.0 KB (22034 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:e588f822894e1e02dca8df8c75d9ed089fb24747342ff3fc45c8d206007d8232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40291098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654cbb04032f5957307c3365f2b354e0f85431a5b177a6c66736fad3edf1e85d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Sep 2025 17:13:29 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
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
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d03f037ee3eb7552d0f39dab5bc4bb4eb4f16bd62982b5ce8f5c9738fd449e0`  
		Last Modified: Mon, 29 Sep 2025 23:55:05 GMT  
		Size: 1.3 MB (1262744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0427d9126547ad7bf15805d56e2a0dde0ce7758ba74f7cfa2ba4b151fe3c126d`  
		Last Modified: Mon, 29 Sep 2025 23:55:05 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e80134f6121db70d5962351d0cf2fe11548a890cde4a16fb13df7d838720c8`  
		Last Modified: Mon, 29 Sep 2025 23:55:07 GMT  
		Size: 11.1 MB (11080574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0848bcb625df5ac5f9d3535d574afa29c6b770cc79d7bc3e83d8f78efea6755`  
		Last Modified: Mon, 29 Sep 2025 23:55:06 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:b7a98d777ebc142e857838c5b95bd7f64bcac9d4a00de46119443508235a91dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988a4c18b4694e972c757282934796d3e3b36a964beab22c1c819ae045b6e1b5`

```dockerfile
```

-	Layers:
	-	`sha256:74ed21d8ec1d521c9dadd26326b4ab39454447836fa8ca183eb019b35c89e7d3`  
		Last Modified: Tue, 30 Sep 2025 00:58:11 GMT  
		Size: 2.1 MB (2102811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b2d6731a47453e755ef72c39978b7909c199c5c861fe8db065d43c5010c1aa2`  
		Last Modified: Tue, 30 Sep 2025 00:58:12 GMT  
		Size: 22.2 KB (22174 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b25f6d546e7f1e571ba7c705705d2d8f6f1d391ae150ffdb83e7cfa5813ab4bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38320192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4275b7bda2d89acc5e4107696fc5a12a779eee100736024d433f1f4f50f0a638`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Sep 2025 17:13:29 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
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
	-	`sha256:0289e98159900b326d4cedde367bf225e25835a3ad879647f17f922e43cfa884`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 26.2 MB (26212758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28473d9064e97951aa48279f76144313ecb67f275a632bff08c7b38126a06de8`  
		Last Modified: Mon, 29 Sep 2025 23:55:03 GMT  
		Size: 1.2 MB (1235933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87dced603f4ad40d22da8d161294c22f1152559cd3d08bb217bed547276e8ac`  
		Last Modified: Mon, 29 Sep 2025 23:55:02 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b084d0516e3598c853cdd3445734db7f6938e5dbce137ce0d4d1c06ad7181a`  
		Last Modified: Mon, 29 Sep 2025 23:55:03 GMT  
		Size: 10.9 MB (10869863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20fc44f00d6f771ed74fd6b3f767498c64f79d8bc2ae1b0197626ac35e14969`  
		Last Modified: Mon, 29 Sep 2025 23:55:04 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:e405fb8dce245b2c42e2d6e4d81979a5da092e4b28c5293395cb5a4e18a9be23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdaea657d8bd0102c58906c41efd7d62b477af4f4ffcab5338deeecfac41d0a`

```dockerfile
```

-	Layers:
	-	`sha256:20989b6d80a503faed94c7e155df0f69ac16d4e16e3695fde05b6d9105739bf5`  
		Last Modified: Tue, 30 Sep 2025 00:58:16 GMT  
		Size: 2.1 MB (2101252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd327fce5bf5894de902ebac98680e48832cba428f0f4845d5d7345106bb9fbe`  
		Last Modified: Tue, 30 Sep 2025 00:58:17 GMT  
		Size: 22.2 KB (22174 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:d7de0a159ddb4f9a08a5a7cb44f19cc36dd0df9f12f29e69b2dc6fd3777e27f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42333518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb97cf8bfd3c109a90bf10ddcbc7f93b55a535c07012ef69365f2d1a87b5f2f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Sep 2025 17:13:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db569fb272e487ef9dbfd5532c3e4674effd99287c36fbbad7c2d6bf887f20aa`  
		Last Modified: Mon, 29 Sep 2025 23:50:15 GMT  
		Size: 1.3 MB (1260910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41b9ba9d787be38d529b822f3517da04deb989fcd1a49a51b8a63e27f28d4e7`  
		Last Modified: Mon, 29 Sep 2025 23:50:15 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cf4fdae674fe799866d1f56ca5878758e3835428ca6c136042e56d1505faa6`  
		Last Modified: Mon, 29 Sep 2025 23:51:13 GMT  
		Size: 10.9 MB (10930128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69dbb8d2e6f69d14904b6d07d7bc01f83e423296a5b5ddcfc26d11d406cf192`  
		Last Modified: Mon, 29 Sep 2025 23:51:12 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:3012c8910eba818dcc9451812c45397a24bd817954a28942221c22758c502fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2122341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf345ba623843acbf35b27124224dc9d6bb2dae1553c166d0420edaef28ec64`

```dockerfile
```

-	Layers:
	-	`sha256:ac9b84d356c646dc620610760a001b3b7a0b4f6d3199f1d8bb75829fda1feca3`  
		Last Modified: Tue, 30 Sep 2025 00:58:21 GMT  
		Size: 2.1 MB (2100124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7a9961a2f51ae6c767aaaa1d6fc6c7065b514373032080ca148d48ab996a619`  
		Last Modified: Tue, 30 Sep 2025 00:58:22 GMT  
		Size: 22.2 KB (22217 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:81b9d0413f84c734b75eab7f206d00df107ee90cae7a71c4ddefb21dd1416ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43291944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc912870fcb133aa1dd459b84d78b003ea3f138e585acc77d25971b1065caff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Sep 2025 17:13:29 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
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
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094faae7e3bb52ffda035e6f3afba37d322e4110136c61e6c8199c4950080ebb`  
		Last Modified: Mon, 29 Sep 2025 23:51:02 GMT  
		Size: 1.3 MB (1286772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfdc9e671b5560e9ec0dd5d6851e4834e1c5efee49f9703573192d4429c4bf9`  
		Last Modified: Mon, 29 Sep 2025 23:51:01 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c478d0a28566046cd2bcc6f012f9fe8f2a0b4f8bc560a8ea95d72dc2e73d870`  
		Last Modified: Mon, 29 Sep 2025 23:52:01 GMT  
		Size: 10.7 MB (10709000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbf9179c7c260078a072ff005f4f5ddf5fd2c7beeb56e0ba53c19738012ec85`  
		Last Modified: Mon, 29 Sep 2025 23:52:01 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:2289491c6bf83e4bfeb606a32993558bacb91ef5255aac3ad754bc3b0773ee85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d7b0ee1da4d41c750899ae9407bdaa06b6e84d9d178e4bf064ebd933e7477e`

```dockerfile
```

-	Layers:
	-	`sha256:35cadbe61b0dd116c6baf9b62b56a62c54f5550a608529a1fafdf0aa8747d542`  
		Last Modified: Tue, 30 Sep 2025 00:58:26 GMT  
		Size: 2.1 MB (2096989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6fae710df13351677cdde145f38d9da9094c406836bd029dc0a2cbc88df3d37`  
		Last Modified: Tue, 30 Sep 2025 00:58:27 GMT  
		Size: 22.0 KB (21980 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:324df8ec59463b444a02887ebd4fa597f5b6db09b3f0d47dfb04d820b81cb9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46555404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40583d0518853eae7f4d3659c5c8045069f7eaa8ee7548a9d92f0fca505aca8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Sep 2025 17:13:29 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8621b5372170e7c7f5575243a6e2882e4eb49a8331460481face64523b404f`  
		Last Modified: Tue, 30 Sep 2025 06:38:23 GMT  
		Size: 1.3 MB (1309681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a56f93a85ea2dbf1f6d2176ea9d7354abd317452105e7e46370a328fe71630`  
		Last Modified: Tue, 30 Sep 2025 06:38:24 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae4438bfed6fb924a66e2980dc6a70a6f000a9697ad461b26e972a2d7c39b3d`  
		Last Modified: Tue, 30 Sep 2025 06:40:09 GMT  
		Size: 11.6 MB (11645632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b580776c35323314569f90a6858040a0d9e7bf06c6b94300a1703ff300b8194`  
		Last Modified: Tue, 30 Sep 2025 06:40:08 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:3e149b1b7b2356c152f6ad9ccb6beaabaf871582a5813d1cc63d0fedfe47e0ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2125473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9ed40a1122d2dd38c0504e3efb6ef648e39b6870a11ae49bb74c740604066b`

```dockerfile
```

-	Layers:
	-	`sha256:d430c6afb07b80412d110d39355620b0c7154982ff2d18fbfbb01c9d5c7d5fe7`  
		Last Modified: Wed, 01 Oct 2025 21:57:27 GMT  
		Size: 2.1 MB (2103365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96672815a843090d3a2b3b9a601d5d32698eeebbeb697170a0174dbd2d66b255`  
		Last Modified: Wed, 01 Oct 2025 21:57:28 GMT  
		Size: 22.1 KB (22108 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; riscv64

```console
$ docker pull haproxy@sha256:75510a61e0b948b23310602965f685c0df44ebc3e30dbac425d54d8caa144fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40172876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3217870e91881b56552693e97f4e9302095aa35eeff514302522fe58fefc1749`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Sep 2025 17:13:29 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56dd911c28dd47dcc9ad517210808993b101075eef803023196d6162faad493b`  
		Last Modified: Tue, 30 Sep 2025 01:47:10 GMT  
		Size: 1.2 MB (1247476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a061c9f0898afae9020548dc4a18dc8e83d4bfe3609ba6d5792b0acba789087`  
		Last Modified: Tue, 30 Sep 2025 01:47:10 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54901c922c0f929d3c8e359b2c8d98fb5607ba3b4000954656ae0475a21b901`  
		Last Modified: Tue, 30 Sep 2025 02:00:28 GMT  
		Size: 10.6 MB (10648259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c229be685a35a1210ea093e46a847836b67e5bb5c43bb0de12b9c98edee6848f`  
		Last Modified: Tue, 30 Sep 2025 02:00:27 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:321688e5691237697b212d9e044a056e17f1c7044068d196a9c4e924a8f6ddb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fc4ccdd840e3d24a84813179f96f662de9e40d64dde5154610cbaa75b916b4`

```dockerfile
```

-	Layers:
	-	`sha256:75afac3d590720f11a3ee821d0577d5123ec33d6f86a39e6eafa7951e97ac100`  
		Last Modified: Tue, 30 Sep 2025 06:57:17 GMT  
		Size: 2.1 MB (2093760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49f3b57948435421a85f8d9d6542fdb776f1f9089e8964a80a1461f1d8cb492`  
		Last Modified: Tue, 30 Sep 2025 06:57:18 GMT  
		Size: 22.1 KB (22107 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:db3fc5bb543bcb4f394b07464a38b784da3c8f5fa2abe1c1df7d2c1f8b7ef198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42428458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1245d7ac661044e191aa2bec017f981020c563bcfa00dfd574801b9fa11e86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 23 Sep 2025 17:13:29 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
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
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b487f227a091c3796afc02a0703e95600d4fe55afa849e5d315e98a2e54663`  
		Last Modified: Tue, 30 Sep 2025 06:17:08 GMT  
		Size: 1.3 MB (1294325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8518a3261a5ef607fdfa28b60b369789b62ce746e5a407c4936d8be8bd2949fd`  
		Last Modified: Tue, 30 Sep 2025 06:17:08 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b285d53bca755dc048be84521e54087b2a1fd71ef4b1072ba591cf5af5dc81d0`  
		Last Modified: Tue, 30 Sep 2025 06:18:26 GMT  
		Size: 11.3 MB (11295265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3a7f56bae390d1746ec2510f99277bf8819d748be3a08a98e110479b7da11d`  
		Last Modified: Tue, 30 Sep 2025 06:18:25 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:e62717d6d3e40048735359c484ea4dea839a532132818f8e804202bddf6ac18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd927d7177ba88e12ffbae45de0e46472206cfaff7cbee58574e775ee7c1bdd`

```dockerfile
```

-	Layers:
	-	`sha256:ae7b43c4bceb4a901d8582dd120e281c507f3246b7141bcdea812d02aa0be175`  
		Last Modified: Wed, 01 Oct 2025 21:57:33 GMT  
		Size: 2.1 MB (2101261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:855943a589d305bf6dbc900e39118e5e4c2ff787f0061a6841142a72682aec78`  
		Last Modified: Wed, 01 Oct 2025 21:57:34 GMT  
		Size: 22.0 KB (22036 bytes)  
		MIME: application/vnd.in-toto+json
