## `docker:28-rc-dind`

```console
$ docker pull docker@sha256:e054cca6ce705d3360313e1c16aabee746b1809ded05c044ff35643171acf35b
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
$ docker pull docker@sha256:f552047a511855ce77b45552daa04fab0d827f28c979938f2d9315f3e31f985a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138864932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:848fde5cb219ee214d7fbea9cfcc17496946576632f2651a9b3653690ddac356`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 07 Feb 2025 04:13:48 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
CMD ["/bin/sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_VERSION=28.0.0-rc.1
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 07 Feb 2025 04:13:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
CMD ["sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
VOLUME [/var/lib/docker]
# Fri, 07 Feb 2025 04:13:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 07 Feb 2025 04:13:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
CMD []
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d305ff8d35d2784d0e9d7b696385172f6cebbadd920fa52bef6d4e125e657a`  
		Last Modified: Fri, 14 Feb 2025 20:33:38 GMT  
		Size: 8.1 MB (8062539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7989d6118437d2674c37c20154d2068ac40bd2ac09208052ba4f833c9c06f866`  
		Last Modified: Fri, 14 Feb 2025 20:33:37 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857b65be10ec729141af2740e90c6193ce5757b64b7742785404f69b4b062f7b`  
		Last Modified: Fri, 14 Feb 2025 20:33:39 GMT  
		Size: 19.4 MB (19444741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f9e5ca03f3c5467b593291b03f0ebda3b32d7e2b9d30717afa3e84cdde9f91`  
		Last Modified: Fri, 14 Feb 2025 20:33:38 GMT  
		Size: 20.2 MB (20234564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a3248c1796ea6f26d156412ac29e5bdee9d47b8b720c04eb3e4e6c5edd4782`  
		Last Modified: Fri, 14 Feb 2025 20:33:39 GMT  
		Size: 20.9 MB (20907747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6026842cca59a3c73fa816ca68df16d7a6114a429b45f10f39af4bd7e4dec1`  
		Last Modified: Fri, 14 Feb 2025 20:33:37 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbc5f088e0f68fba9d84127f6e0b7d10fb1e71eece7875528076bb9382af499`  
		Last Modified: Fri, 14 Feb 2025 20:33:37 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57dc8df5ac608303039ac1d2f20837086a10260f92fd975923ff3d461ac0ebdf`  
		Last Modified: Fri, 14 Feb 2025 20:33:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94aad3b2fba92c6d9a73265b2589c87df27d3ac42840762f5562a9c84b7cd36d`  
		Last Modified: Fri, 14 Feb 2025 21:11:20 GMT  
		Size: 6.7 MB (6733053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8ab0f4516dcb85dcbbe1e3b4b364298439434db7b0d8e4a64b2cd835956a2a`  
		Last Modified: Fri, 14 Feb 2025 21:11:19 GMT  
		Size: 90.3 KB (90315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af382f40c3777c4493c5c499c14be75a084e7d160248a27eaf80e4c25cb025a`  
		Last Modified: Fri, 14 Feb 2025 21:11:18 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38585cc4a3e2ff193416e3d9d9725f3b71ad35f0d0bbb9076051271921f934da`  
		Last Modified: Fri, 14 Feb 2025 21:11:47 GMT  
		Size: 59.7 MB (59741664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcda7163a31c4ceb0e2cb2106d6be2b2d4aba8e76b4a9e5a92fa61b4c84916b5`  
		Last Modified: Fri, 14 Feb 2025 21:11:18 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cbfeabb7418da534dd01d8c3c0fec0491138b4295ea4b46fcd73e29549a79b`  
		Last Modified: Fri, 14 Feb 2025 21:11:18 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f91be4cb635feb64f76160963dff5077f6b18350fbd4ebb90dcfa95389170708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc39a1b86999bc9f45559a5194fb59a85518b49b7dcc0677fe2a7bc135135f4`

```dockerfile
```

-	Layers:
	-	`sha256:f66a5a1b1803fd132ae622390a2ad435e3a1330fff4ac3bdd78cdd9587c7967e`  
		Last Modified: Sat, 15 Feb 2025 00:07:54 GMT  
		Size: 34.1 KB (34115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:56e7f6c2551b7068d193cac13b2cde9f7647d50530e3a8f97bfe03d8650301fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129599086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8fa928276601047f103dd4e7211cbe25efdfeba766ddd73961fcaacfd335f0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 07 Feb 2025 04:13:48 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
CMD ["/bin/sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_VERSION=28.0.0-rc.1
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 07 Feb 2025 04:13:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
CMD ["sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
VOLUME [/var/lib/docker]
# Fri, 07 Feb 2025 04:13:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 07 Feb 2025 04:13:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
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
	-	`sha256:171679689122707fe19397032a878d491bfcfad986744885498ee08ac587b4fc`  
		Last Modified: Fri, 14 Feb 2025 21:08:06 GMT  
		Size: 17.4 MB (17424031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2826ff935891ee53c869e92f4c107b0097ae169b0da44b7004548eb12661cda6`  
		Last Modified: Fri, 14 Feb 2025 21:08:06 GMT  
		Size: 18.8 MB (18843694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40468d3b59ca0c74759913883e18185c1d9da8a76ce4422dd3a60027d43eefc`  
		Last Modified: Fri, 14 Feb 2025 21:08:06 GMT  
		Size: 19.7 MB (19668790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0808deedc16b57272022856065134df09e227ab4764b27366159bd23fd8981cd`  
		Last Modified: Fri, 14 Feb 2025 21:08:05 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60d220c416e9499f6168d995fbfdc13bc5fcf933977883c01bcdb34b28cbf98`  
		Last Modified: Fri, 14 Feb 2025 21:08:05 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1111fab408a7e8d22aef8aafda55651bf5ab7822b020efb4438bbfc4c2563b70`  
		Last Modified: Fri, 14 Feb 2025 21:08:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe56c4a7bff477619ae7e786b376ba533b99c8b591d3883bc3c31f3597d3ff6`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 7.0 MB (7036895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802bff9ecd999e54f40b4427fa48768459b673e357381cbe3ca3cd4a68d962f7`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 89.9 KB (89857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a352d0cae19490c502d61a9aed7ef9d3092498604ce52b4cb00ea1f9f9bd87`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a3d40acbb7ac20a0cdf0b55a5b28d80f5e663d2f954bb0628d086c22482756`  
		Last Modified: Sat, 15 Feb 2025 12:08:04 GMT  
		Size: 55.2 MB (55184883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce05691e570f5d94cf6b41cf23414fcae1eee152bdc4c510f367f53af5d230a6`  
		Last Modified: Sat, 15 Feb 2025 12:08:01 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787dbd1bb8538b29301a5c980524126d68624b17075f223356bfbbbad7b87e01`  
		Last Modified: Sat, 15 Feb 2025 10:11:20 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f5e42e1a48e0d3597c6a57fee5ca10cccb424ff5799508aff665cd0767d59192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ad7b7b6270bc98464bd7ff85710dc899793b8b8d1470d9e246a8235d506a3a`

```dockerfile
```

-	Layers:
	-	`sha256:2c603a2eaea0277898a2dac38586cec8df602c1d105d0ee1e810dac492785bb9`  
		Last Modified: Sat, 15 Feb 2025 12:07:48 GMT  
		Size: 34.3 KB (34275 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:7d91b6f6bf4e2d6feb37b7cd1d82746d9c66bd1fbce5cf4bae1f457187cffe8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129851686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c526d7aed857203c4d76780f55b06587d443023dc98763b923296629194b0161`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_VERSION=28.0.0-rc.1
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 07 Feb 2025 04:13:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
CMD ["sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
VOLUME [/var/lib/docker]
# Fri, 07 Feb 2025 04:13:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 07 Feb 2025 04:13:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
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
	-	`sha256:458ad08ad12636797c7129fccadc772837f910e3dc25d25d2b4cfbd0b449b91a`  
		Last Modified: Thu, 13 Feb 2025 03:09:15 GMT  
		Size: 17.4 MB (17408946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac622654f4ae53b6073171a260c6a3fe7a5d47cdc3ae14d46c7e6d77ef32e4c`  
		Last Modified: Thu, 13 Feb 2025 03:09:16 GMT  
		Size: 18.8 MB (18827819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9679dc79c660b44dc8680566f60440a54ce5ac322ee40c40fd75cbe6924cb3`  
		Last Modified: Thu, 13 Feb 2025 03:09:15 GMT  
		Size: 19.7 MB (19655165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9aefc40ff8d856638d021e7bb1259de6ad3b9f2cdea5f28c984101a867d4c0f`  
		Last Modified: Thu, 13 Feb 2025 03:09:15 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a069c1a3b3b96b345a2efb664a8aab915ca7022f6691730d8448af81ae3fd0af`  
		Last Modified: Thu, 13 Feb 2025 03:09:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc07eb74c1b2e476a89d9c2b2e7279a0dfbc88e085037b453a04ca84499ffb4`  
		Last Modified: Thu, 13 Feb 2025 03:09:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f9b6805c37489e91de5e1eaeb25bb32e1fd444705439a9fad1270362e81a37`  
		Last Modified: Thu, 13 Feb 2025 03:09:16 GMT  
		Size: 8.3 MB (8288342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699a99598cd701dc039b2141bb14bb26088e7b3ae8cd4b0673859bd6ef4c7cb0`  
		Last Modified: Thu, 13 Feb 2025 03:09:15 GMT  
		Size: 86.3 KB (86339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b43d61879623a9a9ed4076fc125aa9ba9f823b18c20df3baf5b02f2dcf5fd9`  
		Last Modified: Thu, 13 Feb 2025 03:09:15 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e5c8b3c5834e2129d7710f43dcdef6cf0719b1f9f08ff58c9f3a27944f302`  
		Last Modified: Thu, 13 Feb 2025 03:09:19 GMT  
		Size: 55.2 MB (55184871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8751a84fb6aa303fbb6820032b54db6c4226e2d46bfc7f3893c5b58b0b9b01d7`  
		Last Modified: Thu, 13 Feb 2025 03:09:16 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c6ce1594f61ecbc47112eafa494d7f72e32014c9a1557bc025257d744f5c37`  
		Last Modified: Thu, 13 Feb 2025 03:09:16 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0dac2bf3ea852cb42ca0ac8f5d6879031da09bff583aa0b1e64bdb1b37802b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab6d62980aea92062111d1da056c531bd05354c677d6673eb13f5d3bbcb81a1`

```dockerfile
```

-	Layers:
	-	`sha256:825204a655bdb9ea2cd62ca7e383a9358b086c165120fa0d9acb724b7f801b53`  
		Last Modified: Thu, 13 Feb 2025 03:08:52 GMT  
		Size: 34.3 KB (34274 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ba619de5f3ce4863927560da589da39c90b6b774a73069c5d2b2e0870f22f27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 MB (130320030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320a42925d8ed5942528250731c9c7e9e0a056d0a8f465ac3697356d7727f00c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 07 Feb 2025 04:13:48 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
CMD ["/bin/sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_VERSION=28.0.0-rc.1
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 07 Feb 2025 04:13:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
CMD ["sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
VOLUME [/var/lib/docker]
# Fri, 07 Feb 2025 04:13:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 07 Feb 2025 04:13:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 07 Feb 2025 04:13:48 GMT
CMD []
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50887e50e270549022e43bbe2d87cd10c6751abd660cb697b26af1b6d7aeaf4e`  
		Last Modified: Sat, 15 Feb 2025 00:08:27 GMT  
		Size: 8.1 MB (8076016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562f2bdd61397238b16334e14bd180796e14ad906cb36e6a14d2bb78ba432d38`  
		Last Modified: Sat, 15 Feb 2025 00:08:26 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a1661da180701a5a463f67f71c321a8d6b3dffe1af1ac0828e5806e1edf0d7`  
		Last Modified: Sat, 15 Feb 2025 00:08:59 GMT  
		Size: 18.4 MB (18369004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727cdde652a623b332bd62c07995c33ccb5a8dd3a5109d48322d99afa507c4ab`  
		Last Modified: Sat, 15 Feb 2025 00:09:00 GMT  
		Size: 18.5 MB (18457779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9fadb3cacbcfb2db66294433f44aeef8eda945f8492bba5a4f29fc38bc125`  
		Last Modified: Sat, 15 Feb 2025 00:08:59 GMT  
		Size: 19.2 MB (19175085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975c230b5e5bee299c9fa8fe9f5fe3b85b201a3dc0807cb30c5b2a7398365770`  
		Last Modified: Sat, 15 Feb 2025 00:08:58 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e2e8fda9062d9389dd0f617718dae9ff3728522275258aa21ebd1fb041659d`  
		Last Modified: Sat, 15 Feb 2025 00:08:58 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce96bc1ddecf73924493365953ee9561bacb941aed33b448674f233234d9a0f0`  
		Last Modified: Sat, 15 Feb 2025 00:08:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e470a8d01c310c79198adbfc5be3a9623a9cb2f4dc1aa7078a4c49c2a0a6b0`  
		Last Modified: Sat, 15 Feb 2025 09:07:51 GMT  
		Size: 7.0 MB (6978852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d462d5148c0875780539fde124c1f2e80e67c681be2f32fca7e13050003b24ce`  
		Last Modified: Sat, 15 Feb 2025 09:07:50 GMT  
		Size: 99.4 KB (99374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d76b74ced37c3d51affd69460bce31255b55e6dcce4642f2eff84edd7b065`  
		Last Modified: Sat, 15 Feb 2025 09:07:50 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcd19b4c76601e5dee3ba77d1a443c310197caaa9e5bcba59a33f70e246c440`  
		Last Modified: Sat, 15 Feb 2025 09:07:52 GMT  
		Size: 55.2 MB (55162828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e66bdaefa44fac1faff32561790cdc9ef25e52ddbc05729f853b3a46a84601`  
		Last Modified: Sat, 15 Feb 2025 09:07:50 GMT  
		Size: 1.6 KB (1638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5037ae12d31449a67e37241e14714309fb661ed82c1e1b1d0f68b6f1ad34ac`  
		Last Modified: Sat, 15 Feb 2025 09:07:51 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0cfe7aa6a25106756df14aad233902c5a82a51f694adaeb5c7dfa918e5c4cd09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5218f5dedda5b4d0eecb8f230ae60ffed970a526624f9f2cc7f1f99c4df7f35`

```dockerfile
```

-	Layers:
	-	`sha256:f777ee4f5035d08f55e26c0b95354ff9e7f377d05438bc5e96258cf76c595f97`  
		Last Modified: Sat, 15 Feb 2025 09:07:44 GMT  
		Size: 34.3 KB (34327 bytes)  
		MIME: application/vnd.in-toto+json
