## `docker:dind`

```console
$ docker pull docker@sha256:baade57b9dc1c2e915fa6d5fabe2b600a4b1e1323aa52c5eca53170739b0db8d
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

### `docker:dind` - linux; amd64

```console
$ docker pull docker@sha256:f649ef046008ca7f926a2571c32b0ac22e5c59eb61b959617f9acc2a4c638cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136913245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2dc198f7d839eae26b5a9cb0e7cdc4e2c97d9cb4ea66dbeb0a4c0c7f0b165f8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sun, 02 Feb 2025 00:04:18 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_VERSION=27.5.1
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sun, 02 Feb 2025 00:04:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
CMD ["sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
VOLUME [/var/lib/docker]
# Sun, 02 Feb 2025 00:04:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sun, 02 Feb 2025 00:04:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabac8a2abd7c65cdb312706c9f10c30ca405295fc8812fc144ffeb4260ca45a`  
		Last Modified: Fri, 14 Feb 2025 20:34:03 GMT  
		Size: 8.1 MB (8062548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1425a2af6f51cf1496840a4abd7ba42e8f21cb5c45bb7163ba9491fa4562fd42`  
		Last Modified: Fri, 14 Feb 2025 20:33:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0666ab41c2be8e89610c8c9c2fef25df0a4db016a1b57a2dfb75f3ce4ef3e44b`  
		Last Modified: Fri, 14 Feb 2025 20:34:03 GMT  
		Size: 18.8 MB (18848905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d14abb201810167d344f9b2a95819d2ef8cee098d05bce8e813602808127132`  
		Last Modified: Fri, 14 Feb 2025 20:34:04 GMT  
		Size: 20.2 MB (20234554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1709176accd82416d366e590e5519846b532a9f70f8d892580844d04e90993a0`  
		Last Modified: Fri, 14 Feb 2025 20:34:06 GMT  
		Size: 20.9 MB (20907746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb841b0d6cf23be3cffa4948d33e10f50646099d9e4778a0d04e623421f998c`  
		Last Modified: Fri, 14 Feb 2025 20:33:54 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f91a2e06588897451478664c509d6d653e2bc580902b4a7672fade922083699`  
		Last Modified: Fri, 14 Feb 2025 20:33:54 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8cf49b6d3cb247a79dd8d34b1580ebded91095b06e87a4fe4667353db3f815`  
		Last Modified: Fri, 14 Feb 2025 20:33:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323b19790f6653a5a5256c97e91b552c81a8ab875a0d92e2e0eeaf4d2ceeb55c`  
		Last Modified: Fri, 14 Feb 2025 21:11:08 GMT  
		Size: 6.7 MB (6733081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe183b8e2a069e0b4f34f0858bf7f37d43a02a6570d1d88cf0cd6e8ebcdd3910`  
		Last Modified: Fri, 14 Feb 2025 21:11:07 GMT  
		Size: 90.3 KB (90312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752b8ed4aa1f4e1d3da23d87fb6faefd1e99647a399850fd203bfc8fd0301ddc`  
		Last Modified: Fri, 14 Feb 2025 21:11:07 GMT  
		Size: 1.0 KB (1006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a91c7e8e64d3bb599cc0f7c17cb33dd0374c5ea079454cacbba84076ec078b`  
		Last Modified: Fri, 14 Feb 2025 21:11:11 GMT  
		Size: 58.4 MB (58385800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e361c405e163dc19281f5cbc8bc7b362102dc09c2e8f8c2ae89d81b5f8dc90`  
		Last Modified: Fri, 14 Feb 2025 21:11:07 GMT  
		Size: 1.6 KB (1634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2498c36ad744a314cba5c6416429e2b90526599b30443be165b0793836cb8d`  
		Last Modified: Fri, 14 Feb 2025 21:11:07 GMT  
		Size: 3.3 KB (3257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:25eac4cb09861590e368010ef10717af0074605933905c29d21881e3323a3505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80e8d30b9f393f62c0a41063d01d8db0bb9ce104fbbf289dee735f1f893288c`

```dockerfile
```

-	Layers:
	-	`sha256:c44b29040b9d2209302724853f95183007d9ff65edbf16ea7e375e5fadc6827d`  
		Last Modified: Sat, 15 Feb 2025 00:07:18 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:a64f93adc7206d308ccc68a0fca7abf4fd4b34901bd0c78de50dd028fb54048b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129973720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9ddb2c6587458ee6fb177b86087d007009fd1ec7ada62af0a120196ad7fd56`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_VERSION=27.5.1
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sun, 02 Feb 2025 00:04:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
CMD ["sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
VOLUME [/var/lib/docker]
# Sun, 02 Feb 2025 00:04:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sun, 02 Feb 2025 00:04:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
CMD []
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ad6872f504f55fd5dfe94a791ed8ab685db4ba2dd3480eb2ad66b1bb83da0b`  
		Last Modified: Wed, 15 Jan 2025 00:19:53 GMT  
		Size: 8.0 MB (7972910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5ebb3ae482a680f38002a6478f8abc7edcd1bf788e37724c95efe3e0a74f1d`  
		Last Modified: Wed, 15 Jan 2025 00:46:14 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed4e5240126a237686beb0364732ea8fb90b8222bb79ece3b01bc65f11255f8`  
		Last Modified: Thu, 23 Jan 2025 07:03:20 GMT  
		Size: 16.9 MB (16866758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc64aa21acc52ff9715cac0a1c9950afe80cf8a4ea1a68baec921a635cb58a9b`  
		Last Modified: Thu, 23 Jan 2025 07:03:20 GMT  
		Size: 18.8 MB (18843713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c298045937c77d9292cabfbb47e9f06e3be5c1d06d80236338330426f288938c`  
		Last Modified: Thu, 13 Feb 2025 02:06:17 GMT  
		Size: 19.7 MB (19668826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f895ceec5f438c82f5637a1fa4eadb1ad1bf9d8b8c833fc878a6af1c1e8dc92`  
		Last Modified: Thu, 13 Feb 2025 02:06:15 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002b9ac08ddac7b9ac671105eaec4a41886e12c2b4febd6d1bd1685969141986`  
		Last Modified: Thu, 13 Feb 2025 02:06:14 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f93673b028bbec2333075d630d9df59a39dab4df11dea998dc9b5cabb27f440`  
		Last Modified: Thu, 13 Feb 2025 02:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c68bdd53c925ffe41ee7a4fb38b674c193418ddd4a5b8b30c8b891fab00f244`  
		Last Modified: Thu, 13 Feb 2025 02:06:17 GMT  
		Size: 9.1 MB (9113292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b065058b73b5da4250a431e6e3efa3c00eb234adf3f5a154f2261ba101a986`  
		Last Modified: Thu, 13 Feb 2025 02:06:17 GMT  
		Size: 89.9 KB (89862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af6c1c4fdabc801403368e68174876f9e1d467b1eb23f7814c7286b769301da`  
		Last Modified: Thu, 13 Feb 2025 02:06:18 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28dfff8c77023e940a9d707acb67d7c42831b47ae67277aef9181a37fee39b2`  
		Last Modified: Thu, 13 Feb 2025 02:06:21 GMT  
		Size: 54.0 MB (54046392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d337510331cf2ab832ef3d708d14bf70c2d50c165d500082765b6ca27b7a51`  
		Last Modified: Thu, 13 Feb 2025 02:06:18 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa56be8ebe89dc014760e8565dd42d061872cdfade6e1ad47490c427987797f`  
		Last Modified: Thu, 13 Feb 2025 02:06:19 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:b2fa91ecd5de8200dc1261b82f9684c8fbca07e0e0bec497cdf64984bc600f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d790ec942534d65fd510edb43c756eccd5490b72692ed1ca5a6211f724bd70b5`

```dockerfile
```

-	Layers:
	-	`sha256:4df356b25d99e6d672a5c774de6cc4e0bf32fbef3f26128363fb3fa8dfc52f87`  
		Last Modified: Thu, 13 Feb 2025 03:07:37 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:b5dd9310bbf6a05fc8e35f7f64fc59db3bdf296a97135ea7bdf1222034bababf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128159939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7837ea2d5b4b24cbca34ab248c40157e531d808a1394a1616f8f13d461734114`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_VERSION=27.5.1
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sun, 02 Feb 2025 00:04:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
CMD ["sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
VOLUME [/var/lib/docker]
# Sun, 02 Feb 2025 00:04:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sun, 02 Feb 2025 00:04:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
CMD []
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f773dfbfa74b529894deefa53b4b4bb911c391d68367f4683e2c499100fab3`  
		Last Modified: Thu, 13 Feb 2025 03:07:56 GMT  
		Size: 7.3 MB (7295024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4663871d4cf0c667b3c5dc878695236bc7c84ecac56ea3dae085b2b651858b`  
		Last Modified: Thu, 13 Feb 2025 03:07:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0788c97a09a12cd9a243854efb159210be2c11f242be759368429deb59c8caa4`  
		Last Modified: Thu, 13 Feb 2025 03:07:56 GMT  
		Size: 16.9 MB (16855762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2883c8e697fca7e4006c64160a53b33a5aac14870fdca3df648f8c76294787`  
		Last Modified: Thu, 13 Feb 2025 03:07:55 GMT  
		Size: 18.8 MB (18827825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a05bb67d85731717b9d66fa1fed454ae25f777206db17b7fc3f413b42a3dec`  
		Last Modified: Thu, 13 Feb 2025 03:07:56 GMT  
		Size: 19.7 MB (19655149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455196388500f3374ccf949c5a1d7cfd76698b1a4a22f8e9f8dd6cc1ec9a1676`  
		Last Modified: Thu, 13 Feb 2025 03:07:54 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9977db9a00fc913f01366e4ca69085fecbb782a359fb19e882944c3598515e`  
		Last Modified: Thu, 13 Feb 2025 03:07:54 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb4fc9f1f17a8182d82fb478ca4642b6245b7b28fb0a29c1cb1f0ae825a2cea`  
		Last Modified: Thu, 13 Feb 2025 03:07:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217de3a213d1f2d81610d2ee08de4be4d7e6bd513a52d3b3e32557b154249e33`  
		Last Modified: Thu, 13 Feb 2025 03:07:55 GMT  
		Size: 8.3 MB (8288308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba63d9bc36a810e7be7dbfeb8baa8bbab28798d01f499a38cc6dddc52e9935b`  
		Last Modified: Thu, 13 Feb 2025 03:07:55 GMT  
		Size: 86.3 KB (86337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9595fa7114a32fa54d87eeb196bb15461f1b47f58f9852e4c6d91233176f3e4a`  
		Last Modified: Thu, 13 Feb 2025 03:07:55 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbeb4a30be4a5c5f0e756b9a61b79a95ff3d3208bd2a2b537d5c15d791f6854`  
		Last Modified: Thu, 13 Feb 2025 03:07:59 GMT  
		Size: 54.0 MB (54046354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d51e3a86c57d495e8c26cea4407b4476fa34d51f3cc2cf46395494b6be76b96`  
		Last Modified: Thu, 13 Feb 2025 03:07:56 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8629b495d0cc39dfcef124836319a0e6bf6f95721fce94305805623df1147f53`  
		Last Modified: Thu, 13 Feb 2025 03:07:56 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a244a0ffa9766cbc361e0ed1b6477c384a75bf27c402943c974327eb74415b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec94abd82b9cf84a67d7fe264395dcbd7ac49c06ae97efc8c4f245f14dac3aed`

```dockerfile
```

-	Layers:
	-	`sha256:f5d9cec1e448d5792002b197fd6f51b1ef3c3ea6dd638e52f6e3ae05c370ff03`  
		Last Modified: Thu, 13 Feb 2025 03:07:39 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:627cdb5f9180cd71ab7de25cdc347d3e0d9b1211d654bfcf21b91eb4dc4fdc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131258792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c2b0c6f6430810eeb9cc7e1117b8d0c07677bad6007861bd78bdb82b2e6721`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_VERSION=27.5.1
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Sun, 02 Feb 2025 00:04:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
CMD ["sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.5.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.5.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.5.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.5.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Sun, 02 Feb 2025 00:04:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 02 Feb 2025 00:04:18 GMT
VOLUME [/var/lib/docker]
# Sun, 02 Feb 2025 00:04:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Sun, 02 Feb 2025 00:04:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Sun, 02 Feb 2025 00:04:18 GMT
CMD []
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a38d031a5afb431598b76502d4dd5eeb9e5f03f4bbefa5e3355a3a20bc74141`  
		Last Modified: Thu, 13 Feb 2025 00:35:06 GMT  
		Size: 8.1 MB (8074393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2ed2ebfaeec2ca6218c7b467abaff52c646bbfa87ee941425c5485464cf68c`  
		Last Modified: Thu, 13 Feb 2025 00:35:05 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b08732b15b4609f59020ca306a1c94988c1244abcc5228dc7460f55f4359bdc`  
		Last Modified: Thu, 13 Feb 2025 00:35:44 GMT  
		Size: 17.8 MB (17794930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c08adfc734e2ca287211047aba4e636f1513c08cc3fd1417d12947a1afed30`  
		Last Modified: Thu, 13 Feb 2025 00:35:44 GMT  
		Size: 18.5 MB (18457794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5fd655d5e682ae39fa53d6481fb1094b0ee82304e7e244e2149ddc5073ccee`  
		Last Modified: Thu, 13 Feb 2025 00:35:42 GMT  
		Size: 19.2 MB (19175083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa49eaf43974d7647a049ba0b12d23d848d02d4f40e85b565917d36c77565e40`  
		Last Modified: Thu, 13 Feb 2025 00:35:41 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b4ef0de34b39cf9d09ad3b094f6cb8f4425e93409ca0f28e37e0b9a884831c`  
		Last Modified: Thu, 13 Feb 2025 00:35:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12830068875b28d2fa4ebcd86f777020cf5b17ded2278f783d23cbbcd967499`  
		Last Modified: Thu, 13 Feb 2025 00:35:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e69c2895affbcb520e75fe5348f64ab08847d04cb9d98454ec1a4455b6f5d5`  
		Last Modified: Thu, 13 Feb 2025 01:08:19 GMT  
		Size: 9.7 MB (9705893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531ebf1ff4ce47e2ad401d8371d01fdddf0b32257c959578438804d9c423e515`  
		Last Modified: Thu, 13 Feb 2025 01:08:18 GMT  
		Size: 99.4 KB (99389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fcd29ba5d81a83ecc9011c82b185e3a3d6c7b53b3b98e2aba42b5e828e359b`  
		Last Modified: Thu, 13 Feb 2025 01:08:18 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2718a502da548138daf6e918c0ecf3993d1d4b62b803fdd7d9782aad2168cb`  
		Last Modified: Thu, 13 Feb 2025 01:08:27 GMT  
		Size: 54.0 MB (53950883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe68300bf2a035303f1b13317887fba32aac7d5b3216c66240809d379ffc1a32`  
		Last Modified: Thu, 13 Feb 2025 01:08:18 GMT  
		Size: 1.6 KB (1637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf988e6efa451c40a702711bc2819c2ed2ba5d6052b6298236e643f0859ed62`  
		Last Modified: Thu, 13 Feb 2025 01:08:17 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:719901201278b33e13eaf71ff0fb0f6692307b7e3604e1a3efec29fef3e6f30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640fb31a915fc6e941341609e21874c8b2a63b91985cb44f71442d478c043bc8`

```dockerfile
```

-	Layers:
	-	`sha256:52ddd6ec3fff2e96c321764aeb88105731f1a852364b563e68228e04c836bc89`  
		Last Modified: Thu, 13 Feb 2025 03:07:40 GMT  
		Size: 34.8 KB (34826 bytes)  
		MIME: application/vnd.in-toto+json
