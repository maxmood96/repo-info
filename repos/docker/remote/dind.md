## `docker:dind`

```console
$ docker pull docker@sha256:173f284a4299164772a90f52b373e73e087583c0963f1334c9995f190ef6f3f5
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
$ docker pull docker@sha256:64d6ee47ea821c986467199baa162f5ac8cde3f57b719f18e23f3ed7a7444131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136139147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c952beec7a22df0c66c8f92b18d92a0f745b177a83d90221552a516b3fc512a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:28:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 18 Dec 2025 00:28:03 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 18 Dec 2025 00:28:04 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 18 Dec 2025 00:28:06 GMT
ENV DOCKER_VERSION=29.1.3
# Thu, 18 Dec 2025 00:28:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 18 Dec 2025 00:28:06 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 18 Dec 2025 00:28:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 18 Dec 2025 00:28:07 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 18 Dec 2025 00:28:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 18 Dec 2025 00:28:07 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 18 Dec 2025 00:28:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:28:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 18 Dec 2025 00:28:07 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 18 Dec 2025 00:28:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:28:07 GMT
CMD ["sh"]
# Thu, 18 Dec 2025 01:13:35 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 18 Dec 2025 01:13:36 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 18 Dec 2025 01:13:36 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 18 Dec 2025 01:13:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 18 Dec 2025 01:13:39 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 18 Dec 2025 01:13:39 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 18 Dec 2025 01:13:39 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:13:39 GMT
VOLUME [/var/lib/docker]
# Thu, 18 Dec 2025 01:13:39 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 18 Dec 2025 01:13:39 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 18 Dec 2025 01:13:39 GMT
CMD []
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60967c368cc936fb476ef3a4e7bc728367476ce4599b4dee1a6ce26be8163a8c`  
		Last Modified: Thu, 18 Dec 2025 00:28:27 GMT  
		Size: 8.4 MB (8399627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4182487b556a8b3a7d5dc5fc06072ddb1ae7e69834e5cc0e05ca0ab2ed82d3d4`  
		Last Modified: Thu, 18 Dec 2025 00:28:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6d42f9105b02eafbfbd821d90be74c656db2ef9e212d29329fc0cc2e55d68d`  
		Last Modified: Thu, 18 Dec 2025 00:28:31 GMT  
		Size: 18.8 MB (18764414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbe6cf7966eeda8f48bf8d05c56c276c9d0c8ca86ff4f1ba19e3e4f524f4ac2`  
		Last Modified: Thu, 18 Dec 2025 00:28:33 GMT  
		Size: 22.9 MB (22905482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70b25e971bfb83fc31b76ec785742c13300cb85fc6283bbdb72bb6a7b207edd`  
		Last Modified: Thu, 18 Dec 2025 00:28:29 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f6c6dcdb0a8e7094f54184254221f594b1c82664143ad6cdc8c1a6488e230b`  
		Last Modified: Thu, 18 Dec 2025 00:28:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34afd31c21777d47a2696876a3fec3b7d7ae64cb0e9a77dd7f2bbe4fd8af4648`  
		Last Modified: Thu, 18 Dec 2025 00:28:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5f2d166f4744227399e04ef8d05eb64d7540fdafc5587f4405fd355167a709`  
		Last Modified: Thu, 18 Dec 2025 00:28:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0421aaee99894304a285959a963080b710e97dee87d99534e823cd16a8b47150`  
		Last Modified: Thu, 18 Dec 2025 01:13:59 GMT  
		Size: 6.9 MB (6933816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17299ef6372ab7ac260d9f94a937470eb2a87a0e22ab2b0daf8643c3e6480719`  
		Last Modified: Thu, 18 Dec 2025 01:13:58 GMT  
		Size: 92.5 KB (92456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337839097e518a63b1a7f4e024766c0ff0d750702a90f4f24a1b3cf50a81bd29`  
		Last Modified: Thu, 18 Dec 2025 01:13:58 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4a51af4bc4a8c84ac8bd32f61c5e9492b3b9736f1984843d1b59bf1d0a332b`  
		Last Modified: Thu, 18 Dec 2025 01:14:09 GMT  
		Size: 64.4 MB (64390654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004e2a39ddc1fa0f42e8f5847bd2894897755a571d12ce578b420939301a1e7`  
		Last Modified: Thu, 18 Dec 2025 01:13:58 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e034e54760505eb95b14294e510de1ed8b9689cc9c96c96277fc3c202d2c89c`  
		Last Modified: Thu, 18 Dec 2025 01:13:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:37f1f6ee87caf10b3f970712958dcd87372a94ccd1b70675c80faa2f33ff2155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5764c926d9131cb9aefd3bef17542d4c15d9fc7802f5c49f0599e662c0d40885`

```dockerfile
```

-	Layers:
	-	`sha256:1c12481c19a820b40095607b49e8eae24e9a57d63569019734dcfeef056f4e56`  
		Last Modified: Thu, 18 Dec 2025 03:07:33 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:3deb7c7e1b22d5e6ed0c8c4c69da6daf0f16c136bbbf50b2d5abc5eb2548eff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128370462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcb85689a625bc9af16285fa4fabb8883c1b5efc7a3c585150de8668bb5ec63`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:28:25 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 18 Dec 2025 00:28:25 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 18 Dec 2025 00:28:25 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 18 Dec 2025 00:28:30 GMT
ENV DOCKER_VERSION=29.1.3
# Thu, 18 Dec 2025 00:28:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 18 Dec 2025 00:28:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 18 Dec 2025 00:28:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 18 Dec 2025 00:28:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 18 Dec 2025 00:28:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 18 Dec 2025 00:28:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 18 Dec 2025 00:28:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:28:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 18 Dec 2025 00:28:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 18 Dec 2025 00:28:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:28:33 GMT
CMD ["sh"]
# Thu, 18 Dec 2025 01:27:33 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 18 Dec 2025 01:27:33 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 18 Dec 2025 01:27:33 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 18 Dec 2025 01:27:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 18 Dec 2025 01:27:37 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 18 Dec 2025 01:27:37 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 18 Dec 2025 01:27:37 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:27:37 GMT
VOLUME [/var/lib/docker]
# Thu, 18 Dec 2025 01:27:37 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 18 Dec 2025 01:27:37 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 18 Dec 2025 01:27:37 GMT
CMD []
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b03a86184eb198c617710819ab38c76a78f503786f7a1c54e7e907ec1f23dc`  
		Last Modified: Thu, 18 Dec 2025 00:28:48 GMT  
		Size: 8.3 MB (8300930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681c510cdccaa78efada2e7101c64026e0979fc5992bde5e1a004d32d5c4f50e`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e81e7bfdfe81c7ccebaa274dbeeba910c9ed6cf28480786814d75b209cf02e2`  
		Last Modified: Thu, 18 Dec 2025 00:28:49 GMT  
		Size: 17.6 MB (17563437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f326f2b8759b3faa44028809cfdcd8d7cf8d6985502f71a2f988c0e3c75f67da`  
		Last Modified: Thu, 18 Dec 2025 00:28:50 GMT  
		Size: 21.5 MB (21476548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbec79695a5faca52898d5cac9041e23c6dd2a7d2a5a1d35d9e72c19500ad24`  
		Last Modified: Thu, 18 Dec 2025 00:28:49 GMT  
		Size: 10.2 MB (10195776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce591b375ea2b0aa1d5c6f55fb237e7d3c33aba9558e6d168bf516ad8cb1c35`  
		Last Modified: Thu, 18 Dec 2025 00:28:49 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1130d51f83c71d1b9b0d2fcce026fc6a26e780e0e2cb8c6dd7606f56c71bc030`  
		Last Modified: Thu, 18 Dec 2025 00:28:49 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e4b6889ba531f92f7bf3dd5b354e025cfea931bc6c07d222838de5c515ca5c`  
		Last Modified: Thu, 18 Dec 2025 00:28:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc601c69eea8f547e1b7999bf72b6df6b7a73c9ca23d9980f6a8e8588c0f3837`  
		Last Modified: Thu, 18 Dec 2025 01:27:56 GMT  
		Size: 7.3 MB (7271034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b6700dd5e269ad28852da27b3e40784485be4d8e445cdbd0b2638a89e25295`  
		Last Modified: Thu, 18 Dec 2025 01:27:56 GMT  
		Size: 91.8 KB (91769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11b1395647108ae5cd2613ef1b4676c229f10a25e3984cea8a7a37bc6c0e515`  
		Last Modified: Thu, 18 Dec 2025 01:27:56 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b60934286a7babaf766349b743c43e811686a59bdb111ad9b507555cf0b96`  
		Last Modified: Thu, 18 Dec 2025 01:28:01 GMT  
		Size: 59.9 MB (59894389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f92a4045f16065b2d38661fa06f3e5c29bfabc5b5a1ffd74a6e6d317411658`  
		Last Modified: Thu, 18 Dec 2025 01:27:56 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86d5178cc489319c11851f37b0d1983712d66b02040d8406023ceb674a4f626`  
		Last Modified: Thu, 18 Dec 2025 01:27:56 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:0bd7e470e663fca2e8c679eeddf5dc804a5d9bdb1333c357cbcf15a8af1f7809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173548f78c590238e5b7bc4aaf5cb49e7bf279f53351ccf1961f3189e5e8b5f2`

```dockerfile
```

-	Layers:
	-	`sha256:263682fbdea247845996796f4cb079ee98c1824603e95903438785f59cce3765`  
		Last Modified: Thu, 18 Dec 2025 03:07:37 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f87ee65c06126192dfec8d9d2d5fd389cff5c17dbfa9f8931ec13987e74e706f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126468403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde1ca6fa5744d84a634635c311b61dc88adac6b231b52b1733b8986df066b9a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:02 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 18 Dec 2025 00:29:02 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 18 Dec 2025 00:29:02 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 18 Dec 2025 00:29:07 GMT
ENV DOCKER_VERSION=29.1.3
# Thu, 18 Dec 2025 00:29:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 18 Dec 2025 00:29:07 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 18 Dec 2025 00:29:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 18 Dec 2025 00:29:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 18 Dec 2025 00:29:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 18 Dec 2025 00:29:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 18 Dec 2025 00:29:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:29:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 18 Dec 2025 00:29:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 18 Dec 2025 00:29:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:29:09 GMT
CMD ["sh"]
# Thu, 18 Dec 2025 01:28:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 18 Dec 2025 01:28:12 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 18 Dec 2025 01:28:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 18 Dec 2025 01:28:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 18 Dec 2025 01:28:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 18 Dec 2025 01:28:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 18 Dec 2025 01:28:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:28:15 GMT
VOLUME [/var/lib/docker]
# Thu, 18 Dec 2025 01:28:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 18 Dec 2025 01:28:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 18 Dec 2025 01:28:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ebf94ba0d036a4243ceb102ce185a2800919d0797a991afeffe4b5ab61ec63`  
		Last Modified: Thu, 18 Dec 2025 00:29:26 GMT  
		Size: 7.6 MB (7597801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc30d8e5305c8a1f0f726f44503aba7c43038703a6bb0769dd140e046375508`  
		Last Modified: Thu, 18 Dec 2025 00:29:25 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99851ebf848a4e694f7a18f70a8b03c0c02c14592ddd7ab17e93edb5c0607e7`  
		Last Modified: Thu, 18 Dec 2025 00:29:28 GMT  
		Size: 17.6 MB (17552133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda4db7e09b897d8d43d7977f1b10e3aa262c62832260022dd78a9fb9466a809`  
		Last Modified: Thu, 18 Dec 2025 00:29:29 GMT  
		Size: 21.5 MB (21454918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151bb328052118d3d35c63e6c2ba49a8c63a53f118472ea17a798984e414a751`  
		Last Modified: Thu, 18 Dec 2025 00:29:28 GMT  
		Size: 10.2 MB (10188514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8373806e162ca648e7a50fe2b3f6df635b46424ed3b214db667755830d2fc558`  
		Last Modified: Thu, 18 Dec 2025 00:29:26 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757c36033cb11efa3a56f42187f80f29f33f70b8355347126092e03e53e38b0a`  
		Last Modified: Thu, 18 Dec 2025 00:29:26 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b051214681ef16cace179dde6e78b718317f23414276fda537cd0ad244d771`  
		Last Modified: Thu, 18 Dec 2025 00:29:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab54882a04974eef1db04eae43a13bdd2f15a73dd1a4618c237bf783a79adf1a`  
		Last Modified: Thu, 18 Dec 2025 01:28:33 GMT  
		Size: 6.6 MB (6572264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0b394431f28f371fa69bad43f6ff2edc6be35a5184706ba43b3b6bef664e6d`  
		Last Modified: Thu, 18 Dec 2025 01:28:33 GMT  
		Size: 88.1 KB (88134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bd5a8e81c74efed550b73801a362a74870b4e9bf63061eb66f2ac79f01fd4a`  
		Last Modified: Thu, 18 Dec 2025 01:28:33 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bc41e27df5182db8b4ef29e9dde98d08800909b00761ae2d2d50822600c10e`  
		Last Modified: Thu, 18 Dec 2025 01:28:40 GMT  
		Size: 59.7 MB (59727102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971ea0c9d0a5d6d435e252c1423113a20c62b03d45ea0ca54fc5bb29e6e36101`  
		Last Modified: Thu, 18 Dec 2025 01:28:33 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a4d6473754f01cf2b7744115b3351ef919de45e6084530f3036a0edaef9837`  
		Last Modified: Thu, 18 Dec 2025 01:28:33 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:029eba8001cfabf0813d9ffb70832746029c54247ff7b55aef1bfca22fcd0497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a548d6c62e971fe730004a39957a8d7e27beed0637dc2fad7d2b6c0fadbe78`

```dockerfile
```

-	Layers:
	-	`sha256:e1e477896441f16320ff946686bca359220c8734517ffd143e0cec03c9c10caf`  
		Last Modified: Thu, 18 Dec 2025 03:07:40 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4fd9ab4dbf153b5bad4d285b104f1e7abaee87ac25daffbd5ee24420a49249fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126323060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cca7e2a7da287ded85087ce88d443a5347163eebf6a9ed0c27bc4cabe90ae7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:28:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 18 Dec 2025 00:28:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 18 Dec 2025 00:28:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 18 Dec 2025 00:28:12 GMT
ENV DOCKER_VERSION=29.1.3
# Thu, 18 Dec 2025 00:28:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 18 Dec 2025 00:28:12 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 18 Dec 2025 00:28:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 18 Dec 2025 00:28:13 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 18 Dec 2025 00:28:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 18 Dec 2025 00:28:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 18 Dec 2025 00:28:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 00:28:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 18 Dec 2025 00:28:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 18 Dec 2025 00:28:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:28:13 GMT
CMD ["sh"]
# Thu, 18 Dec 2025 01:18:25 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 18 Dec 2025 01:18:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 18 Dec 2025 01:18:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 18 Dec 2025 01:18:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 18 Dec 2025 01:18:28 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 18 Dec 2025 01:18:28 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 18 Dec 2025 01:18:28 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 01:18:28 GMT
VOLUME [/var/lib/docker]
# Thu, 18 Dec 2025 01:18:28 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 18 Dec 2025 01:18:28 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 18 Dec 2025 01:18:28 GMT
CMD []
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af285040bb459a8575b7bc307afbb757384afd02e7f04289d21a3a4a6313c2f`  
		Last Modified: Thu, 18 Dec 2025 00:28:30 GMT  
		Size: 8.5 MB (8453517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5edfef6fbf53a6da6d31d686902289c311093a37a0720d64eae7b19edd2674e`  
		Last Modified: Thu, 18 Dec 2025 00:28:29 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3069ea149b76edc6f5f84f9c4b6cebafc26fa19b92ea1b990ab9d0788569568a`  
		Last Modified: Thu, 18 Dec 2025 00:28:37 GMT  
		Size: 17.3 MB (17337705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806f3905f4ae6f1f66384e1412fc2e1f6b7ec517616d61794e74e235f74c33b0`  
		Last Modified: Thu, 18 Dec 2025 00:28:31 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac2c219467023b87d7ebc1bfb959bd81e7d3f041ab5ac4618ab4ab0eacd6f8e`  
		Last Modified: Thu, 18 Dec 2025 00:28:30 GMT  
		Size: 9.9 MB (9938694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d53d3d34bed3e4c2fdb305f6864fae84696efabf457a0d2e51774f3f9718d02`  
		Last Modified: Thu, 18 Dec 2025 00:28:29 GMT  
		Size: 533.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5b98211c3fac2cd84de0b9dd867be2be6be0a36f72c7deff8db61e2b23bde8`  
		Last Modified: Thu, 18 Dec 2025 00:28:29 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949f3e228654d68237778ce48ce75d498187ba6107b35c6045317e19d77fefab`  
		Last Modified: Thu, 18 Dec 2025 00:28:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943df153e50553930e6bbce6bca898fcbd8b44217fb3d559d534b745de9d301b`  
		Last Modified: Thu, 18 Dec 2025 01:18:47 GMT  
		Size: 7.2 MB (7212638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f2007454a078a4dd18cfd18d12ae2096aae89e2d28aef3a543bbc31e812d76`  
		Last Modified: Thu, 18 Dec 2025 01:18:45 GMT  
		Size: 101.3 KB (101291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0fb85d0176b29530fde2a3b71eb0c7fc8cf52f2aa19b6dfe5a9e66114eb76d`  
		Last Modified: Thu, 18 Dec 2025 01:18:45 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1804a533b49e4273587cb694a847089c71352df4a1891b454e5e9acc6948be09`  
		Last Modified: Thu, 18 Dec 2025 01:18:54 GMT  
		Size: 58.4 MB (58430265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d089dfda08ea4f6911c8e15ac4bb6a8bd97032476ee45c1de3d0fd3f10fab642`  
		Last Modified: Thu, 18 Dec 2025 01:18:45 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d21bf3e9960a43d42909b6e58a5d098647bcd9d16472f1fe203cfd7a3659ed`  
		Last Modified: Thu, 18 Dec 2025 01:18:45 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:907cc0686a6a2d0aab81295c45249eaa33c39161087271beff19d02d6abf387d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6381e7861108c4274c173fbfc9521bb859517ba39c18ada694878eff038bdbf8`

```dockerfile
```

-	Layers:
	-	`sha256:4ca11ca20184ad830c8715ac8be6d99b8d98591e8745ca3675ac34016079886e`  
		Last Modified: Thu, 18 Dec 2025 03:07:43 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json
