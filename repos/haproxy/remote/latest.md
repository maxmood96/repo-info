## `haproxy:latest`

```console
$ docker pull haproxy@sha256:d6a7fd1cc98d1c287107dcf95391c700a9a8c2932e0a0d79b405cc204e497014
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

### `haproxy:latest` - linux; amd64

```console
$ docker pull haproxy@sha256:b4f597be92338bf25ffa3ef352e762eae04b9042b00a2305d61bfeaf4bdd650b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46912545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef5daca695b2f7c5211890760020d82de78416e893e7e32eae82264f8d73d4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 31 Jan 2024 18:13:30 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341cf697875fbeaa9decd917e69d344b77697476f38c741b39e22db6f2d5283f`  
		Last Modified: Wed, 31 Jan 2024 23:55:25 GMT  
		Size: 3.3 MB (3299237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb447692b623bff07e46b97320c34bae7a7ea7f576489d90d5687af86af212f`  
		Last Modified: Wed, 31 Jan 2024 23:55:25 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e73485cc2c7f90e650918a480cfa6ae5d97700995ba06bd076c2a8dcf273e1`  
		Last Modified: Wed, 31 Jan 2024 23:55:25 GMT  
		Size: 14.5 MB (14461202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2a73a9b5e1c5afeac1f7390ef8437c448e652cc4be1041d9319fa404303548`  
		Last Modified: Wed, 31 Jan 2024 23:55:25 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:809f2cd7043b875df435fa90a660782670628979288b5e59b6cde546505b98dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3143708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9bc06ac31e13df3cd0067c3355e3fe19b70e12d0dfc9e66d67603679d96150`

```dockerfile
```

-	Layers:
	-	`sha256:0bbf4c2c93cb0e155e146240afc84ad24724de6e361101233ffddbbd221833fb`  
		Last Modified: Wed, 31 Jan 2024 23:55:25 GMT  
		Size: 3.1 MB (3122040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e702adda6e81f9693687ca87234b6ed2a2ad95f6184b5bb4dd75d895697dbca5`  
		Last Modified: Wed, 31 Jan 2024 23:55:25 GMT  
		Size: 21.7 KB (21668 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v5

```console
$ docker pull haproxy@sha256:8e6bf54b236d5c3f8b49417625790c9ccb7b042989923999f21f7139c067bd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42768017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392fa1135f7238b4d20fcf10c048f9da2039fe3a5ab7de963028a731ab7182bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 31 Jan 2024 18:13:30 GMT
ADD file:557a5348da1e680593a9ba709ef059b96baf15e0c89d8f8343e97bf008d9dc05 in / 
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:b508f3272b9b70b8dd19c621a4da1be63880a1f6412063787647ceeb464d772a`  
		Last Modified: Wed, 31 Jan 2024 22:48:00 GMT  
		Size: 26.9 MB (26909323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ae3932debb1bb76ad7429082b66becd7db0890710f001178ebe6f782ee3dac`  
		Last Modified: Thu, 01 Feb 2024 11:49:27 GMT  
		Size: 2.9 MB (2874507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9a50d0639f526664573d09f758fc725e20d4a405a86f72771686640c82b2c0`  
		Last Modified: Thu, 01 Feb 2024 11:49:26 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6a9576d6022914bff1ab6029438790fe4658781207af7d921c9f3bb0c99347`  
		Last Modified: Thu, 01 Feb 2024 11:50:23 GMT  
		Size: 13.0 MB (12982548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38e6243bac9cf93533ef8c3f4b8bc3e2feea3e6a1ccbbb64c54044b222ba3ad`  
		Last Modified: Thu, 01 Feb 2024 11:50:23 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:90d6b335b5b658c18d21a2ce1e057c5d84fd4ba8e52f6fd0bad09c2e659e4440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3118361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20169c5de143dfb64223e202a0166c4c597fd60eef85abc27e7f9385c5aca347`

```dockerfile
```

-	Layers:
	-	`sha256:0be04b16e75d273108c585f69a5356e6a8ac90e4a8ff799f49eb0365e1a4340f`  
		Last Modified: Thu, 01 Feb 2024 11:50:23 GMT  
		Size: 3.1 MB (3096748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a147837f889bd57ca037062349885727245b923dffc6cf743cf625cb7edc99c1`  
		Last Modified: Thu, 01 Feb 2024 11:50:23 GMT  
		Size: 21.6 KB (21613 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:b0155636476807ac1ce7ffe6d97d294c1b22f99ff3783e211e0390e797c37b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40198715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b058f6bc8eaf99b9b06e65e240ed062ca92311d3e8a368925b97c0f0cd67564`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 18 Jan 2024 18:13:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 18:13:47 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Thu, 18 Jan 2024 18:13:47 GMT
ENV HAPROXY_VERSION=2.9.3
# Thu, 18 Jan 2024 18:13:47 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.3.tar.gz
# Thu, 18 Jan 2024 18:13:47 GMT
ENV HAPROXY_SHA256=ed517c65abd86945411f6bcb18c7ec657a706931cb781ea283063ba0a75858c0
# Thu, 18 Jan 2024 18:13:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Thu, 18 Jan 2024 18:13:47 GMT
STOPSIGNAL SIGUSR1
# Thu, 18 Jan 2024 18:13:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 18:13:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 18:13:47 GMT
USER haproxy
# Thu, 18 Jan 2024 18:13:47 GMT
WORKDIR /var/lib/haproxy
# Thu, 18 Jan 2024 18:13:47 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72699e14d5884fdb9c47f8e9de304bf9f9255c8b015ded71609d46db00c48372`  
		Last Modified: Fri, 12 Jan 2024 17:07:54 GMT  
		Size: 2.9 MB (2903597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08524ad81bbccfc9ffa2997a7d03ed0483e6690ebd2d17605297c268d8ee09b`  
		Last Modified: Fri, 12 Jan 2024 17:07:54 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a72c8e87c2b964eb0594e1bb3566a2a267354b0808eb547cfe892879555a8`  
		Last Modified: Fri, 19 Jan 2024 09:10:24 GMT  
		Size: 12.6 MB (12575349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f048d01242c0da2522b8296ee7e5c75c8b9c1619e1ecc2232577d8a7443f25`  
		Last Modified: Fri, 19 Jan 2024 09:10:23 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:bbfce196492586b75600c5227ac5847735665ac2fa50fb0bdc39121c4d3f2481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3118211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2966d529b78d2084fdf4253e36318048b645bb02b1de984623f66c7ec543b5ce`

```dockerfile
```

-	Layers:
	-	`sha256:6ee236d008c092d5480e5b43f88e05ef7298352458f6b912d1cf57be47d62b1c`  
		Last Modified: Fri, 19 Jan 2024 09:10:23 GMT  
		Size: 3.1 MB (3096598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7fb4a893df7b40efa58213a6ed3ef8118987a8a11d50d252dfe4ebff11be7da`  
		Last Modified: Fri, 19 Jan 2024 09:10:23 GMT  
		Size: 21.6 KB (21613 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:e394097062e0d99e70660ad763238e7fa8692023ad69a1b1c8b6088376e6483e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52083886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dcdb44967cd37a7f57a480c8bcbfe793c268e1a9faeb86243be77e2f3929665`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879b6fdeb9ffe3b5dd6fa40fb65abd8eb0d42046b3cfe636122f0a7ada20549d`  
		Last Modified: Tue, 30 Jan 2024 00:04:52 GMT  
		Size: 3.3 MB (3314061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2bf2d6336d8e295f05073a93921611ea4837171c7d4d3256de3554f7514eb7`  
		Last Modified: Tue, 30 Jan 2024 00:04:51 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476cb21a60e694a00d7534a0ef5cb474040e33d6bcb47fd1638b0197e04de4c3`  
		Last Modified: Wed, 31 Jan 2024 22:35:50 GMT  
		Size: 19.6 MB (19610850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460cfc553d31327d9d962f78154959f927483e48d675529e8896d1f29f53a3a1`  
		Last Modified: Wed, 31 Jan 2024 22:35:49 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:92d724edf9c74e86b9595df05ac3318c592fdbde18e56261605da92b1e25798c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3118734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d586fa54d9b0c7bf5f010373b43f3499eba262bcedffa97d3c95d87c3bafc03`

```dockerfile
```

-	Layers:
	-	`sha256:eead5eee8eeade77bdfcc57633e571b3a125a03f03a0b257362debd2c78fc619`  
		Last Modified: Wed, 31 Jan 2024 22:35:50 GMT  
		Size: 3.1 MB (3097219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aec9bf02dac11387b3f000e5626b7b908d045f551ba4d596d04a6e14f900f6f`  
		Last Modified: Wed, 31 Jan 2024 22:35:49 GMT  
		Size: 21.5 KB (21515 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; 386

```console
$ docker pull haproxy@sha256:ba16adc2419870b2c46dcd7e481676d7484799f88d213ff9f2944215d298b33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47162845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2125a59d055f045738e3fa505a6ae0978be0069b05d6cb8b42672ddf0d0143ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 31 Jan 2024 18:13:30 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66d1fcdb604ca9d0548c0ba944d405d112544d680ca16d3f26316c1027cdc75`  
		Last Modified: Wed, 31 Jan 2024 23:55:32 GMT  
		Size: 3.3 MB (3304772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb447692b623bff07e46b97320c34bae7a7ea7f576489d90d5687af86af212f`  
		Last Modified: Wed, 31 Jan 2024 23:55:25 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47071acc76f0e7ef2fbfbbcddcc4b1ceccaf06941406b247814e808cf79f72c`  
		Last Modified: Wed, 31 Jan 2024 23:55:32 GMT  
		Size: 13.7 MB (13691413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dfb8b72c3dd550449204f8206bf5ae65b29c146df91e08b9f83668699a5ff9`  
		Last Modified: Wed, 31 Jan 2024 23:55:31 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:304afb75f6110585a0936ed768f5067f26e13b9937f02d9e7010f164482307b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3137997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6306446320dde1271f819bbf756a585e59fb6c98651ff7abb94e3db8a9f0ea7`

```dockerfile
```

-	Layers:
	-	`sha256:a3c8be24c122f01fff059373ac5821d2149c00b1ad237ef06f9d068413f775a8`  
		Last Modified: Wed, 31 Jan 2024 23:55:32 GMT  
		Size: 3.1 MB (3116372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842a8540facf28e58d30270d2ecc0fbdcb12769188c4d5db5f47dfc0f40303e4`  
		Last Modified: Wed, 31 Jan 2024 23:55:31 GMT  
		Size: 21.6 KB (21625 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; mips64le

```console
$ docker pull haproxy@sha256:1da502756bbedbfc83bd46747838ce6408302073a7606759851652a1b7919c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52098897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0d9c678367a10a15cdd12e6e439a6018bc23b33ea7b539f4d1c5a7aff14eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jan 2024 02:11:46 GMT
ADD file:61bc6da4a8a8247e6b88cf149051dbb04a6a5e6e1ffc5da16a85d1b4f24be297 in / 
# Thu, 11 Jan 2024 02:11:50 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:4f1541106f1f6cee2d65a870d8d3fbbaef35e04dbcb8abaa9623a9f7137a6ae5`  
		Last Modified: Thu, 11 Jan 2024 02:22:46 GMT  
		Size: 29.1 MB (29121397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51d164d9f7f99bfac86f3f1e825719aaa667bd2db1ad806316a227ca5d518c2`  
		Last Modified: Mon, 29 Jan 2024 23:05:06 GMT  
		Size: 2.9 MB (2890259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129afee63e2536bddd880daa0ff7b4bbf0ffc0ade7ec9fc0f5154e3800ffd09a`  
		Last Modified: Mon, 29 Jan 2024 23:05:06 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fb7690ac36ae502a3ec390537023dd1913bc40300a78b066d5b30979468164`  
		Last Modified: Wed, 31 Jan 2024 22:02:33 GMT  
		Size: 20.1 MB (20085602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1b471816afc3359b021edbd199cfd2fdd835c04a9a5c6855ab54931222e696`  
		Last Modified: Wed, 31 Jan 2024 22:02:31 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:2ab6ef8d102182b42e8d93f3fbe6d635a2e3d8b84a8d589874321f58f31f63b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 KB (21367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef140e09787b9c49871ac16234ce1bcc769cc8517814188090011aedf3d5797c`

```dockerfile
```

-	Layers:
	-	`sha256:416d835ba31c8e6ce4cc0854090e79ee93e45c6cc1b451bdf1bb06df6a5bf019`  
		Last Modified: Wed, 31 Jan 2024 22:02:31 GMT  
		Size: 21.4 KB (21367 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; ppc64le

```console
$ docker pull haproxy@sha256:20bb3a78fcd73a51a2d4ffe9f3de95f929f6bcf0969f97e2a816fd5eeb5ed5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51466210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aad7059f39380041ff6faf65f6d595694d0509ada09032b614a3fa55006ee85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Wed, 31 Jan 2024 18:13:30 GMT
ADD file:fca8b919a8d1e36420dd1e3f3e427aaaae28a2f57e46c27207acd8e3df0d7a97 in / 
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:dfeacd5cd8171f4516ea86dadfb60a372eabf49428dc23d2efdda68cff5b05e7`  
		Last Modified: Wed, 31 Jan 2024 22:34:24 GMT  
		Size: 33.1 MB (33142917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410845727ded5f900ee3452c226045e42284a20ca3d3496fbee010658de0e61b`  
		Last Modified: Thu, 01 Feb 2024 12:24:39 GMT  
		Size: 3.5 MB (3501455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f697c52c8337858337ee9b96542e0ee9af2640b925a54057b3e04bce2bb083`  
		Last Modified: Thu, 01 Feb 2024 12:24:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75992209e77e813d64b629c27f25d4ecd92c20e8e940030f77cf190c03a7d66e`  
		Last Modified: Thu, 01 Feb 2024 12:38:39 GMT  
		Size: 14.8 MB (14820195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded93648d3f154767fc29e97206d700cfdb2fbd021b2350e84dff6793b6dea3f`  
		Last Modified: Thu, 01 Feb 2024 12:38:38 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:83332a916a73e831d7c977673e37d10cdce18e5e9001835eca83d8be2a71027d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172bdd335e1e233fd8bece127df110b62cf24234e5b10f577bad60e14584aa7a`

```dockerfile
```

-	Layers:
	-	`sha256:ae4257e838baf36a7dce13b158368f3692f32998b6e7ecfcbdfc56ce085cfd75`  
		Last Modified: Thu, 01 Feb 2024 12:38:38 GMT  
		Size: 3.1 MB (3110568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f47b2fa5d7829e404767ea114391f703d50ac187d87ccbd38471b948920fb8d`  
		Last Modified: Thu, 01 Feb 2024 12:38:38 GMT  
		Size: 21.6 KB (21555 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:latest` - linux; s390x

```console
$ docker pull haproxy@sha256:c4314f2b7ec3b97d90adc3a172ca7a0a354595c1486fc911fd78bcbc242cd101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49174717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419d87c1b0739b5033d4b93d3ed3eeda41d22a395cfae6a2c888661fe0c4ff07`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:08 GMT
ADD file:65dbcebb09bfa0253ba47edc09622e132326164df51df5626ae3a06a0e5d179b in / 
# Thu, 11 Jan 2024 01:45:11 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 	groupadd --gid 99 --system haproxy; 	useradd 		--gid haproxy 		--home-dir /var/lib/haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_VERSION=2.9.4
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/2.9/src/haproxy-2.9.4.tar.gz
# Wed, 31 Jan 2024 18:13:30 GMT
ENV HAPROXY_SHA256=9c3892cc3c084ac4f00125ef22a151cf181416d84aa8a37af6af6aa0399096bc
# Wed, 31 Jan 2024 18:13:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update && apt-get install -y --no-install-recommends 		gcc 		libc6-dev 		liblua5.4-dev 		libpcre2-dev 		libssl-dev 		make 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-glibc 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) makeOpts="$makeOpts ADDLIB=-latomic" ;; 	esac; 		nproc="$(nproc)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		haproxy -v # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
STOPSIGNAL SIGUSR1
# Wed, 31 Jan 2024 18:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 31 Jan 2024 18:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 18:13:30 GMT
USER haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
WORKDIR /var/lib/haproxy
# Wed, 31 Jan 2024 18:13:30 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:a26174f024d942f0adb6db11b3ae9df606c112928e1b40e24779a0fdab24cb41`  
		Last Modified: Thu, 11 Jan 2024 01:50:51 GMT  
		Size: 27.5 MB (27491850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03e23f320166426205dd7165d90fc155bf504765f3ed7970ca61f0bf710164e`  
		Last Modified: Mon, 29 Jan 2024 23:32:39 GMT  
		Size: 3.2 MB (3156944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af9d64d83dd37593b87698551184753da7ec8280064b74a1e46a48bcda9d9c2`  
		Last Modified: Mon, 29 Jan 2024 23:32:40 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4a1f53b562b6cbab469d31fda2266dc0bddc0fd4dd49affc7f4baf6dc4a03c`  
		Last Modified: Wed, 31 Jan 2024 22:17:25 GMT  
		Size: 18.5 MB (18524279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d6849e7f842dcf704f626f6b5d5279a3d38bfaf301bfc2e4e1eebae069f42d`  
		Last Modified: Wed, 31 Jan 2024 22:17:25 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:latest` - unknown; unknown

```console
$ docker pull haproxy@sha256:e4ddbd1bc37c6722369c600b558183550a43810b896ded0dfaa476ecf6a0ea44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eedc390d1da70f9381267cadf173ac44997b8b76577dd64da0de4a7726dd6a4`

```dockerfile
```

-	Layers:
	-	`sha256:04b1af9d23f02d9bdb9ae3a414a178e96606c204c23a4701caaa563e0384f9bd`  
		Last Modified: Wed, 31 Jan 2024 22:17:26 GMT  
		Size: 3.1 MB (3111589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9caea6b0d19178bf5d2e9f499f1de7b8fe68aaff0607e13f5c80df9392253a`  
		Last Modified: Wed, 31 Jan 2024 22:17:25 GMT  
		Size: 21.5 KB (21501 bytes)  
		MIME: application/vnd.in-toto+json
