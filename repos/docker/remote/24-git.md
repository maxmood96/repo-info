## `docker:24-git`

```console
$ docker pull docker@sha256:2860bd7ac6d1eee84f8438b6994230ca87a0a75d1392908df36b8c264b82be6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:24-git` - linux; amd64

```console
$ docker pull docker@sha256:2991111e5ad968c6bbad31a72bd14ba8499b28507e8b12c4c5d428ee9961ce11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127786359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6fcc4e6a5eaa635024cb81d4a049831b692cf372e9d464ab1bbff8a0d94cf1a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64'; 			sha256='2f61856d1b8c9de29ffdaedaa1c6d0a5fc5c79da45068f1f4310feed8d3a3f61'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv6'; 			sha256='69ce7a9753e53856b92bb75823893e116d993f92f1e389e0f1a4dae45f79296e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv7'; 			sha256='82138d1784ba968b59546d19acad85dbca7bbe67f6614ffb84ef4c3cd72f7a4a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-aarch64'; 			sha256='c86efb0d6347b72af6690f06fbd30ed17023fe67e23e28647cacb4b3f6bfb451'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-ppc64le'; 			sha256='4f4dfc8d6834edfd884d8d5326db0bae3a48f25fe31403684be07faea8822aed'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-riscv64'; 			sha256='575f13c8d567d38bf83fc0885163a505564517f013f01f2e5cd12d989cf88fee'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-s390x'; 			sha256='cbcced8480b8c2ed90c0eb3d4d6c45d6ce8ea0d590961b7ef303bd136c8e85c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 Feb 2024 19:50:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2024 19:50:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9abf156005b395a9b2cb60067c629f2538eb1500f07968aad27c86817d1c8c`  
		Last Modified: Fri, 19 Apr 2024 22:50:26 GMT  
		Size: 2.0 MB (2026161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f148a0e956fe8e5fdaf38102356650d53db80668ec02dcf6993910fd01d7cdb3`  
		Last Modified: Fri, 19 Apr 2024 22:50:27 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3005df19bb53f501153e62138c8bb93faf3b920b2b92f70b101a96e52e71f46a`  
		Last Modified: Fri, 19 Apr 2024 22:50:27 GMT  
		Size: 16.4 MB (16410668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49177a2e5195a99f0d3fee6ae4f653b823f18e87426b485df737440fc28452a4`  
		Last Modified: Fri, 19 Apr 2024 22:50:27 GMT  
		Size: 18.1 MB (18078217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1516c0b1ff90d894dddb8095ca8477de9da8e13f96b8978c63d7bbe4e9e5ee`  
		Last Modified: Fri, 19 Apr 2024 22:50:28 GMT  
		Size: 18.7 MB (18669504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3bfe2d61447b2a92fc4fd16b1078721b54ee68ff50baac6a0e57916e3e5374`  
		Last Modified: Fri, 19 Apr 2024 22:50:28 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbebd29dfc6f4881574a161239e4ec1af765cbe742dcba20e5e8deebafd25d84`  
		Last Modified: Fri, 19 Apr 2024 22:50:28 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d15527f729ba1fcb911bdc5be84066cb3fe3fb43369d79cc8c75cd9fe123fcf`  
		Last Modified: Fri, 19 Apr 2024 22:50:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716672717e3620a11287fa83911025f3709c92f78dfdf11698ecbcd9ad65409`  
		Last Modified: Fri, 19 Apr 2024 22:56:24 GMT  
		Size: 14.4 MB (14355101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d4137a77972c9ce5b62eef213837fcb1080f0c70d5a1834315c03b0b1c7a00`  
		Last Modified: Fri, 19 Apr 2024 22:56:24 GMT  
		Size: 89.1 KB (89135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828f2499260d4e6f8d53d831c98dbcce84ed5f752b84c329350ae4862734c951`  
		Last Modified: Fri, 19 Apr 2024 22:56:24 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b944c9428afb09c32173d8e5583efb985cfb1d510cd315f2ef9266c33da9912`  
		Last Modified: Fri, 19 Apr 2024 22:56:25 GMT  
		Size: 54.7 MB (54740516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6177e7db147d6b588249e713476bef3e9af6b1152f3a376b6d11d65277c3f532`  
		Last Modified: Fri, 19 Apr 2024 22:56:25 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38dd0d0c73c040399d8e46d08e4d0af0ac43294a6e97ed19f56a5d1733672b2b`  
		Last Modified: Fri, 19 Apr 2024 22:56:25 GMT  
		Size: 3.3 KB (3252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:e7619c0ce20bb58e048b1d6ae8082bcdd62fee9e6433657354505211c6c3d718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.8 KB (875835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdda8b7f249bc43e391aec33b7a7bf32614d8c1870574bd021bccca10172fd2`

```dockerfile
```

-	Layers:
	-	`sha256:4cd33a2c79f59dfc01e871b15c68b5a666f1d7a70a0254d02f7f627fc3b99a80`  
		Last Modified: Fri, 19 Apr 2024 22:56:24 GMT  
		Size: 839.3 KB (839266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4432a86786317509d416ee12160c92df931460abf8958eee62bbec77065e0a3`  
		Last Modified: Fri, 19 Apr 2024 22:56:24 GMT  
		Size: 36.6 KB (36569 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:5f507836da701bfa4edd2f231d7cdb4c6014b07476e3f5b176bdb388542f2d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120681174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e926f92a6a15945c1580b15a10c39abc22da0516b9d5649cc9c8fc39c02695f5`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64'; 			sha256='2f61856d1b8c9de29ffdaedaa1c6d0a5fc5c79da45068f1f4310feed8d3a3f61'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv6'; 			sha256='69ce7a9753e53856b92bb75823893e116d993f92f1e389e0f1a4dae45f79296e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv7'; 			sha256='82138d1784ba968b59546d19acad85dbca7bbe67f6614ffb84ef4c3cd72f7a4a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-aarch64'; 			sha256='c86efb0d6347b72af6690f06fbd30ed17023fe67e23e28647cacb4b3f6bfb451'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-ppc64le'; 			sha256='4f4dfc8d6834edfd884d8d5326db0bae3a48f25fe31403684be07faea8822aed'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-riscv64'; 			sha256='575f13c8d567d38bf83fc0885163a505564517f013f01f2e5cd12d989cf88fee'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-s390x'; 			sha256='cbcced8480b8c2ed90c0eb3d4d6c45d6ce8ea0d590961b7ef303bd136c8e85c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 Feb 2024 19:50:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2024 19:50:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD []
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d295e3a3b46913424fde607d3e771752e6b7eeb8e288b8d9551c5d557d80db1`  
		Last Modified: Fri, 19 Apr 2024 22:54:01 GMT  
		Size: 2.1 MB (2116782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6506740d0b54257c16df0fad45597132ba9e2a5e48bdb69e44b58e893a42ecce`  
		Last Modified: Fri, 19 Apr 2024 22:54:00 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2209e541a333086ea1fc890eeb8c276cabcad58ea966e63ca494495e578b9e`  
		Last Modified: Fri, 19 Apr 2024 22:55:05 GMT  
		Size: 15.1 MB (15132927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784a4a44341b40b9901ef6c26dd8d8f0e549d95cb8379341e6dc7173cfd1647b`  
		Last Modified: Fri, 19 Apr 2024 22:55:05 GMT  
		Size: 16.9 MB (16915894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cbdb391f4105aa796aabd8064bbac3af18e288b1c0a10686120caf396cb144`  
		Last Modified: Fri, 19 Apr 2024 22:55:05 GMT  
		Size: 17.6 MB (17631473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25aff38aaef9268c71c7ec3ec2773b12b858c8a494913706d3a3e5a9a472b081`  
		Last Modified: Fri, 19 Apr 2024 22:55:04 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0148fa1863299bae9a0d1d4221faf3feefaa53653610a98bfd8c7125461b93`  
		Last Modified: Fri, 19 Apr 2024 22:55:05 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90abd1cc822449c3ad7806e1bafa7de7ce450b0e8c13f67ed6014b7bec996c8`  
		Last Modified: Fri, 19 Apr 2024 22:55:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440388f6dfc1c0df838bfd4c91cbebd9de970bf1b6d7d1935dd64422dafe1f17`  
		Last Modified: Fri, 19 Apr 2024 23:35:36 GMT  
		Size: 14.3 MB (14316638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99850dcb0d690aab7c2606912fab4e26e34c856f21a75d7c44846eb9b04e8a8`  
		Last Modified: Fri, 19 Apr 2024 23:35:36 GMT  
		Size: 88.4 KB (88357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970c995fcff6a2930de6e0da7cfc35d5e74c23547399ae482083576e66696d02`  
		Last Modified: Fri, 19 Apr 2024 23:35:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864222c21c1672308895891eec6588c596f15ccc9ad840debdac13804e508eb1`  
		Last Modified: Fri, 19 Apr 2024 23:35:38 GMT  
		Size: 51.3 MB (51305384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c70702674e5428958e7743068b7802dc391ce3fd01bc5f4a63f43e624646008`  
		Last Modified: Fri, 19 Apr 2024 23:35:36 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c1b32e92b5c99a7e95adaac77b60c3e05e32a47b3602ca170db4859b2cb2cf`  
		Last Modified: Fri, 19 Apr 2024 23:35:37 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:c83ff33b30502f20f57de333dcb6d745ad37cbb54b5dc6ff2422780e2bb1be14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6c7a579f72aeead4749575176484c85e6c1346cca964d4400a8c5ffb48b533c`

```dockerfile
```

-	Layers:
	-	`sha256:c1d24f9163060a0fbccd5351cb43a7592232af838f07a9fa288585fdc376ad01`  
		Last Modified: Fri, 19 Apr 2024 23:35:35 GMT  
		Size: 36.6 KB (36583 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:7d7005ca8acebfad9c7ba97efc8dd2c3b84d8dbdcfcd83985d971a47f23394cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118889903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a4578d8185ac59c4959ae9d1b7aa26d9a19d6d9ab55b9770866752989a8c5e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-amd64'; 			sha256='32f8f17eca35bf2efe6c0e47f40e4692a876f34531b421efc984799a5b41226e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v6'; 			sha256='7a23989eb26ad27e1b7c11a38dda6a8e6a94562969c19165cf8f49e70203ad20'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm-v7'; 			sha256='53b2d827510c6cff41503454caeb0d6613d5ed11201ba10f5ad6c22466cc178c'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-arm64'; 			sha256='38bf0ea9c48743edb8243f14272be65a2bad7092228068337aea584309ea664c'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-ppc64le'; 			sha256='847e665e8f1fef3b85c6a5139d9bc57a81bae84d6a882d3ed71e2b5e2bd94bf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-riscv64'; 			sha256='c853c01f71b6b778b430d985813069d1ca4f2b2e7e039723298350839a556d2b'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.linux-s390x'; 			sha256='6ed2520cf5b7b4b1a985622c61b62d8f65634634b0ef8b3d0594dc1550032d9d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64'; 			sha256='2f61856d1b8c9de29ffdaedaa1c6d0a5fc5c79da45068f1f4310feed8d3a3f61'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv6'; 			sha256='69ce7a9753e53856b92bb75823893e116d993f92f1e389e0f1a4dae45f79296e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv7'; 			sha256='82138d1784ba968b59546d19acad85dbca7bbe67f6614ffb84ef4c3cd72f7a4a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-aarch64'; 			sha256='c86efb0d6347b72af6690f06fbd30ed17023fe67e23e28647cacb4b3f6bfb451'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-ppc64le'; 			sha256='4f4dfc8d6834edfd884d8d5326db0bae3a48f25fe31403684be07faea8822aed'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-riscv64'; 			sha256='575f13c8d567d38bf83fc0885163a505564517f013f01f2e5cd12d989cf88fee'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-s390x'; 			sha256='cbcced8480b8c2ed90c0eb3d4d6c45d6ce8ea0d590961b7ef303bd136c8e85c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 Feb 2024 19:50:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2024 19:50:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD []
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62203ebc003cf77a4ff92a3c67a89cd14dcf1adf84fb125d2f3329ad08ad9a61`  
		Last Modified: Sat, 16 Mar 2024 15:21:10 GMT  
		Size: 1.9 MB (1896160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8418dd6a88f431ade9efd4277500a4c6483d9ac98459ff95a86dbfde7d02e2a`  
		Last Modified: Sat, 16 Mar 2024 15:21:10 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8cafec6b550d963e5bc382529ada61abf96cd399412c7e2fd100417257b6a5`  
		Last Modified: Sat, 16 Mar 2024 15:29:41 GMT  
		Size: 15.1 MB (15129219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c9098c924074c78e42682a59645f986d3326573d5cc412311f75686332a5a9`  
		Last Modified: Fri, 19 Apr 2024 23:18:08 GMT  
		Size: 16.9 MB (16901898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8688f7f7fc4ebe50a1b18066b74551fa63fbefd7bb5803f9286d0bdcb4536b`  
		Last Modified: Fri, 19 Apr 2024 23:18:08 GMT  
		Size: 17.6 MB (17616617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac9e2e5d605e94fbf9cb59c0e285542cb9610bf57402fcffced9aaf5f45f88a`  
		Last Modified: Fri, 19 Apr 2024 23:18:08 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6533315ac20d4f91f0d5dd008a6a281fad5073c7f434319df92850490b0bc12f`  
		Last Modified: Fri, 19 Apr 2024 23:18:08 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0c543f3293cf4a9bda2fb98a6e5840d5f7ccdea3fc79e049180c9234d6081d`  
		Last Modified: Fri, 19 Apr 2024 23:18:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6755db006e16801554e6a879fa1e782188da10b344140f813d863e4454f528f2`  
		Last Modified: Sat, 20 Apr 2024 00:11:28 GMT  
		Size: 13.0 MB (13029114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0b8b0f903f9a9b59ce2e17c74f9c50135d6f84f936bc8d20b014a4e50244e1`  
		Last Modified: Sat, 20 Apr 2024 00:11:27 GMT  
		Size: 84.3 KB (84282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610ebb2a093e9ba8942ac38a11e83cf7be904eaaabdf8d6947799dc22746c2f2`  
		Last Modified: Sat, 20 Apr 2024 00:11:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78910a0ce50ebbab9f089d19848c875dd1960e13821a22cf12be08a6c1b8faa3`  
		Last Modified: Sat, 20 Apr 2024 00:11:29 GMT  
		Size: 51.3 MB (51305391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c481048777b9d62e1fc85f2e74d05c68ce54af96cb7a18c2620986cff3a6cb`  
		Last Modified: Sat, 20 Apr 2024 00:11:28 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ebb4dbe050ab34059a8764155c10f46d1ecb4e0d71afccfcafe6a56f4f8a3e`  
		Last Modified: Sat, 20 Apr 2024 00:11:28 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:fb765d25880e509badc514d0d8ed08421d3ec2eaecf10cf6d410177df1ed66c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **873.7 KB (873662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bd9e526fb02227b285b10f965475d97fae7a23e29cdea96eba4df780c75728`

```dockerfile
```

-	Layers:
	-	`sha256:212b931470c7c00da51dd4a5719eedc4cb63b4e16147042fc3a7ea295e83567d`  
		Last Modified: Sat, 20 Apr 2024 00:11:27 GMT  
		Size: 836.9 KB (836859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b38f7f9657f423c5b790c4dc600c9a3999e21cc34d4cd792235f50ffa2a2f14`  
		Last Modified: Sat, 20 Apr 2024 00:11:26 GMT  
		Size: 36.8 KB (36803 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e711bd399d3d6b4f8ed7570d63d250be83d89baa4f675b9b2134ca0a23bd4791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117037646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4f319a2078544a2434661aefc95a903f3b6584f5cbeb78313798638d2c6ba0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-amd64'; 			sha256='3e2bc8ed25a9125d6aeec07df4e0211edea6288e075b524160ef3fd305d3d74c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v6'; 			sha256='643063c656098e312533fe5ee3411523fa06cc3926bd2e96b4c6239b9cecbf88'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm-v7'; 			sha256='8d42e7823237e777b121070fda6ad68159539aa6597aedfa7630384643ad6f9a'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-arm64'; 			sha256='3ba35a5d38361a64b62aeb9d20acc835ff6862a711cb438e610026b29c0ac489'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-ppc64le'; 			sha256='1d16f7b15706d98523889a1ca50e9dfc44bbaec1f736d883a0528805795b9de2'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-riscv64'; 			sha256='202221c9b7fb881d092986e8ec2497ee71729f17c4afd912384a086af700e1ad'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.linux-s390x'; 			sha256='71d7c39192b1b07790eb71e46742cc69a559f3eb00a1512f4a8d2ea1067408da'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64'; 			sha256='2f61856d1b8c9de29ffdaedaa1c6d0a5fc5c79da45068f1f4310feed8d3a3f61'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv6'; 			sha256='69ce7a9753e53856b92bb75823893e116d993f92f1e389e0f1a4dae45f79296e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-armv7'; 			sha256='82138d1784ba968b59546d19acad85dbca7bbe67f6614ffb84ef4c3cd72f7a4a'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-aarch64'; 			sha256='c86efb0d6347b72af6690f06fbd30ed17023fe67e23e28647cacb4b3f6bfb451'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-ppc64le'; 			sha256='4f4dfc8d6834edfd884d8d5326db0bae3a48f25fe31403684be07faea8822aed'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-riscv64'; 			sha256='575f13c8d567d38bf83fc0885163a505564517f013f01f2e5cd12d989cf88fee'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-s390x'; 			sha256='cbcced8480b8c2ed90c0eb3d4d6c45d6ce8ea0d590961b7ef303bd136c8e85c9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 23 Feb 2024 19:50:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD ["sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2024 19:50:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD []
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b275a3377f65492f727dc46aa2b70be6ec8ff96583fcd9a7b699692b5170bc`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 2.0 MB (2019704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c53acdebd8fb391eae546ed72149f049f8ab4d594f12c74c49be04cc3b9708`  
		Last Modified: Sat, 16 Mar 2024 04:06:08 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e243595b6a4a5354eda3c1c4af2133475005f29ef8acc4da4821fc7fff21a2`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 15.5 MB (15459111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1ea7a6c39e124859c5e26c544d7aff02e08d3965595d626d90a9d54bb420cd`  
		Last Modified: Sat, 16 Mar 2024 04:06:09 GMT  
		Size: 16.3 MB (16349525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47b1caf1176e9021db1cb4a82d6649e1b705faee7a338167eca525758838a70`  
		Last Modified: Mon, 01 Apr 2024 23:55:32 GMT  
		Size: 17.0 MB (17047154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec55f0503b8574ce2c2730d43d1ac8c8ff40891ed453b65414966d92db0039a9`  
		Last Modified: Mon, 01 Apr 2024 23:55:31 GMT  
		Size: 550.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105a3a528ba6190cc80253e5738544cdee4e3186f8365ddffa1b57426ab1e410`  
		Last Modified: Mon, 01 Apr 2024 23:55:31 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d1221d8f75e2a55019877391fb1f88e6badcb6f83ad57aea8e3ddd65c7d886`  
		Last Modified: Mon, 01 Apr 2024 23:55:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9038749b2280256c7facd54ccf1f785af223e2960b15008ee3b9caa3ac247610`  
		Last Modified: Tue, 02 Apr 2024 04:04:51 GMT  
		Size: 12.6 MB (12631528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9e5e7c0c17da379d92302edefaa331040fa89d93787c6211b2d4f82164ba7d`  
		Last Modified: Tue, 02 Apr 2024 04:04:51 GMT  
		Size: 98.4 KB (98393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133636a3b2b44c429755f697a32e8f4977e95da99fcc7273014e83fbad83a17b`  
		Last Modified: Tue, 02 Apr 2024 04:04:51 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6478543edd40267e447974604047de0974012227f17df5d77f0f000c04d2e2`  
		Last Modified: Tue, 02 Apr 2024 04:04:52 GMT  
		Size: 50.1 MB (50076181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04387ca50902bd618ea4f1346802aa0aae9ed03a4462f7e1fa2b56b899265f11`  
		Last Modified: Tue, 02 Apr 2024 04:04:52 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7092c1957a2d70f60ee43ad6f0ad198f6c1d3a70a05f22625f783cb09edb15`  
		Last Modified: Tue, 02 Apr 2024 04:04:52 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:d3a2cd8007a07c6a1820cff96adba0ef9b576c310f458dc24051505409a79e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **868.5 KB (868512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a2d8bae0b9b433fb7ec1fa95e75000ec93105ec8edfb7eaafbee498c071739`

```dockerfile
```

-	Layers:
	-	`sha256:498fdff4acbff89737d0275078c6567cb97b3864e3468b29129509dffceab399`  
		Last Modified: Tue, 02 Apr 2024 04:04:50 GMT  
		Size: 831.9 KB (831867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4cc747b305140fd31a7926683edbfd5b07a980145198bc2deccee3e66e18086`  
		Last Modified: Tue, 02 Apr 2024 04:04:50 GMT  
		Size: 36.6 KB (36645 bytes)  
		MIME: application/vnd.in-toto+json
