## `docker:dind-rootless`

```console
$ docker pull docker@sha256:421dffbe324135321070051128d9d2787f0465a94d728070953b89255438a5c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:353a1727d0e6ac8343824427ff6d442390472e0bb77ca01655da0ddcf51fb9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156655034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfdf4d733c409824955ff98bc575e0384deb01f66c4f8e9a244e158f749ea1f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:23:17 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:23:17 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:23:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:23:19 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:23:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:23:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:23:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:23:20 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:05 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:07 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:07 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:07 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:07 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:07 GMT
CMD []
# Thu, 04 Dec 2025 00:34:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 00:34:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 00:34:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:34:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 00:34:16 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 00:34:16 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 00:34:16 GMT
USER rootless
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf38f401d9eb396102de765687dac64ecc08b1ba8695c40b26c0423b998e0fd`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 8.2 MB (8232315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df15eae0265ff940b83e0bbdb1f584e1d3dbdcfd4774e34481da25e596fbb1a`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb6f42d40901b88b36ad5a053e042551c52ab308ebb60d5e7d0b0b8cdce7b35`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 18.8 MB (18763816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bf5dda2df51e12e79e624b25be7b4091fc7918f1588eccbe0b6ad57310324e`  
		Last Modified: Wed, 03 Dec 2025 23:23:43 GMT  
		Size: 22.9 MB (22905495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152112b65ebf858e9eccab15c0ad2adf153d755aab4ea3a209c3e6b742f57f20`  
		Last Modified: Wed, 03 Dec 2025 23:23:40 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8790966215cc2531c4647abcf56c4e089393d99ca3bfe9476fef3d55bb7eeb7`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cca07e2ead009c060f33ef61f8a75340abc44534f1a7c4bfd888a29bdbf29d6`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a674c83cb4849ab734c2a0b5aa6b625c8ff0df4e521d07fd6898ccbd7f2b58`  
		Last Modified: Wed, 03 Dec 2025 23:23:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5db1b22d958d897b1303e75f6c720a87992a78f1fc88a2b1b7c12fedc789578`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 6.9 MB (6905424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027c458f6df56b11d25fe7ada4531d2dadb44c0b46a80b252df8e15de02f14d8`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 90.4 KB (90403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e35c086d0827f1e744fdde7f43a0ecd4424dafe675f1b1a14347b2a9ad9d91`  
		Last Modified: Thu, 04 Dec 2025 00:10:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f068ccbb78afd5ee04fee12780dd1533744e74761f8600f8e73e4c1b8ef5d456`  
		Last Modified: Thu, 04 Dec 2025 00:10:39 GMT  
		Size: 64.4 MB (64391841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba74257129c615ee0b232945d9f7ae269314d0d92407027aabed2325736bf9e`  
		Last Modified: Thu, 04 Dec 2025 00:10:35 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42349744b1ea7c38fb3d152a7c30f1f2a83d189b7b3dfade63e11c9df75302d`  
		Last Modified: Thu, 04 Dec 2025 00:10:40 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91aa056e56aa4a66ab4445fc928d9900f02526039d0d9e034dbd5f1864ded0e`  
		Last Modified: Thu, 04 Dec 2025 00:34:48 GMT  
		Size: 3.4 MB (3398378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ba6b907925696d4f4bf8e90017155cfc57c2eb3a3daf7b148f8e03ec3e6e46`  
		Last Modified: Thu, 04 Dec 2025 00:34:48 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa8d4bd6998c2fe7060be7b4c380915afb0718f2a048cffec66cfa2b3396679`  
		Last Modified: Thu, 04 Dec 2025 00:34:48 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb4f0a9a116b4469861628ca4fa5396cf4046b9589a4d19291e11bfea5fc4c6`  
		Last Modified: Thu, 04 Dec 2025 00:34:49 GMT  
		Size: 17.4 MB (17370975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0121931059414c5b535a820a06149e50072743b8d7d9d1292e94b5dd7cde587f`  
		Last Modified: Thu, 04 Dec 2025 00:34:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4b08832b0e539cc368981d37d867659cadd73c07d5b17094e24239509d6d408f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2014725d32624c20c843af1525ac27aa85a87442225e3a832e40bb9658fa40`

```dockerfile
```

-	Layers:
	-	`sha256:d430a287400d6e64aca730c1235ea91292ca5733da9bb24288faf42078d9d405`  
		Last Modified: Thu, 04 Dec 2025 03:07:58 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a1db98f222784429b330f778f1957ad3018c290fa95637335ca9ee58c09bd1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147091297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c01b600ca0f7971b32388b10745a1245988aa3e8ca83212a3ea4c2b2eb9609c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 03 Dec 2025 23:22:28 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 03 Dec 2025 23:22:28 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_VERSION=29.1.2
# Wed, 03 Dec 2025 23:22:30 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 03 Dec 2025 23:22:30 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 03 Dec 2025 23:22:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 03 Dec 2025 23:22:32 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 03 Dec 2025 23:22:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 03 Dec 2025 23:22:33 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 03 Dec 2025 23:22:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Dec 2025 23:22:33 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 00:10:52 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 00:10:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 00:10:55 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 00:10:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 00:10:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 00:10:55 GMT
CMD []
# Thu, 04 Dec 2025 00:34:13 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 00:34:13 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 00:34:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 00:34:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 00:34:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 00:34:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 00:34:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57445b997cd55133a9c0a7eb6cf01c663a359bbcd63a79039983b69095ac42f1`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 8.3 MB (8257353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faaf460832bcd7548a203f3dc2f23d89aa0230de6834f3d48850ffccff1a17d`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fef58fc39ee394eb1048dd907b452414fd90f15d622e5bdfb0ae1bb654ca48`  
		Last Modified: Wed, 03 Dec 2025 23:22:56 GMT  
		Size: 17.3 MB (17334889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382df833bdea9f9647be3691afa9e836a9a325d9b56fc17d7bf75a5f937d3300`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 20.6 MB (20645062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7311bdf5d2c5fa464fe3694ace8177f0eb6c6852c0d536b8a4345c57e7fa35`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 9.9 MB (9938701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b595588e1ca2283efda99ac8b6a2f107fadd8daa828c41fc27dff468696d48`  
		Last Modified: Wed, 03 Dec 2025 23:22:54 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdb6e23f3673b57d33d39393ef9d8b59d8ac0fdaba6265ad2bcb3f018f24261`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cde453c109f292df3e15190a9e51e2c80a4240ff7df97c11fe940970e30e0b5`  
		Last Modified: Wed, 03 Dec 2025 23:22:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c3b0fd8787d61d479f985a6af3db37861a089e6626af927e0fe11a521011da`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 7.1 MB (7140902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a978db8775b84c897593e3be041aafd0bfb11490a92d38f2280518637c2074c`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 99.5 KB (99505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e06f60b77f552b49c034f7fbaa7328be13c2750666dd09283bc4f8fd517402`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864738aaf40d7e252d693ab11e69009665fcf70548a8e294996f60baf267ed3`  
		Last Modified: Thu, 04 Dec 2025 00:11:36 GMT  
		Size: 58.4 MB (58428656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d21a4dd1156908d0a7872336b60446c71d7bcf6b5ed180130fa4e9f496e0189`  
		Last Modified: Thu, 04 Dec 2025 00:11:30 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53919f72ea7279e04107b6be6507f1fdb25b13c0cc885064b3d39f7171aced9a`  
		Last Modified: Thu, 04 Dec 2025 00:11:31 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29744f0d4e84a604abd643d72e500a942b93b47aebc9608aeb11c9547505978f`  
		Last Modified: Thu, 04 Dec 2025 00:34:30 GMT  
		Size: 3.4 MB (3389949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd8dfe81186ff0b816407ebca7cde7473e4568a00053e41a9b865506bb318b0`  
		Last Modified: Thu, 04 Dec 2025 00:34:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334d36e8d2a2055d1ce374a4db658c40f1524af962083d9b5da52852d76a46cd`  
		Last Modified: Thu, 04 Dec 2025 00:34:28 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0acb58cf5a910482ee59a629e47ddf2882796d6846f7fcba3860c753046c3`  
		Last Modified: Thu, 04 Dec 2025 00:34:29 GMT  
		Size: 17.7 MB (17708720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68ee96465b587d4e1d201671d6f38af93ce12e3e8de1e4318ce20a9a3a22aa5`  
		Last Modified: Thu, 04 Dec 2025 00:34:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:629ac163c9e7113117c78d53db8ab7c25aba4ee3de17c2844199d515d03b1900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63d85a6970c712972dadb4c3f5562f4814c08c63e23177be3b9fb30441e0646`

```dockerfile
```

-	Layers:
	-	`sha256:a9a45b6a9af3185edc3fef012c4ee2bbc1e2310c25a9b46260487d287c102821`  
		Last Modified: Thu, 04 Dec 2025 03:08:01 GMT  
		Size: 30.7 KB (30747 bytes)  
		MIME: application/vnd.in-toto+json
