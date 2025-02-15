## `docker:28-rc-dind-rootless`

```console
$ docker pull docker@sha256:8560f471ba75b7cb7c5b3b6fde89ed3aa378966917e914561e11c3917112a66f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:b3d7c051ef6058c0fedefe7266785543848cd7d7334e707d9ad9cdd8f2ab5791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157019267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42863e3cc7f19f5bc5e23c191554b9ee975d708884d9369a2c1c027b52b0967b`
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
	-	`sha256:b701fec4c57f9c75a20a417853cc77dd51d4864986142029b49edd6422a6d1cc`  
		Last Modified: Sat, 15 Feb 2025 00:09:14 GMT  
		Size: 986.6 KB (986581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7021e66d98608cf2bbc06cd4abd11627be1bc6651869f11d7b5e3928a333c563`  
		Last Modified: Sat, 15 Feb 2025 00:09:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40944f0f831d4272eded0d6285694971e1baa98502924aabc3172a2809732d66`  
		Last Modified: Sat, 15 Feb 2025 00:09:14 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276fe157491954f6398cfff5f0e21c5a15e4e1307ffb1a82085732db77dd264a`  
		Last Modified: Sat, 15 Feb 2025 00:09:16 GMT  
		Size: 17.2 MB (17166412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f457dea6caa02968d6881e37e44f26b322a74cce32e018c82edb89f68107dcc0`  
		Last Modified: Sat, 15 Feb 2025 00:09:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b6e69783d4e2ea54f04a9f0a5af5f1e0d7f9bd538fbf67808e542e49213aab87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b391155b8612a285ad976a5c731396e262731c9cf9f10be37be8906db8c2a1`

```dockerfile
```

-	Layers:
	-	`sha256:cf764ec5091bab4d1387c071931fc66ac55ee84c438e55896cfbb5df3f605e68`  
		Last Modified: Sat, 15 Feb 2025 00:08:02 GMT  
		Size: 30.2 KB (30202 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f48d6758bbddeca7f749d87d79b553c70dfe1b6a57a4d95e893adcdc1fdad7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153339817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4f4b26966a04bf0990090c6a3240ea0bac9358e151bf302b187f3da655a576`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:396bec15c76c7e51e1061c2e62f9929ecd9547daeba6b1f149a4f391921becd7`  
		Last Modified: Thu, 13 Feb 2025 00:35:14 GMT  
		Size: 18.4 MB (18369015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6e9330692cc4894c3cc45e11a5a8e17407e9b824046776a7d6ffb60a987b29`  
		Last Modified: Thu, 13 Feb 2025 00:35:06 GMT  
		Size: 18.5 MB (18457790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4a379673b221c7053d63005faba4996ce10b3535f7ad3509cec1a23b5d2222`  
		Last Modified: Thu, 13 Feb 2025 00:35:07 GMT  
		Size: 19.2 MB (19175079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ec5604f91cfe0128dc20eb63369af2d273e106a4ccd44ec8179b3ef0110896`  
		Last Modified: Thu, 13 Feb 2025 00:35:05 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dbae713a1de92db26094a86c3823e3714fe276d00fc23ef97093048aca09ef`  
		Last Modified: Thu, 13 Feb 2025 00:35:05 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c7fd5455bf9e7e805439ffdaa0331ff62b66f5e4ca8f103586f6ec3698d077`  
		Last Modified: Thu, 13 Feb 2025 00:35:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab48fc63bdfba44be0d25b56295b12cdc5bf82c5859c3432e2d44449c84dd8f`  
		Last Modified: Thu, 13 Feb 2025 01:07:55 GMT  
		Size: 9.7 MB (9705879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5552461e4146b5bc3c0c5ba1b152f8037600a8a1e797c53d8ddcbc66cf2dd58`  
		Last Modified: Thu, 13 Feb 2025 01:07:54 GMT  
		Size: 99.4 KB (99391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b172f8aae2f50b8aeb0c039dc71f8291a1ea11a9e15dc07a3a38890fb2c42b`  
		Last Modified: Thu, 13 Feb 2025 01:07:54 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd2fa83fe613ae38d8fc35bcb5fc13a0f1e3ab535161c21617367748fab9463`  
		Last Modified: Thu, 13 Feb 2025 01:07:57 GMT  
		Size: 55.2 MB (55162845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4060dcc9cb63122e2f9e80fd43bb5609b3c444a53c4e96b43075751fd7b496`  
		Last Modified: Thu, 13 Feb 2025 01:07:54 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aca2f5c7b6cad156f43b8010865665809e3c3030e22b896f2692872506ab847`  
		Last Modified: Thu, 13 Feb 2025 01:07:54 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d221656e06327fd2908f3dc61af06bb7d4f5ff9293f6fa76ff2c0ea9fcf02dfc`  
		Last Modified: Thu, 13 Feb 2025 03:09:56 GMT  
		Size: 1.0 MB (1014207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084524959625a302c01b29c645f1108f7ea9c193fefb8dc48cab1460aa58b3ff`  
		Last Modified: Thu, 13 Feb 2025 03:09:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dd862efccaa826aadc043f2eedd1739074adfc684689615abd988123157790`  
		Last Modified: Thu, 13 Feb 2025 03:09:56 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8ab9476e4c0053dab9bb00b464a56afe04fbec71a55c16616aa8646c64dbd2`  
		Last Modified: Thu, 13 Feb 2025 03:09:58 GMT  
		Size: 19.3 MB (19279442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92d44e917e8ac2a4e8c7329a043d8bf9f20909a38e12d400b869db1cf5254f6`  
		Last Modified: Thu, 13 Feb 2025 03:09:56 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:418f55fc9cdde6d14168b2cc352a9dabe6aa15178b9e1114dee812e329ec00c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f131ba5a8542aa2946063ea6faff22ebc986a73f6eefa412002c72cd5a5229e`

```dockerfile
```

-	Layers:
	-	`sha256:eebb5b3c491302177f6befd51f635addbc459d9fca0c390887fd792b09a11c60`  
		Last Modified: Thu, 13 Feb 2025 03:09:12 GMT  
		Size: 30.4 KB (30361 bytes)  
		MIME: application/vnd.in-toto+json
