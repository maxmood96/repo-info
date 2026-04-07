<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.4`](#docker294)
-	[`docker:29.4-cli`](#docker294-cli)
-	[`docker:29.4-dind`](#docker294-dind)
-	[`docker:29.4-dind-rootless`](#docker294-dind-rootless)
-	[`docker:29.4-windowsservercore`](#docker294-windowsservercore)
-	[`docker:29.4-windowsservercore-ltsc2022`](#docker294-windowsservercore-ltsc2022)
-	[`docker:29.4-windowsservercore-ltsc2025`](#docker294-windowsservercore-ltsc2025)
-	[`docker:29.4.0`](#docker2940)
-	[`docker:29.4.0-alpine3.23`](#docker2940-alpine323)
-	[`docker:29.4.0-cli`](#docker2940-cli)
-	[`docker:29.4.0-cli-alpine3.23`](#docker2940-cli-alpine323)
-	[`docker:29.4.0-dind`](#docker2940-dind)
-	[`docker:29.4.0-dind-alpine3.23`](#docker2940-dind-alpine323)
-	[`docker:29.4.0-dind-rootless`](#docker2940-dind-rootless)
-	[`docker:29.4.0-windowsservercore`](#docker2940-windowsservercore)
-	[`docker:29.4.0-windowsservercore-ltsc2022`](#docker2940-windowsservercore-ltsc2022)
-	[`docker:29.4.0-windowsservercore-ltsc2025`](#docker2940-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:f80c26212befc1c1988b529495532c6b9180d9b1dab1611f4a1efbe9da8ec821
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

### `docker:29` - linux; amd64

```console
$ docker pull docker@sha256:287ae43017f5d929fe86b951861c6a17c47a18920dbec865d401a08aa827f6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140530015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f374b8d47eebfb2450d5a19efc473c1d20bf645f84c46c21c2854377688446`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:36 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074da42c286968f826b040d456a99617b43bda2cc5bf557dceea3de5d6cc4fe`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 6.9 MB (6941677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f4ce6ca5a90a42c5d8d8c00baea57cee587bb141c85bab7aff5de38c99737`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21abf0696dc4d51910e445d2f536ad172bfde41b5963779800c78584ab0b7c`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa3ba34873437febe66dfabe21b09faedd97173ea3f99cdfac49a4960a6f22`  
		Last Modified: Tue, 07 Apr 2026 18:03:49 GMT  
		Size: 68.3 MB (68266949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7a5643b3f629c64a89c9a7665a2102ef8d1b9fe06893fd322d2184c711b5bf`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911bab9d694e25eb17eb5d3df1bd3e09f0ea52d970ce04fa58c0b41861ff8a`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:73b899bc96cf92b0e9a346d2299d110d3fe56b6155f1219dc06b4d4e6172268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc72525e88ac1b74d2507c98202bc1732e6931e5409efa62649aeecef0bda2cf`

```dockerfile
```

-	Layers:
	-	`sha256:57834d73984ba9824980e22fe7ed18b2b1e911c35b6f27dc4f2b7486672e6a28`  
		Last Modified: Tue, 07 Apr 2026 18:03:46 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:d94555deb39a31975ca0a7df7f6f607745e2e3cea98b85279ecab2d2179e2d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132509296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342e83533005345d07b6aa7ba5cc4aa7efe7c9bf531476ab6309626983b8ad35`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:52:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:52:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:52:27 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:31 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b23450f59ae29757b818023e9e1ec7feecec88f0bdffda20a422b2bf40901`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 8.3 MB (8300867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016992555c050a7efd3e0035e8b9a0552c0b9ed2c184291a79aafac5eec2bdb`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c85acb49acf037dbe3345d449eb1c7352be8603c84cbe00120ea39e3d7c30`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 18.1 MB (18109482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e782e8b1924d10e930976d421346c23ca8082dc4665b434c499c55cacdfb8`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 21.2 MB (21151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521a4f32de85375d05302a7d66d9f4b7b8d2e2750474fe3a0ae65c01908aaee`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 10.4 MB (10388830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615f51faa1cea9baac6124a72554172703a48489cfa064d499cb85dbb594352`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9369afbb000ee5860be68de87ea400bade9c679f1e5f9807ee421b61828989`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70ec8240492116e39d00b6dca97c3a28a1163f7e2170ccc530976b2319f26`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b98d7b3e63b394195345d7cb8704aca5c40c08c77a0bf1332fe636cdf85f8f`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 7.3 MB (7278270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bf81f4773f03aaa784a3470bcce2edc2b6a47934ee47acb8cca08a5f355c98`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 91.8 KB (91782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200628578e34b666753dac7e5f675103937c5bc8b19ee1944b18678f0c46925d`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd2d115f337cd4f0d6b8569b2b846987f6e9ac5e092ef1ff0d4ddf55d6e1bd5`  
		Last Modified: Tue, 07 Apr 2026 18:03:44 GMT  
		Size: 63.6 MB (63610216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cae13c6f8720e02fe0cfac11bf4b7873b5127026edf0fd7d60f3869d6d7419`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f9f1d6532df85ab83bce5d7ef4d79e700e0400906d7758bc10171637fb4789`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:47c1c2e7f2d77d352752eed854ede75fe2b99d09a4d2803179083cb08ff22f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6e98380b13b625be9b687b14bd321547ba3ab0a5453ab8bc4373d0660c5188`

```dockerfile
```

-	Layers:
	-	`sha256:e1ee81fe381e2225b1105e6c67bdff7bcb2289618bb0a726e2ed400b0fcfe1c8`  
		Last Modified: Tue, 07 Apr 2026 18:03:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:2fe5918d6fc855d73d4a3f2a00996b7f0a34b7634e179ac2122c2fbdf43a4875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c711cf90ab57665fc3f8f136101a98f0aaaee0ddc5bc0c9f79d5a22477161a42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:56:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:56:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:56:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:56:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:56:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:56:46 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:04:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:04:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:04:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:04:07 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d02ce67b4a0275f7c58bea67b202248f2e1fadee3c6981a52b02af3245dc7`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 7.6 MB (7597809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae114ba08bb257f6560a48e6f42e0eca1e4275b2b1f5de1a5cee3264ac227117`  
		Last Modified: Tue, 07 Apr 2026 17:56:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c462895e881488d974811c947d011f385c58e7837ee4a36e8eb5347cbfbdead`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 18.1 MB (18096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed288924400fa0ef850973ed05b5d68ad1e971d6db3475e8ec6a66996d1f004e`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 21.1 MB (21129730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562fb47ee8e5eb694e39d13d273c9a20343c2611795f59bf060f8896ad84505`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 10.4 MB (10371866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322fadd946101bd1db893bbeab2210077c079947108eba25d61f69bc80b86918`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee11a625998530da0978a257398229bdf229cb3172d2623d63cdaa10a04dd37`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463989f7f6b0810cca12186041f47307814448d147f72bff8a0f48239efc234`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a7a76c7cd299a0667f840f572155fe9e35f5013b5de4e51f836ad166de3094`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 6.6 MB (6576415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecd37ed33aacb16975753b152fd51f47fa1fbd0fbe582cd884e8bc88c7799c9`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 88.1 KB (88144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30c893cca62c4ce187fe0f0df7e1fd32feb7517ce8a8eb10261e08b67c2278f`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2d730ff02f4343d65bdc6f1fbb29d1061a9c64e3f5203d8cf70317d19e67a9`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 63.4 MB (63443312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa38e3d8f2a4334f08fc240f45a7b0857ce64907ba89486d374dbb923fcf33`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522011f6d7ed1009e68e424d9c164d16256d49b5b7421bdb47645f431d7e045a`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:75635ebd248b76a3aa73452fa66599686679233c7faf894570e4870a738fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02726225a9427a640d5001f15d02f9ac80332f8cbdbc5779ef715424b359cecf`

```dockerfile
```

-	Layers:
	-	`sha256:24502e0bf1bc549b64a110973e89bb2b40d90b3444bca7efb104a37f5c4c2e51`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f56f84c60b1ad8653eb423810cca82f8d86d0f97af8f600b2089d7a79b2c67e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130127448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d9a5c2e9415e93f5577fa9935ab7f163c07791bcca430cfa8100bb716915`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:25 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b00d7b9300d4ebf88506edbb338095cf5ad19da1ef0cbef84ae82dd84a0bcb`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 7.2 MB (7219468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa958935e1bc1165d4187e06c145c326c85b4154be3e340a1f57fffa4ae15fb7`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a18406c30abb1ed5c938e64854db122e53e7024a5ee5c6b95ce9c37675aa5`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e20c26df1d1cb588216d065b94856a954f64f3a2fc7252c355c624cf06f166`  
		Last Modified: Tue, 07 Apr 2026 18:03:36 GMT  
		Size: 61.8 MB (61791015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b1556da54467a07970b25f2f5e904eea0cb264745a4cd40a88db0ff73a276d`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d51a5932c15f504e0507fa22ab23138015cb8597493fd874d959868102059`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:bc33b62b3ef0f1578e119860d5ccc0bd861f6609d97646a69dc27aea75ab9f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21911a20c08d97ff5d0322eed178a80fae80aea719d8f4c5a2093b0e81e79b99`

```dockerfile
```

-	Layers:
	-	`sha256:63938660feb79291b998f4f1c0122abb056fe223055a32f41a8d543218bbadea`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:0befd75049d8903cd5606879d251bd29ac08758cd33f9c7c74583fc6679b737d
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

### `docker:29-cli` - linux; amd64

```console
$ docker pull docker@sha256:162f671f43d999a41de10577c292392d92df278f2b19619bd00f62702b9aa2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65222927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad9b141cd1de25bf040248038f95cd6219a80703fd707e59b2b6a0517308b72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:daf7ceb8c94a68d086116d67088dcb70baa3ccd572ff5c33286ad2106b907897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7290d94403713e42feb20ce8a180e2fdd9faf2f4c61c1e6a56befb117afe1fc8`

```dockerfile
```

-	Layers:
	-	`sha256:b95f79229ba482446ea56f9b087844cfdb759933700550eda0ac85aa7b865ed4`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:01b9514d3a7731ab09e57a066f6f57fc6bfd443cc4bb281b5defbf46434d784f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61523027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e6afc4be332ae73538fea1317c86c824dc8f3fed5bd6479ef0f3623fd66f2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:52:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:52:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:52:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b23450f59ae29757b818023e9e1ec7feecec88f0bdffda20a422b2bf40901`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 8.3 MB (8300867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016992555c050a7efd3e0035e8b9a0552c0b9ed2c184291a79aafac5eec2bdb`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c85acb49acf037dbe3345d449eb1c7352be8603c84cbe00120ea39e3d7c30`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 18.1 MB (18109482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e782e8b1924d10e930976d421346c23ca8082dc4665b434c499c55cacdfb8`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 21.2 MB (21151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521a4f32de85375d05302a7d66d9f4b7b8d2e2750474fe3a0ae65c01908aaee`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 10.4 MB (10388830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615f51faa1cea9baac6124a72554172703a48489cfa064d499cb85dbb594352`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9369afbb000ee5860be68de87ea400bade9c679f1e5f9807ee421b61828989`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70ec8240492116e39d00b6dca97c3a28a1163f7e2170ccc530976b2319f26`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:005090b7bbeeb700acbccd357974890d0823f6b05afd754f62123ce0cc2c9327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746bfb0046c73dc782de8b20a9ce871dc02be903bb3305fb32d83c36465c4b61`

```dockerfile
```

-	Layers:
	-	`sha256:1d9d1c99fe378084950dc2c8f24e70107427c1736e16ba6a42be234d1fc3e615`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:b5e13676109eba75e0291b50c5457e21aa02414b1ba2eca698d6385511dfa8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60479667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431a96e79c5bb0cc3f234407c79cd071478587e33cdf94a2ede1122d0c0f9873`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:56:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:56:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:56:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:56:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:56:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:56:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d02ce67b4a0275f7c58bea67b202248f2e1fadee3c6981a52b02af3245dc7`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 7.6 MB (7597809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae114ba08bb257f6560a48e6f42e0eca1e4275b2b1f5de1a5cee3264ac227117`  
		Last Modified: Tue, 07 Apr 2026 17:56:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c462895e881488d974811c947d011f385c58e7837ee4a36e8eb5347cbfbdead`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 18.1 MB (18096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed288924400fa0ef850973ed05b5d68ad1e971d6db3475e8ec6a66996d1f004e`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 21.1 MB (21129730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562fb47ee8e5eb694e39d13d273c9a20343c2611795f59bf060f8896ad84505`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 10.4 MB (10371866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322fadd946101bd1db893bbeab2210077c079947108eba25d61f69bc80b86918`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee11a625998530da0978a257398229bdf229cb3172d2623d63cdaa10a04dd37`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463989f7f6b0810cca12186041f47307814448d147f72bff8a0f48239efc234`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:00955fd445b2706d6540aec431b00eaff21297aff36f366d2b10b3f4f0e74a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9541b749d18a90c9233171b4a24d5ec5360a879be45ca225522b51eda41825`

```dockerfile
```

-	Layers:
	-	`sha256:58793278463a7baf2e54d0b9ec3edfaaaa4bf35057e379c728b4864ddbed92d5`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:db0c05a4aab745e54662ec56befe45e3c265f485d9d7c7e2d1ffe32f2131448d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61009679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65923880c0dee4eabcf3f64a2fc3e0cc27a7b521fd83945232a7c2c587ae70bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:7b06c415f269961efe974617d3e8b045f801c7e82fe1ef4eac6a74707b63420c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4b4265560dfb409203188b0903d9895666374d935b7351a099c296894efbf8`

```dockerfile
```

-	Layers:
	-	`sha256:983969a38dd490d16487039ccb7e1f62968548fc8a488c859ddd9e62a80382df`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:f80c26212befc1c1988b529495532c6b9180d9b1dab1611f4a1efbe9da8ec821
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

### `docker:29-dind` - linux; amd64

```console
$ docker pull docker@sha256:287ae43017f5d929fe86b951861c6a17c47a18920dbec865d401a08aa827f6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140530015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f374b8d47eebfb2450d5a19efc473c1d20bf645f84c46c21c2854377688446`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:36 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074da42c286968f826b040d456a99617b43bda2cc5bf557dceea3de5d6cc4fe`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 6.9 MB (6941677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f4ce6ca5a90a42c5d8d8c00baea57cee587bb141c85bab7aff5de38c99737`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21abf0696dc4d51910e445d2f536ad172bfde41b5963779800c78584ab0b7c`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa3ba34873437febe66dfabe21b09faedd97173ea3f99cdfac49a4960a6f22`  
		Last Modified: Tue, 07 Apr 2026 18:03:49 GMT  
		Size: 68.3 MB (68266949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7a5643b3f629c64a89c9a7665a2102ef8d1b9fe06893fd322d2184c711b5bf`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911bab9d694e25eb17eb5d3df1bd3e09f0ea52d970ce04fa58c0b41861ff8a`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:73b899bc96cf92b0e9a346d2299d110d3fe56b6155f1219dc06b4d4e6172268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc72525e88ac1b74d2507c98202bc1732e6931e5409efa62649aeecef0bda2cf`

```dockerfile
```

-	Layers:
	-	`sha256:57834d73984ba9824980e22fe7ed18b2b1e911c35b6f27dc4f2b7486672e6a28`  
		Last Modified: Tue, 07 Apr 2026 18:03:46 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:d94555deb39a31975ca0a7df7f6f607745e2e3cea98b85279ecab2d2179e2d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132509296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342e83533005345d07b6aa7ba5cc4aa7efe7c9bf531476ab6309626983b8ad35`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:52:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:52:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:52:27 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:31 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b23450f59ae29757b818023e9e1ec7feecec88f0bdffda20a422b2bf40901`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 8.3 MB (8300867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016992555c050a7efd3e0035e8b9a0552c0b9ed2c184291a79aafac5eec2bdb`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c85acb49acf037dbe3345d449eb1c7352be8603c84cbe00120ea39e3d7c30`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 18.1 MB (18109482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e782e8b1924d10e930976d421346c23ca8082dc4665b434c499c55cacdfb8`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 21.2 MB (21151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521a4f32de85375d05302a7d66d9f4b7b8d2e2750474fe3a0ae65c01908aaee`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 10.4 MB (10388830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615f51faa1cea9baac6124a72554172703a48489cfa064d499cb85dbb594352`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9369afbb000ee5860be68de87ea400bade9c679f1e5f9807ee421b61828989`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70ec8240492116e39d00b6dca97c3a28a1163f7e2170ccc530976b2319f26`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b98d7b3e63b394195345d7cb8704aca5c40c08c77a0bf1332fe636cdf85f8f`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 7.3 MB (7278270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bf81f4773f03aaa784a3470bcce2edc2b6a47934ee47acb8cca08a5f355c98`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 91.8 KB (91782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200628578e34b666753dac7e5f675103937c5bc8b19ee1944b18678f0c46925d`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd2d115f337cd4f0d6b8569b2b846987f6e9ac5e092ef1ff0d4ddf55d6e1bd5`  
		Last Modified: Tue, 07 Apr 2026 18:03:44 GMT  
		Size: 63.6 MB (63610216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cae13c6f8720e02fe0cfac11bf4b7873b5127026edf0fd7d60f3869d6d7419`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f9f1d6532df85ab83bce5d7ef4d79e700e0400906d7758bc10171637fb4789`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:47c1c2e7f2d77d352752eed854ede75fe2b99d09a4d2803179083cb08ff22f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6e98380b13b625be9b687b14bd321547ba3ab0a5453ab8bc4373d0660c5188`

```dockerfile
```

-	Layers:
	-	`sha256:e1ee81fe381e2225b1105e6c67bdff7bcb2289618bb0a726e2ed400b0fcfe1c8`  
		Last Modified: Tue, 07 Apr 2026 18:03:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:2fe5918d6fc855d73d4a3f2a00996b7f0a34b7634e179ac2122c2fbdf43a4875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c711cf90ab57665fc3f8f136101a98f0aaaee0ddc5bc0c9f79d5a22477161a42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:56:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:56:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:56:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:56:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:56:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:56:46 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:04:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:04:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:04:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:04:07 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d02ce67b4a0275f7c58bea67b202248f2e1fadee3c6981a52b02af3245dc7`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 7.6 MB (7597809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae114ba08bb257f6560a48e6f42e0eca1e4275b2b1f5de1a5cee3264ac227117`  
		Last Modified: Tue, 07 Apr 2026 17:56:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c462895e881488d974811c947d011f385c58e7837ee4a36e8eb5347cbfbdead`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 18.1 MB (18096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed288924400fa0ef850973ed05b5d68ad1e971d6db3475e8ec6a66996d1f004e`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 21.1 MB (21129730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562fb47ee8e5eb694e39d13d273c9a20343c2611795f59bf060f8896ad84505`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 10.4 MB (10371866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322fadd946101bd1db893bbeab2210077c079947108eba25d61f69bc80b86918`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee11a625998530da0978a257398229bdf229cb3172d2623d63cdaa10a04dd37`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463989f7f6b0810cca12186041f47307814448d147f72bff8a0f48239efc234`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a7a76c7cd299a0667f840f572155fe9e35f5013b5de4e51f836ad166de3094`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 6.6 MB (6576415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecd37ed33aacb16975753b152fd51f47fa1fbd0fbe582cd884e8bc88c7799c9`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 88.1 KB (88144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30c893cca62c4ce187fe0f0df7e1fd32feb7517ce8a8eb10261e08b67c2278f`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2d730ff02f4343d65bdc6f1fbb29d1061a9c64e3f5203d8cf70317d19e67a9`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 63.4 MB (63443312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa38e3d8f2a4334f08fc240f45a7b0857ce64907ba89486d374dbb923fcf33`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522011f6d7ed1009e68e424d9c164d16256d49b5b7421bdb47645f431d7e045a`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:75635ebd248b76a3aa73452fa66599686679233c7faf894570e4870a738fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02726225a9427a640d5001f15d02f9ac80332f8cbdbc5779ef715424b359cecf`

```dockerfile
```

-	Layers:
	-	`sha256:24502e0bf1bc549b64a110973e89bb2b40d90b3444bca7efb104a37f5c4c2e51`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f56f84c60b1ad8653eb423810cca82f8d86d0f97af8f600b2089d7a79b2c67e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130127448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d9a5c2e9415e93f5577fa9935ab7f163c07791bcca430cfa8100bb716915`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:25 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b00d7b9300d4ebf88506edbb338095cf5ad19da1ef0cbef84ae82dd84a0bcb`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 7.2 MB (7219468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa958935e1bc1165d4187e06c145c326c85b4154be3e340a1f57fffa4ae15fb7`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a18406c30abb1ed5c938e64854db122e53e7024a5ee5c6b95ce9c37675aa5`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e20c26df1d1cb588216d065b94856a954f64f3a2fc7252c355c624cf06f166`  
		Last Modified: Tue, 07 Apr 2026 18:03:36 GMT  
		Size: 61.8 MB (61791015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b1556da54467a07970b25f2f5e904eea0cb264745a4cd40a88db0ff73a276d`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d51a5932c15f504e0507fa22ab23138015cb8597493fd874d959868102059`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:bc33b62b3ef0f1578e119860d5ccc0bd861f6609d97646a69dc27aea75ab9f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21911a20c08d97ff5d0322eed178a80fae80aea719d8f4c5a2093b0e81e79b99`

```dockerfile
```

-	Layers:
	-	`sha256:63938660feb79291b998f4f1c0122abb056fe223055a32f41a8d543218bbadea`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:06cbcbc282cf54fc1c4c2c326d236bb3e8aeaf9928c946f5a5128f1077994913
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e8017dfd3cd4ec88a74e0c0799896877e783a0cc3c936a5b6a58c846b963d5d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161531714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b75307842b323b7da6d0ef282d8bceb758e2399303655d255714432b4e1add`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:36 GMT
CMD []
# Tue, 07 Apr 2026 18:06:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 07 Apr 2026 18:06:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 07 Apr 2026 18:06:51 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074da42c286968f826b040d456a99617b43bda2cc5bf557dceea3de5d6cc4fe`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 6.9 MB (6941677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f4ce6ca5a90a42c5d8d8c00baea57cee587bb141c85bab7aff5de38c99737`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21abf0696dc4d51910e445d2f536ad172bfde41b5963779800c78584ab0b7c`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa3ba34873437febe66dfabe21b09faedd97173ea3f99cdfac49a4960a6f22`  
		Last Modified: Tue, 07 Apr 2026 18:03:49 GMT  
		Size: 68.3 MB (68266949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7a5643b3f629c64a89c9a7665a2102ef8d1b9fe06893fd322d2184c711b5bf`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911bab9d694e25eb17eb5d3df1bd3e09f0ea52d970ce04fa58c0b41861ff8a`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d755e56ce2d2de497c291abe2cb3c543234d57811aa6cc31892539b9612766`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 3.4 MB (3419944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5a1bed895274e6a0aa4e6518ecea2b536c06de2ba8ff8d46f1780b3d1df919`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb54c75cdd29b9362c1d06f6660d0f7d8d7bbe7893e0b9ce825e1b83aaa0561`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab93e7606625323931d20ec97f988d0e03a1d70170464edf09698a7e5ed0c824`  
		Last Modified: Tue, 07 Apr 2026 18:06:58 GMT  
		Size: 17.6 MB (17580413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102bb795e921727afa1a0d32ec9a3ad5a0ee29c9ff396cd792983d41bf76d7c0`  
		Last Modified: Tue, 07 Apr 2026 18:06:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2393d1f43dc15591888c4c108dd057ac24c8b75e437c291786978dfa8055cbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4157e73cac3aafdf5ccdcb29066abeb8fe640483f2b59b1769e2f1b2e1626873`

```dockerfile
```

-	Layers:
	-	`sha256:a427061545c1c404aa1ff5448e2d7ddef22f9ce7690bf471b5c9b5d8cf59b5cf`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d8d9eab16c89792d62362031ddcf62ab255f8de04859c7c424a4da9570ffa2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151405963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd234006ba72c0f64937b10d1d687a972e3973eb0ee05cb2d02dfceac3ea6473`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:25 GMT
CMD []
# Tue, 07 Apr 2026 18:07:07 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 07 Apr 2026 18:07:07 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 07 Apr 2026 18:07:07 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:07:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 07 Apr 2026 18:07:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 07 Apr 2026 18:07:08 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 07 Apr 2026 18:07:08 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b00d7b9300d4ebf88506edbb338095cf5ad19da1ef0cbef84ae82dd84a0bcb`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 7.2 MB (7219468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa958935e1bc1165d4187e06c145c326c85b4154be3e340a1f57fffa4ae15fb7`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a18406c30abb1ed5c938e64854db122e53e7024a5ee5c6b95ce9c37675aa5`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e20c26df1d1cb588216d065b94856a954f64f3a2fc7252c355c624cf06f166`  
		Last Modified: Tue, 07 Apr 2026 18:03:36 GMT  
		Size: 61.8 MB (61791015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b1556da54467a07970b25f2f5e904eea0cb264745a4cd40a88db0ff73a276d`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d51a5932c15f504e0507fa22ab23138015cb8597493fd874d959868102059`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd008e50d6fda4dec99a7345870c1aaa5e47590866dc1a8b580f63be5b4ba1fe`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 3.4 MB (3394378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84d9a19178955f77588d5e575ba89ed64e606150680ee055d3e7f81a7c9e19c`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df25b78e32b01224db4177327e28b0c5aa1fdc8df4fa296b7a11dc254cad6294`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6326173b0d2b0474538dc36d4f09aec863c9d8cc8853c4b8d2b9e6239e5c2de`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 17.9 MB (17882798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e473478b98a0d67b7e5082a1fdfc46efa97b2774cffe12a23e7e330c541ebb4`  
		Last Modified: Tue, 07 Apr 2026 18:07:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a6cf4e5aa66894ec1c5141441bae823cbaf150cdf7799cf03f319eaa34a36fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9213b6754bae917b8aa66937ca0fd9d823685fe09c4ffc75849dfffef3543b9`

```dockerfile
```

-	Layers:
	-	`sha256:185779fc84203fff8c14a24aba62314b0a891054f60dc2387016673e9c80c735`  
		Last Modified: Tue, 07 Apr 2026 18:07:13 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:38716da2bf6648465dcaf041bb44f5a4c216b8ce28dd7b2f1021a590fa6ecc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:1805bfa9662cfa4218077bd8ede9b5a6d69c6646439b7521c0bbbd1d6d516f31
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136863509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9768faff7c37bf673323e8563e2159940625e141fc4292c86de2abcec477d7dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 07 Apr 2026 17:45:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:52 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6349df402a8ae75343c96cbbf6fda362d5255740fa6a27c40633fdd74cb8b486`  
		Last Modified: Tue, 07 Apr 2026 17:47:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbaff7ffcff282be3a7cf2b17c33b81d01113cfd9c33a3dd1fc69933363cb882`  
		Last Modified: Tue, 07 Apr 2026 18:06:25 GMT  
		Size: 381.7 KB (381735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4e33ae54c24d17b8b0322f13394b73fa21b1b3a8aa5f40459be12d90d95e8`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe5a20a0f91f2d088cb920e67e52856b75d803e8f11af764c8d124f2dcd93c`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a11f5b4aabfe9b04c01662839eef4d615567e211f283c6e7818e52b3668d661`  
		Last Modified: Tue, 07 Apr 2026 18:06:27 GMT  
		Size: 20.2 MB (20166075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683aaeb151b66e53b1096f22b39533930cef0c1c98a4745f57e71a5f01fb8a0a`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b99e49f048c1ff00de08fd0e6c43a403ab69c2ba7638830c82c36da218d8d`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683624596fd59caecf2e64b0bbfd45b372c1f6869db5c6cfb23fb047bf51eec5`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3391b63f468d72f2045f24a2a8bf86bc454e7bde74c6d8f9b32fcca119e80b`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 23.4 MB (23447007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3612cdb40d7bf90e6e50f9f05c5c7602d11d06a46cca4a6c6482fdd833f1cac3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8ba35ebad23e35edac88bbe0a734de8b14825a7f0651ae67b85224128272b3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df6d8c50c80a893ae84a723eeb4dec4099df9a827b91826b40e1759a9b99509`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1af4d02e803d87cc569e51d6f3511d7ceaac2fe30774f4ea6d1a356e42f89ef`  
		Last Modified: Tue, 07 Apr 2026 18:06:23 GMT  
		Size: 11.7 MB (11660920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:f37ee3a5fbb958e19138ee2f09d74c58542c532617c7657817359dd37da7472a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2038007541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c93fe0bda8880246418c197b65f4235c5e9f167a5bd4bfd6ce249972e6c5c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 07 Apr 2026 17:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:43 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:46 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:10 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d3d1e4e44fed34fcadd7a99422714da9b20d4f49e0a6fb695d9b5ea818a9ac`  
		Last Modified: Tue, 07 Apr 2026 17:41:02 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9c300c06bd98acbe2efc0c277d580fece563c470038eb8f74d2dd922de94d2`  
		Last Modified: Tue, 07 Apr 2026 18:06:29 GMT  
		Size: 496.2 KB (496237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ff057fe30ee36a89c50acd5ea6585849fb0687ecc19793300b7ee68e4a96bd`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8134fe4ef0e8a711d1eb7bffb1301a576b73a62f71eecd8dfae02f4a50af8d7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bb0fe00c187e5f0aa9c4e431ee26a5472aa893ef9395cead9bc41b53d8bf24`  
		Last Modified: Tue, 07 Apr 2026 18:06:30 GMT  
		Size: 20.1 MB (20143093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3c598636682c6365d6f6dcb67f2fe461dec34bdafe63d7f06138a9b371bdf5`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efee4361413a5695bc83bc76f10df48ec89643440981ead7d535b2b6134a434`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94b089de7840afa203de00c1150ca0636ad534b44e02169335c5c801b3db6b9`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2debda1316a8781d0d548bbf802336d7b4de1ba27198d02473ac96035360f7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 23.4 MB (23432756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca2269f79a5fe310160fcdd23d20b43df2a3547e81e8b04d06f3f25d1dcf8d3`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a834edccd436ba139fc54989c90c4fc8df0d139404714500103d3aa97ccbf512`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906a82b2a03d5ef6e2950ddf7f1680dfea855e0cda9e1123483778f916e7ba8e`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29a6939b1400dc3f52e8fff687d10e51c019eac0f3acf953221086d503f71b6`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 11.6 MB (11642251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c577bbb3fdf12421850d9d7d9c2ede8620846655f6110ad10b6b9c0757a6ad12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:f37ee3a5fbb958e19138ee2f09d74c58542c532617c7657817359dd37da7472a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2038007541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c93fe0bda8880246418c197b65f4235c5e9f167a5bd4bfd6ce249972e6c5c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 07 Apr 2026 17:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:43 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:46 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:10 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d3d1e4e44fed34fcadd7a99422714da9b20d4f49e0a6fb695d9b5ea818a9ac`  
		Last Modified: Tue, 07 Apr 2026 17:41:02 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9c300c06bd98acbe2efc0c277d580fece563c470038eb8f74d2dd922de94d2`  
		Last Modified: Tue, 07 Apr 2026 18:06:29 GMT  
		Size: 496.2 KB (496237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ff057fe30ee36a89c50acd5ea6585849fb0687ecc19793300b7ee68e4a96bd`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8134fe4ef0e8a711d1eb7bffb1301a576b73a62f71eecd8dfae02f4a50af8d7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bb0fe00c187e5f0aa9c4e431ee26a5472aa893ef9395cead9bc41b53d8bf24`  
		Last Modified: Tue, 07 Apr 2026 18:06:30 GMT  
		Size: 20.1 MB (20143093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3c598636682c6365d6f6dcb67f2fe461dec34bdafe63d7f06138a9b371bdf5`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efee4361413a5695bc83bc76f10df48ec89643440981ead7d535b2b6134a434`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94b089de7840afa203de00c1150ca0636ad534b44e02169335c5c801b3db6b9`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2debda1316a8781d0d548bbf802336d7b4de1ba27198d02473ac96035360f7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 23.4 MB (23432756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca2269f79a5fe310160fcdd23d20b43df2a3547e81e8b04d06f3f25d1dcf8d3`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a834edccd436ba139fc54989c90c4fc8df0d139404714500103d3aa97ccbf512`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906a82b2a03d5ef6e2950ddf7f1680dfea855e0cda9e1123483778f916e7ba8e`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29a6939b1400dc3f52e8fff687d10e51c019eac0f3acf953221086d503f71b6`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 11.6 MB (11642251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:822c277e276a37345c2329fab738fdf21ef45e0c7331a3d44f96d3f4520ff5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:1805bfa9662cfa4218077bd8ede9b5a6d69c6646439b7521c0bbbd1d6d516f31
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136863509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9768faff7c37bf673323e8563e2159940625e141fc4292c86de2abcec477d7dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 07 Apr 2026 17:45:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:52 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6349df402a8ae75343c96cbbf6fda362d5255740fa6a27c40633fdd74cb8b486`  
		Last Modified: Tue, 07 Apr 2026 17:47:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbaff7ffcff282be3a7cf2b17c33b81d01113cfd9c33a3dd1fc69933363cb882`  
		Last Modified: Tue, 07 Apr 2026 18:06:25 GMT  
		Size: 381.7 KB (381735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4e33ae54c24d17b8b0322f13394b73fa21b1b3a8aa5f40459be12d90d95e8`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe5a20a0f91f2d088cb920e67e52856b75d803e8f11af764c8d124f2dcd93c`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a11f5b4aabfe9b04c01662839eef4d615567e211f283c6e7818e52b3668d661`  
		Last Modified: Tue, 07 Apr 2026 18:06:27 GMT  
		Size: 20.2 MB (20166075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683aaeb151b66e53b1096f22b39533930cef0c1c98a4745f57e71a5f01fb8a0a`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b99e49f048c1ff00de08fd0e6c43a403ab69c2ba7638830c82c36da218d8d`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683624596fd59caecf2e64b0bbfd45b372c1f6869db5c6cfb23fb047bf51eec5`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3391b63f468d72f2045f24a2a8bf86bc454e7bde74c6d8f9b32fcca119e80b`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 23.4 MB (23447007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3612cdb40d7bf90e6e50f9f05c5c7602d11d06a46cca4a6c6482fdd833f1cac3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8ba35ebad23e35edac88bbe0a734de8b14825a7f0651ae67b85224128272b3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df6d8c50c80a893ae84a723eeb4dec4099df9a827b91826b40e1759a9b99509`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1af4d02e803d87cc569e51d6f3511d7ceaac2fe30774f4ea6d1a356e42f89ef`  
		Last Modified: Tue, 07 Apr 2026 18:06:23 GMT  
		Size: 11.7 MB (11660920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4`

```console
$ docker pull docker@sha256:f80c26212befc1c1988b529495532c6b9180d9b1dab1611f4a1efbe9da8ec821
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

### `docker:29.4` - linux; amd64

```console
$ docker pull docker@sha256:287ae43017f5d929fe86b951861c6a17c47a18920dbec865d401a08aa827f6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140530015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f374b8d47eebfb2450d5a19efc473c1d20bf645f84c46c21c2854377688446`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:36 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074da42c286968f826b040d456a99617b43bda2cc5bf557dceea3de5d6cc4fe`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 6.9 MB (6941677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f4ce6ca5a90a42c5d8d8c00baea57cee587bb141c85bab7aff5de38c99737`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21abf0696dc4d51910e445d2f536ad172bfde41b5963779800c78584ab0b7c`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa3ba34873437febe66dfabe21b09faedd97173ea3f99cdfac49a4960a6f22`  
		Last Modified: Tue, 07 Apr 2026 18:03:49 GMT  
		Size: 68.3 MB (68266949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7a5643b3f629c64a89c9a7665a2102ef8d1b9fe06893fd322d2184c711b5bf`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911bab9d694e25eb17eb5d3df1bd3e09f0ea52d970ce04fa58c0b41861ff8a`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4` - unknown; unknown

```console
$ docker pull docker@sha256:73b899bc96cf92b0e9a346d2299d110d3fe56b6155f1219dc06b4d4e6172268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc72525e88ac1b74d2507c98202bc1732e6931e5409efa62649aeecef0bda2cf`

```dockerfile
```

-	Layers:
	-	`sha256:57834d73984ba9824980e22fe7ed18b2b1e911c35b6f27dc4f2b7486672e6a28`  
		Last Modified: Tue, 07 Apr 2026 18:03:46 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4` - linux; arm variant v6

```console
$ docker pull docker@sha256:d94555deb39a31975ca0a7df7f6f607745e2e3cea98b85279ecab2d2179e2d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132509296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342e83533005345d07b6aa7ba5cc4aa7efe7c9bf531476ab6309626983b8ad35`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:52:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:52:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:52:27 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:31 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b23450f59ae29757b818023e9e1ec7feecec88f0bdffda20a422b2bf40901`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 8.3 MB (8300867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016992555c050a7efd3e0035e8b9a0552c0b9ed2c184291a79aafac5eec2bdb`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c85acb49acf037dbe3345d449eb1c7352be8603c84cbe00120ea39e3d7c30`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 18.1 MB (18109482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e782e8b1924d10e930976d421346c23ca8082dc4665b434c499c55cacdfb8`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 21.2 MB (21151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521a4f32de85375d05302a7d66d9f4b7b8d2e2750474fe3a0ae65c01908aaee`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 10.4 MB (10388830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615f51faa1cea9baac6124a72554172703a48489cfa064d499cb85dbb594352`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9369afbb000ee5860be68de87ea400bade9c679f1e5f9807ee421b61828989`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70ec8240492116e39d00b6dca97c3a28a1163f7e2170ccc530976b2319f26`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b98d7b3e63b394195345d7cb8704aca5c40c08c77a0bf1332fe636cdf85f8f`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 7.3 MB (7278270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bf81f4773f03aaa784a3470bcce2edc2b6a47934ee47acb8cca08a5f355c98`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 91.8 KB (91782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200628578e34b666753dac7e5f675103937c5bc8b19ee1944b18678f0c46925d`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd2d115f337cd4f0d6b8569b2b846987f6e9ac5e092ef1ff0d4ddf55d6e1bd5`  
		Last Modified: Tue, 07 Apr 2026 18:03:44 GMT  
		Size: 63.6 MB (63610216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cae13c6f8720e02fe0cfac11bf4b7873b5127026edf0fd7d60f3869d6d7419`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f9f1d6532df85ab83bce5d7ef4d79e700e0400906d7758bc10171637fb4789`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4` - unknown; unknown

```console
$ docker pull docker@sha256:47c1c2e7f2d77d352752eed854ede75fe2b99d09a4d2803179083cb08ff22f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6e98380b13b625be9b687b14bd321547ba3ab0a5453ab8bc4373d0660c5188`

```dockerfile
```

-	Layers:
	-	`sha256:e1ee81fe381e2225b1105e6c67bdff7bcb2289618bb0a726e2ed400b0fcfe1c8`  
		Last Modified: Tue, 07 Apr 2026 18:03:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4` - linux; arm variant v7

```console
$ docker pull docker@sha256:2fe5918d6fc855d73d4a3f2a00996b7f0a34b7634e179ac2122c2fbdf43a4875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c711cf90ab57665fc3f8f136101a98f0aaaee0ddc5bc0c9f79d5a22477161a42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:56:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:56:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:56:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:56:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:56:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:56:46 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:04:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:04:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:04:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:04:07 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d02ce67b4a0275f7c58bea67b202248f2e1fadee3c6981a52b02af3245dc7`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 7.6 MB (7597809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae114ba08bb257f6560a48e6f42e0eca1e4275b2b1f5de1a5cee3264ac227117`  
		Last Modified: Tue, 07 Apr 2026 17:56:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c462895e881488d974811c947d011f385c58e7837ee4a36e8eb5347cbfbdead`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 18.1 MB (18096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed288924400fa0ef850973ed05b5d68ad1e971d6db3475e8ec6a66996d1f004e`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 21.1 MB (21129730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562fb47ee8e5eb694e39d13d273c9a20343c2611795f59bf060f8896ad84505`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 10.4 MB (10371866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322fadd946101bd1db893bbeab2210077c079947108eba25d61f69bc80b86918`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee11a625998530da0978a257398229bdf229cb3172d2623d63cdaa10a04dd37`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463989f7f6b0810cca12186041f47307814448d147f72bff8a0f48239efc234`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a7a76c7cd299a0667f840f572155fe9e35f5013b5de4e51f836ad166de3094`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 6.6 MB (6576415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecd37ed33aacb16975753b152fd51f47fa1fbd0fbe582cd884e8bc88c7799c9`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 88.1 KB (88144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30c893cca62c4ce187fe0f0df7e1fd32feb7517ce8a8eb10261e08b67c2278f`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2d730ff02f4343d65bdc6f1fbb29d1061a9c64e3f5203d8cf70317d19e67a9`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 63.4 MB (63443312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa38e3d8f2a4334f08fc240f45a7b0857ce64907ba89486d374dbb923fcf33`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522011f6d7ed1009e68e424d9c164d16256d49b5b7421bdb47645f431d7e045a`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4` - unknown; unknown

```console
$ docker pull docker@sha256:75635ebd248b76a3aa73452fa66599686679233c7faf894570e4870a738fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02726225a9427a640d5001f15d02f9ac80332f8cbdbc5779ef715424b359cecf`

```dockerfile
```

-	Layers:
	-	`sha256:24502e0bf1bc549b64a110973e89bb2b40d90b3444bca7efb104a37f5c4c2e51`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f56f84c60b1ad8653eb423810cca82f8d86d0f97af8f600b2089d7a79b2c67e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130127448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d9a5c2e9415e93f5577fa9935ab7f163c07791bcca430cfa8100bb716915`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:25 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b00d7b9300d4ebf88506edbb338095cf5ad19da1ef0cbef84ae82dd84a0bcb`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 7.2 MB (7219468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa958935e1bc1165d4187e06c145c326c85b4154be3e340a1f57fffa4ae15fb7`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a18406c30abb1ed5c938e64854db122e53e7024a5ee5c6b95ce9c37675aa5`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e20c26df1d1cb588216d065b94856a954f64f3a2fc7252c355c624cf06f166`  
		Last Modified: Tue, 07 Apr 2026 18:03:36 GMT  
		Size: 61.8 MB (61791015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b1556da54467a07970b25f2f5e904eea0cb264745a4cd40a88db0ff73a276d`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d51a5932c15f504e0507fa22ab23138015cb8597493fd874d959868102059`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4` - unknown; unknown

```console
$ docker pull docker@sha256:bc33b62b3ef0f1578e119860d5ccc0bd861f6609d97646a69dc27aea75ab9f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21911a20c08d97ff5d0322eed178a80fae80aea719d8f4c5a2093b0e81e79b99`

```dockerfile
```

-	Layers:
	-	`sha256:63938660feb79291b998f4f1c0122abb056fe223055a32f41a8d543218bbadea`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4-cli`

```console
$ docker pull docker@sha256:0befd75049d8903cd5606879d251bd29ac08758cd33f9c7c74583fc6679b737d
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

### `docker:29.4-cli` - linux; amd64

```console
$ docker pull docker@sha256:162f671f43d999a41de10577c292392d92df278f2b19619bd00f62702b9aa2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65222927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad9b141cd1de25bf040248038f95cd6219a80703fd707e59b2b6a0517308b72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:daf7ceb8c94a68d086116d67088dcb70baa3ccd572ff5c33286ad2106b907897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7290d94403713e42feb20ce8a180e2fdd9faf2f4c61c1e6a56befb117afe1fc8`

```dockerfile
```

-	Layers:
	-	`sha256:b95f79229ba482446ea56f9b087844cfdb759933700550eda0ac85aa7b865ed4`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:01b9514d3a7731ab09e57a066f6f57fc6bfd443cc4bb281b5defbf46434d784f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61523027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e6afc4be332ae73538fea1317c86c824dc8f3fed5bd6479ef0f3623fd66f2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:52:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:52:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:52:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b23450f59ae29757b818023e9e1ec7feecec88f0bdffda20a422b2bf40901`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 8.3 MB (8300867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016992555c050a7efd3e0035e8b9a0552c0b9ed2c184291a79aafac5eec2bdb`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c85acb49acf037dbe3345d449eb1c7352be8603c84cbe00120ea39e3d7c30`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 18.1 MB (18109482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e782e8b1924d10e930976d421346c23ca8082dc4665b434c499c55cacdfb8`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 21.2 MB (21151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521a4f32de85375d05302a7d66d9f4b7b8d2e2750474fe3a0ae65c01908aaee`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 10.4 MB (10388830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615f51faa1cea9baac6124a72554172703a48489cfa064d499cb85dbb594352`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9369afbb000ee5860be68de87ea400bade9c679f1e5f9807ee421b61828989`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70ec8240492116e39d00b6dca97c3a28a1163f7e2170ccc530976b2319f26`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:005090b7bbeeb700acbccd357974890d0823f6b05afd754f62123ce0cc2c9327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746bfb0046c73dc782de8b20a9ce871dc02be903bb3305fb32d83c36465c4b61`

```dockerfile
```

-	Layers:
	-	`sha256:1d9d1c99fe378084950dc2c8f24e70107427c1736e16ba6a42be234d1fc3e615`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:b5e13676109eba75e0291b50c5457e21aa02414b1ba2eca698d6385511dfa8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60479667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431a96e79c5bb0cc3f234407c79cd071478587e33cdf94a2ede1122d0c0f9873`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:56:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:56:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:56:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:56:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:56:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:56:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d02ce67b4a0275f7c58bea67b202248f2e1fadee3c6981a52b02af3245dc7`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 7.6 MB (7597809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae114ba08bb257f6560a48e6f42e0eca1e4275b2b1f5de1a5cee3264ac227117`  
		Last Modified: Tue, 07 Apr 2026 17:56:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c462895e881488d974811c947d011f385c58e7837ee4a36e8eb5347cbfbdead`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 18.1 MB (18096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed288924400fa0ef850973ed05b5d68ad1e971d6db3475e8ec6a66996d1f004e`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 21.1 MB (21129730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562fb47ee8e5eb694e39d13d273c9a20343c2611795f59bf060f8896ad84505`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 10.4 MB (10371866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322fadd946101bd1db893bbeab2210077c079947108eba25d61f69bc80b86918`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee11a625998530da0978a257398229bdf229cb3172d2623d63cdaa10a04dd37`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463989f7f6b0810cca12186041f47307814448d147f72bff8a0f48239efc234`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:00955fd445b2706d6540aec431b00eaff21297aff36f366d2b10b3f4f0e74a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9541b749d18a90c9233171b4a24d5ec5360a879be45ca225522b51eda41825`

```dockerfile
```

-	Layers:
	-	`sha256:58793278463a7baf2e54d0b9ec3edfaaaa4bf35057e379c728b4864ddbed92d5`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:db0c05a4aab745e54662ec56befe45e3c265f485d9d7c7e2d1ffe32f2131448d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61009679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65923880c0dee4eabcf3f64a2fc3e0cc27a7b521fd83945232a7c2c587ae70bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-cli` - unknown; unknown

```console
$ docker pull docker@sha256:7b06c415f269961efe974617d3e8b045f801c7e82fe1ef4eac6a74707b63420c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4b4265560dfb409203188b0903d9895666374d935b7351a099c296894efbf8`

```dockerfile
```

-	Layers:
	-	`sha256:983969a38dd490d16487039ccb7e1f62968548fc8a488c859ddd9e62a80382df`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4-dind`

```console
$ docker pull docker@sha256:f80c26212befc1c1988b529495532c6b9180d9b1dab1611f4a1efbe9da8ec821
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

### `docker:29.4-dind` - linux; amd64

```console
$ docker pull docker@sha256:287ae43017f5d929fe86b951861c6a17c47a18920dbec865d401a08aa827f6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140530015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f374b8d47eebfb2450d5a19efc473c1d20bf645f84c46c21c2854377688446`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:36 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074da42c286968f826b040d456a99617b43bda2cc5bf557dceea3de5d6cc4fe`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 6.9 MB (6941677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f4ce6ca5a90a42c5d8d8c00baea57cee587bb141c85bab7aff5de38c99737`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21abf0696dc4d51910e445d2f536ad172bfde41b5963779800c78584ab0b7c`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa3ba34873437febe66dfabe21b09faedd97173ea3f99cdfac49a4960a6f22`  
		Last Modified: Tue, 07 Apr 2026 18:03:49 GMT  
		Size: 68.3 MB (68266949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7a5643b3f629c64a89c9a7665a2102ef8d1b9fe06893fd322d2184c711b5bf`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911bab9d694e25eb17eb5d3df1bd3e09f0ea52d970ce04fa58c0b41861ff8a`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:73b899bc96cf92b0e9a346d2299d110d3fe56b6155f1219dc06b4d4e6172268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc72525e88ac1b74d2507c98202bc1732e6931e5409efa62649aeecef0bda2cf`

```dockerfile
```

-	Layers:
	-	`sha256:57834d73984ba9824980e22fe7ed18b2b1e911c35b6f27dc4f2b7486672e6a28`  
		Last Modified: Tue, 07 Apr 2026 18:03:46 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:d94555deb39a31975ca0a7df7f6f607745e2e3cea98b85279ecab2d2179e2d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132509296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342e83533005345d07b6aa7ba5cc4aa7efe7c9bf531476ab6309626983b8ad35`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:52:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:52:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:52:27 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:31 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b23450f59ae29757b818023e9e1ec7feecec88f0bdffda20a422b2bf40901`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 8.3 MB (8300867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016992555c050a7efd3e0035e8b9a0552c0b9ed2c184291a79aafac5eec2bdb`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c85acb49acf037dbe3345d449eb1c7352be8603c84cbe00120ea39e3d7c30`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 18.1 MB (18109482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e782e8b1924d10e930976d421346c23ca8082dc4665b434c499c55cacdfb8`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 21.2 MB (21151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521a4f32de85375d05302a7d66d9f4b7b8d2e2750474fe3a0ae65c01908aaee`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 10.4 MB (10388830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615f51faa1cea9baac6124a72554172703a48489cfa064d499cb85dbb594352`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9369afbb000ee5860be68de87ea400bade9c679f1e5f9807ee421b61828989`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70ec8240492116e39d00b6dca97c3a28a1163f7e2170ccc530976b2319f26`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b98d7b3e63b394195345d7cb8704aca5c40c08c77a0bf1332fe636cdf85f8f`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 7.3 MB (7278270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bf81f4773f03aaa784a3470bcce2edc2b6a47934ee47acb8cca08a5f355c98`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 91.8 KB (91782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200628578e34b666753dac7e5f675103937c5bc8b19ee1944b18678f0c46925d`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd2d115f337cd4f0d6b8569b2b846987f6e9ac5e092ef1ff0d4ddf55d6e1bd5`  
		Last Modified: Tue, 07 Apr 2026 18:03:44 GMT  
		Size: 63.6 MB (63610216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cae13c6f8720e02fe0cfac11bf4b7873b5127026edf0fd7d60f3869d6d7419`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f9f1d6532df85ab83bce5d7ef4d79e700e0400906d7758bc10171637fb4789`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:47c1c2e7f2d77d352752eed854ede75fe2b99d09a4d2803179083cb08ff22f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6e98380b13b625be9b687b14bd321547ba3ab0a5453ab8bc4373d0660c5188`

```dockerfile
```

-	Layers:
	-	`sha256:e1ee81fe381e2225b1105e6c67bdff7bcb2289618bb0a726e2ed400b0fcfe1c8`  
		Last Modified: Tue, 07 Apr 2026 18:03:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:2fe5918d6fc855d73d4a3f2a00996b7f0a34b7634e179ac2122c2fbdf43a4875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c711cf90ab57665fc3f8f136101a98f0aaaee0ddc5bc0c9f79d5a22477161a42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:56:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:56:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:56:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:56:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:56:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:56:46 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:04:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:04:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:04:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:04:07 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d02ce67b4a0275f7c58bea67b202248f2e1fadee3c6981a52b02af3245dc7`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 7.6 MB (7597809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae114ba08bb257f6560a48e6f42e0eca1e4275b2b1f5de1a5cee3264ac227117`  
		Last Modified: Tue, 07 Apr 2026 17:56:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c462895e881488d974811c947d011f385c58e7837ee4a36e8eb5347cbfbdead`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 18.1 MB (18096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed288924400fa0ef850973ed05b5d68ad1e971d6db3475e8ec6a66996d1f004e`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 21.1 MB (21129730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562fb47ee8e5eb694e39d13d273c9a20343c2611795f59bf060f8896ad84505`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 10.4 MB (10371866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322fadd946101bd1db893bbeab2210077c079947108eba25d61f69bc80b86918`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee11a625998530da0978a257398229bdf229cb3172d2623d63cdaa10a04dd37`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463989f7f6b0810cca12186041f47307814448d147f72bff8a0f48239efc234`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a7a76c7cd299a0667f840f572155fe9e35f5013b5de4e51f836ad166de3094`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 6.6 MB (6576415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecd37ed33aacb16975753b152fd51f47fa1fbd0fbe582cd884e8bc88c7799c9`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 88.1 KB (88144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30c893cca62c4ce187fe0f0df7e1fd32feb7517ce8a8eb10261e08b67c2278f`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2d730ff02f4343d65bdc6f1fbb29d1061a9c64e3f5203d8cf70317d19e67a9`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 63.4 MB (63443312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa38e3d8f2a4334f08fc240f45a7b0857ce64907ba89486d374dbb923fcf33`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522011f6d7ed1009e68e424d9c164d16256d49b5b7421bdb47645f431d7e045a`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:75635ebd248b76a3aa73452fa66599686679233c7faf894570e4870a738fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02726225a9427a640d5001f15d02f9ac80332f8cbdbc5779ef715424b359cecf`

```dockerfile
```

-	Layers:
	-	`sha256:24502e0bf1bc549b64a110973e89bb2b40d90b3444bca7efb104a37f5c4c2e51`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f56f84c60b1ad8653eb423810cca82f8d86d0f97af8f600b2089d7a79b2c67e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130127448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d9a5c2e9415e93f5577fa9935ab7f163c07791bcca430cfa8100bb716915`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:25 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b00d7b9300d4ebf88506edbb338095cf5ad19da1ef0cbef84ae82dd84a0bcb`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 7.2 MB (7219468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa958935e1bc1165d4187e06c145c326c85b4154be3e340a1f57fffa4ae15fb7`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a18406c30abb1ed5c938e64854db122e53e7024a5ee5c6b95ce9c37675aa5`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e20c26df1d1cb588216d065b94856a954f64f3a2fc7252c355c624cf06f166`  
		Last Modified: Tue, 07 Apr 2026 18:03:36 GMT  
		Size: 61.8 MB (61791015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b1556da54467a07970b25f2f5e904eea0cb264745a4cd40a88db0ff73a276d`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d51a5932c15f504e0507fa22ab23138015cb8597493fd874d959868102059`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind` - unknown; unknown

```console
$ docker pull docker@sha256:bc33b62b3ef0f1578e119860d5ccc0bd861f6609d97646a69dc27aea75ab9f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21911a20c08d97ff5d0322eed178a80fae80aea719d8f4c5a2093b0e81e79b99`

```dockerfile
```

-	Layers:
	-	`sha256:63938660feb79291b998f4f1c0122abb056fe223055a32f41a8d543218bbadea`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4-dind-rootless`

```console
$ docker pull docker@sha256:06cbcbc282cf54fc1c4c2c326d236bb3e8aeaf9928c946f5a5128f1077994913
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.4-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e8017dfd3cd4ec88a74e0c0799896877e783a0cc3c936a5b6a58c846b963d5d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161531714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b75307842b323b7da6d0ef282d8bceb758e2399303655d255714432b4e1add`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:36 GMT
CMD []
# Tue, 07 Apr 2026 18:06:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 07 Apr 2026 18:06:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 07 Apr 2026 18:06:51 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074da42c286968f826b040d456a99617b43bda2cc5bf557dceea3de5d6cc4fe`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 6.9 MB (6941677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f4ce6ca5a90a42c5d8d8c00baea57cee587bb141c85bab7aff5de38c99737`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21abf0696dc4d51910e445d2f536ad172bfde41b5963779800c78584ab0b7c`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa3ba34873437febe66dfabe21b09faedd97173ea3f99cdfac49a4960a6f22`  
		Last Modified: Tue, 07 Apr 2026 18:03:49 GMT  
		Size: 68.3 MB (68266949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7a5643b3f629c64a89c9a7665a2102ef8d1b9fe06893fd322d2184c711b5bf`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911bab9d694e25eb17eb5d3df1bd3e09f0ea52d970ce04fa58c0b41861ff8a`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d755e56ce2d2de497c291abe2cb3c543234d57811aa6cc31892539b9612766`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 3.4 MB (3419944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5a1bed895274e6a0aa4e6518ecea2b536c06de2ba8ff8d46f1780b3d1df919`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb54c75cdd29b9362c1d06f6660d0f7d8d7bbe7893e0b9ce825e1b83aaa0561`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab93e7606625323931d20ec97f988d0e03a1d70170464edf09698a7e5ed0c824`  
		Last Modified: Tue, 07 Apr 2026 18:06:58 GMT  
		Size: 17.6 MB (17580413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102bb795e921727afa1a0d32ec9a3ad5a0ee29c9ff396cd792983d41bf76d7c0`  
		Last Modified: Tue, 07 Apr 2026 18:06:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2393d1f43dc15591888c4c108dd057ac24c8b75e437c291786978dfa8055cbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4157e73cac3aafdf5ccdcb29066abeb8fe640483f2b59b1769e2f1b2e1626873`

```dockerfile
```

-	Layers:
	-	`sha256:a427061545c1c404aa1ff5448e2d7ddef22f9ce7690bf471b5c9b5d8cf59b5cf`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d8d9eab16c89792d62362031ddcf62ab255f8de04859c7c424a4da9570ffa2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151405963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd234006ba72c0f64937b10d1d687a972e3973eb0ee05cb2d02dfceac3ea6473`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:25 GMT
CMD []
# Tue, 07 Apr 2026 18:07:07 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 07 Apr 2026 18:07:07 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 07 Apr 2026 18:07:07 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:07:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 07 Apr 2026 18:07:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 07 Apr 2026 18:07:08 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 07 Apr 2026 18:07:08 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b00d7b9300d4ebf88506edbb338095cf5ad19da1ef0cbef84ae82dd84a0bcb`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 7.2 MB (7219468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa958935e1bc1165d4187e06c145c326c85b4154be3e340a1f57fffa4ae15fb7`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a18406c30abb1ed5c938e64854db122e53e7024a5ee5c6b95ce9c37675aa5`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e20c26df1d1cb588216d065b94856a954f64f3a2fc7252c355c624cf06f166`  
		Last Modified: Tue, 07 Apr 2026 18:03:36 GMT  
		Size: 61.8 MB (61791015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b1556da54467a07970b25f2f5e904eea0cb264745a4cd40a88db0ff73a276d`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d51a5932c15f504e0507fa22ab23138015cb8597493fd874d959868102059`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd008e50d6fda4dec99a7345870c1aaa5e47590866dc1a8b580f63be5b4ba1fe`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 3.4 MB (3394378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84d9a19178955f77588d5e575ba89ed64e606150680ee055d3e7f81a7c9e19c`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df25b78e32b01224db4177327e28b0c5aa1fdc8df4fa296b7a11dc254cad6294`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6326173b0d2b0474538dc36d4f09aec863c9d8cc8853c4b8d2b9e6239e5c2de`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 17.9 MB (17882798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e473478b98a0d67b7e5082a1fdfc46efa97b2774cffe12a23e7e330c541ebb4`  
		Last Modified: Tue, 07 Apr 2026 18:07:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a6cf4e5aa66894ec1c5141441bae823cbaf150cdf7799cf03f319eaa34a36fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9213b6754bae917b8aa66937ca0fd9d823685fe09c4ffc75849dfffef3543b9`

```dockerfile
```

-	Layers:
	-	`sha256:185779fc84203fff8c14a24aba62314b0a891054f60dc2387016673e9c80c735`  
		Last Modified: Tue, 07 Apr 2026 18:07:13 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4-windowsservercore`

```console
$ docker pull docker@sha256:38716da2bf6648465dcaf041bb44f5a4c216b8ce28dd7b2f1021a590fa6ecc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `docker:29.4-windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:1805bfa9662cfa4218077bd8ede9b5a6d69c6646439b7521c0bbbd1d6d516f31
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136863509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9768faff7c37bf673323e8563e2159940625e141fc4292c86de2abcec477d7dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 07 Apr 2026 17:45:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:52 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6349df402a8ae75343c96cbbf6fda362d5255740fa6a27c40633fdd74cb8b486`  
		Last Modified: Tue, 07 Apr 2026 17:47:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbaff7ffcff282be3a7cf2b17c33b81d01113cfd9c33a3dd1fc69933363cb882`  
		Last Modified: Tue, 07 Apr 2026 18:06:25 GMT  
		Size: 381.7 KB (381735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4e33ae54c24d17b8b0322f13394b73fa21b1b3a8aa5f40459be12d90d95e8`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe5a20a0f91f2d088cb920e67e52856b75d803e8f11af764c8d124f2dcd93c`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a11f5b4aabfe9b04c01662839eef4d615567e211f283c6e7818e52b3668d661`  
		Last Modified: Tue, 07 Apr 2026 18:06:27 GMT  
		Size: 20.2 MB (20166075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683aaeb151b66e53b1096f22b39533930cef0c1c98a4745f57e71a5f01fb8a0a`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b99e49f048c1ff00de08fd0e6c43a403ab69c2ba7638830c82c36da218d8d`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683624596fd59caecf2e64b0bbfd45b372c1f6869db5c6cfb23fb047bf51eec5`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3391b63f468d72f2045f24a2a8bf86bc454e7bde74c6d8f9b32fcca119e80b`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 23.4 MB (23447007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3612cdb40d7bf90e6e50f9f05c5c7602d11d06a46cca4a6c6482fdd833f1cac3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8ba35ebad23e35edac88bbe0a734de8b14825a7f0651ae67b85224128272b3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df6d8c50c80a893ae84a723eeb4dec4099df9a827b91826b40e1759a9b99509`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1af4d02e803d87cc569e51d6f3511d7ceaac2fe30774f4ea6d1a356e42f89ef`  
		Last Modified: Tue, 07 Apr 2026 18:06:23 GMT  
		Size: 11.7 MB (11660920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.4-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:f37ee3a5fbb958e19138ee2f09d74c58542c532617c7657817359dd37da7472a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2038007541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c93fe0bda8880246418c197b65f4235c5e9f167a5bd4bfd6ce249972e6c5c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 07 Apr 2026 17:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:43 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:46 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:10 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d3d1e4e44fed34fcadd7a99422714da9b20d4f49e0a6fb695d9b5ea818a9ac`  
		Last Modified: Tue, 07 Apr 2026 17:41:02 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9c300c06bd98acbe2efc0c277d580fece563c470038eb8f74d2dd922de94d2`  
		Last Modified: Tue, 07 Apr 2026 18:06:29 GMT  
		Size: 496.2 KB (496237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ff057fe30ee36a89c50acd5ea6585849fb0687ecc19793300b7ee68e4a96bd`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8134fe4ef0e8a711d1eb7bffb1301a576b73a62f71eecd8dfae02f4a50af8d7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bb0fe00c187e5f0aa9c4e431ee26a5472aa893ef9395cead9bc41b53d8bf24`  
		Last Modified: Tue, 07 Apr 2026 18:06:30 GMT  
		Size: 20.1 MB (20143093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3c598636682c6365d6f6dcb67f2fe461dec34bdafe63d7f06138a9b371bdf5`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efee4361413a5695bc83bc76f10df48ec89643440981ead7d535b2b6134a434`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94b089de7840afa203de00c1150ca0636ad534b44e02169335c5c801b3db6b9`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2debda1316a8781d0d548bbf802336d7b4de1ba27198d02473ac96035360f7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 23.4 MB (23432756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca2269f79a5fe310160fcdd23d20b43df2a3547e81e8b04d06f3f25d1dcf8d3`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a834edccd436ba139fc54989c90c4fc8df0d139404714500103d3aa97ccbf512`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906a82b2a03d5ef6e2950ddf7f1680dfea855e0cda9e1123483778f916e7ba8e`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29a6939b1400dc3f52e8fff687d10e51c019eac0f3acf953221086d503f71b6`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 11.6 MB (11642251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c577bbb3fdf12421850d9d7d9c2ede8620846655f6110ad10b6b9c0757a6ad12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `docker:29.4-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:f37ee3a5fbb958e19138ee2f09d74c58542c532617c7657817359dd37da7472a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2038007541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c93fe0bda8880246418c197b65f4235c5e9f167a5bd4bfd6ce249972e6c5c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 07 Apr 2026 17:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:43 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:46 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:10 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d3d1e4e44fed34fcadd7a99422714da9b20d4f49e0a6fb695d9b5ea818a9ac`  
		Last Modified: Tue, 07 Apr 2026 17:41:02 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9c300c06bd98acbe2efc0c277d580fece563c470038eb8f74d2dd922de94d2`  
		Last Modified: Tue, 07 Apr 2026 18:06:29 GMT  
		Size: 496.2 KB (496237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ff057fe30ee36a89c50acd5ea6585849fb0687ecc19793300b7ee68e4a96bd`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8134fe4ef0e8a711d1eb7bffb1301a576b73a62f71eecd8dfae02f4a50af8d7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bb0fe00c187e5f0aa9c4e431ee26a5472aa893ef9395cead9bc41b53d8bf24`  
		Last Modified: Tue, 07 Apr 2026 18:06:30 GMT  
		Size: 20.1 MB (20143093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3c598636682c6365d6f6dcb67f2fe461dec34bdafe63d7f06138a9b371bdf5`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efee4361413a5695bc83bc76f10df48ec89643440981ead7d535b2b6134a434`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94b089de7840afa203de00c1150ca0636ad534b44e02169335c5c801b3db6b9`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2debda1316a8781d0d548bbf802336d7b4de1ba27198d02473ac96035360f7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 23.4 MB (23432756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca2269f79a5fe310160fcdd23d20b43df2a3547e81e8b04d06f3f25d1dcf8d3`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a834edccd436ba139fc54989c90c4fc8df0d139404714500103d3aa97ccbf512`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906a82b2a03d5ef6e2950ddf7f1680dfea855e0cda9e1123483778f916e7ba8e`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29a6939b1400dc3f52e8fff687d10e51c019eac0f3acf953221086d503f71b6`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 11.6 MB (11642251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:822c277e276a37345c2329fab738fdf21ef45e0c7331a3d44f96d3f4520ff5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:29.4-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:1805bfa9662cfa4218077bd8ede9b5a6d69c6646439b7521c0bbbd1d6d516f31
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136863509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9768faff7c37bf673323e8563e2159940625e141fc4292c86de2abcec477d7dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 07 Apr 2026 17:45:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:52 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6349df402a8ae75343c96cbbf6fda362d5255740fa6a27c40633fdd74cb8b486`  
		Last Modified: Tue, 07 Apr 2026 17:47:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbaff7ffcff282be3a7cf2b17c33b81d01113cfd9c33a3dd1fc69933363cb882`  
		Last Modified: Tue, 07 Apr 2026 18:06:25 GMT  
		Size: 381.7 KB (381735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4e33ae54c24d17b8b0322f13394b73fa21b1b3a8aa5f40459be12d90d95e8`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe5a20a0f91f2d088cb920e67e52856b75d803e8f11af764c8d124f2dcd93c`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a11f5b4aabfe9b04c01662839eef4d615567e211f283c6e7818e52b3668d661`  
		Last Modified: Tue, 07 Apr 2026 18:06:27 GMT  
		Size: 20.2 MB (20166075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683aaeb151b66e53b1096f22b39533930cef0c1c98a4745f57e71a5f01fb8a0a`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b99e49f048c1ff00de08fd0e6c43a403ab69c2ba7638830c82c36da218d8d`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683624596fd59caecf2e64b0bbfd45b372c1f6869db5c6cfb23fb047bf51eec5`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3391b63f468d72f2045f24a2a8bf86bc454e7bde74c6d8f9b32fcca119e80b`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 23.4 MB (23447007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3612cdb40d7bf90e6e50f9f05c5c7602d11d06a46cca4a6c6482fdd833f1cac3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8ba35ebad23e35edac88bbe0a734de8b14825a7f0651ae67b85224128272b3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df6d8c50c80a893ae84a723eeb4dec4099df9a827b91826b40e1759a9b99509`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1af4d02e803d87cc569e51d6f3511d7ceaac2fe30774f4ea6d1a356e42f89ef`  
		Last Modified: Tue, 07 Apr 2026 18:06:23 GMT  
		Size: 11.7 MB (11660920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4.0`

```console
$ docker pull docker@sha256:f80c26212befc1c1988b529495532c6b9180d9b1dab1611f4a1efbe9da8ec821
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

### `docker:29.4.0` - linux; amd64

```console
$ docker pull docker@sha256:287ae43017f5d929fe86b951861c6a17c47a18920dbec865d401a08aa827f6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140530015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f374b8d47eebfb2450d5a19efc473c1d20bf645f84c46c21c2854377688446`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:36 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074da42c286968f826b040d456a99617b43bda2cc5bf557dceea3de5d6cc4fe`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 6.9 MB (6941677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f4ce6ca5a90a42c5d8d8c00baea57cee587bb141c85bab7aff5de38c99737`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21abf0696dc4d51910e445d2f536ad172bfde41b5963779800c78584ab0b7c`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa3ba34873437febe66dfabe21b09faedd97173ea3f99cdfac49a4960a6f22`  
		Last Modified: Tue, 07 Apr 2026 18:03:49 GMT  
		Size: 68.3 MB (68266949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7a5643b3f629c64a89c9a7665a2102ef8d1b9fe06893fd322d2184c711b5bf`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911bab9d694e25eb17eb5d3df1bd3e09f0ea52d970ce04fa58c0b41861ff8a`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0` - unknown; unknown

```console
$ docker pull docker@sha256:73b899bc96cf92b0e9a346d2299d110d3fe56b6155f1219dc06b4d4e6172268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc72525e88ac1b74d2507c98202bc1732e6931e5409efa62649aeecef0bda2cf`

```dockerfile
```

-	Layers:
	-	`sha256:57834d73984ba9824980e22fe7ed18b2b1e911c35b6f27dc4f2b7486672e6a28`  
		Last Modified: Tue, 07 Apr 2026 18:03:46 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:d94555deb39a31975ca0a7df7f6f607745e2e3cea98b85279ecab2d2179e2d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132509296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342e83533005345d07b6aa7ba5cc4aa7efe7c9bf531476ab6309626983b8ad35`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:52:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:52:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:52:27 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:31 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b23450f59ae29757b818023e9e1ec7feecec88f0bdffda20a422b2bf40901`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 8.3 MB (8300867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016992555c050a7efd3e0035e8b9a0552c0b9ed2c184291a79aafac5eec2bdb`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c85acb49acf037dbe3345d449eb1c7352be8603c84cbe00120ea39e3d7c30`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 18.1 MB (18109482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e782e8b1924d10e930976d421346c23ca8082dc4665b434c499c55cacdfb8`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 21.2 MB (21151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521a4f32de85375d05302a7d66d9f4b7b8d2e2750474fe3a0ae65c01908aaee`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 10.4 MB (10388830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615f51faa1cea9baac6124a72554172703a48489cfa064d499cb85dbb594352`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9369afbb000ee5860be68de87ea400bade9c679f1e5f9807ee421b61828989`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70ec8240492116e39d00b6dca97c3a28a1163f7e2170ccc530976b2319f26`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b98d7b3e63b394195345d7cb8704aca5c40c08c77a0bf1332fe636cdf85f8f`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 7.3 MB (7278270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bf81f4773f03aaa784a3470bcce2edc2b6a47934ee47acb8cca08a5f355c98`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 91.8 KB (91782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200628578e34b666753dac7e5f675103937c5bc8b19ee1944b18678f0c46925d`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd2d115f337cd4f0d6b8569b2b846987f6e9ac5e092ef1ff0d4ddf55d6e1bd5`  
		Last Modified: Tue, 07 Apr 2026 18:03:44 GMT  
		Size: 63.6 MB (63610216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cae13c6f8720e02fe0cfac11bf4b7873b5127026edf0fd7d60f3869d6d7419`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f9f1d6532df85ab83bce5d7ef4d79e700e0400906d7758bc10171637fb4789`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0` - unknown; unknown

```console
$ docker pull docker@sha256:47c1c2e7f2d77d352752eed854ede75fe2b99d09a4d2803179083cb08ff22f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6e98380b13b625be9b687b14bd321547ba3ab0a5453ab8bc4373d0660c5188`

```dockerfile
```

-	Layers:
	-	`sha256:e1ee81fe381e2225b1105e6c67bdff7bcb2289618bb0a726e2ed400b0fcfe1c8`  
		Last Modified: Tue, 07 Apr 2026 18:03:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:2fe5918d6fc855d73d4a3f2a00996b7f0a34b7634e179ac2122c2fbdf43a4875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c711cf90ab57665fc3f8f136101a98f0aaaee0ddc5bc0c9f79d5a22477161a42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:56:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:56:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:56:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:56:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:56:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:56:46 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:04:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:04:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:04:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:04:07 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d02ce67b4a0275f7c58bea67b202248f2e1fadee3c6981a52b02af3245dc7`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 7.6 MB (7597809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae114ba08bb257f6560a48e6f42e0eca1e4275b2b1f5de1a5cee3264ac227117`  
		Last Modified: Tue, 07 Apr 2026 17:56:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c462895e881488d974811c947d011f385c58e7837ee4a36e8eb5347cbfbdead`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 18.1 MB (18096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed288924400fa0ef850973ed05b5d68ad1e971d6db3475e8ec6a66996d1f004e`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 21.1 MB (21129730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562fb47ee8e5eb694e39d13d273c9a20343c2611795f59bf060f8896ad84505`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 10.4 MB (10371866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322fadd946101bd1db893bbeab2210077c079947108eba25d61f69bc80b86918`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee11a625998530da0978a257398229bdf229cb3172d2623d63cdaa10a04dd37`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463989f7f6b0810cca12186041f47307814448d147f72bff8a0f48239efc234`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a7a76c7cd299a0667f840f572155fe9e35f5013b5de4e51f836ad166de3094`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 6.6 MB (6576415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecd37ed33aacb16975753b152fd51f47fa1fbd0fbe582cd884e8bc88c7799c9`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 88.1 KB (88144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30c893cca62c4ce187fe0f0df7e1fd32feb7517ce8a8eb10261e08b67c2278f`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2d730ff02f4343d65bdc6f1fbb29d1061a9c64e3f5203d8cf70317d19e67a9`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 63.4 MB (63443312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa38e3d8f2a4334f08fc240f45a7b0857ce64907ba89486d374dbb923fcf33`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522011f6d7ed1009e68e424d9c164d16256d49b5b7421bdb47645f431d7e045a`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0` - unknown; unknown

```console
$ docker pull docker@sha256:75635ebd248b76a3aa73452fa66599686679233c7faf894570e4870a738fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02726225a9427a640d5001f15d02f9ac80332f8cbdbc5779ef715424b359cecf`

```dockerfile
```

-	Layers:
	-	`sha256:24502e0bf1bc549b64a110973e89bb2b40d90b3444bca7efb104a37f5c4c2e51`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f56f84c60b1ad8653eb423810cca82f8d86d0f97af8f600b2089d7a79b2c67e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130127448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d9a5c2e9415e93f5577fa9935ab7f163c07791bcca430cfa8100bb716915`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:25 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b00d7b9300d4ebf88506edbb338095cf5ad19da1ef0cbef84ae82dd84a0bcb`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 7.2 MB (7219468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa958935e1bc1165d4187e06c145c326c85b4154be3e340a1f57fffa4ae15fb7`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a18406c30abb1ed5c938e64854db122e53e7024a5ee5c6b95ce9c37675aa5`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e20c26df1d1cb588216d065b94856a954f64f3a2fc7252c355c624cf06f166`  
		Last Modified: Tue, 07 Apr 2026 18:03:36 GMT  
		Size: 61.8 MB (61791015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b1556da54467a07970b25f2f5e904eea0cb264745a4cd40a88db0ff73a276d`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d51a5932c15f504e0507fa22ab23138015cb8597493fd874d959868102059`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0` - unknown; unknown

```console
$ docker pull docker@sha256:bc33b62b3ef0f1578e119860d5ccc0bd861f6609d97646a69dc27aea75ab9f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21911a20c08d97ff5d0322eed178a80fae80aea719d8f4c5a2093b0e81e79b99`

```dockerfile
```

-	Layers:
	-	`sha256:63938660feb79291b998f4f1c0122abb056fe223055a32f41a8d543218bbadea`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4.0-alpine3.23`

```console
$ docker pull docker@sha256:f80c26212befc1c1988b529495532c6b9180d9b1dab1611f4a1efbe9da8ec821
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

### `docker:29.4.0-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:287ae43017f5d929fe86b951861c6a17c47a18920dbec865d401a08aa827f6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140530015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f374b8d47eebfb2450d5a19efc473c1d20bf645f84c46c21c2854377688446`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:36 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074da42c286968f826b040d456a99617b43bda2cc5bf557dceea3de5d6cc4fe`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 6.9 MB (6941677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f4ce6ca5a90a42c5d8d8c00baea57cee587bb141c85bab7aff5de38c99737`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21abf0696dc4d51910e445d2f536ad172bfde41b5963779800c78584ab0b7c`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa3ba34873437febe66dfabe21b09faedd97173ea3f99cdfac49a4960a6f22`  
		Last Modified: Tue, 07 Apr 2026 18:03:49 GMT  
		Size: 68.3 MB (68266949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7a5643b3f629c64a89c9a7665a2102ef8d1b9fe06893fd322d2184c711b5bf`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911bab9d694e25eb17eb5d3df1bd3e09f0ea52d970ce04fa58c0b41861ff8a`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:73b899bc96cf92b0e9a346d2299d110d3fe56b6155f1219dc06b4d4e6172268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc72525e88ac1b74d2507c98202bc1732e6931e5409efa62649aeecef0bda2cf`

```dockerfile
```

-	Layers:
	-	`sha256:57834d73984ba9824980e22fe7ed18b2b1e911c35b6f27dc4f2b7486672e6a28`  
		Last Modified: Tue, 07 Apr 2026 18:03:46 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:d94555deb39a31975ca0a7df7f6f607745e2e3cea98b85279ecab2d2179e2d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132509296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342e83533005345d07b6aa7ba5cc4aa7efe7c9bf531476ab6309626983b8ad35`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:52:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:52:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:52:27 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:31 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b23450f59ae29757b818023e9e1ec7feecec88f0bdffda20a422b2bf40901`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 8.3 MB (8300867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016992555c050a7efd3e0035e8b9a0552c0b9ed2c184291a79aafac5eec2bdb`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c85acb49acf037dbe3345d449eb1c7352be8603c84cbe00120ea39e3d7c30`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 18.1 MB (18109482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e782e8b1924d10e930976d421346c23ca8082dc4665b434c499c55cacdfb8`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 21.2 MB (21151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521a4f32de85375d05302a7d66d9f4b7b8d2e2750474fe3a0ae65c01908aaee`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 10.4 MB (10388830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615f51faa1cea9baac6124a72554172703a48489cfa064d499cb85dbb594352`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9369afbb000ee5860be68de87ea400bade9c679f1e5f9807ee421b61828989`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70ec8240492116e39d00b6dca97c3a28a1163f7e2170ccc530976b2319f26`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b98d7b3e63b394195345d7cb8704aca5c40c08c77a0bf1332fe636cdf85f8f`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 7.3 MB (7278270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bf81f4773f03aaa784a3470bcce2edc2b6a47934ee47acb8cca08a5f355c98`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 91.8 KB (91782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200628578e34b666753dac7e5f675103937c5bc8b19ee1944b18678f0c46925d`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd2d115f337cd4f0d6b8569b2b846987f6e9ac5e092ef1ff0d4ddf55d6e1bd5`  
		Last Modified: Tue, 07 Apr 2026 18:03:44 GMT  
		Size: 63.6 MB (63610216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cae13c6f8720e02fe0cfac11bf4b7873b5127026edf0fd7d60f3869d6d7419`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f9f1d6532df85ab83bce5d7ef4d79e700e0400906d7758bc10171637fb4789`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:47c1c2e7f2d77d352752eed854ede75fe2b99d09a4d2803179083cb08ff22f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6e98380b13b625be9b687b14bd321547ba3ab0a5453ab8bc4373d0660c5188`

```dockerfile
```

-	Layers:
	-	`sha256:e1ee81fe381e2225b1105e6c67bdff7bcb2289618bb0a726e2ed400b0fcfe1c8`  
		Last Modified: Tue, 07 Apr 2026 18:03:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:2fe5918d6fc855d73d4a3f2a00996b7f0a34b7634e179ac2122c2fbdf43a4875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c711cf90ab57665fc3f8f136101a98f0aaaee0ddc5bc0c9f79d5a22477161a42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:56:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:56:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:56:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:56:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:56:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:56:46 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:04:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:04:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:04:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:04:07 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d02ce67b4a0275f7c58bea67b202248f2e1fadee3c6981a52b02af3245dc7`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 7.6 MB (7597809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae114ba08bb257f6560a48e6f42e0eca1e4275b2b1f5de1a5cee3264ac227117`  
		Last Modified: Tue, 07 Apr 2026 17:56:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c462895e881488d974811c947d011f385c58e7837ee4a36e8eb5347cbfbdead`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 18.1 MB (18096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed288924400fa0ef850973ed05b5d68ad1e971d6db3475e8ec6a66996d1f004e`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 21.1 MB (21129730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562fb47ee8e5eb694e39d13d273c9a20343c2611795f59bf060f8896ad84505`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 10.4 MB (10371866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322fadd946101bd1db893bbeab2210077c079947108eba25d61f69bc80b86918`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee11a625998530da0978a257398229bdf229cb3172d2623d63cdaa10a04dd37`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463989f7f6b0810cca12186041f47307814448d147f72bff8a0f48239efc234`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a7a76c7cd299a0667f840f572155fe9e35f5013b5de4e51f836ad166de3094`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 6.6 MB (6576415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecd37ed33aacb16975753b152fd51f47fa1fbd0fbe582cd884e8bc88c7799c9`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 88.1 KB (88144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30c893cca62c4ce187fe0f0df7e1fd32feb7517ce8a8eb10261e08b67c2278f`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2d730ff02f4343d65bdc6f1fbb29d1061a9c64e3f5203d8cf70317d19e67a9`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 63.4 MB (63443312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa38e3d8f2a4334f08fc240f45a7b0857ce64907ba89486d374dbb923fcf33`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522011f6d7ed1009e68e424d9c164d16256d49b5b7421bdb47645f431d7e045a`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:75635ebd248b76a3aa73452fa66599686679233c7faf894570e4870a738fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02726225a9427a640d5001f15d02f9ac80332f8cbdbc5779ef715424b359cecf`

```dockerfile
```

-	Layers:
	-	`sha256:24502e0bf1bc549b64a110973e89bb2b40d90b3444bca7efb104a37f5c4c2e51`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f56f84c60b1ad8653eb423810cca82f8d86d0f97af8f600b2089d7a79b2c67e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130127448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d9a5c2e9415e93f5577fa9935ab7f163c07791bcca430cfa8100bb716915`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:25 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b00d7b9300d4ebf88506edbb338095cf5ad19da1ef0cbef84ae82dd84a0bcb`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 7.2 MB (7219468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa958935e1bc1165d4187e06c145c326c85b4154be3e340a1f57fffa4ae15fb7`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a18406c30abb1ed5c938e64854db122e53e7024a5ee5c6b95ce9c37675aa5`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e20c26df1d1cb588216d065b94856a954f64f3a2fc7252c355c624cf06f166`  
		Last Modified: Tue, 07 Apr 2026 18:03:36 GMT  
		Size: 61.8 MB (61791015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b1556da54467a07970b25f2f5e904eea0cb264745a4cd40a88db0ff73a276d`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d51a5932c15f504e0507fa22ab23138015cb8597493fd874d959868102059`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:bc33b62b3ef0f1578e119860d5ccc0bd861f6609d97646a69dc27aea75ab9f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21911a20c08d97ff5d0322eed178a80fae80aea719d8f4c5a2093b0e81e79b99`

```dockerfile
```

-	Layers:
	-	`sha256:63938660feb79291b998f4f1c0122abb056fe223055a32f41a8d543218bbadea`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4.0-cli`

```console
$ docker pull docker@sha256:0befd75049d8903cd5606879d251bd29ac08758cd33f9c7c74583fc6679b737d
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

### `docker:29.4.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:162f671f43d999a41de10577c292392d92df278f2b19619bd00f62702b9aa2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65222927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad9b141cd1de25bf040248038f95cd6219a80703fd707e59b2b6a0517308b72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:daf7ceb8c94a68d086116d67088dcb70baa3ccd572ff5c33286ad2106b907897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7290d94403713e42feb20ce8a180e2fdd9faf2f4c61c1e6a56befb117afe1fc8`

```dockerfile
```

-	Layers:
	-	`sha256:b95f79229ba482446ea56f9b087844cfdb759933700550eda0ac85aa7b865ed4`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:01b9514d3a7731ab09e57a066f6f57fc6bfd443cc4bb281b5defbf46434d784f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61523027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e6afc4be332ae73538fea1317c86c824dc8f3fed5bd6479ef0f3623fd66f2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:52:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:52:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:52:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b23450f59ae29757b818023e9e1ec7feecec88f0bdffda20a422b2bf40901`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 8.3 MB (8300867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016992555c050a7efd3e0035e8b9a0552c0b9ed2c184291a79aafac5eec2bdb`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c85acb49acf037dbe3345d449eb1c7352be8603c84cbe00120ea39e3d7c30`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 18.1 MB (18109482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e782e8b1924d10e930976d421346c23ca8082dc4665b434c499c55cacdfb8`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 21.2 MB (21151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521a4f32de85375d05302a7d66d9f4b7b8d2e2750474fe3a0ae65c01908aaee`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 10.4 MB (10388830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615f51faa1cea9baac6124a72554172703a48489cfa064d499cb85dbb594352`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9369afbb000ee5860be68de87ea400bade9c679f1e5f9807ee421b61828989`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70ec8240492116e39d00b6dca97c3a28a1163f7e2170ccc530976b2319f26`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:005090b7bbeeb700acbccd357974890d0823f6b05afd754f62123ce0cc2c9327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746bfb0046c73dc782de8b20a9ce871dc02be903bb3305fb32d83c36465c4b61`

```dockerfile
```

-	Layers:
	-	`sha256:1d9d1c99fe378084950dc2c8f24e70107427c1736e16ba6a42be234d1fc3e615`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:b5e13676109eba75e0291b50c5457e21aa02414b1ba2eca698d6385511dfa8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60479667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431a96e79c5bb0cc3f234407c79cd071478587e33cdf94a2ede1122d0c0f9873`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:56:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:56:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:56:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:56:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:56:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:56:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d02ce67b4a0275f7c58bea67b202248f2e1fadee3c6981a52b02af3245dc7`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 7.6 MB (7597809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae114ba08bb257f6560a48e6f42e0eca1e4275b2b1f5de1a5cee3264ac227117`  
		Last Modified: Tue, 07 Apr 2026 17:56:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c462895e881488d974811c947d011f385c58e7837ee4a36e8eb5347cbfbdead`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 18.1 MB (18096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed288924400fa0ef850973ed05b5d68ad1e971d6db3475e8ec6a66996d1f004e`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 21.1 MB (21129730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562fb47ee8e5eb694e39d13d273c9a20343c2611795f59bf060f8896ad84505`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 10.4 MB (10371866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322fadd946101bd1db893bbeab2210077c079947108eba25d61f69bc80b86918`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee11a625998530da0978a257398229bdf229cb3172d2623d63cdaa10a04dd37`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463989f7f6b0810cca12186041f47307814448d147f72bff8a0f48239efc234`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:00955fd445b2706d6540aec431b00eaff21297aff36f366d2b10b3f4f0e74a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9541b749d18a90c9233171b4a24d5ec5360a879be45ca225522b51eda41825`

```dockerfile
```

-	Layers:
	-	`sha256:58793278463a7baf2e54d0b9ec3edfaaaa4bf35057e379c728b4864ddbed92d5`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:db0c05a4aab745e54662ec56befe45e3c265f485d9d7c7e2d1ffe32f2131448d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61009679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65923880c0dee4eabcf3f64a2fc3e0cc27a7b521fd83945232a7c2c587ae70bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:7b06c415f269961efe974617d3e8b045f801c7e82fe1ef4eac6a74707b63420c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4b4265560dfb409203188b0903d9895666374d935b7351a099c296894efbf8`

```dockerfile
```

-	Layers:
	-	`sha256:983969a38dd490d16487039ccb7e1f62968548fc8a488c859ddd9e62a80382df`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4.0-cli-alpine3.23`

```console
$ docker pull docker@sha256:0befd75049d8903cd5606879d251bd29ac08758cd33f9c7c74583fc6679b737d
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

### `docker:29.4.0-cli-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:162f671f43d999a41de10577c292392d92df278f2b19619bd00f62702b9aa2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65222927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad9b141cd1de25bf040248038f95cd6219a80703fd707e59b2b6a0517308b72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:daf7ceb8c94a68d086116d67088dcb70baa3ccd572ff5c33286ad2106b907897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7290d94403713e42feb20ce8a180e2fdd9faf2f4c61c1e6a56befb117afe1fc8`

```dockerfile
```

-	Layers:
	-	`sha256:b95f79229ba482446ea56f9b087844cfdb759933700550eda0ac85aa7b865ed4`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-cli-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:01b9514d3a7731ab09e57a066f6f57fc6bfd443cc4bb281b5defbf46434d784f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61523027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e6afc4be332ae73538fea1317c86c824dc8f3fed5bd6479ef0f3623fd66f2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:52:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:52:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:52:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b23450f59ae29757b818023e9e1ec7feecec88f0bdffda20a422b2bf40901`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 8.3 MB (8300867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016992555c050a7efd3e0035e8b9a0552c0b9ed2c184291a79aafac5eec2bdb`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c85acb49acf037dbe3345d449eb1c7352be8603c84cbe00120ea39e3d7c30`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 18.1 MB (18109482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e782e8b1924d10e930976d421346c23ca8082dc4665b434c499c55cacdfb8`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 21.2 MB (21151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521a4f32de85375d05302a7d66d9f4b7b8d2e2750474fe3a0ae65c01908aaee`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 10.4 MB (10388830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615f51faa1cea9baac6124a72554172703a48489cfa064d499cb85dbb594352`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9369afbb000ee5860be68de87ea400bade9c679f1e5f9807ee421b61828989`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70ec8240492116e39d00b6dca97c3a28a1163f7e2170ccc530976b2319f26`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:005090b7bbeeb700acbccd357974890d0823f6b05afd754f62123ce0cc2c9327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746bfb0046c73dc782de8b20a9ce871dc02be903bb3305fb32d83c36465c4b61`

```dockerfile
```

-	Layers:
	-	`sha256:1d9d1c99fe378084950dc2c8f24e70107427c1736e16ba6a42be234d1fc3e615`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-cli-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:b5e13676109eba75e0291b50c5457e21aa02414b1ba2eca698d6385511dfa8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60479667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431a96e79c5bb0cc3f234407c79cd071478587e33cdf94a2ede1122d0c0f9873`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:56:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:56:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:56:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:56:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:56:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:56:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d02ce67b4a0275f7c58bea67b202248f2e1fadee3c6981a52b02af3245dc7`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 7.6 MB (7597809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae114ba08bb257f6560a48e6f42e0eca1e4275b2b1f5de1a5cee3264ac227117`  
		Last Modified: Tue, 07 Apr 2026 17:56:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c462895e881488d974811c947d011f385c58e7837ee4a36e8eb5347cbfbdead`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 18.1 MB (18096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed288924400fa0ef850973ed05b5d68ad1e971d6db3475e8ec6a66996d1f004e`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 21.1 MB (21129730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562fb47ee8e5eb694e39d13d273c9a20343c2611795f59bf060f8896ad84505`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 10.4 MB (10371866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322fadd946101bd1db893bbeab2210077c079947108eba25d61f69bc80b86918`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee11a625998530da0978a257398229bdf229cb3172d2623d63cdaa10a04dd37`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463989f7f6b0810cca12186041f47307814448d147f72bff8a0f48239efc234`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:00955fd445b2706d6540aec431b00eaff21297aff36f366d2b10b3f4f0e74a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9541b749d18a90c9233171b4a24d5ec5360a879be45ca225522b51eda41825`

```dockerfile
```

-	Layers:
	-	`sha256:58793278463a7baf2e54d0b9ec3edfaaaa4bf35057e379c728b4864ddbed92d5`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-cli-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:db0c05a4aab745e54662ec56befe45e3c265f485d9d7c7e2d1ffe32f2131448d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61009679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65923880c0dee4eabcf3f64a2fc3e0cc27a7b521fd83945232a7c2c587ae70bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:7b06c415f269961efe974617d3e8b045f801c7e82fe1ef4eac6a74707b63420c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4b4265560dfb409203188b0903d9895666374d935b7351a099c296894efbf8`

```dockerfile
```

-	Layers:
	-	`sha256:983969a38dd490d16487039ccb7e1f62968548fc8a488c859ddd9e62a80382df`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4.0-dind`

```console
$ docker pull docker@sha256:f80c26212befc1c1988b529495532c6b9180d9b1dab1611f4a1efbe9da8ec821
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

### `docker:29.4.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:287ae43017f5d929fe86b951861c6a17c47a18920dbec865d401a08aa827f6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140530015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f374b8d47eebfb2450d5a19efc473c1d20bf645f84c46c21c2854377688446`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:36 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074da42c286968f826b040d456a99617b43bda2cc5bf557dceea3de5d6cc4fe`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 6.9 MB (6941677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f4ce6ca5a90a42c5d8d8c00baea57cee587bb141c85bab7aff5de38c99737`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21abf0696dc4d51910e445d2f536ad172bfde41b5963779800c78584ab0b7c`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa3ba34873437febe66dfabe21b09faedd97173ea3f99cdfac49a4960a6f22`  
		Last Modified: Tue, 07 Apr 2026 18:03:49 GMT  
		Size: 68.3 MB (68266949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7a5643b3f629c64a89c9a7665a2102ef8d1b9fe06893fd322d2184c711b5bf`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911bab9d694e25eb17eb5d3df1bd3e09f0ea52d970ce04fa58c0b41861ff8a`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:73b899bc96cf92b0e9a346d2299d110d3fe56b6155f1219dc06b4d4e6172268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc72525e88ac1b74d2507c98202bc1732e6931e5409efa62649aeecef0bda2cf`

```dockerfile
```

-	Layers:
	-	`sha256:57834d73984ba9824980e22fe7ed18b2b1e911c35b6f27dc4f2b7486672e6a28`  
		Last Modified: Tue, 07 Apr 2026 18:03:46 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:d94555deb39a31975ca0a7df7f6f607745e2e3cea98b85279ecab2d2179e2d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132509296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342e83533005345d07b6aa7ba5cc4aa7efe7c9bf531476ab6309626983b8ad35`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:52:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:52:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:52:27 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:31 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b23450f59ae29757b818023e9e1ec7feecec88f0bdffda20a422b2bf40901`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 8.3 MB (8300867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016992555c050a7efd3e0035e8b9a0552c0b9ed2c184291a79aafac5eec2bdb`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c85acb49acf037dbe3345d449eb1c7352be8603c84cbe00120ea39e3d7c30`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 18.1 MB (18109482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e782e8b1924d10e930976d421346c23ca8082dc4665b434c499c55cacdfb8`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 21.2 MB (21151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521a4f32de85375d05302a7d66d9f4b7b8d2e2750474fe3a0ae65c01908aaee`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 10.4 MB (10388830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615f51faa1cea9baac6124a72554172703a48489cfa064d499cb85dbb594352`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9369afbb000ee5860be68de87ea400bade9c679f1e5f9807ee421b61828989`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70ec8240492116e39d00b6dca97c3a28a1163f7e2170ccc530976b2319f26`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b98d7b3e63b394195345d7cb8704aca5c40c08c77a0bf1332fe636cdf85f8f`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 7.3 MB (7278270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bf81f4773f03aaa784a3470bcce2edc2b6a47934ee47acb8cca08a5f355c98`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 91.8 KB (91782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200628578e34b666753dac7e5f675103937c5bc8b19ee1944b18678f0c46925d`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd2d115f337cd4f0d6b8569b2b846987f6e9ac5e092ef1ff0d4ddf55d6e1bd5`  
		Last Modified: Tue, 07 Apr 2026 18:03:44 GMT  
		Size: 63.6 MB (63610216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cae13c6f8720e02fe0cfac11bf4b7873b5127026edf0fd7d60f3869d6d7419`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f9f1d6532df85ab83bce5d7ef4d79e700e0400906d7758bc10171637fb4789`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:47c1c2e7f2d77d352752eed854ede75fe2b99d09a4d2803179083cb08ff22f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6e98380b13b625be9b687b14bd321547ba3ab0a5453ab8bc4373d0660c5188`

```dockerfile
```

-	Layers:
	-	`sha256:e1ee81fe381e2225b1105e6c67bdff7bcb2289618bb0a726e2ed400b0fcfe1c8`  
		Last Modified: Tue, 07 Apr 2026 18:03:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:2fe5918d6fc855d73d4a3f2a00996b7f0a34b7634e179ac2122c2fbdf43a4875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c711cf90ab57665fc3f8f136101a98f0aaaee0ddc5bc0c9f79d5a22477161a42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:56:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:56:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:56:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:56:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:56:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:56:46 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:04:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:04:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:04:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:04:07 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d02ce67b4a0275f7c58bea67b202248f2e1fadee3c6981a52b02af3245dc7`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 7.6 MB (7597809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae114ba08bb257f6560a48e6f42e0eca1e4275b2b1f5de1a5cee3264ac227117`  
		Last Modified: Tue, 07 Apr 2026 17:56:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c462895e881488d974811c947d011f385c58e7837ee4a36e8eb5347cbfbdead`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 18.1 MB (18096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed288924400fa0ef850973ed05b5d68ad1e971d6db3475e8ec6a66996d1f004e`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 21.1 MB (21129730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562fb47ee8e5eb694e39d13d273c9a20343c2611795f59bf060f8896ad84505`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 10.4 MB (10371866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322fadd946101bd1db893bbeab2210077c079947108eba25d61f69bc80b86918`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee11a625998530da0978a257398229bdf229cb3172d2623d63cdaa10a04dd37`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463989f7f6b0810cca12186041f47307814448d147f72bff8a0f48239efc234`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a7a76c7cd299a0667f840f572155fe9e35f5013b5de4e51f836ad166de3094`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 6.6 MB (6576415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecd37ed33aacb16975753b152fd51f47fa1fbd0fbe582cd884e8bc88c7799c9`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 88.1 KB (88144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30c893cca62c4ce187fe0f0df7e1fd32feb7517ce8a8eb10261e08b67c2278f`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2d730ff02f4343d65bdc6f1fbb29d1061a9c64e3f5203d8cf70317d19e67a9`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 63.4 MB (63443312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa38e3d8f2a4334f08fc240f45a7b0857ce64907ba89486d374dbb923fcf33`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522011f6d7ed1009e68e424d9c164d16256d49b5b7421bdb47645f431d7e045a`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:75635ebd248b76a3aa73452fa66599686679233c7faf894570e4870a738fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02726225a9427a640d5001f15d02f9ac80332f8cbdbc5779ef715424b359cecf`

```dockerfile
```

-	Layers:
	-	`sha256:24502e0bf1bc549b64a110973e89bb2b40d90b3444bca7efb104a37f5c4c2e51`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f56f84c60b1ad8653eb423810cca82f8d86d0f97af8f600b2089d7a79b2c67e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130127448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d9a5c2e9415e93f5577fa9935ab7f163c07791bcca430cfa8100bb716915`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:25 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b00d7b9300d4ebf88506edbb338095cf5ad19da1ef0cbef84ae82dd84a0bcb`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 7.2 MB (7219468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa958935e1bc1165d4187e06c145c326c85b4154be3e340a1f57fffa4ae15fb7`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a18406c30abb1ed5c938e64854db122e53e7024a5ee5c6b95ce9c37675aa5`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e20c26df1d1cb588216d065b94856a954f64f3a2fc7252c355c624cf06f166`  
		Last Modified: Tue, 07 Apr 2026 18:03:36 GMT  
		Size: 61.8 MB (61791015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b1556da54467a07970b25f2f5e904eea0cb264745a4cd40a88db0ff73a276d`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d51a5932c15f504e0507fa22ab23138015cb8597493fd874d959868102059`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:bc33b62b3ef0f1578e119860d5ccc0bd861f6609d97646a69dc27aea75ab9f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21911a20c08d97ff5d0322eed178a80fae80aea719d8f4c5a2093b0e81e79b99`

```dockerfile
```

-	Layers:
	-	`sha256:63938660feb79291b998f4f1c0122abb056fe223055a32f41a8d543218bbadea`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4.0-dind-alpine3.23`

```console
$ docker pull docker@sha256:f80c26212befc1c1988b529495532c6b9180d9b1dab1611f4a1efbe9da8ec821
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

### `docker:29.4.0-dind-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:287ae43017f5d929fe86b951861c6a17c47a18920dbec865d401a08aa827f6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140530015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f374b8d47eebfb2450d5a19efc473c1d20bf645f84c46c21c2854377688446`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:36 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074da42c286968f826b040d456a99617b43bda2cc5bf557dceea3de5d6cc4fe`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 6.9 MB (6941677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f4ce6ca5a90a42c5d8d8c00baea57cee587bb141c85bab7aff5de38c99737`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21abf0696dc4d51910e445d2f536ad172bfde41b5963779800c78584ab0b7c`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa3ba34873437febe66dfabe21b09faedd97173ea3f99cdfac49a4960a6f22`  
		Last Modified: Tue, 07 Apr 2026 18:03:49 GMT  
		Size: 68.3 MB (68266949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7a5643b3f629c64a89c9a7665a2102ef8d1b9fe06893fd322d2184c711b5bf`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911bab9d694e25eb17eb5d3df1bd3e09f0ea52d970ce04fa58c0b41861ff8a`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:73b899bc96cf92b0e9a346d2299d110d3fe56b6155f1219dc06b4d4e6172268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc72525e88ac1b74d2507c98202bc1732e6931e5409efa62649aeecef0bda2cf`

```dockerfile
```

-	Layers:
	-	`sha256:57834d73984ba9824980e22fe7ed18b2b1e911c35b6f27dc4f2b7486672e6a28`  
		Last Modified: Tue, 07 Apr 2026 18:03:46 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-dind-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:d94555deb39a31975ca0a7df7f6f607745e2e3cea98b85279ecab2d2179e2d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132509296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342e83533005345d07b6aa7ba5cc4aa7efe7c9bf531476ab6309626983b8ad35`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:52:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:52:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:52:27 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:31 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b23450f59ae29757b818023e9e1ec7feecec88f0bdffda20a422b2bf40901`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 8.3 MB (8300867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016992555c050a7efd3e0035e8b9a0552c0b9ed2c184291a79aafac5eec2bdb`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c85acb49acf037dbe3345d449eb1c7352be8603c84cbe00120ea39e3d7c30`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 18.1 MB (18109482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e782e8b1924d10e930976d421346c23ca8082dc4665b434c499c55cacdfb8`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 21.2 MB (21151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521a4f32de85375d05302a7d66d9f4b7b8d2e2750474fe3a0ae65c01908aaee`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 10.4 MB (10388830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615f51faa1cea9baac6124a72554172703a48489cfa064d499cb85dbb594352`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9369afbb000ee5860be68de87ea400bade9c679f1e5f9807ee421b61828989`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70ec8240492116e39d00b6dca97c3a28a1163f7e2170ccc530976b2319f26`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b98d7b3e63b394195345d7cb8704aca5c40c08c77a0bf1332fe636cdf85f8f`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 7.3 MB (7278270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bf81f4773f03aaa784a3470bcce2edc2b6a47934ee47acb8cca08a5f355c98`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 91.8 KB (91782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200628578e34b666753dac7e5f675103937c5bc8b19ee1944b18678f0c46925d`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd2d115f337cd4f0d6b8569b2b846987f6e9ac5e092ef1ff0d4ddf55d6e1bd5`  
		Last Modified: Tue, 07 Apr 2026 18:03:44 GMT  
		Size: 63.6 MB (63610216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cae13c6f8720e02fe0cfac11bf4b7873b5127026edf0fd7d60f3869d6d7419`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f9f1d6532df85ab83bce5d7ef4d79e700e0400906d7758bc10171637fb4789`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:47c1c2e7f2d77d352752eed854ede75fe2b99d09a4d2803179083cb08ff22f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6e98380b13b625be9b687b14bd321547ba3ab0a5453ab8bc4373d0660c5188`

```dockerfile
```

-	Layers:
	-	`sha256:e1ee81fe381e2225b1105e6c67bdff7bcb2289618bb0a726e2ed400b0fcfe1c8`  
		Last Modified: Tue, 07 Apr 2026 18:03:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-dind-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:2fe5918d6fc855d73d4a3f2a00996b7f0a34b7634e179ac2122c2fbdf43a4875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c711cf90ab57665fc3f8f136101a98f0aaaee0ddc5bc0c9f79d5a22477161a42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:56:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:56:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:56:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:56:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:56:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:56:46 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:04:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:04:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:04:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:04:07 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d02ce67b4a0275f7c58bea67b202248f2e1fadee3c6981a52b02af3245dc7`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 7.6 MB (7597809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae114ba08bb257f6560a48e6f42e0eca1e4275b2b1f5de1a5cee3264ac227117`  
		Last Modified: Tue, 07 Apr 2026 17:56:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c462895e881488d974811c947d011f385c58e7837ee4a36e8eb5347cbfbdead`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 18.1 MB (18096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed288924400fa0ef850973ed05b5d68ad1e971d6db3475e8ec6a66996d1f004e`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 21.1 MB (21129730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562fb47ee8e5eb694e39d13d273c9a20343c2611795f59bf060f8896ad84505`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 10.4 MB (10371866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322fadd946101bd1db893bbeab2210077c079947108eba25d61f69bc80b86918`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee11a625998530da0978a257398229bdf229cb3172d2623d63cdaa10a04dd37`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463989f7f6b0810cca12186041f47307814448d147f72bff8a0f48239efc234`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a7a76c7cd299a0667f840f572155fe9e35f5013b5de4e51f836ad166de3094`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 6.6 MB (6576415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecd37ed33aacb16975753b152fd51f47fa1fbd0fbe582cd884e8bc88c7799c9`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 88.1 KB (88144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30c893cca62c4ce187fe0f0df7e1fd32feb7517ce8a8eb10261e08b67c2278f`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2d730ff02f4343d65bdc6f1fbb29d1061a9c64e3f5203d8cf70317d19e67a9`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 63.4 MB (63443312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa38e3d8f2a4334f08fc240f45a7b0857ce64907ba89486d374dbb923fcf33`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522011f6d7ed1009e68e424d9c164d16256d49b5b7421bdb47645f431d7e045a`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:75635ebd248b76a3aa73452fa66599686679233c7faf894570e4870a738fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02726225a9427a640d5001f15d02f9ac80332f8cbdbc5779ef715424b359cecf`

```dockerfile
```

-	Layers:
	-	`sha256:24502e0bf1bc549b64a110973e89bb2b40d90b3444bca7efb104a37f5c4c2e51`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-dind-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f56f84c60b1ad8653eb423810cca82f8d86d0f97af8f600b2089d7a79b2c67e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130127448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d9a5c2e9415e93f5577fa9935ab7f163c07791bcca430cfa8100bb716915`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:25 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b00d7b9300d4ebf88506edbb338095cf5ad19da1ef0cbef84ae82dd84a0bcb`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 7.2 MB (7219468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa958935e1bc1165d4187e06c145c326c85b4154be3e340a1f57fffa4ae15fb7`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a18406c30abb1ed5c938e64854db122e53e7024a5ee5c6b95ce9c37675aa5`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e20c26df1d1cb588216d065b94856a954f64f3a2fc7252c355c624cf06f166`  
		Last Modified: Tue, 07 Apr 2026 18:03:36 GMT  
		Size: 61.8 MB (61791015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b1556da54467a07970b25f2f5e904eea0cb264745a4cd40a88db0ff73a276d`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d51a5932c15f504e0507fa22ab23138015cb8597493fd874d959868102059`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:bc33b62b3ef0f1578e119860d5ccc0bd861f6609d97646a69dc27aea75ab9f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21911a20c08d97ff5d0322eed178a80fae80aea719d8f4c5a2093b0e81e79b99`

```dockerfile
```

-	Layers:
	-	`sha256:63938660feb79291b998f4f1c0122abb056fe223055a32f41a8d543218bbadea`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4.0-dind-rootless`

```console
$ docker pull docker@sha256:06cbcbc282cf54fc1c4c2c326d236bb3e8aeaf9928c946f5a5128f1077994913
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.4.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e8017dfd3cd4ec88a74e0c0799896877e783a0cc3c936a5b6a58c846b963d5d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161531714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b75307842b323b7da6d0ef282d8bceb758e2399303655d255714432b4e1add`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:36 GMT
CMD []
# Tue, 07 Apr 2026 18:06:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 07 Apr 2026 18:06:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 07 Apr 2026 18:06:51 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074da42c286968f826b040d456a99617b43bda2cc5bf557dceea3de5d6cc4fe`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 6.9 MB (6941677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f4ce6ca5a90a42c5d8d8c00baea57cee587bb141c85bab7aff5de38c99737`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21abf0696dc4d51910e445d2f536ad172bfde41b5963779800c78584ab0b7c`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa3ba34873437febe66dfabe21b09faedd97173ea3f99cdfac49a4960a6f22`  
		Last Modified: Tue, 07 Apr 2026 18:03:49 GMT  
		Size: 68.3 MB (68266949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7a5643b3f629c64a89c9a7665a2102ef8d1b9fe06893fd322d2184c711b5bf`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911bab9d694e25eb17eb5d3df1bd3e09f0ea52d970ce04fa58c0b41861ff8a`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d755e56ce2d2de497c291abe2cb3c543234d57811aa6cc31892539b9612766`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 3.4 MB (3419944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5a1bed895274e6a0aa4e6518ecea2b536c06de2ba8ff8d46f1780b3d1df919`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb54c75cdd29b9362c1d06f6660d0f7d8d7bbe7893e0b9ce825e1b83aaa0561`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab93e7606625323931d20ec97f988d0e03a1d70170464edf09698a7e5ed0c824`  
		Last Modified: Tue, 07 Apr 2026 18:06:58 GMT  
		Size: 17.6 MB (17580413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102bb795e921727afa1a0d32ec9a3ad5a0ee29c9ff396cd792983d41bf76d7c0`  
		Last Modified: Tue, 07 Apr 2026 18:06:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2393d1f43dc15591888c4c108dd057ac24c8b75e437c291786978dfa8055cbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4157e73cac3aafdf5ccdcb29066abeb8fe640483f2b59b1769e2f1b2e1626873`

```dockerfile
```

-	Layers:
	-	`sha256:a427061545c1c404aa1ff5448e2d7ddef22f9ce7690bf471b5c9b5d8cf59b5cf`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.4.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d8d9eab16c89792d62362031ddcf62ab255f8de04859c7c424a4da9570ffa2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151405963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd234006ba72c0f64937b10d1d687a972e3973eb0ee05cb2d02dfceac3ea6473`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:25 GMT
CMD []
# Tue, 07 Apr 2026 18:07:07 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 07 Apr 2026 18:07:07 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 07 Apr 2026 18:07:07 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:07:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 07 Apr 2026 18:07:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 07 Apr 2026 18:07:08 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 07 Apr 2026 18:07:08 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b00d7b9300d4ebf88506edbb338095cf5ad19da1ef0cbef84ae82dd84a0bcb`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 7.2 MB (7219468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa958935e1bc1165d4187e06c145c326c85b4154be3e340a1f57fffa4ae15fb7`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a18406c30abb1ed5c938e64854db122e53e7024a5ee5c6b95ce9c37675aa5`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e20c26df1d1cb588216d065b94856a954f64f3a2fc7252c355c624cf06f166`  
		Last Modified: Tue, 07 Apr 2026 18:03:36 GMT  
		Size: 61.8 MB (61791015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b1556da54467a07970b25f2f5e904eea0cb264745a4cd40a88db0ff73a276d`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d51a5932c15f504e0507fa22ab23138015cb8597493fd874d959868102059`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd008e50d6fda4dec99a7345870c1aaa5e47590866dc1a8b580f63be5b4ba1fe`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 3.4 MB (3394378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84d9a19178955f77588d5e575ba89ed64e606150680ee055d3e7f81a7c9e19c`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df25b78e32b01224db4177327e28b0c5aa1fdc8df4fa296b7a11dc254cad6294`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6326173b0d2b0474538dc36d4f09aec863c9d8cc8853c4b8d2b9e6239e5c2de`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 17.9 MB (17882798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e473478b98a0d67b7e5082a1fdfc46efa97b2774cffe12a23e7e330c541ebb4`  
		Last Modified: Tue, 07 Apr 2026 18:07:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.4.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a6cf4e5aa66894ec1c5141441bae823cbaf150cdf7799cf03f319eaa34a36fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9213b6754bae917b8aa66937ca0fd9d823685fe09c4ffc75849dfffef3543b9`

```dockerfile
```

-	Layers:
	-	`sha256:185779fc84203fff8c14a24aba62314b0a891054f60dc2387016673e9c80c735`  
		Last Modified: Tue, 07 Apr 2026 18:07:13 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.4.0-windowsservercore`

```console
$ docker pull docker@sha256:38716da2bf6648465dcaf041bb44f5a4c216b8ce28dd7b2f1021a590fa6ecc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `docker:29.4.0-windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:1805bfa9662cfa4218077bd8ede9b5a6d69c6646439b7521c0bbbd1d6d516f31
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136863509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9768faff7c37bf673323e8563e2159940625e141fc4292c86de2abcec477d7dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 07 Apr 2026 17:45:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:52 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6349df402a8ae75343c96cbbf6fda362d5255740fa6a27c40633fdd74cb8b486`  
		Last Modified: Tue, 07 Apr 2026 17:47:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbaff7ffcff282be3a7cf2b17c33b81d01113cfd9c33a3dd1fc69933363cb882`  
		Last Modified: Tue, 07 Apr 2026 18:06:25 GMT  
		Size: 381.7 KB (381735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4e33ae54c24d17b8b0322f13394b73fa21b1b3a8aa5f40459be12d90d95e8`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe5a20a0f91f2d088cb920e67e52856b75d803e8f11af764c8d124f2dcd93c`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a11f5b4aabfe9b04c01662839eef4d615567e211f283c6e7818e52b3668d661`  
		Last Modified: Tue, 07 Apr 2026 18:06:27 GMT  
		Size: 20.2 MB (20166075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683aaeb151b66e53b1096f22b39533930cef0c1c98a4745f57e71a5f01fb8a0a`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b99e49f048c1ff00de08fd0e6c43a403ab69c2ba7638830c82c36da218d8d`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683624596fd59caecf2e64b0bbfd45b372c1f6869db5c6cfb23fb047bf51eec5`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3391b63f468d72f2045f24a2a8bf86bc454e7bde74c6d8f9b32fcca119e80b`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 23.4 MB (23447007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3612cdb40d7bf90e6e50f9f05c5c7602d11d06a46cca4a6c6482fdd833f1cac3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8ba35ebad23e35edac88bbe0a734de8b14825a7f0651ae67b85224128272b3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df6d8c50c80a893ae84a723eeb4dec4099df9a827b91826b40e1759a9b99509`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1af4d02e803d87cc569e51d6f3511d7ceaac2fe30774f4ea6d1a356e42f89ef`  
		Last Modified: Tue, 07 Apr 2026 18:06:23 GMT  
		Size: 11.7 MB (11660920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.4.0-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:f37ee3a5fbb958e19138ee2f09d74c58542c532617c7657817359dd37da7472a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2038007541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c93fe0bda8880246418c197b65f4235c5e9f167a5bd4bfd6ce249972e6c5c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 07 Apr 2026 17:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:43 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:46 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:10 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d3d1e4e44fed34fcadd7a99422714da9b20d4f49e0a6fb695d9b5ea818a9ac`  
		Last Modified: Tue, 07 Apr 2026 17:41:02 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9c300c06bd98acbe2efc0c277d580fece563c470038eb8f74d2dd922de94d2`  
		Last Modified: Tue, 07 Apr 2026 18:06:29 GMT  
		Size: 496.2 KB (496237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ff057fe30ee36a89c50acd5ea6585849fb0687ecc19793300b7ee68e4a96bd`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8134fe4ef0e8a711d1eb7bffb1301a576b73a62f71eecd8dfae02f4a50af8d7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bb0fe00c187e5f0aa9c4e431ee26a5472aa893ef9395cead9bc41b53d8bf24`  
		Last Modified: Tue, 07 Apr 2026 18:06:30 GMT  
		Size: 20.1 MB (20143093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3c598636682c6365d6f6dcb67f2fe461dec34bdafe63d7f06138a9b371bdf5`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efee4361413a5695bc83bc76f10df48ec89643440981ead7d535b2b6134a434`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94b089de7840afa203de00c1150ca0636ad534b44e02169335c5c801b3db6b9`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2debda1316a8781d0d548bbf802336d7b4de1ba27198d02473ac96035360f7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 23.4 MB (23432756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca2269f79a5fe310160fcdd23d20b43df2a3547e81e8b04d06f3f25d1dcf8d3`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a834edccd436ba139fc54989c90c4fc8df0d139404714500103d3aa97ccbf512`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906a82b2a03d5ef6e2950ddf7f1680dfea855e0cda9e1123483778f916e7ba8e`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29a6939b1400dc3f52e8fff687d10e51c019eac0f3acf953221086d503f71b6`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 11.6 MB (11642251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c577bbb3fdf12421850d9d7d9c2ede8620846655f6110ad10b6b9c0757a6ad12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `docker:29.4.0-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:f37ee3a5fbb958e19138ee2f09d74c58542c532617c7657817359dd37da7472a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2038007541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c93fe0bda8880246418c197b65f4235c5e9f167a5bd4bfd6ce249972e6c5c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 07 Apr 2026 17:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:43 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:46 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:10 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d3d1e4e44fed34fcadd7a99422714da9b20d4f49e0a6fb695d9b5ea818a9ac`  
		Last Modified: Tue, 07 Apr 2026 17:41:02 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9c300c06bd98acbe2efc0c277d580fece563c470038eb8f74d2dd922de94d2`  
		Last Modified: Tue, 07 Apr 2026 18:06:29 GMT  
		Size: 496.2 KB (496237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ff057fe30ee36a89c50acd5ea6585849fb0687ecc19793300b7ee68e4a96bd`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8134fe4ef0e8a711d1eb7bffb1301a576b73a62f71eecd8dfae02f4a50af8d7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bb0fe00c187e5f0aa9c4e431ee26a5472aa893ef9395cead9bc41b53d8bf24`  
		Last Modified: Tue, 07 Apr 2026 18:06:30 GMT  
		Size: 20.1 MB (20143093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3c598636682c6365d6f6dcb67f2fe461dec34bdafe63d7f06138a9b371bdf5`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efee4361413a5695bc83bc76f10df48ec89643440981ead7d535b2b6134a434`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94b089de7840afa203de00c1150ca0636ad534b44e02169335c5c801b3db6b9`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2debda1316a8781d0d548bbf802336d7b4de1ba27198d02473ac96035360f7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 23.4 MB (23432756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca2269f79a5fe310160fcdd23d20b43df2a3547e81e8b04d06f3f25d1dcf8d3`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a834edccd436ba139fc54989c90c4fc8df0d139404714500103d3aa97ccbf512`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906a82b2a03d5ef6e2950ddf7f1680dfea855e0cda9e1123483778f916e7ba8e`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29a6939b1400dc3f52e8fff687d10e51c019eac0f3acf953221086d503f71b6`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 11.6 MB (11642251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.4.0-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:822c277e276a37345c2329fab738fdf21ef45e0c7331a3d44f96d3f4520ff5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:29.4.0-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:1805bfa9662cfa4218077bd8ede9b5a6d69c6646439b7521c0bbbd1d6d516f31
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136863509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9768faff7c37bf673323e8563e2159940625e141fc4292c86de2abcec477d7dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 07 Apr 2026 17:45:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:52 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6349df402a8ae75343c96cbbf6fda362d5255740fa6a27c40633fdd74cb8b486`  
		Last Modified: Tue, 07 Apr 2026 17:47:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbaff7ffcff282be3a7cf2b17c33b81d01113cfd9c33a3dd1fc69933363cb882`  
		Last Modified: Tue, 07 Apr 2026 18:06:25 GMT  
		Size: 381.7 KB (381735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4e33ae54c24d17b8b0322f13394b73fa21b1b3a8aa5f40459be12d90d95e8`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe5a20a0f91f2d088cb920e67e52856b75d803e8f11af764c8d124f2dcd93c`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a11f5b4aabfe9b04c01662839eef4d615567e211f283c6e7818e52b3668d661`  
		Last Modified: Tue, 07 Apr 2026 18:06:27 GMT  
		Size: 20.2 MB (20166075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683aaeb151b66e53b1096f22b39533930cef0c1c98a4745f57e71a5f01fb8a0a`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b99e49f048c1ff00de08fd0e6c43a403ab69c2ba7638830c82c36da218d8d`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683624596fd59caecf2e64b0bbfd45b372c1f6869db5c6cfb23fb047bf51eec5`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3391b63f468d72f2045f24a2a8bf86bc454e7bde74c6d8f9b32fcca119e80b`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 23.4 MB (23447007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3612cdb40d7bf90e6e50f9f05c5c7602d11d06a46cca4a6c6482fdd833f1cac3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8ba35ebad23e35edac88bbe0a734de8b14825a7f0651ae67b85224128272b3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df6d8c50c80a893ae84a723eeb4dec4099df9a827b91826b40e1759a9b99509`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1af4d02e803d87cc569e51d6f3511d7ceaac2fe30774f4ea6d1a356e42f89ef`  
		Last Modified: Tue, 07 Apr 2026 18:06:23 GMT  
		Size: 11.7 MB (11660920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:0befd75049d8903cd5606879d251bd29ac08758cd33f9c7c74583fc6679b737d
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

### `docker:cli` - linux; amd64

```console
$ docker pull docker@sha256:162f671f43d999a41de10577c292392d92df278f2b19619bd00f62702b9aa2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65222927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad9b141cd1de25bf040248038f95cd6219a80703fd707e59b2b6a0517308b72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:daf7ceb8c94a68d086116d67088dcb70baa3ccd572ff5c33286ad2106b907897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7290d94403713e42feb20ce8a180e2fdd9faf2f4c61c1e6a56befb117afe1fc8`

```dockerfile
```

-	Layers:
	-	`sha256:b95f79229ba482446ea56f9b087844cfdb759933700550eda0ac85aa7b865ed4`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:01b9514d3a7731ab09e57a066f6f57fc6bfd443cc4bb281b5defbf46434d784f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61523027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e6afc4be332ae73538fea1317c86c824dc8f3fed5bd6479ef0f3623fd66f2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:52:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:52:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:52:27 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b23450f59ae29757b818023e9e1ec7feecec88f0bdffda20a422b2bf40901`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 8.3 MB (8300867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016992555c050a7efd3e0035e8b9a0552c0b9ed2c184291a79aafac5eec2bdb`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c85acb49acf037dbe3345d449eb1c7352be8603c84cbe00120ea39e3d7c30`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 18.1 MB (18109482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e782e8b1924d10e930976d421346c23ca8082dc4665b434c499c55cacdfb8`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 21.2 MB (21151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521a4f32de85375d05302a7d66d9f4b7b8d2e2750474fe3a0ae65c01908aaee`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 10.4 MB (10388830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615f51faa1cea9baac6124a72554172703a48489cfa064d499cb85dbb594352`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9369afbb000ee5860be68de87ea400bade9c679f1e5f9807ee421b61828989`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70ec8240492116e39d00b6dca97c3a28a1163f7e2170ccc530976b2319f26`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:005090b7bbeeb700acbccd357974890d0823f6b05afd754f62123ce0cc2c9327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746bfb0046c73dc782de8b20a9ce871dc02be903bb3305fb32d83c36465c4b61`

```dockerfile
```

-	Layers:
	-	`sha256:1d9d1c99fe378084950dc2c8f24e70107427c1736e16ba6a42be234d1fc3e615`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:b5e13676109eba75e0291b50c5457e21aa02414b1ba2eca698d6385511dfa8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60479667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431a96e79c5bb0cc3f234407c79cd071478587e33cdf94a2ede1122d0c0f9873`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:56:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:56:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:56:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:56:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:56:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:56:46 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d02ce67b4a0275f7c58bea67b202248f2e1fadee3c6981a52b02af3245dc7`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 7.6 MB (7597809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae114ba08bb257f6560a48e6f42e0eca1e4275b2b1f5de1a5cee3264ac227117`  
		Last Modified: Tue, 07 Apr 2026 17:56:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c462895e881488d974811c947d011f385c58e7837ee4a36e8eb5347cbfbdead`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 18.1 MB (18096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed288924400fa0ef850973ed05b5d68ad1e971d6db3475e8ec6a66996d1f004e`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 21.1 MB (21129730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562fb47ee8e5eb694e39d13d273c9a20343c2611795f59bf060f8896ad84505`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 10.4 MB (10371866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322fadd946101bd1db893bbeab2210077c079947108eba25d61f69bc80b86918`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee11a625998530da0978a257398229bdf229cb3172d2623d63cdaa10a04dd37`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463989f7f6b0810cca12186041f47307814448d147f72bff8a0f48239efc234`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:00955fd445b2706d6540aec431b00eaff21297aff36f366d2b10b3f4f0e74a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9541b749d18a90c9233171b4a24d5ec5360a879be45ca225522b51eda41825`

```dockerfile
```

-	Layers:
	-	`sha256:58793278463a7baf2e54d0b9ec3edfaaaa4bf35057e379c728b4864ddbed92d5`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:db0c05a4aab745e54662ec56befe45e3c265f485d9d7c7e2d1ffe32f2131448d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61009679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65923880c0dee4eabcf3f64a2fc3e0cc27a7b521fd83945232a7c2c587ae70bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:7b06c415f269961efe974617d3e8b045f801c7e82fe1ef4eac6a74707b63420c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4b4265560dfb409203188b0903d9895666374d935b7351a099c296894efbf8`

```dockerfile
```

-	Layers:
	-	`sha256:983969a38dd490d16487039ccb7e1f62968548fc8a488c859ddd9e62a80382df`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:f80c26212befc1c1988b529495532c6b9180d9b1dab1611f4a1efbe9da8ec821
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
$ docker pull docker@sha256:287ae43017f5d929fe86b951861c6a17c47a18920dbec865d401a08aa827f6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140530015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f374b8d47eebfb2450d5a19efc473c1d20bf645f84c46c21c2854377688446`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:36 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074da42c286968f826b040d456a99617b43bda2cc5bf557dceea3de5d6cc4fe`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 6.9 MB (6941677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f4ce6ca5a90a42c5d8d8c00baea57cee587bb141c85bab7aff5de38c99737`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21abf0696dc4d51910e445d2f536ad172bfde41b5963779800c78584ab0b7c`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa3ba34873437febe66dfabe21b09faedd97173ea3f99cdfac49a4960a6f22`  
		Last Modified: Tue, 07 Apr 2026 18:03:49 GMT  
		Size: 68.3 MB (68266949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7a5643b3f629c64a89c9a7665a2102ef8d1b9fe06893fd322d2184c711b5bf`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911bab9d694e25eb17eb5d3df1bd3e09f0ea52d970ce04fa58c0b41861ff8a`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:73b899bc96cf92b0e9a346d2299d110d3fe56b6155f1219dc06b4d4e6172268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc72525e88ac1b74d2507c98202bc1732e6931e5409efa62649aeecef0bda2cf`

```dockerfile
```

-	Layers:
	-	`sha256:57834d73984ba9824980e22fe7ed18b2b1e911c35b6f27dc4f2b7486672e6a28`  
		Last Modified: Tue, 07 Apr 2026 18:03:46 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:d94555deb39a31975ca0a7df7f6f607745e2e3cea98b85279ecab2d2179e2d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132509296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342e83533005345d07b6aa7ba5cc4aa7efe7c9bf531476ab6309626983b8ad35`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:52:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:52:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:52:27 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:31 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b23450f59ae29757b818023e9e1ec7feecec88f0bdffda20a422b2bf40901`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 8.3 MB (8300867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016992555c050a7efd3e0035e8b9a0552c0b9ed2c184291a79aafac5eec2bdb`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c85acb49acf037dbe3345d449eb1c7352be8603c84cbe00120ea39e3d7c30`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 18.1 MB (18109482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e782e8b1924d10e930976d421346c23ca8082dc4665b434c499c55cacdfb8`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 21.2 MB (21151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521a4f32de85375d05302a7d66d9f4b7b8d2e2750474fe3a0ae65c01908aaee`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 10.4 MB (10388830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615f51faa1cea9baac6124a72554172703a48489cfa064d499cb85dbb594352`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9369afbb000ee5860be68de87ea400bade9c679f1e5f9807ee421b61828989`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70ec8240492116e39d00b6dca97c3a28a1163f7e2170ccc530976b2319f26`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b98d7b3e63b394195345d7cb8704aca5c40c08c77a0bf1332fe636cdf85f8f`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 7.3 MB (7278270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bf81f4773f03aaa784a3470bcce2edc2b6a47934ee47acb8cca08a5f355c98`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 91.8 KB (91782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200628578e34b666753dac7e5f675103937c5bc8b19ee1944b18678f0c46925d`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd2d115f337cd4f0d6b8569b2b846987f6e9ac5e092ef1ff0d4ddf55d6e1bd5`  
		Last Modified: Tue, 07 Apr 2026 18:03:44 GMT  
		Size: 63.6 MB (63610216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cae13c6f8720e02fe0cfac11bf4b7873b5127026edf0fd7d60f3869d6d7419`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f9f1d6532df85ab83bce5d7ef4d79e700e0400906d7758bc10171637fb4789`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:47c1c2e7f2d77d352752eed854ede75fe2b99d09a4d2803179083cb08ff22f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6e98380b13b625be9b687b14bd321547ba3ab0a5453ab8bc4373d0660c5188`

```dockerfile
```

-	Layers:
	-	`sha256:e1ee81fe381e2225b1105e6c67bdff7bcb2289618bb0a726e2ed400b0fcfe1c8`  
		Last Modified: Tue, 07 Apr 2026 18:03:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:2fe5918d6fc855d73d4a3f2a00996b7f0a34b7634e179ac2122c2fbdf43a4875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c711cf90ab57665fc3f8f136101a98f0aaaee0ddc5bc0c9f79d5a22477161a42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:56:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:56:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:56:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:56:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:56:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:56:46 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:04:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:04:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:04:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:04:07 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d02ce67b4a0275f7c58bea67b202248f2e1fadee3c6981a52b02af3245dc7`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 7.6 MB (7597809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae114ba08bb257f6560a48e6f42e0eca1e4275b2b1f5de1a5cee3264ac227117`  
		Last Modified: Tue, 07 Apr 2026 17:56:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c462895e881488d974811c947d011f385c58e7837ee4a36e8eb5347cbfbdead`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 18.1 MB (18096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed288924400fa0ef850973ed05b5d68ad1e971d6db3475e8ec6a66996d1f004e`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 21.1 MB (21129730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562fb47ee8e5eb694e39d13d273c9a20343c2611795f59bf060f8896ad84505`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 10.4 MB (10371866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322fadd946101bd1db893bbeab2210077c079947108eba25d61f69bc80b86918`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee11a625998530da0978a257398229bdf229cb3172d2623d63cdaa10a04dd37`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463989f7f6b0810cca12186041f47307814448d147f72bff8a0f48239efc234`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a7a76c7cd299a0667f840f572155fe9e35f5013b5de4e51f836ad166de3094`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 6.6 MB (6576415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecd37ed33aacb16975753b152fd51f47fa1fbd0fbe582cd884e8bc88c7799c9`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 88.1 KB (88144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30c893cca62c4ce187fe0f0df7e1fd32feb7517ce8a8eb10261e08b67c2278f`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2d730ff02f4343d65bdc6f1fbb29d1061a9c64e3f5203d8cf70317d19e67a9`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 63.4 MB (63443312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa38e3d8f2a4334f08fc240f45a7b0857ce64907ba89486d374dbb923fcf33`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522011f6d7ed1009e68e424d9c164d16256d49b5b7421bdb47645f431d7e045a`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:75635ebd248b76a3aa73452fa66599686679233c7faf894570e4870a738fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02726225a9427a640d5001f15d02f9ac80332f8cbdbc5779ef715424b359cecf`

```dockerfile
```

-	Layers:
	-	`sha256:24502e0bf1bc549b64a110973e89bb2b40d90b3444bca7efb104a37f5c4c2e51`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f56f84c60b1ad8653eb423810cca82f8d86d0f97af8f600b2089d7a79b2c67e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130127448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d9a5c2e9415e93f5577fa9935ab7f163c07791bcca430cfa8100bb716915`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:25 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b00d7b9300d4ebf88506edbb338095cf5ad19da1ef0cbef84ae82dd84a0bcb`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 7.2 MB (7219468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa958935e1bc1165d4187e06c145c326c85b4154be3e340a1f57fffa4ae15fb7`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a18406c30abb1ed5c938e64854db122e53e7024a5ee5c6b95ce9c37675aa5`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e20c26df1d1cb588216d065b94856a954f64f3a2fc7252c355c624cf06f166`  
		Last Modified: Tue, 07 Apr 2026 18:03:36 GMT  
		Size: 61.8 MB (61791015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b1556da54467a07970b25f2f5e904eea0cb264745a4cd40a88db0ff73a276d`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d51a5932c15f504e0507fa22ab23138015cb8597493fd874d959868102059`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:bc33b62b3ef0f1578e119860d5ccc0bd861f6609d97646a69dc27aea75ab9f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21911a20c08d97ff5d0322eed178a80fae80aea719d8f4c5a2093b0e81e79b99`

```dockerfile
```

-	Layers:
	-	`sha256:63938660feb79291b998f4f1c0122abb056fe223055a32f41a8d543218bbadea`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:06cbcbc282cf54fc1c4c2c326d236bb3e8aeaf9928c946f5a5128f1077994913
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e8017dfd3cd4ec88a74e0c0799896877e783a0cc3c936a5b6a58c846b963d5d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161531714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b75307842b323b7da6d0ef282d8bceb758e2399303655d255714432b4e1add`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:36 GMT
CMD []
# Tue, 07 Apr 2026 18:06:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 07 Apr 2026 18:06:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 07 Apr 2026 18:06:51 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 07 Apr 2026 18:06:51 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074da42c286968f826b040d456a99617b43bda2cc5bf557dceea3de5d6cc4fe`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 6.9 MB (6941677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f4ce6ca5a90a42c5d8d8c00baea57cee587bb141c85bab7aff5de38c99737`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21abf0696dc4d51910e445d2f536ad172bfde41b5963779800c78584ab0b7c`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa3ba34873437febe66dfabe21b09faedd97173ea3f99cdfac49a4960a6f22`  
		Last Modified: Tue, 07 Apr 2026 18:03:49 GMT  
		Size: 68.3 MB (68266949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7a5643b3f629c64a89c9a7665a2102ef8d1b9fe06893fd322d2184c711b5bf`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911bab9d694e25eb17eb5d3df1bd3e09f0ea52d970ce04fa58c0b41861ff8a`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d755e56ce2d2de497c291abe2cb3c543234d57811aa6cc31892539b9612766`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 3.4 MB (3419944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5a1bed895274e6a0aa4e6518ecea2b536c06de2ba8ff8d46f1780b3d1df919`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb54c75cdd29b9362c1d06f6660d0f7d8d7bbe7893e0b9ce825e1b83aaa0561`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab93e7606625323931d20ec97f988d0e03a1d70170464edf09698a7e5ed0c824`  
		Last Modified: Tue, 07 Apr 2026 18:06:58 GMT  
		Size: 17.6 MB (17580413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102bb795e921727afa1a0d32ec9a3ad5a0ee29c9ff396cd792983d41bf76d7c0`  
		Last Modified: Tue, 07 Apr 2026 18:06:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2393d1f43dc15591888c4c108dd057ac24c8b75e437c291786978dfa8055cbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4157e73cac3aafdf5ccdcb29066abeb8fe640483f2b59b1769e2f1b2e1626873`

```dockerfile
```

-	Layers:
	-	`sha256:a427061545c1c404aa1ff5448e2d7ddef22f9ce7690bf471b5c9b5d8cf59b5cf`  
		Last Modified: Tue, 07 Apr 2026 18:06:57 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d8d9eab16c89792d62362031ddcf62ab255f8de04859c7c424a4da9570ffa2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151405963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd234006ba72c0f64937b10d1d687a972e3973eb0ee05cb2d02dfceac3ea6473`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:25 GMT
CMD []
# Tue, 07 Apr 2026 18:07:07 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 07 Apr 2026 18:07:07 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 07 Apr 2026 18:07:07 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:07:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 07 Apr 2026 18:07:08 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 07 Apr 2026 18:07:08 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 07 Apr 2026 18:07:08 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b00d7b9300d4ebf88506edbb338095cf5ad19da1ef0cbef84ae82dd84a0bcb`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 7.2 MB (7219468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa958935e1bc1165d4187e06c145c326c85b4154be3e340a1f57fffa4ae15fb7`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a18406c30abb1ed5c938e64854db122e53e7024a5ee5c6b95ce9c37675aa5`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e20c26df1d1cb588216d065b94856a954f64f3a2fc7252c355c624cf06f166`  
		Last Modified: Tue, 07 Apr 2026 18:03:36 GMT  
		Size: 61.8 MB (61791015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b1556da54467a07970b25f2f5e904eea0cb264745a4cd40a88db0ff73a276d`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d51a5932c15f504e0507fa22ab23138015cb8597493fd874d959868102059`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd008e50d6fda4dec99a7345870c1aaa5e47590866dc1a8b580f63be5b4ba1fe`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 3.4 MB (3394378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84d9a19178955f77588d5e575ba89ed64e606150680ee055d3e7f81a7c9e19c`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df25b78e32b01224db4177327e28b0c5aa1fdc8df4fa296b7a11dc254cad6294`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6326173b0d2b0474538dc36d4f09aec863c9d8cc8853c4b8d2b9e6239e5c2de`  
		Last Modified: Tue, 07 Apr 2026 18:07:14 GMT  
		Size: 17.9 MB (17882798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e473478b98a0d67b7e5082a1fdfc46efa97b2774cffe12a23e7e330c541ebb4`  
		Last Modified: Tue, 07 Apr 2026 18:07:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a6cf4e5aa66894ec1c5141441bae823cbaf150cdf7799cf03f319eaa34a36fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9213b6754bae917b8aa66937ca0fd9d823685fe09c4ffc75849dfffef3543b9`

```dockerfile
```

-	Layers:
	-	`sha256:185779fc84203fff8c14a24aba62314b0a891054f60dc2387016673e9c80c735`  
		Last Modified: Tue, 07 Apr 2026 18:07:13 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:f80c26212befc1c1988b529495532c6b9180d9b1dab1611f4a1efbe9da8ec821
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

### `docker:latest` - linux; amd64

```console
$ docker pull docker@sha256:287ae43017f5d929fe86b951861c6a17c47a18920dbec865d401a08aa827f6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140530015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f374b8d47eebfb2450d5a19efc473c1d20bf645f84c46c21c2854377688446`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:11 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:13 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:36 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:36 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:36 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:36 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:36 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee469356d395f8925f2f4741e96a7315da8a01eb8d4b2f528674b71f26efc5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 8.4 MB (8399815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d20e0f320311eec225e48d2f05f6d4b4e7d7b94c5a50503d12cb9e33aff1c1`  
		Last Modified: Tue, 07 Apr 2026 17:51:19 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56b28218d1d1b2916f1fb82a78b4d975df7e07d8898a3ed1236b090bc8ada16`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 19.5 MB (19464810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3568f9ed6257326e4980b1780a472a58b70264e10515c2d6c9bcbff2a558863`  
		Last Modified: Tue, 07 Apr 2026 17:51:20 GMT  
		Size: 22.5 MB (22539223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ac3564cdb8322c89d3d5eb623ae5aaf10c06e709009e68b3c2e583db6c62aa`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 11.0 MB (10955102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4904a2b71511936b435a9df2f69a96753aac01c3db532903e1272a7506cd5b`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5545be0b2cda9ce15849ac83c28b57a6f68fd0bea4301aacf49479ae764adf`  
		Last Modified: Tue, 07 Apr 2026 17:51:21 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86662591a9e9c87dd487ca3a1b45f5cad2aebfc9fe36ec40780e7d6f56bad1`  
		Last Modified: Tue, 07 Apr 2026 17:51:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5074da42c286968f826b040d456a99617b43bda2cc5bf557dceea3de5d6cc4fe`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 6.9 MB (6941677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6f4ce6ca5a90a42c5d8d8c00baea57cee587bb141c85bab7aff5de38c99737`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 92.5 KB (92465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21abf0696dc4d51910e445d2f536ad172bfde41b5963779800c78584ab0b7c`  
		Last Modified: Tue, 07 Apr 2026 18:03:47 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aa3ba34873437febe66dfabe21b09faedd97173ea3f99cdfac49a4960a6f22`  
		Last Modified: Tue, 07 Apr 2026 18:03:49 GMT  
		Size: 68.3 MB (68266949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7a5643b3f629c64a89c9a7665a2102ef8d1b9fe06893fd322d2184c711b5bf`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911bab9d694e25eb17eb5d3df1bd3e09f0ea52d970ce04fa58c0b41861ff8a`  
		Last Modified: Tue, 07 Apr 2026 18:03:48 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:73b899bc96cf92b0e9a346d2299d110d3fe56b6155f1219dc06b4d4e6172268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc72525e88ac1b74d2507c98202bc1732e6931e5409efa62649aeecef0bda2cf`

```dockerfile
```

-	Layers:
	-	`sha256:57834d73984ba9824980e22fe7ed18b2b1e911c35b6f27dc4f2b7486672e6a28`  
		Last Modified: Tue, 07 Apr 2026 18:03:46 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:d94555deb39a31975ca0a7df7f6f607745e2e3cea98b85279ecab2d2179e2d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132509296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342e83533005345d07b6aa7ba5cc4aa7efe7c9bf531476ab6309626983b8ad35`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:52:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:52:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:52:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:52:23 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:52:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:52:25 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:52:27 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:52:27 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:52:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:52:27 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:27 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:31 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:31 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32b23450f59ae29757b818023e9e1ec7feecec88f0bdffda20a422b2bf40901`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 8.3 MB (8300867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7016992555c050a7efd3e0035e8b9a0552c0b9ed2c184291a79aafac5eec2bdb`  
		Last Modified: Tue, 07 Apr 2026 17:52:33 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4c85acb49acf037dbe3345d449eb1c7352be8603c84cbe00120ea39e3d7c30`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 18.1 MB (18109482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e782e8b1924d10e930976d421346c23ca8082dc4665b434c499c55cacdfb8`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 21.2 MB (21151871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0521a4f32de85375d05302a7d66d9f4b7b8d2e2750474fe3a0ae65c01908aaee`  
		Last Modified: Tue, 07 Apr 2026 17:52:34 GMT  
		Size: 10.4 MB (10388830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7615f51faa1cea9baac6124a72554172703a48489cfa064d499cb85dbb594352`  
		Last Modified: Tue, 07 Apr 2026 17:52:35 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9369afbb000ee5860be68de87ea400bade9c679f1e5f9807ee421b61828989`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70ec8240492116e39d00b6dca97c3a28a1163f7e2170ccc530976b2319f26`  
		Last Modified: Tue, 07 Apr 2026 17:52:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b98d7b3e63b394195345d7cb8704aca5c40c08c77a0bf1332fe636cdf85f8f`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 7.3 MB (7278270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bf81f4773f03aaa784a3470bcce2edc2b6a47934ee47acb8cca08a5f355c98`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 91.8 KB (91782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200628578e34b666753dac7e5f675103937c5bc8b19ee1944b18678f0c46925d`  
		Last Modified: Tue, 07 Apr 2026 18:03:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd2d115f337cd4f0d6b8569b2b846987f6e9ac5e092ef1ff0d4ddf55d6e1bd5`  
		Last Modified: Tue, 07 Apr 2026 18:03:44 GMT  
		Size: 63.6 MB (63610216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cae13c6f8720e02fe0cfac11bf4b7873b5127026edf0fd7d60f3869d6d7419`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f9f1d6532df85ab83bce5d7ef4d79e700e0400906d7758bc10171637fb4789`  
		Last Modified: Tue, 07 Apr 2026 18:03:43 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:47c1c2e7f2d77d352752eed854ede75fe2b99d09a4d2803179083cb08ff22f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6e98380b13b625be9b687b14bd321547ba3ab0a5453ab8bc4373d0660c5188`

```dockerfile
```

-	Layers:
	-	`sha256:e1ee81fe381e2225b1105e6c67bdff7bcb2289618bb0a726e2ed400b0fcfe1c8`  
		Last Modified: Tue, 07 Apr 2026 18:03:41 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:2fe5918d6fc855d73d4a3f2a00996b7f0a34b7634e179ac2122c2fbdf43a4875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130593536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c711cf90ab57665fc3f8f136101a98f0aaaee0ddc5bc0c9f79d5a22477161a42`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:56:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:56:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:56:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:56:42 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:56:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:56:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:56:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:56:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:56:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:56:46 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:04:02 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:04:03 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:04:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:04:07 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:04:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:04:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:04:07 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40d02ce67b4a0275f7c58bea67b202248f2e1fadee3c6981a52b02af3245dc7`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 7.6 MB (7597809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae114ba08bb257f6560a48e6f42e0eca1e4275b2b1f5de1a5cee3264ac227117`  
		Last Modified: Tue, 07 Apr 2026 17:56:52 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c462895e881488d974811c947d011f385c58e7837ee4a36e8eb5347cbfbdead`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 18.1 MB (18096386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed288924400fa0ef850973ed05b5d68ad1e971d6db3475e8ec6a66996d1f004e`  
		Last Modified: Tue, 07 Apr 2026 17:56:53 GMT  
		Size: 21.1 MB (21129730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562fb47ee8e5eb694e39d13d273c9a20343c2611795f59bf060f8896ad84505`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 10.4 MB (10371866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322fadd946101bd1db893bbeab2210077c079947108eba25d61f69bc80b86918`  
		Last Modified: Tue, 07 Apr 2026 17:56:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee11a625998530da0978a257398229bdf229cb3172d2623d63cdaa10a04dd37`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463989f7f6b0810cca12186041f47307814448d147f72bff8a0f48239efc234`  
		Last Modified: Tue, 07 Apr 2026 17:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a7a76c7cd299a0667f840f572155fe9e35f5013b5de4e51f836ad166de3094`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 6.6 MB (6576415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecd37ed33aacb16975753b152fd51f47fa1fbd0fbe582cd884e8bc88c7799c9`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 88.1 KB (88144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30c893cca62c4ce187fe0f0df7e1fd32feb7517ce8a8eb10261e08b67c2278f`  
		Last Modified: Tue, 07 Apr 2026 18:04:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2d730ff02f4343d65bdc6f1fbb29d1061a9c64e3f5203d8cf70317d19e67a9`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 63.4 MB (63443312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfa38e3d8f2a4334f08fc240f45a7b0857ce64907ba89486d374dbb923fcf33`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522011f6d7ed1009e68e424d9c164d16256d49b5b7421bdb47645f431d7e045a`  
		Last Modified: Tue, 07 Apr 2026 18:04:19 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:75635ebd248b76a3aa73452fa66599686679233c7faf894570e4870a738fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02726225a9427a640d5001f15d02f9ac80332f8cbdbc5779ef715424b359cecf`

```dockerfile
```

-	Layers:
	-	`sha256:24502e0bf1bc549b64a110973e89bb2b40d90b3444bca7efb104a37f5c4c2e51`  
		Last Modified: Tue, 07 Apr 2026 18:04:17 GMT  
		Size: 34.7 KB (34721 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f56f84c60b1ad8653eb423810cca82f8d86d0f97af8f600b2089d7a79b2c67e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130127448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5640d9a5c2e9415e93f5577fa9935ab7f163c07791bcca430cfa8100bb716915`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:51:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 07 Apr 2026 17:51:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 17:51:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 07 Apr 2026 17:51:47 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 17:51:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-amd64'; 			sha256='9426a15411f35f635afef3f5d3bae53155c3e30d26dee430cc968e13d34be49f'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v6'; 			sha256='b33311b149623316b840ce25f0b6686433c6aecaca560d8b35906423f8f597bb'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm-v7'; 			sha256='4d80358ce3d217f38ac9e914cb8501fd4a8a45bc3ac3c23d303e623f275a45df'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-arm64'; 			sha256='204dc28447d3bb48f42ed1ce5747e0885cd57e306506a39029311becdb1ef786'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-ppc64le'; 			sha256='46b0444858c8db8c6f741dca20b815f50046a2d73f4874a54dae2719df145ad3'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-riscv64'; 			sha256='5003b19409f2dfb38fc5f00a8eac4b1d810f6087b88ae007c6983287b93095dd'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.linux-s390x'; 			sha256='17fbec8163440e73d1e784d55faf483b17782aac471d867a525fa370f3ed317c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 07 Apr 2026 17:51:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 17:51:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-x86_64'; 			sha256='2ac954c9d506b912a12477d72f01601dc72ec918c429c7bae48fd707bdf0f3e5'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv6'; 			sha256='dbc7d5be282b2f465fb76841588e446f5fee10104c73428e8130bfa9baf1f1e2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-armv7'; 			sha256='5cf43b83c705b24df9dbee1d35a6f085189ee2c1169444147192daf932683ed4'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-aarch64'; 			sha256='4b5c42952b7dd81f508d01a771df2a9e5dbffe9b8c5c7d983e738504ad38f056'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-ppc64le'; 			sha256='e131760ddd58dd5fc42b80ce9e4c49ecb6e8c26638a1c4bc3aa526f58c2440bf'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-riscv64'; 			sha256='8f0df39eaf9014bce4c2505c91d067eb22631e894caabba7c5dae56c72c316f2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-linux-s390x'; 			sha256='87c0b606dcaf49b61f651f2b4e946e03a14e06e1dc16557a408a85e9796884f2'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 07 Apr 2026 17:51:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 07 Apr 2026 17:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:51:49 GMT
CMD ["sh"]
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 07 Apr 2026 18:03:21 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 07 Apr 2026 18:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.4.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.4.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.4.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.4.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 07 Apr 2026 18:03:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 18:03:25 GMT
VOLUME [/var/lib/docker]
# Tue, 07 Apr 2026 18:03:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 07 Apr 2026 18:03:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 07 Apr 2026 18:03:25 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f060d64149ad4825cb612b3f4e427654e3679d32d088aed7b5ec471523553`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 8.5 MB (8453641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f1e927af592cbd885ed02504825761a8b96d640a100d279a0aca3db11d18d`  
		Last Modified: Tue, 07 Apr 2026 17:51:54 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb231ab3447494426dc10d95fe91d208d7e68f3c26c1c77b38705d2157e4124`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 17.9 MB (17921079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dadc8649f2abf7790115538b2ac183efcdbe3a30c1406e05f3783667dde1fa`  
		Last Modified: Tue, 07 Apr 2026 17:51:55 GMT  
		Size: 20.5 MB (20453110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aabf907d46da7ab83cadadb23364475a8df59df67b32649eacb54e3ba59f64a`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 10.0 MB (9982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0a4f1e12b187cbc5347cc1f7e28ef3a1b4c405b0c125ce3d1c7fbd8ded5f88`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32c19b3ecc8fea725785bd6ba9690cab099ec58d838857be88323fa0c384775`  
		Last Modified: Tue, 07 Apr 2026 17:51:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87933c90dd97620f18855170f6b9860dd225ef5c2617f326ab57f1b8860e5c42`  
		Last Modified: Tue, 07 Apr 2026 17:51:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b00d7b9300d4ebf88506edbb338095cf5ad19da1ef0cbef84ae82dd84a0bcb`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 7.2 MB (7219468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa958935e1bc1165d4187e06c145c326c85b4154be3e340a1f57fffa4ae15fb7`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46a18406c30abb1ed5c938e64854db122e53e7024a5ee5c6b95ce9c37675aa5`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e20c26df1d1cb588216d065b94856a954f64f3a2fc7252c355c624cf06f166`  
		Last Modified: Tue, 07 Apr 2026 18:03:36 GMT  
		Size: 61.8 MB (61791015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b1556da54467a07970b25f2f5e904eea0cb264745a4cd40a88db0ff73a276d`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d51a5932c15f504e0507fa22ab23138015cb8597493fd874d959868102059`  
		Last Modified: Tue, 07 Apr 2026 18:03:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:bc33b62b3ef0f1578e119860d5ccc0bd861f6609d97646a69dc27aea75ab9f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21911a20c08d97ff5d0322eed178a80fae80aea719d8f4c5a2093b0e81e79b99`

```dockerfile
```

-	Layers:
	-	`sha256:63938660feb79291b998f4f1c0122abb056fe223055a32f41a8d543218bbadea`  
		Last Modified: Tue, 07 Apr 2026 18:03:34 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:38716da2bf6648465dcaf041bb44f5a4c216b8ce28dd7b2f1021a590fa6ecc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:1805bfa9662cfa4218077bd8ede9b5a6d69c6646439b7521c0bbbd1d6d516f31
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136863509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9768faff7c37bf673323e8563e2159940625e141fc4292c86de2abcec477d7dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 07 Apr 2026 17:45:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:52 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6349df402a8ae75343c96cbbf6fda362d5255740fa6a27c40633fdd74cb8b486`  
		Last Modified: Tue, 07 Apr 2026 17:47:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbaff7ffcff282be3a7cf2b17c33b81d01113cfd9c33a3dd1fc69933363cb882`  
		Last Modified: Tue, 07 Apr 2026 18:06:25 GMT  
		Size: 381.7 KB (381735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4e33ae54c24d17b8b0322f13394b73fa21b1b3a8aa5f40459be12d90d95e8`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe5a20a0f91f2d088cb920e67e52856b75d803e8f11af764c8d124f2dcd93c`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a11f5b4aabfe9b04c01662839eef4d615567e211f283c6e7818e52b3668d661`  
		Last Modified: Tue, 07 Apr 2026 18:06:27 GMT  
		Size: 20.2 MB (20166075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683aaeb151b66e53b1096f22b39533930cef0c1c98a4745f57e71a5f01fb8a0a`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b99e49f048c1ff00de08fd0e6c43a403ab69c2ba7638830c82c36da218d8d`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683624596fd59caecf2e64b0bbfd45b372c1f6869db5c6cfb23fb047bf51eec5`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3391b63f468d72f2045f24a2a8bf86bc454e7bde74c6d8f9b32fcca119e80b`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 23.4 MB (23447007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3612cdb40d7bf90e6e50f9f05c5c7602d11d06a46cca4a6c6482fdd833f1cac3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8ba35ebad23e35edac88bbe0a734de8b14825a7f0651ae67b85224128272b3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df6d8c50c80a893ae84a723eeb4dec4099df9a827b91826b40e1759a9b99509`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1af4d02e803d87cc569e51d6f3511d7ceaac2fe30774f4ea6d1a356e42f89ef`  
		Last Modified: Tue, 07 Apr 2026 18:06:23 GMT  
		Size: 11.7 MB (11660920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:f37ee3a5fbb958e19138ee2f09d74c58542c532617c7657817359dd37da7472a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2038007541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c93fe0bda8880246418c197b65f4235c5e9f167a5bd4bfd6ce249972e6c5c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 07 Apr 2026 17:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:43 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:46 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:10 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d3d1e4e44fed34fcadd7a99422714da9b20d4f49e0a6fb695d9b5ea818a9ac`  
		Last Modified: Tue, 07 Apr 2026 17:41:02 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9c300c06bd98acbe2efc0c277d580fece563c470038eb8f74d2dd922de94d2`  
		Last Modified: Tue, 07 Apr 2026 18:06:29 GMT  
		Size: 496.2 KB (496237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ff057fe30ee36a89c50acd5ea6585849fb0687ecc19793300b7ee68e4a96bd`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8134fe4ef0e8a711d1eb7bffb1301a576b73a62f71eecd8dfae02f4a50af8d7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bb0fe00c187e5f0aa9c4e431ee26a5472aa893ef9395cead9bc41b53d8bf24`  
		Last Modified: Tue, 07 Apr 2026 18:06:30 GMT  
		Size: 20.1 MB (20143093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3c598636682c6365d6f6dcb67f2fe461dec34bdafe63d7f06138a9b371bdf5`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efee4361413a5695bc83bc76f10df48ec89643440981ead7d535b2b6134a434`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94b089de7840afa203de00c1150ca0636ad534b44e02169335c5c801b3db6b9`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2debda1316a8781d0d548bbf802336d7b4de1ba27198d02473ac96035360f7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 23.4 MB (23432756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca2269f79a5fe310160fcdd23d20b43df2a3547e81e8b04d06f3f25d1dcf8d3`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a834edccd436ba139fc54989c90c4fc8df0d139404714500103d3aa97ccbf512`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906a82b2a03d5ef6e2950ddf7f1680dfea855e0cda9e1123483778f916e7ba8e`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29a6939b1400dc3f52e8fff687d10e51c019eac0f3acf953221086d503f71b6`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 11.6 MB (11642251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c577bbb3fdf12421850d9d7d9c2ede8620846655f6110ad10b6b9c0757a6ad12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:f37ee3a5fbb958e19138ee2f09d74c58542c532617c7657817359dd37da7472a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2038007541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c93fe0bda8880246418c197b65f4235c5e9f167a5bd4bfd6ce249972e6c5c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 07 Apr 2026 17:39:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:43 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:46 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:10 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d3d1e4e44fed34fcadd7a99422714da9b20d4f49e0a6fb695d9b5ea818a9ac`  
		Last Modified: Tue, 07 Apr 2026 17:41:02 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9c300c06bd98acbe2efc0c277d580fece563c470038eb8f74d2dd922de94d2`  
		Last Modified: Tue, 07 Apr 2026 18:06:29 GMT  
		Size: 496.2 KB (496237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ff057fe30ee36a89c50acd5ea6585849fb0687ecc19793300b7ee68e4a96bd`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8134fe4ef0e8a711d1eb7bffb1301a576b73a62f71eecd8dfae02f4a50af8d7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bb0fe00c187e5f0aa9c4e431ee26a5472aa893ef9395cead9bc41b53d8bf24`  
		Last Modified: Tue, 07 Apr 2026 18:06:30 GMT  
		Size: 20.1 MB (20143093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3c598636682c6365d6f6dcb67f2fe461dec34bdafe63d7f06138a9b371bdf5`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efee4361413a5695bc83bc76f10df48ec89643440981ead7d535b2b6134a434`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94b089de7840afa203de00c1150ca0636ad534b44e02169335c5c801b3db6b9`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2debda1316a8781d0d548bbf802336d7b4de1ba27198d02473ac96035360f7`  
		Last Modified: Tue, 07 Apr 2026 18:06:28 GMT  
		Size: 23.4 MB (23432756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca2269f79a5fe310160fcdd23d20b43df2a3547e81e8b04d06f3f25d1dcf8d3`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a834edccd436ba139fc54989c90c4fc8df0d139404714500103d3aa97ccbf512`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906a82b2a03d5ef6e2950ddf7f1680dfea855e0cda9e1123483778f916e7ba8e`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29a6939b1400dc3f52e8fff687d10e51c019eac0f3acf953221086d503f71b6`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 11.6 MB (11642251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:822c277e276a37345c2329fab738fdf21ef45e0c7331a3d44f96d3f4520ff5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:1805bfa9662cfa4218077bd8ede9b5a6d69c6646439b7521c0bbbd1d6d516f31
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136863509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9768faff7c37bf673323e8563e2159940625e141fc4292c86de2abcec477d7dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 07 Apr 2026 17:45:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Apr 2026 18:05:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Apr 2026 18:05:34 GMT
ENV DOCKER_VERSION=29.4.0
# Tue, 07 Apr 2026 18:05:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.4.0.zip
# Tue, 07 Apr 2026 18:05:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Tue, 07 Apr 2026 18:05:51 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Tue, 07 Apr 2026 18:05:52 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Tue, 07 Apr 2026 18:06:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Tue, 07 Apr 2026 18:06:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Tue, 07 Apr 2026 18:06:09 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Tue, 07 Apr 2026 18:06:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6349df402a8ae75343c96cbbf6fda362d5255740fa6a27c40633fdd74cb8b486`  
		Last Modified: Tue, 07 Apr 2026 17:47:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbaff7ffcff282be3a7cf2b17c33b81d01113cfd9c33a3dd1fc69933363cb882`  
		Last Modified: Tue, 07 Apr 2026 18:06:25 GMT  
		Size: 381.7 KB (381735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4e33ae54c24d17b8b0322f13394b73fa21b1b3a8aa5f40459be12d90d95e8`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfe5a20a0f91f2d088cb920e67e52856b75d803e8f11af764c8d124f2dcd93c`  
		Last Modified: Tue, 07 Apr 2026 18:06:24 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a11f5b4aabfe9b04c01662839eef4d615567e211f283c6e7818e52b3668d661`  
		Last Modified: Tue, 07 Apr 2026 18:06:27 GMT  
		Size: 20.2 MB (20166075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683aaeb151b66e53b1096f22b39533930cef0c1c98a4745f57e71a5f01fb8a0a`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b99e49f048c1ff00de08fd0e6c43a403ab69c2ba7638830c82c36da218d8d`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683624596fd59caecf2e64b0bbfd45b372c1f6869db5c6cfb23fb047bf51eec5`  
		Last Modified: Tue, 07 Apr 2026 18:06:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3391b63f468d72f2045f24a2a8bf86bc454e7bde74c6d8f9b32fcca119e80b`  
		Last Modified: Tue, 07 Apr 2026 18:06:26 GMT  
		Size: 23.4 MB (23447007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3612cdb40d7bf90e6e50f9f05c5c7602d11d06a46cca4a6c6482fdd833f1cac3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8ba35ebad23e35edac88bbe0a734de8b14825a7f0651ae67b85224128272b3`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df6d8c50c80a893ae84a723eeb4dec4099df9a827b91826b40e1759a9b99509`  
		Last Modified: Tue, 07 Apr 2026 18:06:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1af4d02e803d87cc569e51d6f3511d7ceaac2fe30774f4ea6d1a356e42f89ef`  
		Last Modified: Tue, 07 Apr 2026 18:06:23 GMT  
		Size: 11.7 MB (11660920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
