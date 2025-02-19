## `docker:rc-dind`

```console
$ docker pull docker@sha256:8943debd2128a515289ceda86ac156b80c3931476f58e46c0be82fdb95410092
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

### `docker:rc-dind` - linux; amd64

```console
$ docker pull docker@sha256:08bcd439b366649ed4b8e8dc1db53a6fa77d61e4c2e4fc8f2752efa97b7fa49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139358747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55033351a734265f70c9e1d2b659aefd2e26b4d25faf0beebdb514a67c275f06`
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

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:19b95af73fd6ac571639499c4a0201a871896a18388fdbab8d0d224f3b274a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 KB (34115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001e2a6cfee9aef78aa3f2d9cf3640e316d52dcdef8976d8238b6cd3dc4feb29`

```dockerfile
```

-	Layers:
	-	`sha256:2f20e39e75ab114fedcc8c0cc2c80153a02c42903dbc8a8e8d4b80f7551b5166`  
		Last Modified: Wed, 19 Feb 2025 03:07:46 GMT  
		Size: 34.1 KB (34115 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:64ddbeefb1b86639e5306ea43d8101c8360c90b5323d4c331429c5fbf8c48ea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130030003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b44b698fe802834edb99fc4757fc9c59e9b76b690ea5a8f18123a218859ef9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:d7234d68f7ac48b328abd770e95c263a85df857966e29b1c7ecd562c490aa85a`  
		Last Modified: Wed, 19 Feb 2025 00:37:21 GMT  
		Size: 17.5 MB (17454267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dcbe088185e6cd718e24f0a6e2584b56dc730f4d4a43bfa7c6d9da656e600f`  
		Last Modified: Wed, 19 Feb 2025 00:37:22 GMT  
		Size: 18.8 MB (18843692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc5e484303066f1c368873ab8b295e103d9a4634233dff6a0d56e18331934b9`  
		Last Modified: Wed, 19 Feb 2025 00:37:21 GMT  
		Size: 19.7 MB (19668787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa69456ebc2118910f258da3b5ebe3f4d05054780a9061b53f5d5b116a4b0ec`  
		Last Modified: Wed, 19 Feb 2025 00:37:08 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd078a4c3f7ce6ae8a1992bbce74fa94727fe67766cda41c017a3101614875af`  
		Last Modified: Wed, 19 Feb 2025 00:37:08 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bfc57c40f2201bf2ede08c6659a3549ab75f809e84d020b75a5aefec1b7ada`  
		Last Modified: Wed, 19 Feb 2025 00:37:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b243dc28e77c5f535895fc648d0182091a218aae7092b1e70cd0dffeb463d614`  
		Last Modified: Wed, 19 Feb 2025 01:08:06 GMT  
		Size: 7.0 MB (7036922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5127696f17ca5098cd061c2f0c70d83e5d94de7ac4ace7c8573f1e4b26b9c2cf`  
		Last Modified: Wed, 19 Feb 2025 01:08:05 GMT  
		Size: 89.9 KB (89859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a203f23f0ca263112e2f3d77fb7567b6854191c440ba4ce38c728c5f1e82ff`  
		Last Modified: Wed, 19 Feb 2025 01:08:04 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a489e832fac8bb0a59b81b125030512e61c972dea975ac8764528193dea60a76`  
		Last Modified: Wed, 19 Feb 2025 01:08:23 GMT  
		Size: 55.6 MB (55585541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1fc5ec21bf05af4c67e9a3e3f95fa17cffae04891597f8114bc87c6bb8006b`  
		Last Modified: Wed, 19 Feb 2025 01:08:05 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dde3c115e1215dbbc4909422480e4ca8bb795e85a5ada68e68a0be398df089a`  
		Last Modified: Wed, 19 Feb 2025 01:08:06 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ad2b3a3949a09e8b2eb2166182333289cbe680d89f617dc140852e1d7f21d969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28834508abca65b54d5bda06373d67ca494f75adf5e15b9f4c6ec0dd38fd66be`

```dockerfile
```

-	Layers:
	-	`sha256:08bd5e87fb3b497fb9e67e2f08642ca9bcd46d0738ab53ef35960fd0a9685327`  
		Last Modified: Wed, 19 Feb 2025 03:07:47 GMT  
		Size: 34.3 KB (34275 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:1861960678e34c0011b1609bd052c3b87e86cdb41425ab16cd568e7ce2fd222e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128371452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c83d8334ba5d399c9c7adc1ccc5bbd58ca29d85928f66ec6a2bbf6254750dbf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afc7bee112990bef2a515fbc55be504e50544ea48db6d66a8c03f6e5a0beb99`  
		Last Modified: Wed, 19 Feb 2025 00:32:22 GMT  
		Size: 7.3 MB (7299510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9a3e868f911d9326457475962e0b02b2f3531a0be73bf92021c8d086c95a38`  
		Last Modified: Wed, 19 Feb 2025 00:32:11 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4a32e85d1fe7ed454f391c5833ff087c4772262b0b91cd112d88b1a09cae86`  
		Last Modified: Wed, 19 Feb 2025 00:32:15 GMT  
		Size: 17.4 MB (17444624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cf8d22453e0f4351b939a048b50b75422f80a11c750c7330cafd77f1ecf903`  
		Last Modified: Wed, 19 Feb 2025 00:32:26 GMT  
		Size: 18.8 MB (18827826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd84372de4aaefc1e6a17de2678725d39594832f8f6d9b3b94f265910742afc`  
		Last Modified: Wed, 19 Feb 2025 00:32:16 GMT  
		Size: 19.7 MB (19655160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa87100299182d8b312b811f83b17c9e57851a234edfbc6b4f12b35f7263832e`  
		Last Modified: Wed, 19 Feb 2025 00:32:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b351cba7a96343e64e98de78d387f4122bbdf8824ba85b2e84a3142289481038`  
		Last Modified: Wed, 19 Feb 2025 00:32:13 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33ced1bec23a621bf77bfc77634ae4430f5eb2df8caef974b8bb2c332ce2cdc`  
		Last Modified: Wed, 19 Feb 2025 00:32:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e1984a56969a43e847edf80a06e71c5df588390fe55b4b3f89c243fc373f7c`  
		Last Modified: Wed, 19 Feb 2025 01:35:52 GMT  
		Size: 6.4 MB (6366288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b02a44c51bd608d74a88d5c1fa7fe14d7cb1fb15c7879e730a4ca06b36b4308`  
		Last Modified: Wed, 19 Feb 2025 01:35:43 GMT  
		Size: 86.3 KB (86341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1161e91aa5143b524653583983f9bb1a0a68b0157e91b0888d72d4ac3472df08`  
		Last Modified: Wed, 19 Feb 2025 01:35:42 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2d01d21e1f2f4a6e851cdf3c684c3c80977bf26f98963073fcac7434b0e975`  
		Last Modified: Wed, 19 Feb 2025 01:36:00 GMT  
		Size: 55.6 MB (55585522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d200ed47d55ac087c1ce4dbdd3fe16b57a7a6ee1449fc3f9860220d34a74c8`  
		Last Modified: Wed, 19 Feb 2025 01:35:41 GMT  
		Size: 1.6 KB (1639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75521b3548b62e6eacb9900ba1e55cc223e1636e424cc5b0c189aaa1d191e734`  
		Last Modified: Wed, 19 Feb 2025 01:35:41 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6e4dda6906520c4ba27c1fbf978da613cbf50ff31d631abe6b7a4dd06c319113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bddf01f9da92ae80affcd401a80791a810db662dfb7d2a0194abf9826a1ea1`

```dockerfile
```

-	Layers:
	-	`sha256:9c098d990f7536c692f7b7481914696c84e63b4da1e9b1ba86260f81f06c8e9f`  
		Last Modified: Wed, 19 Feb 2025 03:07:49 GMT  
		Size: 34.3 KB (34274 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bd4de34ae7dd35f3e6a8295f6be4bd044e0bb06e03fa2c447ae860c2769cc71e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130760579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4a543b051d017b52063b53631db33f293b215edd101187f0c9d5609e0a5016`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6b21c65895ab4ccb4535e6f2a459798fec69f7ca32c2906eb483dba6b27e3e`  
		Last Modified: Wed, 19 Feb 2025 00:35:00 GMT  
		Size: 8.1 MB (8076408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49fc72f06f50b6f6fe90c7a889f45f4d351146aefa3b48cb82f6365ad1f30e0`  
		Last Modified: Wed, 19 Feb 2025 00:34:57 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469a2cfbab6a4a4f2c13b4f7817c53516791aaa912e5468c1cbb6e0c25910bd0`  
		Last Modified: Wed, 19 Feb 2025 00:35:01 GMT  
		Size: 18.4 MB (18414061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e5d21c3706301dada42c817a4d0c407cbf365ef45e22323b2ec2f161a20dd5`  
		Last Modified: Wed, 19 Feb 2025 00:35:00 GMT  
		Size: 18.5 MB (18457791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e23d261bfaa3f79a809d2698360893da1db9cd4ba7004ea26bf2b333472b11a`  
		Last Modified: Wed, 19 Feb 2025 00:35:11 GMT  
		Size: 19.2 MB (19175083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67b98d3173a83b7439eae2d8558969e63b5823710402da93350109a5142671f`  
		Last Modified: Wed, 19 Feb 2025 00:34:57 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e464a5572291458a52151139b4abb735e42ae46bae14d9f364b1eb71a9422589`  
		Last Modified: Wed, 19 Feb 2025 00:34:57 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259601177f443e3b079bc67d8bfe36b915823dd4dec287a35a5192c3bc303e39`  
		Last Modified: Wed, 19 Feb 2025 00:34:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ce5aa086d9a8b3a85bc1bd66537f8565fde69a246366da1e24efaf6624426f`  
		Last Modified: Wed, 19 Feb 2025 01:24:47 GMT  
		Size: 7.0 MB (6978852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c328031e43d8d46a46ed7c77fa7ec760f6410194db2b186a67e8b2ad5641db92`  
		Last Modified: Wed, 19 Feb 2025 01:24:37 GMT  
		Size: 99.4 KB (99383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1d83a9c867396b6aeac8233a9aa5462939425bb89cccc067e619c0f2da9dba`  
		Last Modified: Wed, 19 Feb 2025 01:24:37 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31596fbd1101167676453e187803f031c6a00f22cb9b12a545c25136ab18381`  
		Last Modified: Wed, 19 Feb 2025 01:24:57 GMT  
		Size: 55.6 MB (55557907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49642f9890ffbc0300314835d5e51d1dbbb5b51992fef12006f2d60ca8bba210`  
		Last Modified: Wed, 19 Feb 2025 01:24:38 GMT  
		Size: 1.6 KB (1640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1b47b312c214a39bad47264c953ec6fe175d921f9ef8505c73bc158dcd719c`  
		Last Modified: Wed, 19 Feb 2025 01:24:37 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4c77335f6c5fe5d731228dc48d80f0596609c612fd8e084b9690b282b489ee05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4891128c1e9fec4d3042a8358bd5be612b437867931f73e0a98f774b7914c23b`

```dockerfile
```

-	Layers:
	-	`sha256:813af08b799fb1bbb4ca28c7368020c4821739a87941a14c2886c263b93ea2ee`  
		Last Modified: Wed, 19 Feb 2025 03:07:50 GMT  
		Size: 34.3 KB (34327 bytes)  
		MIME: application/vnd.in-toto+json
