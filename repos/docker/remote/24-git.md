## `docker:24-git`

```console
$ docker pull docker@sha256:f0946124f996454f57736d1179c148fdbed06c985179c8dcce18cf46bdd1e5ef
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
$ docker pull docker@sha256:c7bfa9ea5f89087155d8eac5b84f5839ac4e3f0ad51585d01fce367a7fa246dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126336711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f497b0f9924c2b9b64035bae32b7b9ceedc54d98058cd3845b34d94c4c841fa`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 23 Feb 2024 19:50:50 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Fri, 23 Feb 2024 19:50:50 GMT
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
ENV DOCKER_BUILDX_VERSION=0.15.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-x86_64'; 			sha256='6fbaf6e93ccc43078a71a12db1d38224725cb5a9675391c38510355073f24066'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv6'; 			sha256='10b465c1771c262d372e24b09ed30fdc63687e35ae61c2365089e3998372a776'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv7'; 			sha256='b5bd40dfadf089617fe9cacb7a08d6fd5fae28e2a465191be1f25f22ffead344'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-aarch64'; 			sha256='de8c48203f4876fe3ae8bf27081a9aa69dc87de67a705f9d76c3a3ad776ed0c2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-ppc64le'; 			sha256='5810b3e6184032edbd21f12ed165ddecc823b8222ff5e4f6c55112af6f617c6d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-riscv64'; 			sha256='2c138daa9eaa909434c808018c4ab748a5f25caee16e3a7810fbeb3897b40878'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-s390x'; 			sha256='4084bdab8782e98c57a5f7aa7384699490048ce117dc7e70cad183702cc1645b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4f76e3a90f62a8c5ca873581e3e8f28d444b96f943aa335f784361f3f5212b`  
		Last Modified: Thu, 20 Jun 2024 23:59:23 GMT  
		Size: 2.0 MB (2010462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f253291606f48f10a81cde2e83de164d3af65f91f7b280c51913ca9e345f84a4`  
		Last Modified: Thu, 20 Jun 2024 23:59:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6880d4eeef18bad680c7a1efac227acef1864d8cbbba937c25347a5aa8e40a89`  
		Last Modified: Thu, 20 Jun 2024 23:59:24 GMT  
		Size: 16.4 MB (16410666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f6777a79d00a7173d08c8dafe2a5d7c4faa732261db617eafd6e56a9bf46a1`  
		Last Modified: Thu, 20 Jun 2024 23:59:24 GMT  
		Size: 18.2 MB (18178850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d13a55c91d119178eb5d2a5c4d37171ff667abac1e818b0c549f9eeceff187a`  
		Last Modified: Thu, 20 Jun 2024 23:59:25 GMT  
		Size: 18.8 MB (18770948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28030efc338d61ba3068ff249376d2080e6df5338a0e189f76113bf1ea99d16`  
		Last Modified: Thu, 20 Jun 2024 23:59:24 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9ea6be471518295e9b902dc2fc342207911c8d12e8c9472e26c5f3918705cb`  
		Last Modified: Thu, 20 Jun 2024 23:59:25 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3f49bf3cfee990cf139d87453b204bc3a65066023c40c77debbc0145206414`  
		Last Modified: Thu, 20 Jun 2024 23:59:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedf8c72dc7fe9a770d0dd8d0fb138f271f07c97b59a61b10648db1167a5c85d`  
		Last Modified: Fri, 21 Jun 2024 01:02:47 GMT  
		Size: 12.5 MB (12504290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27450857966d0929370cf45369fb93234b3f3157a462fa7130bfc0ae4e4cafb`  
		Last Modified: Fri, 21 Jun 2024 01:02:46 GMT  
		Size: 89.2 KB (89184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbdf4109703eb8d3f5df95ae6399c3e1ecc6102496a3f1671dbc2797b9153af`  
		Last Modified: Fri, 21 Jun 2024 01:02:47 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e28b440e907596487beb98b51c7d880b57d6d3719e9ec8d2170a6c9178e6d09`  
		Last Modified: Fri, 21 Jun 2024 01:02:48 GMT  
		Size: 54.7 MB (54740517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb64cc101108ff22eb4871388e87d808859f30ea993b2ab0bfeb898e8d97937`  
		Last Modified: Fri, 21 Jun 2024 01:02:47 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e1831d1c836eef0b9f69cebf436e241f02c003525d3a1752059742e4077ce7`  
		Last Modified: Fri, 21 Jun 2024 01:02:47 GMT  
		Size: 3.3 KB (3253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:7da2bee941d426bd76edc48c667b99184e94637656e68505c5099f2515e28185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1244c25718c5d270fca332872d7ed967216430da3d5a46cda6801ce13534cd4f`

```dockerfile
```

-	Layers:
	-	`sha256:643fb747b8bbef2106d029e08be2a8102f3d4a1781aff7642c1c5376be99c651`  
		Last Modified: Fri, 21 Jun 2024 01:02:47 GMT  
		Size: 34.8 KB (34836 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-git` - linux; arm variant v6

```console
$ docker pull docker@sha256:e3d5ff6b5f93afce7a0fd8d6c4a48579fdbb3578f51d94d51febeb912d09880d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119420906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466f06919b3b9ef4bcad7a65394322646aeec7a0b372978589a3d8fa5ca3eaed`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 23 Feb 2024 19:50:50 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Fri, 23 Feb 2024 19:50:50 GMT
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
ENV DOCKER_BUILDX_VERSION=0.15.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-x86_64'; 			sha256='6fbaf6e93ccc43078a71a12db1d38224725cb5a9675391c38510355073f24066'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv6'; 			sha256='10b465c1771c262d372e24b09ed30fdc63687e35ae61c2365089e3998372a776'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv7'; 			sha256='b5bd40dfadf089617fe9cacb7a08d6fd5fae28e2a465191be1f25f22ffead344'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-aarch64'; 			sha256='de8c48203f4876fe3ae8bf27081a9aa69dc87de67a705f9d76c3a3ad776ed0c2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-ppc64le'; 			sha256='5810b3e6184032edbd21f12ed165ddecc823b8222ff5e4f6c55112af6f617c6d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-riscv64'; 			sha256='2c138daa9eaa909434c808018c4ab748a5f25caee16e3a7810fbeb3897b40878'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-s390x'; 			sha256='4084bdab8782e98c57a5f7aa7384699490048ce117dc7e70cad183702cc1645b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5067b7efbba2a62adf7a972d95d87aacc3c1e8189af2936bd564da60e005f92e`  
		Last Modified: Fri, 21 Jun 2024 12:18:32 GMT  
		Size: 2.0 MB (1993302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45e793ddccf50c3a6d0f8deb45b412373ec816e1781f384ec2733ed8726ae31`  
		Last Modified: Fri, 21 Jun 2024 12:18:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a5d953d326c305fd4f74f22fef1bdb9212e4054a95714809afeccd454a44a0`  
		Last Modified: Fri, 21 Jun 2024 12:18:32 GMT  
		Size: 15.1 MB (15132944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8310bea86b6e72d3a162ade162017711b50df36cd829a8bddc32589797206d7`  
		Last Modified: Fri, 21 Jun 2024 12:18:32 GMT  
		Size: 17.0 MB (17010803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef451ffddaaab64ce0d90a3aa5e405131677fadba9a242ee7ad6c2ceec6324e`  
		Last Modified: Fri, 21 Jun 2024 12:18:33 GMT  
		Size: 17.7 MB (17734989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a252414a35367e694826f95cd2ae364494866f20033cdd5195c387844c036a31`  
		Last Modified: Fri, 21 Jun 2024 12:18:33 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26fe9efb58b230ffe459d6d0b5b4c7a487f4cea5f5800a291a01c2d8b5ce15`  
		Last Modified: Fri, 21 Jun 2024 12:18:33 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa56aa9ce1ebd461503e93b5f7c5cfec54f6c6daa35078be60cf5a0f7016576`  
		Last Modified: Fri, 21 Jun 2024 12:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ece91e66f51ce312d2d553fd81b4b0eeabe54da544e7ea123f6ff9084888e4`  
		Last Modified: Fri, 21 Jun 2024 12:54:23 GMT  
		Size: 12.8 MB (12779986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ec800c93d5e97d708066f80c51bace07b1f469c5cae93fd666947a7dddd9a2`  
		Last Modified: Fri, 21 Jun 2024 12:54:23 GMT  
		Size: 88.4 KB (88392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363757126fd454bfc13dafaec3a24706be21571ca1f459b4f77cd31340ec7610`  
		Last Modified: Fri, 21 Jun 2024 12:54:23 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ba511763b787fb6657a05830edcda30025a28720454b9b2949d1c6c1a46137`  
		Last Modified: Fri, 21 Jun 2024 12:54:25 GMT  
		Size: 51.3 MB (51305384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67df82cc46fb6e39250723228053cf951fae1d5c4112992347307c84c26d229b`  
		Last Modified: Fri, 21 Jun 2024 12:54:24 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9352578c07e336a2db0e336f6c399767f05f0e399da20c2ab73159a86365655`  
		Last Modified: Fri, 21 Jun 2024 12:54:24 GMT  
		Size: 3.3 KB (3253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:5ad066a2599c40be17c1919d6e9f7c633daac8a2aabae34b592c2359b8718c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 KB (35062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3ccc5d66cb75eb5d6ff63521b82cdc7265c0c4b8ccdf5a3e6ab556f6d49d7c`

```dockerfile
```

-	Layers:
	-	`sha256:679211e153294802c3feab1daae1591602cb4c6156cca3d7b2a196ac9892fe5a`  
		Last Modified: Fri, 21 Jun 2024 12:54:21 GMT  
		Size: 35.1 KB (35062 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-git` - linux; arm variant v7

```console
$ docker pull docker@sha256:84cec092abad38a2087c9e8986a5ba8ceed497231c2834365fa1ff2e163b306e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117770397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f60e52069e016fb4b7a2219a766fc1086cc34992f03d3a4938eeecc0d119a8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 23 Feb 2024 19:50:50 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Fri, 23 Feb 2024 19:50:50 GMT
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
ENV DOCKER_BUILDX_VERSION=0.15.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-x86_64'; 			sha256='6fbaf6e93ccc43078a71a12db1d38224725cb5a9675391c38510355073f24066'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv6'; 			sha256='10b465c1771c262d372e24b09ed30fdc63687e35ae61c2365089e3998372a776'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv7'; 			sha256='b5bd40dfadf089617fe9cacb7a08d6fd5fae28e2a465191be1f25f22ffead344'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-aarch64'; 			sha256='de8c48203f4876fe3ae8bf27081a9aa69dc87de67a705f9d76c3a3ad776ed0c2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-ppc64le'; 			sha256='5810b3e6184032edbd21f12ed165ddecc823b8222ff5e4f6c55112af6f617c6d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-riscv64'; 			sha256='2c138daa9eaa909434c808018c4ab748a5f25caee16e3a7810fbeb3897b40878'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-s390x'; 			sha256='4084bdab8782e98c57a5f7aa7384699490048ce117dc7e70cad183702cc1645b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d5fc77a3649e760b52d8af6db88dd8af095e57ac6c527e16fcad61fea16019`  
		Last Modified: Fri, 21 Jun 2024 05:19:24 GMT  
		Size: 1.8 MB (1841237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea74d84101664675bbdd6f6d17eb8bc8ddb61da400e0c567fb92a984902f616c`  
		Last Modified: Fri, 21 Jun 2024 05:19:24 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eba5a9f552a9a997e6e6849f9ae00d4746340f972c6cef941e929d5f058a634`  
		Last Modified: Fri, 21 Jun 2024 05:19:55 GMT  
		Size: 15.1 MB (15129224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4469eb9ac5fd715331c658d2a04d5ed44bed6d7f57010cfa76acd0dce38389f5`  
		Last Modified: Fri, 21 Jun 2024 05:19:55 GMT  
		Size: 17.0 MB (16998014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8294b841b3b31ce66f34dea00cda94bcbb6e4d2a65c1354084ef0a98547334b7`  
		Last Modified: Fri, 21 Jun 2024 05:19:55 GMT  
		Size: 17.7 MB (17715377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d75e4f037c19293d992a4e182dfd9d39c0551a833eb302a9329cb901e9fde6a`  
		Last Modified: Fri, 21 Jun 2024 05:19:54 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7815bdd2f50b0ef8f6482e44324c88e10150a729d7d1ac583ebfadd5f8c6606`  
		Last Modified: Fri, 21 Jun 2024 05:19:55 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a7e41e3a5e864a97389a62117704dae6c0cd3f56fc5e32f2cc09d8f98cf516`  
		Last Modified: Fri, 21 Jun 2024 05:19:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c8e1b6824ddb084a27218025a5d6b2a13ac1ae6c873fe528485c76bd0e8c31`  
		Last Modified: Fri, 21 Jun 2024 12:24:45 GMT  
		Size: 11.6 MB (11593865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7c5fa25ea04109908ee9c4c27a0ea99f9b8cbb808a1a2a18e1e70947cd1a12`  
		Last Modified: Fri, 21 Jun 2024 12:24:44 GMT  
		Size: 84.5 KB (84473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2416b1dec103dbc85abf8ccaabba41a04a47c64248169c59c1c8bb144a1a692`  
		Last Modified: Fri, 21 Jun 2024 12:24:44 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d001a3f11aebf5a98bd9763e975e857bd8b1125e2954201e9cf83850100e4ef`  
		Last Modified: Fri, 21 Jun 2024 12:24:46 GMT  
		Size: 51.3 MB (51305402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7011eeee018593247eb9e40e3419de5ab5127e19386c72fc77b408d02661e75`  
		Last Modified: Fri, 21 Jun 2024 12:24:45 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d974fe9e6ea6b64d149efbf6a68a73108f325106ca5925e78ecb4e137a71afe0`  
		Last Modified: Fri, 21 Jun 2024 12:24:45 GMT  
		Size: 3.3 KB (3253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:c00e08f50535640482cfa679cc6a387b641bd03d899f0a431d62567982b4a000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 KB (35062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf08ff156a8929208270a0c045c11ccc39f55dfa11a493c13119dbc7ff78cd2f`

```dockerfile
```

-	Layers:
	-	`sha256:9f81835080aa86f12523b07beffbf14008201aaa603c351b2dcba86053a37d44`  
		Last Modified: Fri, 21 Jun 2024 12:24:44 GMT  
		Size: 35.1 KB (35062 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-git` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:426ce1cf381ef41a08976c722ae4ac69d1ead29c32fae52d7bfe70a7272e9c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118404477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b35648c8f564dab0acb6f3d147802ab24686fefd02aa6b6d0cc5fb20c0ba71`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 23 Feb 2024 19:50:50 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Fri, 23 Feb 2024 19:50:50 GMT
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
ENV DOCKER_BUILDX_VERSION=0.15.1
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-x86_64'; 			sha256='6fbaf6e93ccc43078a71a12db1d38224725cb5a9675391c38510355073f24066'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv6'; 			sha256='10b465c1771c262d372e24b09ed30fdc63687e35ae61c2365089e3998372a776'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv7'; 			sha256='b5bd40dfadf089617fe9cacb7a08d6fd5fae28e2a465191be1f25f22ffead344'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-aarch64'; 			sha256='de8c48203f4876fe3ae8bf27081a9aa69dc87de67a705f9d76c3a3ad776ed0c2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-ppc64le'; 			sha256='5810b3e6184032edbd21f12ed165ddecc823b8222ff5e4f6c55112af6f617c6d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-riscv64'; 			sha256='2c138daa9eaa909434c808018c4ab748a5f25caee16e3a7810fbeb3897b40878'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-s390x'; 			sha256='4084bdab8782e98c57a5f7aa7384699490048ce117dc7e70cad183702cc1645b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b04307e7332c3b65641cd58699f2bc8e8afe54c5025b70c16fcdabd402f24b3`  
		Last Modified: Fri, 21 Jun 2024 07:17:16 GMT  
		Size: 2.0 MB (2006609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905719f6317149e9bc4db54583007ed02cedda492f4e24810f9e13d071bdcfef`  
		Last Modified: Fri, 21 Jun 2024 07:17:16 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91ca182391e48e480f439ac5efc3c7f3a3041e63c8832927e766f7c7c5215f7`  
		Last Modified: Fri, 21 Jun 2024 07:17:43 GMT  
		Size: 15.5 MB (15459116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d4a7b53fa9cfee2b8053787139e12dce34ef94a4146d127939ead23c7ce38b`  
		Last Modified: Fri, 21 Jun 2024 07:17:43 GMT  
		Size: 16.5 MB (16538046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634c9bc5e1ee9613f1bf88a76b1bcfe3830553ff8a0c29ac7737231db53856a5`  
		Last Modified: Fri, 21 Jun 2024 07:17:43 GMT  
		Size: 17.1 MB (17137909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f460134f345fd6342cfec7a5f09281d077303f7afe99b144ca4a11e88c9767`  
		Last Modified: Fri, 21 Jun 2024 07:17:42 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9201746e51a5fd8b3a930b3ad250d9f73eba884d6e38cf7794f3aee3acab612a`  
		Last Modified: Fri, 21 Jun 2024 07:17:43 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013cfa9d1505e978036460fbdeb7e026036d59050267a09b9bc20956fc1a0e28`  
		Last Modified: Fri, 21 Jun 2024 07:17:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22197594ed2b127d4e9bc6d372eccab9495554abb91768ba750d2c58582f2b06`  
		Last Modified: Fri, 21 Jun 2024 15:53:55 GMT  
		Size: 13.0 MB (12991240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841ec5f551a46605133b97ff967b1c18318f96b34c0412b333db8efd132df613`  
		Last Modified: Fri, 21 Jun 2024 15:53:54 GMT  
		Size: 98.6 KB (98628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae4117d8b3d1bd6cf7b90b267eb26701ee535e3cae2fe5ce8e5150fd3d07cfb`  
		Last Modified: Fri, 21 Jun 2024 15:53:54 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1de1648424535392391f9136c750f6d94b4a30ce798048e12dc5f6b6efab64`  
		Last Modified: Fri, 21 Jun 2024 15:53:56 GMT  
		Size: 50.1 MB (50076175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d974495d833d3860527fae0c09e36ea0aaa5eeeb9ff057f3ba0e1cda60381fa4`  
		Last Modified: Fri, 21 Jun 2024 15:53:55 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd890ee047a70cddcd8093291e566a860bc3a9b0fbb4765068335ada20a99cba`  
		Last Modified: Fri, 21 Jun 2024 15:53:56 GMT  
		Size: 3.3 KB (3254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-git` - unknown; unknown

```console
$ docker pull docker@sha256:9622b70ec1153677d6a89db713e6e10891d355a4be577cc16fc3d0bc64840e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 KB (35346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e54be6e9a9b864bd841294435aa8f2d0295d7505149a4c7a85437aca25032ce`

```dockerfile
```

-	Layers:
	-	`sha256:6dea10f7091973cdbeb8fb3cd39fea6b737fb9129c32343edbf3b26bf252d06d`  
		Last Modified: Fri, 21 Jun 2024 15:53:54 GMT  
		Size: 35.3 KB (35346 bytes)  
		MIME: application/vnd.in-toto+json
