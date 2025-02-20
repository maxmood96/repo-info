## `docker:28-rc-dind`

```console
$ docker pull docker@sha256:008120fd2b0681d86604840f9f239d0d36fa55060800d42e66ec6189ebb345e7
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

### `docker:28-rc-dind` - linux; amd64

```console
$ docker pull docker@sha256:0f810305f7f77782b4fed9ce16c6ea8996d50bf00cbecccad260d4b69f20e851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139363919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6261d105f46c3eaa419f787088aaa14c1ed6430569416c28486bcd85a0e028`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_VERSION=28.0.0-rc.3
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Feb 2025 00:04:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
CMD ["sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Feb 2025 00:04:40 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Feb 2025 00:04:40 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aaf86294e20a08869e62f102687e1a19149fab47342f7bbae209ae4723dc569`  
		Last Modified: Wed, 19 Feb 2025 19:27:34 GMT  
		Size: 8.1 MB (8062969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e912116c79aff248a322e4ff551a41ab56412dbb6b6d4026d41782521a9f8a`  
		Last Modified: Wed, 19 Feb 2025 19:27:32 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515ddf0af814829b15136e59a16be2d0eb62e7292ef3c35d9b37b04fd003a41d`  
		Last Modified: Wed, 19 Feb 2025 19:27:38 GMT  
		Size: 19.5 MB (19492203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420764532edc8d5531861800eb911c8c050756c37bca7a6b43481d9354ca30a0`  
		Last Modified: Wed, 19 Feb 2025 19:27:37 GMT  
		Size: 20.2 MB (20234558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9ad968c592bdaf775a13b18d8c158bd629437a6b295bf467b20fce0edf4106`  
		Last Modified: Wed, 19 Feb 2025 19:27:37 GMT  
		Size: 20.9 MB (20907752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085d56e5e5b1e345928d1affd42c476dc0da83272f84c6579fc96827e618a0c3`  
		Last Modified: Wed, 19 Feb 2025 19:27:34 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b451a705f54bd9322b0af4aa948f7b8687b6ed7eec476fc962f45a137c75ba4c`  
		Last Modified: Wed, 19 Feb 2025 19:27:36 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5016cfbd98dfb93b621c700514b0fe7f94e896ad92879362eaff8e0e745aac20`  
		Last Modified: Wed, 19 Feb 2025 19:27:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfaf9e09c8841fc8914e7b30230a16792aaff0656a440e7870d93f9a102d4a4`  
		Last Modified: Wed, 19 Feb 2025 20:28:59 GMT  
		Size: 6.7 MB (6733047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96e38ce42a0c13c027e61f13b788bcd4deda12d584244eca48e4a474aa2004c`  
		Last Modified: Wed, 19 Feb 2025 20:28:51 GMT  
		Size: 90.3 KB (90320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192132175ab3c70eec860a50665c32a2546e4e99719a004c108b7d09e91126b2`  
		Last Modified: Wed, 19 Feb 2025 20:28:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49fb1a9d02172a2c473bfec29d81f6486fb45b12bb77cfd07c46fb9b4652f10`  
		Last Modified: Wed, 19 Feb 2025 20:29:08 GMT  
		Size: 60.2 MB (60192772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b4fbe34aeae0f0e24c508fe58b067a4f83665a5c7d9dcd3383b2e7a7df829c`  
		Last Modified: Wed, 19 Feb 2025 20:28:49 GMT  
		Size: 1.6 KB (1633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473c6b786ad27d86a1865b1cc723edbcebc828fad29041271757dc2453d4b63e`  
		Last Modified: Wed, 19 Feb 2025 20:28:49 GMT  
		Size: 3.3 KB (3254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1dfa8e6184b853730c3d29ae5c7bbfbbb1d795f042b9dab38151b375d5f7b35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff189e45d57ac9e50936841c05ce4ae91d4d40546a06e7b888cf768bcbef710b`

```dockerfile
```

-	Layers:
	-	`sha256:8b37ad85f36a868c9987042b79dc43886fde69193ccb39a9a8896e98c0c93a6c`  
		Last Modified: Thu, 20 Feb 2025 00:08:09 GMT  
		Size: 34.1 KB (34115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:160745b33f840ce31233e9a3e909f0b79a3e485cbabb305cbd7e07781f87fa29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130031758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150c42f2ea29418913dc7ed4208e14e9e38210bc6c5d9405e89206b0f6769017`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_VERSION=28.0.0-rc.3
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Feb 2025 00:04:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
CMD ["sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Feb 2025 00:04:40 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Feb 2025 00:04:40 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
CMD []
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3e40b3641449ca47aef50c48f620eb6d3a3bc2292e5cf4ea267f5f03e6c7bc`  
		Last Modified: Fri, 14 Feb 2025 21:07:35 GMT  
		Size: 8.0 MB (7978133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df16922f358c97f513c6d0b9457abb36aefc588e45374edd23692381878a7`  
		Last Modified: Fri, 14 Feb 2025 21:07:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2989278eb432c3d61a437074997b2a8d083a58a8a1952f406ae5f091fc91dded`  
		Last Modified: Wed, 19 Feb 2025 19:27:22 GMT  
		Size: 17.5 MB (17453945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350b097c4c81e510aaaed293a45ccbe6b158d0461dca0e7a53c07a62d152c40b`  
		Last Modified: Wed, 19 Feb 2025 19:27:22 GMT  
		Size: 18.8 MB (18843704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff81fcbee56d80f2e74c03d5a361e6e0d2c4567cab0cc3e879758a8c816ede9`  
		Last Modified: Wed, 19 Feb 2025 19:27:12 GMT  
		Size: 19.7 MB (19668814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea36efcc41bcd877ac3f3b9d94de27b1d20d77c862646fd0dc3bddbf1d779220`  
		Last Modified: Wed, 19 Feb 2025 19:27:09 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edacc644c22bc0dafac9d40ddcd73ccb589815887003b9c5c670deaa0e3a1fb`  
		Last Modified: Wed, 19 Feb 2025 19:27:09 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026b876a0dc57340334fd25cbdbfcdac649422104d27894c6cd218f7f91dfc68`  
		Last Modified: Wed, 19 Feb 2025 19:27:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5027864a9eb9c966ef2a4974ee91f664039fbb5e66814273ff4cea81e1c3368`  
		Last Modified: Wed, 19 Feb 2025 21:27:59 GMT  
		Size: 7.0 MB (7036922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4c2b528561cd5b47d09e1b6157d44278d28edf92e0cfc844a77599075e5b8e`  
		Last Modified: Wed, 19 Feb 2025 21:27:50 GMT  
		Size: 89.9 KB (89855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ee2c0c6d7e89f076bf071b0b36aa6b3cf3df32f8c703d00c4dfa9b6cef19c7`  
		Last Modified: Wed, 19 Feb 2025 21:27:50 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bb714c6500d031ac1a63f1182494ea05ae8efba4b6df65e9b9f439452ab68a`  
		Last Modified: Wed, 19 Feb 2025 21:28:07 GMT  
		Size: 55.6 MB (55587582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dd5e2a0ccbeaf6ffb07058855850e6f46454ac5c21508b6c1fd80697b716df`  
		Last Modified: Wed, 19 Feb 2025 21:27:49 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaa1fd46dbe342be3b6490ae74c631f4dc76f930c44a7165e9e1b452d4521df`  
		Last Modified: Wed, 19 Feb 2025 21:27:49 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:90d1915c17ff904fed366b3a4525450e25783354cbf4144c956f5d20e7e94b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b333019bea2f27d3ed65f7377b78c1547b914afcb16a1ee8239619491e2a23d8`

```dockerfile
```

-	Layers:
	-	`sha256:c6669e4ced7b03593abaa10ed915b52201361772977d3dac34234715631f19a2`  
		Last Modified: Thu, 20 Feb 2025 00:08:10 GMT  
		Size: 34.3 KB (34275 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:4396a065024ec54b7218d2ee8b2041203ccdc5ab084fd371c98d8f282b82c80b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128373329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585c0a971117334e8a28455af06380762be911f028c790c727f9aa742980eb0c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_VERSION=28.0.0-rc.3
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Feb 2025 00:04:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
CMD ["sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Feb 2025 00:04:40 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Feb 2025 00:04:40 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
CMD []
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca56d88020444be93af4c6a8701a2522308d870a3f40c5390a4734fb56ab524`  
		Last Modified: Wed, 19 Feb 2025 19:26:32 GMT  
		Size: 7.3 MB (7299505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652f991d39a023e6b2b69879744700f92b6603310c6d1b68af41a9bed6765d44`  
		Last Modified: Wed, 19 Feb 2025 19:26:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3734970ae21bd729763331826c4e8bd55823262e1c352e4d223ce89eee9ecbd8`  
		Last Modified: Wed, 19 Feb 2025 19:26:33 GMT  
		Size: 17.4 MB (17444471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31602278f970debb91d94d38794eeb2ef93f45e0dceb54cdf38f1034d40a2b7b`  
		Last Modified: Wed, 19 Feb 2025 19:26:33 GMT  
		Size: 18.8 MB (18827818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d5ded06e8b83aeeefc24e99c66abc04c0f9346291e8af44c47f8c9e7173e6d`  
		Last Modified: Wed, 19 Feb 2025 19:26:33 GMT  
		Size: 19.7 MB (19655143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e536bb00b7312f154d3d18c74409d066a4f059d99f390048c0e99a77c537e80b`  
		Last Modified: Wed, 19 Feb 2025 19:26:31 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a175ab09c727596f26f063fd8b27f5075cb03b269005f965d1030652089e1d`  
		Last Modified: Wed, 19 Feb 2025 19:26:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5285297849fb693621c9a7d23d4691437c9eb4ab5e2efea7abca7ff8390d9eb`  
		Last Modified: Wed, 19 Feb 2025 19:26:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe962676e4fcce84d4bfb325976d4946b5dd70e5b5c119c956accdbcbb084fc`  
		Last Modified: Wed, 19 Feb 2025 21:28:03 GMT  
		Size: 6.4 MB (6366218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5741f123580e3e12e882b38830f33452076fcef850a07ba859bccd916645655b`  
		Last Modified: Wed, 19 Feb 2025 21:27:54 GMT  
		Size: 86.4 KB (86351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d932f44526fa546be4bcc472adb8bc6d016c9d46ed3b06a904c0710d7058cd`  
		Last Modified: Wed, 19 Feb 2025 21:27:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164520d16d01cd92491f62e3decdd3a2d163b9603d220dc736672cec7075b518`  
		Last Modified: Wed, 19 Feb 2025 21:28:11 GMT  
		Size: 55.6 MB (55587640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5c0f9b551bfe74ec961bebf816c4600f9150dea315f052184851c4a667153e`  
		Last Modified: Wed, 19 Feb 2025 21:27:53 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931ecf02578d5ff735cdc3cf4a51cecaa0215b1ad9dafdb4ac24a94ebc4215ce`  
		Last Modified: Wed, 19 Feb 2025 21:27:53 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:7aab3e4068a31fe0ff3d34fd87da30ff0c59944d4b12c0e864efa9a15f3c09dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41f4301128d388ae6a1a720fa3cdec9d2801e82c619faa4a4f60764d10520e5`

```dockerfile
```

-	Layers:
	-	`sha256:131b29c762ff502288be62f25bae2e4578af26d5783a8c2e0bed13393cd33e50`  
		Last Modified: Thu, 20 Feb 2025 00:08:12 GMT  
		Size: 34.3 KB (34274 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:92fb161934abaa6bd0117bbaa0028e7eab575addccfc32b6c6b649ea5f9d64b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130767383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84719ec8b1b4db74032ac6f5852be8900db2e540968470bbdafa79021342fdd8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_VERSION=28.0.0-rc.3
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 19 Feb 2025 00:04:40 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
CMD ["sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Wed, 19 Feb 2025 00:04:40 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 00:04:40 GMT
VOLUME [/var/lib/docker]
# Wed, 19 Feb 2025 00:04:40 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 19 Feb 2025 00:04:40 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 19 Feb 2025 00:04:40 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ac8b8412c3ffa81dcde5740aef1953c47f791be525bcb421e89bc9051e6bad`  
		Last Modified: Wed, 19 Feb 2025 19:26:14 GMT  
		Size: 8.1 MB (8076372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c517bd3bb254433972817513e72788f2394e42d64f5e7de914be9b4990fec21d`  
		Last Modified: Wed, 19 Feb 2025 19:26:13 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d9d462aa77ec007fbeffc1dee42df4cd4a71183e9e8428cdd7953d37bf652`  
		Last Modified: Wed, 19 Feb 2025 19:26:15 GMT  
		Size: 18.4 MB (18413407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ebefb617d29bf3d664c14a93a8d6af6169ff30bede662b6427222e19ead23e`  
		Last Modified: Wed, 19 Feb 2025 19:26:16 GMT  
		Size: 18.5 MB (18457784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfde26c05a0c43440279088e13663a7a1d54d60fc79a334f7efc7c2d97ac5cf4`  
		Last Modified: Wed, 19 Feb 2025 19:26:15 GMT  
		Size: 19.2 MB (19175087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63356e70e776cf3f69c9c71c36110eef0d389fa3d3031f61530a5690b4aef020`  
		Last Modified: Wed, 19 Feb 2025 19:26:13 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623035a000b7c0fd3795aadbe0a1896ab131817b4d53c047c6698f65f4c910ab`  
		Last Modified: Wed, 19 Feb 2025 19:26:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c85bbe716c49f7bb8731d7ac0bf65f0b6d6d65a93e1d5f9344d3cca378f284`  
		Last Modified: Wed, 19 Feb 2025 19:26:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d77018210f192a8f3a153def365573764b3b2bbc2a225a7d7f121de0d359ba4`  
		Last Modified: Wed, 19 Feb 2025 20:33:00 GMT  
		Size: 7.0 MB (6978851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46306e777430bd461589041ef5e1b2732743f437985659be3ff93ced09d8042`  
		Last Modified: Wed, 19 Feb 2025 20:32:51 GMT  
		Size: 99.4 KB (99381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde0afecbb84ea048248cd26c2553798898a1f1856a9c2318f81b40e47798954`  
		Last Modified: Wed, 19 Feb 2025 20:32:50 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ef1d8041a787834ea307ebc08a6c7a732c521fad26992f0fe82409b302de6a`  
		Last Modified: Wed, 19 Feb 2025 20:33:07 GMT  
		Size: 55.6 MB (55565415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b553d4ac0e9d181c727f58d22104b70b1db592d987dd2d81dbe68c047bef9`  
		Last Modified: Wed, 19 Feb 2025 20:32:50 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ec7eb8ba81e2cf67cea95fbf7089386677fae3ccd50d30918e4dfda64151b6`  
		Last Modified: Wed, 19 Feb 2025 20:32:49 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4e35e28f108131153e9696002821c069458aa658629d4adb0c08d45f19349d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c6720f09ff885df995770ca1d10e2a5668a4dbc457a5c532413dd658791ebb`

```dockerfile
```

-	Layers:
	-	`sha256:c921013bae926dd0d25a59bce5bd9d2b701b566c1cf4d8ca098c1015310a36ae`  
		Last Modified: Thu, 20 Feb 2025 00:08:13 GMT  
		Size: 34.3 KB (34327 bytes)  
		MIME: application/vnd.in-toto+json
