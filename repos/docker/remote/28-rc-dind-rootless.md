## `docker:28-rc-dind-rootless`

```console
$ docker pull docker@sha256:6521ddbd2eeb47acbc2f9c02a119b68cbe2ab7f989a85f8987a978a01416fa22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:1b04f38bc5c339d7995de534dd36c9d629d2cba95c6f1f497503a226ac500cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157513065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7148180676889313ffef5e38f7d8fc309f32365b358f06752201ea7259f72e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 18 Feb 2025 12:01:18 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
ENV DOCKER_VERSION=28.0.0-rc.2
# Tue, 18 Feb 2025 12:01:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Tue, 18 Feb 2025 12:01:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-amd64'; 			sha256='8c38f60308a895fa570f1410e453c5de11aafd65a99fa99965d96d24b6225a78'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v6'; 			sha256='ba0929f3389db9c407c23debb7c02faaf5e1d09da48c94905f0759736a39ee2f'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm-v7'; 			sha256='52672d1810f359685c171e85f7c96f71e32aa5f170d7841b32282a8e3ba16fce'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-arm64'; 			sha256='f7d867e9f1a3c00b32dd580f56594e229df05e3fb1b083b7099c91c2e7d2ce1e'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-ppc64le'; 			sha256='7bee10600a6fb9f01cecae11e92e5b5271a732e5641580037b7f74fb84c033ea'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-riscv64'; 			sha256='f4cf6e6a6f27e571e5210cf6324b720c10548b0a0b59e0b1381b43fde0604c65'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.linux-s390x'; 			sha256='93d547dcecaeddd6fe6cc384110b532bf204126ef4ee3aa9ad9765c813a1b809'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Tue, 18 Feb 2025 12:01:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-x86_64'; 			sha256='6395dbb256db6ea28d5c6695bc9bc33866c07ad1c93792f8d85857f1c21c34ee'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv6'; 			sha256='360976f92dbf4b575bb9beb2737952709c685d1441eebd90c7eeb63225a44ada'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-armv7'; 			sha256='69c5e0b8764876ef7521b4274eba470d0d6686d3def74e2ba0c216bf2bf6f077'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-aarch64'; 			sha256='03a42a0fc0614ffc3c9ebca521cab75e02c427b68e45e3f6867d9510b9a28818'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-ppc64le'; 			sha256='3e1c3ba91bbf27c0966ad384a96dbecb867c2cbda4fde929165ca35b99075023'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-riscv64'; 			sha256='dffcdfbc88189a97c0000d1995476fa6712396d1472d6fbe24bfb424f46da7c3'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-linux-s390x'; 			sha256='3f809fd846e3e38bc3dcb88546f88141a68e1bb4578a74c71ed5b563f95a45bb'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 18 Feb 2025 12:01:18 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Feb 2025 12:01:18 GMT
CMD ["sh"]
# Tue, 18 Feb 2025 12:01:18 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
ENV DIND_COMMIT=c43aa0b6aa7c88343f0951ba9a39c69aa51c54ef
# Tue, 18 Feb 2025 12:01:18 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
VOLUME [/var/lib/docker]
# Tue, 18 Feb 2025 12:01:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 18 Feb 2025 12:01:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 18 Feb 2025 12:01:18 GMT
CMD []
# Tue, 18 Feb 2025 12:01:18 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 18 Feb 2025 12:01:18 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 18 Feb 2025 12:01:18 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2649636f38474ef7c9d2d4bb81667f7177feea6afa91e4dab1cc7d87d9fb78c8`  
		Last Modified: Wed, 19 Feb 2025 00:28:56 GMT  
		Size: 8.1 MB (8062992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f364872f3a0fa3902131d4bd2e503554e3e6da4eb50f1d8cf37a5110b1c0d3ff`  
		Last Modified: Wed, 19 Feb 2025 00:28:54 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e85053d918c89ce53f66f614dd06356c6c90d15cd739a6ac60a0a074fdd0b4`  
		Last Modified: Wed, 19 Feb 2025 00:29:08 GMT  
		Size: 19.5 MB (19493501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0558c04c5206c50935ccd70770da39d35ff9785fe08fe349a380653640b85cc3`  
		Last Modified: Wed, 19 Feb 2025 00:28:58 GMT  
		Size: 20.2 MB (20234556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57ab6cbbf564daef1ae1328bbedcd505dd3737c91ce9c7873affac4558fc3ef`  
		Last Modified: Wed, 19 Feb 2025 00:28:59 GMT  
		Size: 20.9 MB (20907747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b19165ff6b0381a0b6ec0b0f180505ba4811df66f1502f951d6589a35d8f6a`  
		Last Modified: Wed, 19 Feb 2025 00:28:56 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5ae00b94126e1d860f4dd7b4180d0a6f34718ed8f16be342ddd202c9df8f42`  
		Last Modified: Wed, 19 Feb 2025 00:28:56 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f679c300d473d397dbdeb1a62de613d2041f0826cf3b4ab0b9eed1d39f182377`  
		Last Modified: Wed, 19 Feb 2025 00:28:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010c31196e2349b0e57cc087ae5e2e5b42e5f277d6106d262dda9a47348a4a61`  
		Last Modified: Wed, 19 Feb 2025 01:08:26 GMT  
		Size: 6.7 MB (6733028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181b3c14aa8822d89e7dfdff9c64c7193b2425571225cc02d4dc9ffd8855490`  
		Last Modified: Wed, 19 Feb 2025 01:08:17 GMT  
		Size: 90.3 KB (90318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed541f7ef267792d6c2f648e26432f4b880d88321bb9b49fac8b37aab179ac56`  
		Last Modified: Wed, 19 Feb 2025 01:08:15 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c968c840cd1eaa89a3fb61ad146a14f7df24c1c7072cd9d5d6d222d9e7d54be`  
		Last Modified: Wed, 19 Feb 2025 01:08:35 GMT  
		Size: 60.2 MB (60186300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904433a26de6274ef41a1e4d4263ee949b538cbf9e767560a9ea1d329861e2d5`  
		Last Modified: Wed, 19 Feb 2025 01:08:16 GMT  
		Size: 1.6 KB (1635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469b392aa7e9c65e25974aa73caf5064d723c2b03839e9de9a2a715ca214ec01`  
		Last Modified: Wed, 19 Feb 2025 01:08:15 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd49cfba6271941dd3580231b051f14e30630cd2cbe5eca100eee7e26a1e18e`  
		Last Modified: Wed, 19 Feb 2025 02:08:17 GMT  
		Size: 986.6 KB (986565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84698651fd63cc4f1e76ece5e86a85f211f1c565dea5b3e448056e03561619c`  
		Last Modified: Wed, 19 Feb 2025 02:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e52b9c20b5b2b7899a24e14154a8004d12ea3d6eea8b4f790ddd5488db09159`  
		Last Modified: Wed, 19 Feb 2025 02:08:17 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b928af76338e19138f55300a804624d4bada9ee2a19d1146ff9b67fa97eda4e8`  
		Last Modified: Wed, 19 Feb 2025 02:08:19 GMT  
		Size: 17.2 MB (17166411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584b789c0763a49b0acfaca3d4e7909c79423ca9877f5d17c725b3658dc9d632`  
		Last Modified: Wed, 19 Feb 2025 02:08:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:32f6e41f80c6d5207c7e4d7cf446e1ffae20fb1a09c92776b1a6e1a4390689b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f25aa2f4996b726deff39fd4c502a68d5f0e844e5020a07cdea504fb7d2f06`

```dockerfile
```

-	Layers:
	-	`sha256:2a0f241d4253e42cdc35abe0aea6a783840cea7f0ba4568d6cc084eeba888e95`  
		Last Modified: Wed, 19 Feb 2025 03:08:29 GMT  
		Size: 30.2 KB (30203 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c83934b9ba0487b82d1db0adfc0de6e061471a9e22e0967832f71ab97f7b810c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150615002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd24749b9319d6fcbbb62d985ffdc200ab3bc696a64df7b732356bdf46df4bb`
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
# Fri, 07 Feb 2025 04:13:48 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 07 Feb 2025 04:13:48 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 07 Feb 2025 04:13:48 GMT
USER rootless
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
	-	`sha256:846b49e6d21626033ee755e5cf093d745273ec807af4591fd34bc8dd192db3bd`  
		Last Modified: Sat, 15 Feb 2025 12:08:04 GMT  
		Size: 1.0 MB (1014197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275b47caeb846ef3ff41e1e0a075eae379906ec19279c017044f8181d76f185a`  
		Last Modified: Sat, 15 Feb 2025 12:08:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496bcc5e652b187ea8188184cda318eb983f3b4c28fbb8da17381d729fa5ca5a`  
		Last Modified: Sat, 15 Feb 2025 12:08:03 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334552dadde5889537f95fe63bc1a672bd276d18a2d47363ca0c2b8a184d0348`  
		Last Modified: Sat, 15 Feb 2025 12:08:05 GMT  
		Size: 19.3 MB (19279434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85244502d3a60326bbee5d6d76e5b4e4b54f31f4e075918b20bb79e2f8f97b1a`  
		Last Modified: Sat, 15 Feb 2025 12:08:04 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2508436a53b37715bf76af1ec75b337fc808468b95955449b3869f648ec88fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370717275c95ea5ee36a86dc9611966911e74bfb6010b49bdc02aa2b518eeb16`

```dockerfile
```

-	Layers:
	-	`sha256:40817456e4c9476b9accc35e4a4adc0484b22e991715694a402525b9cb2a172d`  
		Last Modified: Sat, 15 Feb 2025 12:07:55 GMT  
		Size: 30.4 KB (30361 bytes)  
		MIME: application/vnd.in-toto+json
