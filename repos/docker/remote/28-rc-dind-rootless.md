## `docker:28-rc-dind-rootless`

```console
$ docker pull docker@sha256:77270ab977167a6cea4b2eb3bef7842fcdc3a2cf98526f7125104cb13df5b36c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6c71e363f4e312eff57c56dce6758dd5c246152d4850eae958517928033dcfdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159430081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ef9da908b9979050af01bf0f5fc709a3ea0c362f5837e5f8bbe64a1d82f299`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9802149262e7c48c0d713d6287afc4c4acb2fbaae8e954e40710f85e3e4653`  
		Last Modified: Thu, 13 Feb 2025 00:27:23 GMT  
		Size: 8.1 MB (8059995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a47cfcdae555df6d18b31aa64d0a334a2f657a57816ce0fe3c14e723380047d`  
		Last Modified: Thu, 13 Feb 2025 00:27:22 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80441eff69ae0c6455a6f271f554b8f0fbc4d4847336877c0e4b4cc1d118e50f`  
		Last Modified: Thu, 13 Feb 2025 00:27:23 GMT  
		Size: 19.4 MB (19444750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5b7dfea4097947c1d0b446d5360ea7f9cbd56263473960b08626a7e895eec6`  
		Last Modified: Thu, 13 Feb 2025 00:27:23 GMT  
		Size: 20.2 MB (20234558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e04eacffa3e71f76e9963503b015e4ff78b2cbfb460dfc79f3c8f4c81baabd`  
		Last Modified: Thu, 13 Feb 2025 00:27:23 GMT  
		Size: 20.9 MB (20907773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f08514eb4d929a96ff26f9393cd415417991dd4fa236519f16ea741193cfac4`  
		Last Modified: Thu, 13 Feb 2025 00:27:22 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0012c73f5b8ea9fa020d64345284c89d82bd4572e40aa8a3c32f5680faa9edf3`  
		Last Modified: Thu, 13 Feb 2025 00:27:22 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88dad8827682b0ba13e138c5691524822beee922d3327e81be7eb7bef6cb9106`  
		Last Modified: Thu, 13 Feb 2025 00:27:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3eb103451025f9ed735414e11531e9d95151ec2852a0dd208a9c27be226f0a6`  
		Last Modified: Thu, 13 Feb 2025 00:28:20 GMT  
		Size: 9.1 MB (9146903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0fc31cab378ae332c2e5264f205863146d32e11d844304371359340c692045`  
		Last Modified: Thu, 13 Feb 2025 00:28:20 GMT  
		Size: 90.3 KB (90326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702442469b1a59bc5f0397d0a1b0b97c31eec8305e253d57c5aea1d2fa8620c2`  
		Last Modified: Thu, 13 Feb 2025 00:28:20 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a21811d6f7e3a209357c5b2dd02088b17b59158c5d0aacd9e5b563853d57ef`  
		Last Modified: Thu, 13 Feb 2025 00:28:24 GMT  
		Size: 59.7 MB (59741642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4215f905b3d632e2cb269c293ba9ed547dab804b06a4cec7368da69c96cfb7cf`  
		Last Modified: Thu, 13 Feb 2025 00:28:20 GMT  
		Size: 1.6 KB (1636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6fc16656ab994ef8f37804092cce182bd9171089f72174ea7475b05b04effb`  
		Last Modified: Thu, 13 Feb 2025 00:28:20 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9cc815fb002f132b49c77d8606e17d96a1c1b285e1d42a5b25f590b240fd90`  
		Last Modified: Thu, 13 Feb 2025 03:09:56 GMT  
		Size: 986.6 KB (986603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7754dd24e7433d051a861b398a2b9dc8137fb6f79576b6cc627bf335499cc3d`  
		Last Modified: Thu, 13 Feb 2025 03:09:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfa5b04e19928b6eff67a43f8daec89b337e1da3a593f311758cbb91b07b5dc`  
		Last Modified: Thu, 13 Feb 2025 03:09:56 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ce6f2dbfd9a7eb233e8afff2dc238a9553a1b59a4980e772441ef7ef8b8d63`  
		Last Modified: Thu, 13 Feb 2025 03:09:57 GMT  
		Size: 17.2 MB (17166405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f95ab80b9fe1b617dcc5c2e2d7118e7f6e07bbdc4829da2c6a98696b90ea7d`  
		Last Modified: Thu, 13 Feb 2025 03:09:56 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:bfe64332b53f8ccbe09d091d67eb9d2dcf3926d16e6fd256dd65be3f23954613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d3aa804aa5a6a3325ab47ec6d2be856dfbef3589f481302230adfe672246a8`

```dockerfile
```

-	Layers:
	-	`sha256:37ab2ff7e0bf3bbfa653bee7d26b54fd85c9e018e3b15be9239c73bcefbd64e2`  
		Last Modified: Thu, 13 Feb 2025 03:09:11 GMT  
		Size: 30.2 KB (30204 bytes)  
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
