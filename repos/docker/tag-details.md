<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.1`](#docker291)
-	[`docker:29.1-cli`](#docker291-cli)
-	[`docker:29.1-dind`](#docker291-dind)
-	[`docker:29.1-dind-rootless`](#docker291-dind-rootless)
-	[`docker:29.1-windowsservercore`](#docker291-windowsservercore)
-	[`docker:29.1-windowsservercore-ltsc2022`](#docker291-windowsservercore-ltsc2022)
-	[`docker:29.1-windowsservercore-ltsc2025`](#docker291-windowsservercore-ltsc2025)
-	[`docker:29.1.3`](#docker2913)
-	[`docker:29.1.3-alpine3.23`](#docker2913-alpine323)
-	[`docker:29.1.3-cli`](#docker2913-cli)
-	[`docker:29.1.3-cli-alpine3.23`](#docker2913-cli-alpine323)
-	[`docker:29.1.3-dind`](#docker2913-dind)
-	[`docker:29.1.3-dind-alpine3.23`](#docker2913-dind-alpine323)
-	[`docker:29.1.3-dind-rootless`](#docker2913-dind-rootless)
-	[`docker:29.1.3-windowsservercore`](#docker2913-windowsservercore)
-	[`docker:29.1.3-windowsservercore-ltsc2022`](#docker2913-windowsservercore-ltsc2022)
-	[`docker:29.1.3-windowsservercore-ltsc2025`](#docker2913-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:7370a6c49b7e708fb969b422dffe6cdd78a9f0ff5b3bfba0e0cddce736c49eaf
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
$ docker pull docker@sha256:614db3c0aa1f5a2fe91d4bbbb0df8190c5d233d6ad55aa0f285c29f54227f7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136136542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8274856237f1b49083c42adab01ae804b00b8eeddb621e75b53e8c7a18657249`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:14 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6395790a96f25fe9ae60e8642bb53dc32742cc2a952240e2430c727343070f94`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 6.9 MB (6932404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0e7dad2234067bcdefdfbe8a95f9d27a127e90c2547a0b535e998e62492f9`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 92.5 KB (92451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d2dd2748ca8b7279cc840f1717a591f741f79ca77fccc303369e23381404e`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be03fb08c790242db2d11f5c8abd1e27779400315ae4bebf6812421eb196f424`  
		Last Modified: Fri, 12 Dec 2025 23:10:36 GMT  
		Size: 64.4 MB (64390653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969ded5ab7c174111a0938c32df0c859eae02e11a1f03b285260d4e52ada118`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15928226105bb78669d71594057c0a40684760f66de44e473fe4559e048a1fc4`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:d872ccf708c0c6cf248b60f3628d4f6c144e2b9b28d7249d5e99349e036598bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2e79926af9c2cfd84fb6eaa06ee2a235ee5389bbc8f0c528a68c05c925f98c`

```dockerfile
```

-	Layers:
	-	`sha256:dfa8b777c70191bcd2b044ff54627b657daadee8f5c1dfcae039cb25aa6d9e66`  
		Last Modified: Sat, 13 Dec 2025 03:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:e290522631fba31e8ef320a62d0efe0f7bd279c504aacea1b231502c56c75d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128368324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52adaa135524f86585c09c3b6ea713da7b19764a9bb3853687c4410ff4057193`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:01:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:01:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:01:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:01:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:01:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:01:06 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:29 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:29 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:29 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a442d3375c6cf3a0d64cab9a5657f13a2ad79d715217080e57d4091d88c4324`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 8.3 MB (8301082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d2ff8b4dcb5e27c0a3ebecc8f29e07008e917fc5a5a7a6dfeece3f50f8613`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf22d2b96392d2b3c9f1cb454ed14bc66a1dfdef830883f46ed5613c0133d4`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 17.6 MB (17563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be201cbc63828006213cbca3a3f8b91138447829d70553ea57b47fb7b36316`  
		Last Modified: Fri, 12 Dec 2025 23:01:28 GMT  
		Size: 21.5 MB (21476558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e492ed6855e1816d78b7edbd4cdc38ef0cb81d978dfc857129d58d22c754fa`  
		Last Modified: Fri, 12 Dec 2025 23:01:25 GMT  
		Size: 10.2 MB (10195786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50a36847c59872394550e672e167266ae450d58950ec050895f9a2b8b650e3`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836b06438ad83afcbbb80d394f9a68dc224a96dbc3f7446ef31113fbd4fc107`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844bcb311c659e5cab12e879fb055dd4d63aaca8e759553df1c68ad8f8572a0`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f78a51ea72b486ea303cfe9a35e0936165e64f6c1ce623050f1bbc03783827e`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 7.3 MB (7269237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150a1e8e9e07769ffd55ede4c3ebe7b37a7d4a52e59841483c2f1dc104a73cd`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 91.7 KB (91744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d880baf4277f9d0addd5734ad6cd8ef5e32b361ae8196dffbee590ccd63e28c2`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba95d05539ea20cd2ad894c3b01011b5412ac30470cf2067be3a4de6893fb49`  
		Last Modified: Fri, 12 Dec 2025 23:09:51 GMT  
		Size: 59.9 MB (59894425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d365292960a46a15ee408a118f8ed3443f9de61abacc32b1e1c93ca107c203b`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad152b473b5d59ed3116b07b37f35d4bc0fc85aa8364882c610816bea229f3bf`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:c70c7dcb7dfdb1cc89722c4c1299406e1924186e972fd94deb54abbd1052301a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bec62c6dbaf983fd287f9991784c3219e307aceca7be3d32fe32b63d7b2187f`

```dockerfile
```

-	Layers:
	-	`sha256:fff0c79b6617bada32062564279ba2c4c61cab0f5d7fb8bcdb5ac4e87f9f393c`  
		Last Modified: Sat, 13 Dec 2025 03:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:71a0b301e07cfb3145b58f5e33589420b2f0e643d9376d35097d4d402673c64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126466294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e849666bdf05465f46c218af24544c6a84be85d4505f05f1a67f2439df655afb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:48 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:22 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbf8f000eac737bf318d60725474e05cf5bb1d57c289c8f1a9fc5a087446bbb`  
		Last Modified: Fri, 12 Dec 2025 23:04:10 GMT  
		Size: 7.6 MB (7597999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c0b74efc53c5a11551937b3c0ac0e558dda2c21c713a42b1a8c90c83e929a`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26fc85eb088676c2237ad1410f2d06bf4167acef7e7573aa468e85f49ee8`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 17.6 MB (17552135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c0880b371ae9def4a59c648a03dc32de73c939a82863ed46189b5d3c1b26`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 21.5 MB (21454919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dfae8792ac984c5843e7a75359342e09ed6b06094284d3d9afef64ef8d37`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 10.2 MB (10188515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c8dcf60105513f337a71a7a302174c703f2ac4b01eca1a6976550cabbc9cb`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078bbc407a642525a8ecd8f3f56ec5f42ea4276b7984629db0dada8b0ecf69c`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091878b07b4fafc28f7778946a2e29d096eb34042255686f44fcadaea5d597`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e785e66500d9f73341d04a0d0fe01a7ca6a4ce3d3b9288e82242bc725426b`  
		Last Modified: Fri, 12 Dec 2025 23:10:40 GMT  
		Size: 6.6 MB (6570882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928ed8314751e2e9eaeabdc972d4af1311ab6177479d3b6f80a5539231796da7`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9abf1ec541ec0b256d5eab59239d0b754ddab5d999b8dc430585b6f948e604e`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233d3deeb4102367ed1ec89b7ef2fc760d574be2fc7fedd4ea2e4108be9aba6`  
		Last Modified: Fri, 12 Dec 2025 23:10:45 GMT  
		Size: 59.7 MB (59727126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b55b2d0cde4acdec0d0647c16445382a856fdacd9c1cd5fdf7116a5f96dbb4`  
		Last Modified: Fri, 12 Dec 2025 23:10:50 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603edd3336b192e57264b4a135254f9b4dc1a5761163fe26d86596342fe422de`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:0c9b638681007c9d6737a03cc64eac228cfd924c10100f3189602dd4d65d73bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70074d9836671bcf71409a77556f876fa92be1526c11bc44cf503e7077324561`

```dockerfile
```

-	Layers:
	-	`sha256:18a5d28b03d244c5685e86038be1cc676b25e374d481bfba7ced9ce1023ebe95`  
		Last Modified: Sat, 13 Dec 2025 03:07:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ae8fb276f238b912024b6b5805e3e244f0919648b835cf7a1ad0c1b791638ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126321327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b51d82ca438a87cf78f035539342acb921ff3b8a7c5c316c5dd827b52838dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1f8bb5ac9908d8a2f05285d5bafaaa09c4639ad5ec575f506b7f94eb9b027`  
		Last Modified: Fri, 12 Dec 2025 23:09:43 GMT  
		Size: 7.2 MB (7211487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07fdd52b461065d91e16e325ebe1351e98a49811bfe1953d3ffe9d71f66976`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 101.3 KB (101259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d775131bce9a8efbc68a01168997189db83ec2f6764633a853bb6c4013ba98b9`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1bdb364f96a9e042c2a09900dea9f490b2fd714dc314a9b36df5e470baa327`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 58.4 MB (58430278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039982dd10164d6a2e84e3eba3fd37ce736fbfcb0f9e03881c7ba02615b5c87`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22468ff67dbfccb6e8991c334fe5d9d379c964a9ecfe16c05d804125837727f8`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:3c36eabf6e66c492c055fbc625e84d44c47a923d35e2f46f5d13f8c90174aca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae5563a6811d6d3cc3a1e6303828b71d9608a6a4fc125183d83423348c5f2a6`

```dockerfile
```

-	Layers:
	-	`sha256:f88b5a51b8c8deb7c3b298f4e2252c16a18f817fb711be330fa64e81a65284e0`  
		Last Modified: Sat, 13 Dec 2025 03:07:37 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:fef89d736d81ca03bb9bac2fabdc7bbf5f0b1485a708c94028225cb8623d1084
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
$ docker pull docker@sha256:460bd54747e38686f19906b2c7871d7a24159b2149fab3d2576d5cfd201cad73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64715034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4453f9079883af7ee6a02d1d59e76df1c5254647118c2fcd31dad73a7868a2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:18efc4ebd9cdbdf6b6ce77046066d86d2ca19db8332ee23cf54e560fbc3731bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76513174b1ca50e674ed0be90a756d3e124b07462362dbb3baab908e1537cb85`

```dockerfile
```

-	Layers:
	-	`sha256:7a2736719c9b6d24bbb2e67120ddc54c6a898296084a245f781f6e63d2158f2a`  
		Last Modified: Sat, 13 Dec 2025 00:07:29 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ed3d4022bcc3b84bda70aaae6c5f5fc5fcfe3c166b59a310eb546de5b1b93419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61106920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95404e10bb74578f403ba9578c56111c25597aa98a33490d2ea3bc7ac17c48b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:01:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:01:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:01:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:01:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:01:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:01:06 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a442d3375c6cf3a0d64cab9a5657f13a2ad79d715217080e57d4091d88c4324`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 8.3 MB (8301082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d2ff8b4dcb5e27c0a3ebecc8f29e07008e917fc5a5a7a6dfeece3f50f8613`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf22d2b96392d2b3c9f1cb454ed14bc66a1dfdef830883f46ed5613c0133d4`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 17.6 MB (17563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be201cbc63828006213cbca3a3f8b91138447829d70553ea57b47fb7b36316`  
		Last Modified: Fri, 12 Dec 2025 23:01:28 GMT  
		Size: 21.5 MB (21476558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e492ed6855e1816d78b7edbd4cdc38ef0cb81d978dfc857129d58d22c754fa`  
		Last Modified: Fri, 12 Dec 2025 23:01:25 GMT  
		Size: 10.2 MB (10195786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50a36847c59872394550e672e167266ae450d58950ec050895f9a2b8b650e3`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836b06438ad83afcbbb80d394f9a68dc224a96dbc3f7446ef31113fbd4fc107`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844bcb311c659e5cab12e879fb055dd4d63aaca8e759553df1c68ad8f8572a0`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:050b2baec8a743beab976d109ade8bbd2255f907abf6ed7c521825f031ebfb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8711322ffdbfc1512d835bdbb3d1aab5d63286fc0edb80507d74fd721e7093`

```dockerfile
```

-	Layers:
	-	`sha256:3462d33a19054d0414ea3eb7bdc0b282352efc598442d721e9c2f5e3e7af653d`  
		Last Modified: Sat, 13 Dec 2025 00:07:32 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:7b6ba4909381a6b3ca8380db56b5e0566e94241d29ad12196b4871bcd0751e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60074186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273d97076d24ffa898e7608f96246fe2f9c6a75ca258cfa233e728c2a3d00b89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbf8f000eac737bf318d60725474e05cf5bb1d57c289c8f1a9fc5a087446bbb`  
		Last Modified: Fri, 12 Dec 2025 23:04:10 GMT  
		Size: 7.6 MB (7597999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c0b74efc53c5a11551937b3c0ac0e558dda2c21c713a42b1a8c90c83e929a`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26fc85eb088676c2237ad1410f2d06bf4167acef7e7573aa468e85f49ee8`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 17.6 MB (17552135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c0880b371ae9def4a59c648a03dc32de73c939a82863ed46189b5d3c1b26`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 21.5 MB (21454919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dfae8792ac984c5843e7a75359342e09ed6b06094284d3d9afef64ef8d37`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 10.2 MB (10188515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c8dcf60105513f337a71a7a302174c703f2ac4b01eca1a6976550cabbc9cb`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078bbc407a642525a8ecd8f3f56ec5f42ea4276b7984629db0dada8b0ecf69c`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091878b07b4fafc28f7778946a2e29d096eb34042255686f44fcadaea5d597`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2cd5fe33035b9b245d7633d313b6c10663c4b4a15539e1049ed543ae30b0895b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0eafce598b67ac57b3e56ed0966055137da7f5a73489083c1c5a72c6e7febc`

```dockerfile
```

-	Layers:
	-	`sha256:5453b680a91095b07fa3308adfcd6460856cd978700e2fcac203bbcd490a8b4c`  
		Last Modified: Sat, 13 Dec 2025 00:07:35 GMT  
		Size: 38.2 KB (38220 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cd7a8fb27fb7769bd1e99c859cd81b6b5907a48159fe0c5978d36dac92832ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60572305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9fc8e3c559250bb84f436eb83db1fca5000b54667762710ed0053847f4df6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3fc751e1389e0e81e12e5a50e51cd4c8c9f09bc6f5c22868892d33f362494bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d129b4abe449d1af4183719346aec5b3c50a1a8a0a42844f5299279d54a22a`

```dockerfile
```

-	Layers:
	-	`sha256:847c010774232d19f586d313e7adf4e52cf76fbf7d80543c31098ce2d449ddbc`  
		Last Modified: Sat, 13 Dec 2025 00:08:01 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:7370a6c49b7e708fb969b422dffe6cdd78a9f0ff5b3bfba0e0cddce736c49eaf
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
$ docker pull docker@sha256:614db3c0aa1f5a2fe91d4bbbb0df8190c5d233d6ad55aa0f285c29f54227f7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136136542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8274856237f1b49083c42adab01ae804b00b8eeddb621e75b53e8c7a18657249`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:14 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6395790a96f25fe9ae60e8642bb53dc32742cc2a952240e2430c727343070f94`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 6.9 MB (6932404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0e7dad2234067bcdefdfbe8a95f9d27a127e90c2547a0b535e998e62492f9`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 92.5 KB (92451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d2dd2748ca8b7279cc840f1717a591f741f79ca77fccc303369e23381404e`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be03fb08c790242db2d11f5c8abd1e27779400315ae4bebf6812421eb196f424`  
		Last Modified: Fri, 12 Dec 2025 23:10:36 GMT  
		Size: 64.4 MB (64390653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969ded5ab7c174111a0938c32df0c859eae02e11a1f03b285260d4e52ada118`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15928226105bb78669d71594057c0a40684760f66de44e473fe4559e048a1fc4`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d872ccf708c0c6cf248b60f3628d4f6c144e2b9b28d7249d5e99349e036598bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2e79926af9c2cfd84fb6eaa06ee2a235ee5389bbc8f0c528a68c05c925f98c`

```dockerfile
```

-	Layers:
	-	`sha256:dfa8b777c70191bcd2b044ff54627b657daadee8f5c1dfcae039cb25aa6d9e66`  
		Last Modified: Sat, 13 Dec 2025 03:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:e290522631fba31e8ef320a62d0efe0f7bd279c504aacea1b231502c56c75d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128368324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52adaa135524f86585c09c3b6ea713da7b19764a9bb3853687c4410ff4057193`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:01:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:01:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:01:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:01:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:01:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:01:06 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:29 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:29 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:29 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a442d3375c6cf3a0d64cab9a5657f13a2ad79d715217080e57d4091d88c4324`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 8.3 MB (8301082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d2ff8b4dcb5e27c0a3ebecc8f29e07008e917fc5a5a7a6dfeece3f50f8613`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf22d2b96392d2b3c9f1cb454ed14bc66a1dfdef830883f46ed5613c0133d4`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 17.6 MB (17563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be201cbc63828006213cbca3a3f8b91138447829d70553ea57b47fb7b36316`  
		Last Modified: Fri, 12 Dec 2025 23:01:28 GMT  
		Size: 21.5 MB (21476558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e492ed6855e1816d78b7edbd4cdc38ef0cb81d978dfc857129d58d22c754fa`  
		Last Modified: Fri, 12 Dec 2025 23:01:25 GMT  
		Size: 10.2 MB (10195786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50a36847c59872394550e672e167266ae450d58950ec050895f9a2b8b650e3`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836b06438ad83afcbbb80d394f9a68dc224a96dbc3f7446ef31113fbd4fc107`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844bcb311c659e5cab12e879fb055dd4d63aaca8e759553df1c68ad8f8572a0`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f78a51ea72b486ea303cfe9a35e0936165e64f6c1ce623050f1bbc03783827e`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 7.3 MB (7269237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150a1e8e9e07769ffd55ede4c3ebe7b37a7d4a52e59841483c2f1dc104a73cd`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 91.7 KB (91744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d880baf4277f9d0addd5734ad6cd8ef5e32b361ae8196dffbee590ccd63e28c2`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba95d05539ea20cd2ad894c3b01011b5412ac30470cf2067be3a4de6893fb49`  
		Last Modified: Fri, 12 Dec 2025 23:09:51 GMT  
		Size: 59.9 MB (59894425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d365292960a46a15ee408a118f8ed3443f9de61abacc32b1e1c93ca107c203b`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad152b473b5d59ed3116b07b37f35d4bc0fc85aa8364882c610816bea229f3bf`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:c70c7dcb7dfdb1cc89722c4c1299406e1924186e972fd94deb54abbd1052301a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bec62c6dbaf983fd287f9991784c3219e307aceca7be3d32fe32b63d7b2187f`

```dockerfile
```

-	Layers:
	-	`sha256:fff0c79b6617bada32062564279ba2c4c61cab0f5d7fb8bcdb5ac4e87f9f393c`  
		Last Modified: Sat, 13 Dec 2025 03:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:71a0b301e07cfb3145b58f5e33589420b2f0e643d9376d35097d4d402673c64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126466294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e849666bdf05465f46c218af24544c6a84be85d4505f05f1a67f2439df655afb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:48 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:22 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbf8f000eac737bf318d60725474e05cf5bb1d57c289c8f1a9fc5a087446bbb`  
		Last Modified: Fri, 12 Dec 2025 23:04:10 GMT  
		Size: 7.6 MB (7597999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c0b74efc53c5a11551937b3c0ac0e558dda2c21c713a42b1a8c90c83e929a`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26fc85eb088676c2237ad1410f2d06bf4167acef7e7573aa468e85f49ee8`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 17.6 MB (17552135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c0880b371ae9def4a59c648a03dc32de73c939a82863ed46189b5d3c1b26`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 21.5 MB (21454919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dfae8792ac984c5843e7a75359342e09ed6b06094284d3d9afef64ef8d37`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 10.2 MB (10188515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c8dcf60105513f337a71a7a302174c703f2ac4b01eca1a6976550cabbc9cb`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078bbc407a642525a8ecd8f3f56ec5f42ea4276b7984629db0dada8b0ecf69c`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091878b07b4fafc28f7778946a2e29d096eb34042255686f44fcadaea5d597`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e785e66500d9f73341d04a0d0fe01a7ca6a4ce3d3b9288e82242bc725426b`  
		Last Modified: Fri, 12 Dec 2025 23:10:40 GMT  
		Size: 6.6 MB (6570882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928ed8314751e2e9eaeabdc972d4af1311ab6177479d3b6f80a5539231796da7`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9abf1ec541ec0b256d5eab59239d0b754ddab5d999b8dc430585b6f948e604e`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233d3deeb4102367ed1ec89b7ef2fc760d574be2fc7fedd4ea2e4108be9aba6`  
		Last Modified: Fri, 12 Dec 2025 23:10:45 GMT  
		Size: 59.7 MB (59727126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b55b2d0cde4acdec0d0647c16445382a856fdacd9c1cd5fdf7116a5f96dbb4`  
		Last Modified: Fri, 12 Dec 2025 23:10:50 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603edd3336b192e57264b4a135254f9b4dc1a5761163fe26d86596342fe422de`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0c9b638681007c9d6737a03cc64eac228cfd924c10100f3189602dd4d65d73bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70074d9836671bcf71409a77556f876fa92be1526c11bc44cf503e7077324561`

```dockerfile
```

-	Layers:
	-	`sha256:18a5d28b03d244c5685e86038be1cc676b25e374d481bfba7ced9ce1023ebe95`  
		Last Modified: Sat, 13 Dec 2025 03:07:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ae8fb276f238b912024b6b5805e3e244f0919648b835cf7a1ad0c1b791638ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126321327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b51d82ca438a87cf78f035539342acb921ff3b8a7c5c316c5dd827b52838dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1f8bb5ac9908d8a2f05285d5bafaaa09c4639ad5ec575f506b7f94eb9b027`  
		Last Modified: Fri, 12 Dec 2025 23:09:43 GMT  
		Size: 7.2 MB (7211487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07fdd52b461065d91e16e325ebe1351e98a49811bfe1953d3ffe9d71f66976`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 101.3 KB (101259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d775131bce9a8efbc68a01168997189db83ec2f6764633a853bb6c4013ba98b9`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1bdb364f96a9e042c2a09900dea9f490b2fd714dc314a9b36df5e470baa327`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 58.4 MB (58430278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039982dd10164d6a2e84e3eba3fd37ce736fbfcb0f9e03881c7ba02615b5c87`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22468ff67dbfccb6e8991c334fe5d9d379c964a9ecfe16c05d804125837727f8`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3c36eabf6e66c492c055fbc625e84d44c47a923d35e2f46f5d13f8c90174aca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae5563a6811d6d3cc3a1e6303828b71d9608a6a4fc125183d83423348c5f2a6`

```dockerfile
```

-	Layers:
	-	`sha256:f88b5a51b8c8deb7c3b298f4e2252c16a18f817fb711be330fa64e81a65284e0`  
		Last Modified: Sat, 13 Dec 2025 03:07:37 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:ac12412d8bc07bdbc71e1bd730572dc5010a5d2116987775b30f849d1268380e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:09950db32d89c1662f1970578f51562812eab9a3eb50feb7326519f7e5514235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156928803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17a49738c68db9b440e165269dc75f5f3e74a89e9a75426199cd466b0383cd6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:14 GMT
CMD []
# Sat, 13 Dec 2025 00:10:12 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 13 Dec 2025 00:10:12 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 13 Dec 2025 00:10:12 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 13 Dec 2025 00:10:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 13 Dec 2025 00:10:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 13 Dec 2025 00:10:13 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 13 Dec 2025 00:10:13 GMT
USER rootless
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6395790a96f25fe9ae60e8642bb53dc32742cc2a952240e2430c727343070f94`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 6.9 MB (6932404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0e7dad2234067bcdefdfbe8a95f9d27a127e90c2547a0b535e998e62492f9`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 92.5 KB (92451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d2dd2748ca8b7279cc840f1717a591f741f79ca77fccc303369e23381404e`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be03fb08c790242db2d11f5c8abd1e27779400315ae4bebf6812421eb196f424`  
		Last Modified: Fri, 12 Dec 2025 23:10:36 GMT  
		Size: 64.4 MB (64390653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969ded5ab7c174111a0938c32df0c859eae02e11a1f03b285260d4e52ada118`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15928226105bb78669d71594057c0a40684760f66de44e473fe4559e048a1fc4`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7efc67e74d7bff7198949770096adae0c34ad7c6a32faa6e3d0bab24e69da51`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 3.4 MB (3419931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0ea6cd17928c2035157de458119f33ee511ec1deee23008735895ce2472b79`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b30c307447754a05b3912b60fa4a43ebe6eb174bb107be0d85866ce5cf6d0b6`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab6e3723d2a693205fe1725bd19abcfbfd2ac1331a374d8b35b7897742941c5`  
		Last Modified: Sat, 13 Dec 2025 00:10:37 GMT  
		Size: 17.4 MB (17370991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7db2853efa7da1fc8d7b3143c0f861bdc77ee5a9cce03278ff21f1568ef69c5`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:336e04652a588e2ad4e195e403ef93c675ba97007c75e40a9efe962cb4f16bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd1e5b602cf458f135106fdc1b6bee98d42185597cd98c67410b6c1c42dc34f`

```dockerfile
```

-	Layers:
	-	`sha256:e3a762cb9f51fe6d372134b550c76079147291d858530a914cc826e7d8dbc1d9`  
		Last Modified: Sat, 13 Dec 2025 03:07:42 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7deb6a567eeef7d5a72412f239f2170d024ede941b350b13f24ebf9abc29721e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147425780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229ad388f6f6b781e7a9b6825675f4deeb04ea90f1123729e79549a7b32b83ac`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:25 GMT
CMD []
# Sat, 13 Dec 2025 00:09:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 13 Dec 2025 00:09:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 13 Dec 2025 00:09:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 13 Dec 2025 00:10:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 13 Dec 2025 00:10:01 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 13 Dec 2025 00:10:01 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 13 Dec 2025 00:10:01 GMT
USER rootless
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1f8bb5ac9908d8a2f05285d5bafaaa09c4639ad5ec575f506b7f94eb9b027`  
		Last Modified: Fri, 12 Dec 2025 23:09:43 GMT  
		Size: 7.2 MB (7211487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07fdd52b461065d91e16e325ebe1351e98a49811bfe1953d3ffe9d71f66976`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 101.3 KB (101259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d775131bce9a8efbc68a01168997189db83ec2f6764633a853bb6c4013ba98b9`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1bdb364f96a9e042c2a09900dea9f490b2fd714dc314a9b36df5e470baa327`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 58.4 MB (58430278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039982dd10164d6a2e84e3eba3fd37ce736fbfcb0f9e03881c7ba02615b5c87`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22468ff67dbfccb6e8991c334fe5d9d379c964a9ecfe16c05d804125837727f8`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb2d13730b1a2b9437f55aa38844a2d4f3a41baff03b9ba200fd6c8e3640f65`  
		Last Modified: Sat, 13 Dec 2025 00:10:27 GMT  
		Size: 3.4 MB (3394382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c5eda520ed158582d67f72a42c82eef1d312c24f5fb51f16441c4772825971`  
		Last Modified: Sat, 13 Dec 2025 00:10:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05db2d742efc92d52e078c87f0af299e70fb014fbfaea3a18b757374eca9af`  
		Last Modified: Sat, 13 Dec 2025 00:10:27 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9af16ab409354af0d1a5b9a8dd6362e6886e59680f35e8fc253d99c504af99`  
		Last Modified: Sat, 13 Dec 2025 00:10:32 GMT  
		Size: 17.7 MB (17708729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffd4a2a8cc857d1398fdf583e20112730537572a29d8c9100512be073ec09d8`  
		Last Modified: Sat, 13 Dec 2025 00:10:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6eab544cd873580b808013fbe86c7cc254767cc99c60313d1cd9f4e5eccb9f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c814e243bbda6587996667fdd159361b2cc27f15e889e349a1976482785bda18`

```dockerfile
```

-	Layers:
	-	`sha256:3a3842cd2beb5724ad7a78418740bfd432103bce0f213347880883022e4a0094`  
		Last Modified: Sat, 13 Dec 2025 03:07:45 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:24e3252850071e0729b50e765be6eb141aec202a2709217891272b9d2a8efb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:072f69cc9a1bc2cb016cd912ee5dcb075d0f2e73df576a46f98ddb1f3f8a4ea2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308280068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e356747fea9e9e69ddc2df399e0a31cb31c5c255da4f7f8ff52e08eef859a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Fri, 12 Dec 2025 23:51:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:51:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:51:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:33 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:51:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:43 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:51:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49db97996aeb50d6cc3bb59d05b2805a04f9a341f791d3bbf78f96c91ea6ea46`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e012252a5c78e6736aa02ede33d15956b820e11e10d32c0eed00f4ac4c0642ed`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 365.2 KB (365173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba990e6755d56a5110398c67645345164f3cb13a4f31f2c87cd0cf475b2fddc`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df48c7a2c9538324b83a4a6378f6ecbcf5c51d2b4c853c98b154d3d2e1fe23c`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9a30b43b8cff73e13f7e796431a6d59d40548fd5ed22e9f0f643554cffa66`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 19.4 MB (19430080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053e9422e23dca07aade3c64cf9355ecc9227c50dd075cde8a77bf5f588fdf07`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d53e5a50955843cf8df23bd9852867dc4e044732ab6a2c3dff445d30a03969`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6a3bffb040caaef43c930bcf019f71c62523c17c8c3aa21340ce83fd63c367`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5297cc0777d4cd44c02f2f373fa189394855ab3f6e99fb51e0e9b14dcbe7719`  
		Last Modified: Sat, 13 Dec 2025 00:10:41 GMT  
		Size: 23.9 MB (23916756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d343979aeb667bd44bc30f0385636c1525e1007c30d7a56b0c4b2929e986e3ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e484e796b3e881c2c53ab847de762b0acce3ce695452b588333031fd16f4722`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1d8d8a0183df8a67af7c17491af2ce9bcc2f1e5bed8a1b7337d9cc59d72a48`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e066997579a2dbc121185aac60816764e96c1cbce7d351630d1ae1a79062f7ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 11.4 MB (11435912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:6c63e74fbbe6a6853d2eed17e74a22a1f27caa6652d65e73237c8cdae1584560
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835158901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31a8d2106c0d362d41e18b340f4ce9fcb284d2750fd96d7010599996e10f95a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Fri, 12 Dec 2025 23:42:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:42:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:42:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:35 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:42:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:42:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a59061a4bd19a5f5104deac5c13f08378f0d057b550fa44336edd48c297a30`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d45f349269329c39cb7f626e581200a0cfd951639d64b460dc496e827a02d3`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 496.4 KB (496422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbbd38f48aebab5ee03921c61d62bc51aafa5296de9f243a1b119cb5b9b59e8`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38e962b0dcf2e2174265dd10ed886b4ac610012a54d0a165b374784dfbfaf5b`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b233205356122f2ba9d651e4d85f51b9efc8720271061a670c3d376808be4df`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 19.4 MB (19421634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4696a1bc6b20cc354eebea761ac5c3e7bee2e41055c2310c9e1efda5acac04cc`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8453a804e2b4641b89e10a12a6711adc2ed009fb0687ea447f9edc9d0ce9b9`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05197d8ed628728e4a93c7c6f52a0cafa2263039f4526e490b5f873167e1144`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b28a4909f7f0860e1395562cbebd921b09728397d7a533d1f7cd4b5d31e1671`  
		Last Modified: Fri, 12 Dec 2025 23:43:12 GMT  
		Size: 23.9 MB (23918113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926c23fb5c1c50e722a5b86e6ae921cd02d73d170dff76ff2af4910598654ae`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594a752382b75756d57cf29a40ab0bde12a567d548acf7cd83772f09c4a21930`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1087bd776bf52196852d02423f98f410d12929744cedd00d7c48c7c0b2113`  
		Last Modified: Fri, 12 Dec 2025 23:43:10 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e85bde05b43a43ab482a075807c5b38bbe7bf9b47871b3147d117cff05b772`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 11.4 MB (11431570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c0c8ea04bc96a986cc33445b9d46d8a5607e447352d26cc9bd8c0a8845fca4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:6c63e74fbbe6a6853d2eed17e74a22a1f27caa6652d65e73237c8cdae1584560
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835158901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31a8d2106c0d362d41e18b340f4ce9fcb284d2750fd96d7010599996e10f95a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Fri, 12 Dec 2025 23:42:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:42:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:42:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:35 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:42:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:42:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a59061a4bd19a5f5104deac5c13f08378f0d057b550fa44336edd48c297a30`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d45f349269329c39cb7f626e581200a0cfd951639d64b460dc496e827a02d3`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 496.4 KB (496422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbbd38f48aebab5ee03921c61d62bc51aafa5296de9f243a1b119cb5b9b59e8`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38e962b0dcf2e2174265dd10ed886b4ac610012a54d0a165b374784dfbfaf5b`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b233205356122f2ba9d651e4d85f51b9efc8720271061a670c3d376808be4df`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 19.4 MB (19421634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4696a1bc6b20cc354eebea761ac5c3e7bee2e41055c2310c9e1efda5acac04cc`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8453a804e2b4641b89e10a12a6711adc2ed009fb0687ea447f9edc9d0ce9b9`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05197d8ed628728e4a93c7c6f52a0cafa2263039f4526e490b5f873167e1144`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b28a4909f7f0860e1395562cbebd921b09728397d7a533d1f7cd4b5d31e1671`  
		Last Modified: Fri, 12 Dec 2025 23:43:12 GMT  
		Size: 23.9 MB (23918113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926c23fb5c1c50e722a5b86e6ae921cd02d73d170dff76ff2af4910598654ae`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594a752382b75756d57cf29a40ab0bde12a567d548acf7cd83772f09c4a21930`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1087bd776bf52196852d02423f98f410d12929744cedd00d7c48c7c0b2113`  
		Last Modified: Fri, 12 Dec 2025 23:43:10 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e85bde05b43a43ab482a075807c5b38bbe7bf9b47871b3147d117cff05b772`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 11.4 MB (11431570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:f862456b5cfe6c2b259f159ae0b967e1a05ad2839c2798b3c9b755e2447508dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:072f69cc9a1bc2cb016cd912ee5dcb075d0f2e73df576a46f98ddb1f3f8a4ea2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308280068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e356747fea9e9e69ddc2df399e0a31cb31c5c255da4f7f8ff52e08eef859a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Fri, 12 Dec 2025 23:51:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:51:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:51:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:33 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:51:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:43 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:51:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49db97996aeb50d6cc3bb59d05b2805a04f9a341f791d3bbf78f96c91ea6ea46`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e012252a5c78e6736aa02ede33d15956b820e11e10d32c0eed00f4ac4c0642ed`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 365.2 KB (365173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba990e6755d56a5110398c67645345164f3cb13a4f31f2c87cd0cf475b2fddc`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df48c7a2c9538324b83a4a6378f6ecbcf5c51d2b4c853c98b154d3d2e1fe23c`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9a30b43b8cff73e13f7e796431a6d59d40548fd5ed22e9f0f643554cffa66`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 19.4 MB (19430080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053e9422e23dca07aade3c64cf9355ecc9227c50dd075cde8a77bf5f588fdf07`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d53e5a50955843cf8df23bd9852867dc4e044732ab6a2c3dff445d30a03969`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6a3bffb040caaef43c930bcf019f71c62523c17c8c3aa21340ce83fd63c367`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5297cc0777d4cd44c02f2f373fa189394855ab3f6e99fb51e0e9b14dcbe7719`  
		Last Modified: Sat, 13 Dec 2025 00:10:41 GMT  
		Size: 23.9 MB (23916756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d343979aeb667bd44bc30f0385636c1525e1007c30d7a56b0c4b2929e986e3ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e484e796b3e881c2c53ab847de762b0acce3ce695452b588333031fd16f4722`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1d8d8a0183df8a67af7c17491af2ce9bcc2f1e5bed8a1b7337d9cc59d72a48`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e066997579a2dbc121185aac60816764e96c1cbce7d351630d1ae1a79062f7ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 11.4 MB (11435912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1`

```console
$ docker pull docker@sha256:7370a6c49b7e708fb969b422dffe6cdd78a9f0ff5b3bfba0e0cddce736c49eaf
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

### `docker:29.1` - linux; amd64

```console
$ docker pull docker@sha256:614db3c0aa1f5a2fe91d4bbbb0df8190c5d233d6ad55aa0f285c29f54227f7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136136542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8274856237f1b49083c42adab01ae804b00b8eeddb621e75b53e8c7a18657249`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:14 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6395790a96f25fe9ae60e8642bb53dc32742cc2a952240e2430c727343070f94`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 6.9 MB (6932404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0e7dad2234067bcdefdfbe8a95f9d27a127e90c2547a0b535e998e62492f9`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 92.5 KB (92451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d2dd2748ca8b7279cc840f1717a591f741f79ca77fccc303369e23381404e`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be03fb08c790242db2d11f5c8abd1e27779400315ae4bebf6812421eb196f424`  
		Last Modified: Fri, 12 Dec 2025 23:10:36 GMT  
		Size: 64.4 MB (64390653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969ded5ab7c174111a0938c32df0c859eae02e11a1f03b285260d4e52ada118`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15928226105bb78669d71594057c0a40684760f66de44e473fe4559e048a1fc4`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:d872ccf708c0c6cf248b60f3628d4f6c144e2b9b28d7249d5e99349e036598bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2e79926af9c2cfd84fb6eaa06ee2a235ee5389bbc8f0c528a68c05c925f98c`

```dockerfile
```

-	Layers:
	-	`sha256:dfa8b777c70191bcd2b044ff54627b657daadee8f5c1dfcae039cb25aa6d9e66`  
		Last Modified: Sat, 13 Dec 2025 03:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:e290522631fba31e8ef320a62d0efe0f7bd279c504aacea1b231502c56c75d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128368324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52adaa135524f86585c09c3b6ea713da7b19764a9bb3853687c4410ff4057193`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:01:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:01:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:01:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:01:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:01:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:01:06 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:29 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:29 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:29 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a442d3375c6cf3a0d64cab9a5657f13a2ad79d715217080e57d4091d88c4324`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 8.3 MB (8301082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d2ff8b4dcb5e27c0a3ebecc8f29e07008e917fc5a5a7a6dfeece3f50f8613`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf22d2b96392d2b3c9f1cb454ed14bc66a1dfdef830883f46ed5613c0133d4`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 17.6 MB (17563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be201cbc63828006213cbca3a3f8b91138447829d70553ea57b47fb7b36316`  
		Last Modified: Fri, 12 Dec 2025 23:01:28 GMT  
		Size: 21.5 MB (21476558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e492ed6855e1816d78b7edbd4cdc38ef0cb81d978dfc857129d58d22c754fa`  
		Last Modified: Fri, 12 Dec 2025 23:01:25 GMT  
		Size: 10.2 MB (10195786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50a36847c59872394550e672e167266ae450d58950ec050895f9a2b8b650e3`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836b06438ad83afcbbb80d394f9a68dc224a96dbc3f7446ef31113fbd4fc107`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844bcb311c659e5cab12e879fb055dd4d63aaca8e759553df1c68ad8f8572a0`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f78a51ea72b486ea303cfe9a35e0936165e64f6c1ce623050f1bbc03783827e`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 7.3 MB (7269237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150a1e8e9e07769ffd55ede4c3ebe7b37a7d4a52e59841483c2f1dc104a73cd`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 91.7 KB (91744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d880baf4277f9d0addd5734ad6cd8ef5e32b361ae8196dffbee590ccd63e28c2`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba95d05539ea20cd2ad894c3b01011b5412ac30470cf2067be3a4de6893fb49`  
		Last Modified: Fri, 12 Dec 2025 23:09:51 GMT  
		Size: 59.9 MB (59894425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d365292960a46a15ee408a118f8ed3443f9de61abacc32b1e1c93ca107c203b`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad152b473b5d59ed3116b07b37f35d4bc0fc85aa8364882c610816bea229f3bf`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:c70c7dcb7dfdb1cc89722c4c1299406e1924186e972fd94deb54abbd1052301a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bec62c6dbaf983fd287f9991784c3219e307aceca7be3d32fe32b63d7b2187f`

```dockerfile
```

-	Layers:
	-	`sha256:fff0c79b6617bada32062564279ba2c4c61cab0f5d7fb8bcdb5ac4e87f9f393c`  
		Last Modified: Sat, 13 Dec 2025 03:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:71a0b301e07cfb3145b58f5e33589420b2f0e643d9376d35097d4d402673c64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126466294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e849666bdf05465f46c218af24544c6a84be85d4505f05f1a67f2439df655afb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:48 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:22 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbf8f000eac737bf318d60725474e05cf5bb1d57c289c8f1a9fc5a087446bbb`  
		Last Modified: Fri, 12 Dec 2025 23:04:10 GMT  
		Size: 7.6 MB (7597999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c0b74efc53c5a11551937b3c0ac0e558dda2c21c713a42b1a8c90c83e929a`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26fc85eb088676c2237ad1410f2d06bf4167acef7e7573aa468e85f49ee8`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 17.6 MB (17552135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c0880b371ae9def4a59c648a03dc32de73c939a82863ed46189b5d3c1b26`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 21.5 MB (21454919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dfae8792ac984c5843e7a75359342e09ed6b06094284d3d9afef64ef8d37`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 10.2 MB (10188515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c8dcf60105513f337a71a7a302174c703f2ac4b01eca1a6976550cabbc9cb`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078bbc407a642525a8ecd8f3f56ec5f42ea4276b7984629db0dada8b0ecf69c`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091878b07b4fafc28f7778946a2e29d096eb34042255686f44fcadaea5d597`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e785e66500d9f73341d04a0d0fe01a7ca6a4ce3d3b9288e82242bc725426b`  
		Last Modified: Fri, 12 Dec 2025 23:10:40 GMT  
		Size: 6.6 MB (6570882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928ed8314751e2e9eaeabdc972d4af1311ab6177479d3b6f80a5539231796da7`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9abf1ec541ec0b256d5eab59239d0b754ddab5d999b8dc430585b6f948e604e`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233d3deeb4102367ed1ec89b7ef2fc760d574be2fc7fedd4ea2e4108be9aba6`  
		Last Modified: Fri, 12 Dec 2025 23:10:45 GMT  
		Size: 59.7 MB (59727126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b55b2d0cde4acdec0d0647c16445382a856fdacd9c1cd5fdf7116a5f96dbb4`  
		Last Modified: Fri, 12 Dec 2025 23:10:50 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603edd3336b192e57264b4a135254f9b4dc1a5761163fe26d86596342fe422de`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:0c9b638681007c9d6737a03cc64eac228cfd924c10100f3189602dd4d65d73bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70074d9836671bcf71409a77556f876fa92be1526c11bc44cf503e7077324561`

```dockerfile
```

-	Layers:
	-	`sha256:18a5d28b03d244c5685e86038be1cc676b25e374d481bfba7ced9ce1023ebe95`  
		Last Modified: Sat, 13 Dec 2025 03:07:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ae8fb276f238b912024b6b5805e3e244f0919648b835cf7a1ad0c1b791638ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126321327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b51d82ca438a87cf78f035539342acb921ff3b8a7c5c316c5dd827b52838dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1f8bb5ac9908d8a2f05285d5bafaaa09c4639ad5ec575f506b7f94eb9b027`  
		Last Modified: Fri, 12 Dec 2025 23:09:43 GMT  
		Size: 7.2 MB (7211487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07fdd52b461065d91e16e325ebe1351e98a49811bfe1953d3ffe9d71f66976`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 101.3 KB (101259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d775131bce9a8efbc68a01168997189db83ec2f6764633a853bb6c4013ba98b9`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1bdb364f96a9e042c2a09900dea9f490b2fd714dc314a9b36df5e470baa327`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 58.4 MB (58430278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039982dd10164d6a2e84e3eba3fd37ce736fbfcb0f9e03881c7ba02615b5c87`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22468ff67dbfccb6e8991c334fe5d9d379c964a9ecfe16c05d804125837727f8`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:3c36eabf6e66c492c055fbc625e84d44c47a923d35e2f46f5d13f8c90174aca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae5563a6811d6d3cc3a1e6303828b71d9608a6a4fc125183d83423348c5f2a6`

```dockerfile
```

-	Layers:
	-	`sha256:f88b5a51b8c8deb7c3b298f4e2252c16a18f817fb711be330fa64e81a65284e0`  
		Last Modified: Sat, 13 Dec 2025 03:07:37 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1-cli`

```console
$ docker pull docker@sha256:fef89d736d81ca03bb9bac2fabdc7bbf5f0b1485a708c94028225cb8623d1084
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

### `docker:29.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:460bd54747e38686f19906b2c7871d7a24159b2149fab3d2576d5cfd201cad73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64715034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4453f9079883af7ee6a02d1d59e76df1c5254647118c2fcd31dad73a7868a2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:18efc4ebd9cdbdf6b6ce77046066d86d2ca19db8332ee23cf54e560fbc3731bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76513174b1ca50e674ed0be90a756d3e124b07462362dbb3baab908e1537cb85`

```dockerfile
```

-	Layers:
	-	`sha256:7a2736719c9b6d24bbb2e67120ddc54c6a898296084a245f781f6e63d2158f2a`  
		Last Modified: Sat, 13 Dec 2025 00:07:29 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ed3d4022bcc3b84bda70aaae6c5f5fc5fcfe3c166b59a310eb546de5b1b93419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61106920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95404e10bb74578f403ba9578c56111c25597aa98a33490d2ea3bc7ac17c48b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:01:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:01:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:01:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:01:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:01:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:01:06 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a442d3375c6cf3a0d64cab9a5657f13a2ad79d715217080e57d4091d88c4324`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 8.3 MB (8301082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d2ff8b4dcb5e27c0a3ebecc8f29e07008e917fc5a5a7a6dfeece3f50f8613`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf22d2b96392d2b3c9f1cb454ed14bc66a1dfdef830883f46ed5613c0133d4`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 17.6 MB (17563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be201cbc63828006213cbca3a3f8b91138447829d70553ea57b47fb7b36316`  
		Last Modified: Fri, 12 Dec 2025 23:01:28 GMT  
		Size: 21.5 MB (21476558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e492ed6855e1816d78b7edbd4cdc38ef0cb81d978dfc857129d58d22c754fa`  
		Last Modified: Fri, 12 Dec 2025 23:01:25 GMT  
		Size: 10.2 MB (10195786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50a36847c59872394550e672e167266ae450d58950ec050895f9a2b8b650e3`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836b06438ad83afcbbb80d394f9a68dc224a96dbc3f7446ef31113fbd4fc107`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844bcb311c659e5cab12e879fb055dd4d63aaca8e759553df1c68ad8f8572a0`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:050b2baec8a743beab976d109ade8bbd2255f907abf6ed7c521825f031ebfb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8711322ffdbfc1512d835bdbb3d1aab5d63286fc0edb80507d74fd721e7093`

```dockerfile
```

-	Layers:
	-	`sha256:3462d33a19054d0414ea3eb7bdc0b282352efc598442d721e9c2f5e3e7af653d`  
		Last Modified: Sat, 13 Dec 2025 00:07:32 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:7b6ba4909381a6b3ca8380db56b5e0566e94241d29ad12196b4871bcd0751e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60074186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273d97076d24ffa898e7608f96246fe2f9c6a75ca258cfa233e728c2a3d00b89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbf8f000eac737bf318d60725474e05cf5bb1d57c289c8f1a9fc5a087446bbb`  
		Last Modified: Fri, 12 Dec 2025 23:04:10 GMT  
		Size: 7.6 MB (7597999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c0b74efc53c5a11551937b3c0ac0e558dda2c21c713a42b1a8c90c83e929a`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26fc85eb088676c2237ad1410f2d06bf4167acef7e7573aa468e85f49ee8`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 17.6 MB (17552135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c0880b371ae9def4a59c648a03dc32de73c939a82863ed46189b5d3c1b26`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 21.5 MB (21454919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dfae8792ac984c5843e7a75359342e09ed6b06094284d3d9afef64ef8d37`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 10.2 MB (10188515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c8dcf60105513f337a71a7a302174c703f2ac4b01eca1a6976550cabbc9cb`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078bbc407a642525a8ecd8f3f56ec5f42ea4276b7984629db0dada8b0ecf69c`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091878b07b4fafc28f7778946a2e29d096eb34042255686f44fcadaea5d597`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2cd5fe33035b9b245d7633d313b6c10663c4b4a15539e1049ed543ae30b0895b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0eafce598b67ac57b3e56ed0966055137da7f5a73489083c1c5a72c6e7febc`

```dockerfile
```

-	Layers:
	-	`sha256:5453b680a91095b07fa3308adfcd6460856cd978700e2fcac203bbcd490a8b4c`  
		Last Modified: Sat, 13 Dec 2025 00:07:35 GMT  
		Size: 38.2 KB (38220 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cd7a8fb27fb7769bd1e99c859cd81b6b5907a48159fe0c5978d36dac92832ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60572305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9fc8e3c559250bb84f436eb83db1fca5000b54667762710ed0053847f4df6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3fc751e1389e0e81e12e5a50e51cd4c8c9f09bc6f5c22868892d33f362494bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d129b4abe449d1af4183719346aec5b3c50a1a8a0a42844f5299279d54a22a`

```dockerfile
```

-	Layers:
	-	`sha256:847c010774232d19f586d313e7adf4e52cf76fbf7d80543c31098ce2d449ddbc`  
		Last Modified: Sat, 13 Dec 2025 00:08:01 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1-dind`

```console
$ docker pull docker@sha256:7370a6c49b7e708fb969b422dffe6cdd78a9f0ff5b3bfba0e0cddce736c49eaf
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

### `docker:29.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:614db3c0aa1f5a2fe91d4bbbb0df8190c5d233d6ad55aa0f285c29f54227f7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136136542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8274856237f1b49083c42adab01ae804b00b8eeddb621e75b53e8c7a18657249`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:14 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6395790a96f25fe9ae60e8642bb53dc32742cc2a952240e2430c727343070f94`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 6.9 MB (6932404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0e7dad2234067bcdefdfbe8a95f9d27a127e90c2547a0b535e998e62492f9`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 92.5 KB (92451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d2dd2748ca8b7279cc840f1717a591f741f79ca77fccc303369e23381404e`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be03fb08c790242db2d11f5c8abd1e27779400315ae4bebf6812421eb196f424`  
		Last Modified: Fri, 12 Dec 2025 23:10:36 GMT  
		Size: 64.4 MB (64390653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969ded5ab7c174111a0938c32df0c859eae02e11a1f03b285260d4e52ada118`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15928226105bb78669d71594057c0a40684760f66de44e473fe4559e048a1fc4`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d872ccf708c0c6cf248b60f3628d4f6c144e2b9b28d7249d5e99349e036598bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2e79926af9c2cfd84fb6eaa06ee2a235ee5389bbc8f0c528a68c05c925f98c`

```dockerfile
```

-	Layers:
	-	`sha256:dfa8b777c70191bcd2b044ff54627b657daadee8f5c1dfcae039cb25aa6d9e66`  
		Last Modified: Sat, 13 Dec 2025 03:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:e290522631fba31e8ef320a62d0efe0f7bd279c504aacea1b231502c56c75d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128368324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52adaa135524f86585c09c3b6ea713da7b19764a9bb3853687c4410ff4057193`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:01:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:01:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:01:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:01:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:01:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:01:06 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:29 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:29 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:29 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a442d3375c6cf3a0d64cab9a5657f13a2ad79d715217080e57d4091d88c4324`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 8.3 MB (8301082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d2ff8b4dcb5e27c0a3ebecc8f29e07008e917fc5a5a7a6dfeece3f50f8613`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf22d2b96392d2b3c9f1cb454ed14bc66a1dfdef830883f46ed5613c0133d4`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 17.6 MB (17563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be201cbc63828006213cbca3a3f8b91138447829d70553ea57b47fb7b36316`  
		Last Modified: Fri, 12 Dec 2025 23:01:28 GMT  
		Size: 21.5 MB (21476558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e492ed6855e1816d78b7edbd4cdc38ef0cb81d978dfc857129d58d22c754fa`  
		Last Modified: Fri, 12 Dec 2025 23:01:25 GMT  
		Size: 10.2 MB (10195786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50a36847c59872394550e672e167266ae450d58950ec050895f9a2b8b650e3`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836b06438ad83afcbbb80d394f9a68dc224a96dbc3f7446ef31113fbd4fc107`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844bcb311c659e5cab12e879fb055dd4d63aaca8e759553df1c68ad8f8572a0`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f78a51ea72b486ea303cfe9a35e0936165e64f6c1ce623050f1bbc03783827e`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 7.3 MB (7269237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150a1e8e9e07769ffd55ede4c3ebe7b37a7d4a52e59841483c2f1dc104a73cd`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 91.7 KB (91744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d880baf4277f9d0addd5734ad6cd8ef5e32b361ae8196dffbee590ccd63e28c2`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba95d05539ea20cd2ad894c3b01011b5412ac30470cf2067be3a4de6893fb49`  
		Last Modified: Fri, 12 Dec 2025 23:09:51 GMT  
		Size: 59.9 MB (59894425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d365292960a46a15ee408a118f8ed3443f9de61abacc32b1e1c93ca107c203b`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad152b473b5d59ed3116b07b37f35d4bc0fc85aa8364882c610816bea229f3bf`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:c70c7dcb7dfdb1cc89722c4c1299406e1924186e972fd94deb54abbd1052301a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bec62c6dbaf983fd287f9991784c3219e307aceca7be3d32fe32b63d7b2187f`

```dockerfile
```

-	Layers:
	-	`sha256:fff0c79b6617bada32062564279ba2c4c61cab0f5d7fb8bcdb5ac4e87f9f393c`  
		Last Modified: Sat, 13 Dec 2025 03:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:71a0b301e07cfb3145b58f5e33589420b2f0e643d9376d35097d4d402673c64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126466294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e849666bdf05465f46c218af24544c6a84be85d4505f05f1a67f2439df655afb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:48 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:22 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbf8f000eac737bf318d60725474e05cf5bb1d57c289c8f1a9fc5a087446bbb`  
		Last Modified: Fri, 12 Dec 2025 23:04:10 GMT  
		Size: 7.6 MB (7597999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c0b74efc53c5a11551937b3c0ac0e558dda2c21c713a42b1a8c90c83e929a`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26fc85eb088676c2237ad1410f2d06bf4167acef7e7573aa468e85f49ee8`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 17.6 MB (17552135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c0880b371ae9def4a59c648a03dc32de73c939a82863ed46189b5d3c1b26`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 21.5 MB (21454919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dfae8792ac984c5843e7a75359342e09ed6b06094284d3d9afef64ef8d37`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 10.2 MB (10188515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c8dcf60105513f337a71a7a302174c703f2ac4b01eca1a6976550cabbc9cb`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078bbc407a642525a8ecd8f3f56ec5f42ea4276b7984629db0dada8b0ecf69c`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091878b07b4fafc28f7778946a2e29d096eb34042255686f44fcadaea5d597`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e785e66500d9f73341d04a0d0fe01a7ca6a4ce3d3b9288e82242bc725426b`  
		Last Modified: Fri, 12 Dec 2025 23:10:40 GMT  
		Size: 6.6 MB (6570882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928ed8314751e2e9eaeabdc972d4af1311ab6177479d3b6f80a5539231796da7`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9abf1ec541ec0b256d5eab59239d0b754ddab5d999b8dc430585b6f948e604e`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233d3deeb4102367ed1ec89b7ef2fc760d574be2fc7fedd4ea2e4108be9aba6`  
		Last Modified: Fri, 12 Dec 2025 23:10:45 GMT  
		Size: 59.7 MB (59727126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b55b2d0cde4acdec0d0647c16445382a856fdacd9c1cd5fdf7116a5f96dbb4`  
		Last Modified: Fri, 12 Dec 2025 23:10:50 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603edd3336b192e57264b4a135254f9b4dc1a5761163fe26d86596342fe422de`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0c9b638681007c9d6737a03cc64eac228cfd924c10100f3189602dd4d65d73bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70074d9836671bcf71409a77556f876fa92be1526c11bc44cf503e7077324561`

```dockerfile
```

-	Layers:
	-	`sha256:18a5d28b03d244c5685e86038be1cc676b25e374d481bfba7ced9ce1023ebe95`  
		Last Modified: Sat, 13 Dec 2025 03:07:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ae8fb276f238b912024b6b5805e3e244f0919648b835cf7a1ad0c1b791638ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126321327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b51d82ca438a87cf78f035539342acb921ff3b8a7c5c316c5dd827b52838dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1f8bb5ac9908d8a2f05285d5bafaaa09c4639ad5ec575f506b7f94eb9b027`  
		Last Modified: Fri, 12 Dec 2025 23:09:43 GMT  
		Size: 7.2 MB (7211487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07fdd52b461065d91e16e325ebe1351e98a49811bfe1953d3ffe9d71f66976`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 101.3 KB (101259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d775131bce9a8efbc68a01168997189db83ec2f6764633a853bb6c4013ba98b9`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1bdb364f96a9e042c2a09900dea9f490b2fd714dc314a9b36df5e470baa327`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 58.4 MB (58430278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039982dd10164d6a2e84e3eba3fd37ce736fbfcb0f9e03881c7ba02615b5c87`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22468ff67dbfccb6e8991c334fe5d9d379c964a9ecfe16c05d804125837727f8`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3c36eabf6e66c492c055fbc625e84d44c47a923d35e2f46f5d13f8c90174aca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae5563a6811d6d3cc3a1e6303828b71d9608a6a4fc125183d83423348c5f2a6`

```dockerfile
```

-	Layers:
	-	`sha256:f88b5a51b8c8deb7c3b298f4e2252c16a18f817fb711be330fa64e81a65284e0`  
		Last Modified: Sat, 13 Dec 2025 03:07:37 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1-dind-rootless`

```console
$ docker pull docker@sha256:ac12412d8bc07bdbc71e1bd730572dc5010a5d2116987775b30f849d1268380e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:09950db32d89c1662f1970578f51562812eab9a3eb50feb7326519f7e5514235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156928803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17a49738c68db9b440e165269dc75f5f3e74a89e9a75426199cd466b0383cd6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:14 GMT
CMD []
# Sat, 13 Dec 2025 00:10:12 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 13 Dec 2025 00:10:12 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 13 Dec 2025 00:10:12 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 13 Dec 2025 00:10:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 13 Dec 2025 00:10:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 13 Dec 2025 00:10:13 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 13 Dec 2025 00:10:13 GMT
USER rootless
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6395790a96f25fe9ae60e8642bb53dc32742cc2a952240e2430c727343070f94`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 6.9 MB (6932404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0e7dad2234067bcdefdfbe8a95f9d27a127e90c2547a0b535e998e62492f9`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 92.5 KB (92451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d2dd2748ca8b7279cc840f1717a591f741f79ca77fccc303369e23381404e`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be03fb08c790242db2d11f5c8abd1e27779400315ae4bebf6812421eb196f424`  
		Last Modified: Fri, 12 Dec 2025 23:10:36 GMT  
		Size: 64.4 MB (64390653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969ded5ab7c174111a0938c32df0c859eae02e11a1f03b285260d4e52ada118`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15928226105bb78669d71594057c0a40684760f66de44e473fe4559e048a1fc4`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7efc67e74d7bff7198949770096adae0c34ad7c6a32faa6e3d0bab24e69da51`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 3.4 MB (3419931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0ea6cd17928c2035157de458119f33ee511ec1deee23008735895ce2472b79`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b30c307447754a05b3912b60fa4a43ebe6eb174bb107be0d85866ce5cf6d0b6`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab6e3723d2a693205fe1725bd19abcfbfd2ac1331a374d8b35b7897742941c5`  
		Last Modified: Sat, 13 Dec 2025 00:10:37 GMT  
		Size: 17.4 MB (17370991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7db2853efa7da1fc8d7b3143c0f861bdc77ee5a9cce03278ff21f1568ef69c5`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:336e04652a588e2ad4e195e403ef93c675ba97007c75e40a9efe962cb4f16bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd1e5b602cf458f135106fdc1b6bee98d42185597cd98c67410b6c1c42dc34f`

```dockerfile
```

-	Layers:
	-	`sha256:e3a762cb9f51fe6d372134b550c76079147291d858530a914cc826e7d8dbc1d9`  
		Last Modified: Sat, 13 Dec 2025 03:07:42 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7deb6a567eeef7d5a72412f239f2170d024ede941b350b13f24ebf9abc29721e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147425780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229ad388f6f6b781e7a9b6825675f4deeb04ea90f1123729e79549a7b32b83ac`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:25 GMT
CMD []
# Sat, 13 Dec 2025 00:09:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 13 Dec 2025 00:09:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 13 Dec 2025 00:09:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 13 Dec 2025 00:10:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 13 Dec 2025 00:10:01 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 13 Dec 2025 00:10:01 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 13 Dec 2025 00:10:01 GMT
USER rootless
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1f8bb5ac9908d8a2f05285d5bafaaa09c4639ad5ec575f506b7f94eb9b027`  
		Last Modified: Fri, 12 Dec 2025 23:09:43 GMT  
		Size: 7.2 MB (7211487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07fdd52b461065d91e16e325ebe1351e98a49811bfe1953d3ffe9d71f66976`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 101.3 KB (101259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d775131bce9a8efbc68a01168997189db83ec2f6764633a853bb6c4013ba98b9`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1bdb364f96a9e042c2a09900dea9f490b2fd714dc314a9b36df5e470baa327`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 58.4 MB (58430278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039982dd10164d6a2e84e3eba3fd37ce736fbfcb0f9e03881c7ba02615b5c87`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22468ff67dbfccb6e8991c334fe5d9d379c964a9ecfe16c05d804125837727f8`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb2d13730b1a2b9437f55aa38844a2d4f3a41baff03b9ba200fd6c8e3640f65`  
		Last Modified: Sat, 13 Dec 2025 00:10:27 GMT  
		Size: 3.4 MB (3394382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c5eda520ed158582d67f72a42c82eef1d312c24f5fb51f16441c4772825971`  
		Last Modified: Sat, 13 Dec 2025 00:10:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05db2d742efc92d52e078c87f0af299e70fb014fbfaea3a18b757374eca9af`  
		Last Modified: Sat, 13 Dec 2025 00:10:27 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9af16ab409354af0d1a5b9a8dd6362e6886e59680f35e8fc253d99c504af99`  
		Last Modified: Sat, 13 Dec 2025 00:10:32 GMT  
		Size: 17.7 MB (17708729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffd4a2a8cc857d1398fdf583e20112730537572a29d8c9100512be073ec09d8`  
		Last Modified: Sat, 13 Dec 2025 00:10:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6eab544cd873580b808013fbe86c7cc254767cc99c60313d1cd9f4e5eccb9f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c814e243bbda6587996667fdd159361b2cc27f15e889e349a1976482785bda18`

```dockerfile
```

-	Layers:
	-	`sha256:3a3842cd2beb5724ad7a78418740bfd432103bce0f213347880883022e4a0094`  
		Last Modified: Sat, 13 Dec 2025 03:07:45 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1-windowsservercore`

```console
$ docker pull docker@sha256:24e3252850071e0729b50e765be6eb141aec202a2709217891272b9d2a8efb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `docker:29.1-windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:072f69cc9a1bc2cb016cd912ee5dcb075d0f2e73df576a46f98ddb1f3f8a4ea2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308280068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e356747fea9e9e69ddc2df399e0a31cb31c5c255da4f7f8ff52e08eef859a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Fri, 12 Dec 2025 23:51:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:51:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:51:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:33 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:51:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:43 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:51:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49db97996aeb50d6cc3bb59d05b2805a04f9a341f791d3bbf78f96c91ea6ea46`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e012252a5c78e6736aa02ede33d15956b820e11e10d32c0eed00f4ac4c0642ed`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 365.2 KB (365173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba990e6755d56a5110398c67645345164f3cb13a4f31f2c87cd0cf475b2fddc`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df48c7a2c9538324b83a4a6378f6ecbcf5c51d2b4c853c98b154d3d2e1fe23c`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9a30b43b8cff73e13f7e796431a6d59d40548fd5ed22e9f0f643554cffa66`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 19.4 MB (19430080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053e9422e23dca07aade3c64cf9355ecc9227c50dd075cde8a77bf5f588fdf07`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d53e5a50955843cf8df23bd9852867dc4e044732ab6a2c3dff445d30a03969`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6a3bffb040caaef43c930bcf019f71c62523c17c8c3aa21340ce83fd63c367`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5297cc0777d4cd44c02f2f373fa189394855ab3f6e99fb51e0e9b14dcbe7719`  
		Last Modified: Sat, 13 Dec 2025 00:10:41 GMT  
		Size: 23.9 MB (23916756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d343979aeb667bd44bc30f0385636c1525e1007c30d7a56b0c4b2929e986e3ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e484e796b3e881c2c53ab847de762b0acce3ce695452b588333031fd16f4722`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1d8d8a0183df8a67af7c17491af2ce9bcc2f1e5bed8a1b7337d9cc59d72a48`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e066997579a2dbc121185aac60816764e96c1cbce7d351630d1ae1a79062f7ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 11.4 MB (11435912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.1-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:6c63e74fbbe6a6853d2eed17e74a22a1f27caa6652d65e73237c8cdae1584560
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835158901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31a8d2106c0d362d41e18b340f4ce9fcb284d2750fd96d7010599996e10f95a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Fri, 12 Dec 2025 23:42:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:42:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:42:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:35 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:42:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:42:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a59061a4bd19a5f5104deac5c13f08378f0d057b550fa44336edd48c297a30`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d45f349269329c39cb7f626e581200a0cfd951639d64b460dc496e827a02d3`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 496.4 KB (496422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbbd38f48aebab5ee03921c61d62bc51aafa5296de9f243a1b119cb5b9b59e8`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38e962b0dcf2e2174265dd10ed886b4ac610012a54d0a165b374784dfbfaf5b`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b233205356122f2ba9d651e4d85f51b9efc8720271061a670c3d376808be4df`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 19.4 MB (19421634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4696a1bc6b20cc354eebea761ac5c3e7bee2e41055c2310c9e1efda5acac04cc`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8453a804e2b4641b89e10a12a6711adc2ed009fb0687ea447f9edc9d0ce9b9`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05197d8ed628728e4a93c7c6f52a0cafa2263039f4526e490b5f873167e1144`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b28a4909f7f0860e1395562cbebd921b09728397d7a533d1f7cd4b5d31e1671`  
		Last Modified: Fri, 12 Dec 2025 23:43:12 GMT  
		Size: 23.9 MB (23918113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926c23fb5c1c50e722a5b86e6ae921cd02d73d170dff76ff2af4910598654ae`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594a752382b75756d57cf29a40ab0bde12a567d548acf7cd83772f09c4a21930`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1087bd776bf52196852d02423f98f410d12929744cedd00d7c48c7c0b2113`  
		Last Modified: Fri, 12 Dec 2025 23:43:10 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e85bde05b43a43ab482a075807c5b38bbe7bf9b47871b3147d117cff05b772`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 11.4 MB (11431570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c0c8ea04bc96a986cc33445b9d46d8a5607e447352d26cc9bd8c0a8845fca4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `docker:29.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:6c63e74fbbe6a6853d2eed17e74a22a1f27caa6652d65e73237c8cdae1584560
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835158901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31a8d2106c0d362d41e18b340f4ce9fcb284d2750fd96d7010599996e10f95a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Fri, 12 Dec 2025 23:42:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:42:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:42:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:35 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:42:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:42:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a59061a4bd19a5f5104deac5c13f08378f0d057b550fa44336edd48c297a30`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d45f349269329c39cb7f626e581200a0cfd951639d64b460dc496e827a02d3`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 496.4 KB (496422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbbd38f48aebab5ee03921c61d62bc51aafa5296de9f243a1b119cb5b9b59e8`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38e962b0dcf2e2174265dd10ed886b4ac610012a54d0a165b374784dfbfaf5b`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b233205356122f2ba9d651e4d85f51b9efc8720271061a670c3d376808be4df`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 19.4 MB (19421634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4696a1bc6b20cc354eebea761ac5c3e7bee2e41055c2310c9e1efda5acac04cc`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8453a804e2b4641b89e10a12a6711adc2ed009fb0687ea447f9edc9d0ce9b9`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05197d8ed628728e4a93c7c6f52a0cafa2263039f4526e490b5f873167e1144`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b28a4909f7f0860e1395562cbebd921b09728397d7a533d1f7cd4b5d31e1671`  
		Last Modified: Fri, 12 Dec 2025 23:43:12 GMT  
		Size: 23.9 MB (23918113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926c23fb5c1c50e722a5b86e6ae921cd02d73d170dff76ff2af4910598654ae`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594a752382b75756d57cf29a40ab0bde12a567d548acf7cd83772f09c4a21930`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1087bd776bf52196852d02423f98f410d12929744cedd00d7c48c7c0b2113`  
		Last Modified: Fri, 12 Dec 2025 23:43:10 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e85bde05b43a43ab482a075807c5b38bbe7bf9b47871b3147d117cff05b772`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 11.4 MB (11431570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:f862456b5cfe6c2b259f159ae0b967e1a05ad2839c2798b3c9b755e2447508dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `docker:29.1-windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:072f69cc9a1bc2cb016cd912ee5dcb075d0f2e73df576a46f98ddb1f3f8a4ea2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308280068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e356747fea9e9e69ddc2df399e0a31cb31c5c255da4f7f8ff52e08eef859a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Fri, 12 Dec 2025 23:51:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:51:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:51:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:33 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:51:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:43 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:51:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49db97996aeb50d6cc3bb59d05b2805a04f9a341f791d3bbf78f96c91ea6ea46`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e012252a5c78e6736aa02ede33d15956b820e11e10d32c0eed00f4ac4c0642ed`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 365.2 KB (365173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba990e6755d56a5110398c67645345164f3cb13a4f31f2c87cd0cf475b2fddc`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df48c7a2c9538324b83a4a6378f6ecbcf5c51d2b4c853c98b154d3d2e1fe23c`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9a30b43b8cff73e13f7e796431a6d59d40548fd5ed22e9f0f643554cffa66`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 19.4 MB (19430080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053e9422e23dca07aade3c64cf9355ecc9227c50dd075cde8a77bf5f588fdf07`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d53e5a50955843cf8df23bd9852867dc4e044732ab6a2c3dff445d30a03969`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6a3bffb040caaef43c930bcf019f71c62523c17c8c3aa21340ce83fd63c367`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5297cc0777d4cd44c02f2f373fa189394855ab3f6e99fb51e0e9b14dcbe7719`  
		Last Modified: Sat, 13 Dec 2025 00:10:41 GMT  
		Size: 23.9 MB (23916756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d343979aeb667bd44bc30f0385636c1525e1007c30d7a56b0c4b2929e986e3ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e484e796b3e881c2c53ab847de762b0acce3ce695452b588333031fd16f4722`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1d8d8a0183df8a67af7c17491af2ce9bcc2f1e5bed8a1b7337d9cc59d72a48`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e066997579a2dbc121185aac60816764e96c1cbce7d351630d1ae1a79062f7ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 11.4 MB (11435912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1.3`

```console
$ docker pull docker@sha256:7370a6c49b7e708fb969b422dffe6cdd78a9f0ff5b3bfba0e0cddce736c49eaf
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

### `docker:29.1.3` - linux; amd64

```console
$ docker pull docker@sha256:614db3c0aa1f5a2fe91d4bbbb0df8190c5d233d6ad55aa0f285c29f54227f7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136136542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8274856237f1b49083c42adab01ae804b00b8eeddb621e75b53e8c7a18657249`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:14 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6395790a96f25fe9ae60e8642bb53dc32742cc2a952240e2430c727343070f94`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 6.9 MB (6932404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0e7dad2234067bcdefdfbe8a95f9d27a127e90c2547a0b535e998e62492f9`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 92.5 KB (92451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d2dd2748ca8b7279cc840f1717a591f741f79ca77fccc303369e23381404e`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be03fb08c790242db2d11f5c8abd1e27779400315ae4bebf6812421eb196f424`  
		Last Modified: Fri, 12 Dec 2025 23:10:36 GMT  
		Size: 64.4 MB (64390653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969ded5ab7c174111a0938c32df0c859eae02e11a1f03b285260d4e52ada118`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15928226105bb78669d71594057c0a40684760f66de44e473fe4559e048a1fc4`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3` - unknown; unknown

```console
$ docker pull docker@sha256:d872ccf708c0c6cf248b60f3628d4f6c144e2b9b28d7249d5e99349e036598bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2e79926af9c2cfd84fb6eaa06ee2a235ee5389bbc8f0c528a68c05c925f98c`

```dockerfile
```

-	Layers:
	-	`sha256:dfa8b777c70191bcd2b044ff54627b657daadee8f5c1dfcae039cb25aa6d9e66`  
		Last Modified: Sat, 13 Dec 2025 03:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3` - linux; arm variant v6

```console
$ docker pull docker@sha256:e290522631fba31e8ef320a62d0efe0f7bd279c504aacea1b231502c56c75d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128368324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52adaa135524f86585c09c3b6ea713da7b19764a9bb3853687c4410ff4057193`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:01:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:01:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:01:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:01:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:01:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:01:06 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:29 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:29 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:29 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a442d3375c6cf3a0d64cab9a5657f13a2ad79d715217080e57d4091d88c4324`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 8.3 MB (8301082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d2ff8b4dcb5e27c0a3ebecc8f29e07008e917fc5a5a7a6dfeece3f50f8613`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf22d2b96392d2b3c9f1cb454ed14bc66a1dfdef830883f46ed5613c0133d4`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 17.6 MB (17563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be201cbc63828006213cbca3a3f8b91138447829d70553ea57b47fb7b36316`  
		Last Modified: Fri, 12 Dec 2025 23:01:28 GMT  
		Size: 21.5 MB (21476558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e492ed6855e1816d78b7edbd4cdc38ef0cb81d978dfc857129d58d22c754fa`  
		Last Modified: Fri, 12 Dec 2025 23:01:25 GMT  
		Size: 10.2 MB (10195786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50a36847c59872394550e672e167266ae450d58950ec050895f9a2b8b650e3`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836b06438ad83afcbbb80d394f9a68dc224a96dbc3f7446ef31113fbd4fc107`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844bcb311c659e5cab12e879fb055dd4d63aaca8e759553df1c68ad8f8572a0`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f78a51ea72b486ea303cfe9a35e0936165e64f6c1ce623050f1bbc03783827e`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 7.3 MB (7269237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150a1e8e9e07769ffd55ede4c3ebe7b37a7d4a52e59841483c2f1dc104a73cd`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 91.7 KB (91744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d880baf4277f9d0addd5734ad6cd8ef5e32b361ae8196dffbee590ccd63e28c2`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba95d05539ea20cd2ad894c3b01011b5412ac30470cf2067be3a4de6893fb49`  
		Last Modified: Fri, 12 Dec 2025 23:09:51 GMT  
		Size: 59.9 MB (59894425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d365292960a46a15ee408a118f8ed3443f9de61abacc32b1e1c93ca107c203b`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad152b473b5d59ed3116b07b37f35d4bc0fc85aa8364882c610816bea229f3bf`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3` - unknown; unknown

```console
$ docker pull docker@sha256:c70c7dcb7dfdb1cc89722c4c1299406e1924186e972fd94deb54abbd1052301a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bec62c6dbaf983fd287f9991784c3219e307aceca7be3d32fe32b63d7b2187f`

```dockerfile
```

-	Layers:
	-	`sha256:fff0c79b6617bada32062564279ba2c4c61cab0f5d7fb8bcdb5ac4e87f9f393c`  
		Last Modified: Sat, 13 Dec 2025 03:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3` - linux; arm variant v7

```console
$ docker pull docker@sha256:71a0b301e07cfb3145b58f5e33589420b2f0e643d9376d35097d4d402673c64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126466294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e849666bdf05465f46c218af24544c6a84be85d4505f05f1a67f2439df655afb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:48 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:22 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbf8f000eac737bf318d60725474e05cf5bb1d57c289c8f1a9fc5a087446bbb`  
		Last Modified: Fri, 12 Dec 2025 23:04:10 GMT  
		Size: 7.6 MB (7597999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c0b74efc53c5a11551937b3c0ac0e558dda2c21c713a42b1a8c90c83e929a`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26fc85eb088676c2237ad1410f2d06bf4167acef7e7573aa468e85f49ee8`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 17.6 MB (17552135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c0880b371ae9def4a59c648a03dc32de73c939a82863ed46189b5d3c1b26`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 21.5 MB (21454919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dfae8792ac984c5843e7a75359342e09ed6b06094284d3d9afef64ef8d37`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 10.2 MB (10188515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c8dcf60105513f337a71a7a302174c703f2ac4b01eca1a6976550cabbc9cb`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078bbc407a642525a8ecd8f3f56ec5f42ea4276b7984629db0dada8b0ecf69c`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091878b07b4fafc28f7778946a2e29d096eb34042255686f44fcadaea5d597`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e785e66500d9f73341d04a0d0fe01a7ca6a4ce3d3b9288e82242bc725426b`  
		Last Modified: Fri, 12 Dec 2025 23:10:40 GMT  
		Size: 6.6 MB (6570882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928ed8314751e2e9eaeabdc972d4af1311ab6177479d3b6f80a5539231796da7`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9abf1ec541ec0b256d5eab59239d0b754ddab5d999b8dc430585b6f948e604e`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233d3deeb4102367ed1ec89b7ef2fc760d574be2fc7fedd4ea2e4108be9aba6`  
		Last Modified: Fri, 12 Dec 2025 23:10:45 GMT  
		Size: 59.7 MB (59727126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b55b2d0cde4acdec0d0647c16445382a856fdacd9c1cd5fdf7116a5f96dbb4`  
		Last Modified: Fri, 12 Dec 2025 23:10:50 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603edd3336b192e57264b4a135254f9b4dc1a5761163fe26d86596342fe422de`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3` - unknown; unknown

```console
$ docker pull docker@sha256:0c9b638681007c9d6737a03cc64eac228cfd924c10100f3189602dd4d65d73bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70074d9836671bcf71409a77556f876fa92be1526c11bc44cf503e7077324561`

```dockerfile
```

-	Layers:
	-	`sha256:18a5d28b03d244c5685e86038be1cc676b25e374d481bfba7ced9ce1023ebe95`  
		Last Modified: Sat, 13 Dec 2025 03:07:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ae8fb276f238b912024b6b5805e3e244f0919648b835cf7a1ad0c1b791638ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126321327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b51d82ca438a87cf78f035539342acb921ff3b8a7c5c316c5dd827b52838dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1f8bb5ac9908d8a2f05285d5bafaaa09c4639ad5ec575f506b7f94eb9b027`  
		Last Modified: Fri, 12 Dec 2025 23:09:43 GMT  
		Size: 7.2 MB (7211487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07fdd52b461065d91e16e325ebe1351e98a49811bfe1953d3ffe9d71f66976`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 101.3 KB (101259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d775131bce9a8efbc68a01168997189db83ec2f6764633a853bb6c4013ba98b9`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1bdb364f96a9e042c2a09900dea9f490b2fd714dc314a9b36df5e470baa327`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 58.4 MB (58430278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039982dd10164d6a2e84e3eba3fd37ce736fbfcb0f9e03881c7ba02615b5c87`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22468ff67dbfccb6e8991c334fe5d9d379c964a9ecfe16c05d804125837727f8`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3` - unknown; unknown

```console
$ docker pull docker@sha256:3c36eabf6e66c492c055fbc625e84d44c47a923d35e2f46f5d13f8c90174aca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae5563a6811d6d3cc3a1e6303828b71d9608a6a4fc125183d83423348c5f2a6`

```dockerfile
```

-	Layers:
	-	`sha256:f88b5a51b8c8deb7c3b298f4e2252c16a18f817fb711be330fa64e81a65284e0`  
		Last Modified: Sat, 13 Dec 2025 03:07:37 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1.3-alpine3.23`

```console
$ docker pull docker@sha256:7370a6c49b7e708fb969b422dffe6cdd78a9f0ff5b3bfba0e0cddce736c49eaf
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

### `docker:29.1.3-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:614db3c0aa1f5a2fe91d4bbbb0df8190c5d233d6ad55aa0f285c29f54227f7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136136542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8274856237f1b49083c42adab01ae804b00b8eeddb621e75b53e8c7a18657249`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:14 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6395790a96f25fe9ae60e8642bb53dc32742cc2a952240e2430c727343070f94`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 6.9 MB (6932404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0e7dad2234067bcdefdfbe8a95f9d27a127e90c2547a0b535e998e62492f9`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 92.5 KB (92451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d2dd2748ca8b7279cc840f1717a591f741f79ca77fccc303369e23381404e`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be03fb08c790242db2d11f5c8abd1e27779400315ae4bebf6812421eb196f424`  
		Last Modified: Fri, 12 Dec 2025 23:10:36 GMT  
		Size: 64.4 MB (64390653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969ded5ab7c174111a0938c32df0c859eae02e11a1f03b285260d4e52ada118`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15928226105bb78669d71594057c0a40684760f66de44e473fe4559e048a1fc4`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:d872ccf708c0c6cf248b60f3628d4f6c144e2b9b28d7249d5e99349e036598bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2e79926af9c2cfd84fb6eaa06ee2a235ee5389bbc8f0c528a68c05c925f98c`

```dockerfile
```

-	Layers:
	-	`sha256:dfa8b777c70191bcd2b044ff54627b657daadee8f5c1dfcae039cb25aa6d9e66`  
		Last Modified: Sat, 13 Dec 2025 03:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:e290522631fba31e8ef320a62d0efe0f7bd279c504aacea1b231502c56c75d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128368324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52adaa135524f86585c09c3b6ea713da7b19764a9bb3853687c4410ff4057193`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:01:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:01:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:01:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:01:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:01:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:01:06 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:29 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:29 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:29 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a442d3375c6cf3a0d64cab9a5657f13a2ad79d715217080e57d4091d88c4324`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 8.3 MB (8301082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d2ff8b4dcb5e27c0a3ebecc8f29e07008e917fc5a5a7a6dfeece3f50f8613`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf22d2b96392d2b3c9f1cb454ed14bc66a1dfdef830883f46ed5613c0133d4`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 17.6 MB (17563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be201cbc63828006213cbca3a3f8b91138447829d70553ea57b47fb7b36316`  
		Last Modified: Fri, 12 Dec 2025 23:01:28 GMT  
		Size: 21.5 MB (21476558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e492ed6855e1816d78b7edbd4cdc38ef0cb81d978dfc857129d58d22c754fa`  
		Last Modified: Fri, 12 Dec 2025 23:01:25 GMT  
		Size: 10.2 MB (10195786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50a36847c59872394550e672e167266ae450d58950ec050895f9a2b8b650e3`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836b06438ad83afcbbb80d394f9a68dc224a96dbc3f7446ef31113fbd4fc107`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844bcb311c659e5cab12e879fb055dd4d63aaca8e759553df1c68ad8f8572a0`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f78a51ea72b486ea303cfe9a35e0936165e64f6c1ce623050f1bbc03783827e`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 7.3 MB (7269237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150a1e8e9e07769ffd55ede4c3ebe7b37a7d4a52e59841483c2f1dc104a73cd`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 91.7 KB (91744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d880baf4277f9d0addd5734ad6cd8ef5e32b361ae8196dffbee590ccd63e28c2`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba95d05539ea20cd2ad894c3b01011b5412ac30470cf2067be3a4de6893fb49`  
		Last Modified: Fri, 12 Dec 2025 23:09:51 GMT  
		Size: 59.9 MB (59894425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d365292960a46a15ee408a118f8ed3443f9de61abacc32b1e1c93ca107c203b`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad152b473b5d59ed3116b07b37f35d4bc0fc85aa8364882c610816bea229f3bf`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:c70c7dcb7dfdb1cc89722c4c1299406e1924186e972fd94deb54abbd1052301a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bec62c6dbaf983fd287f9991784c3219e307aceca7be3d32fe32b63d7b2187f`

```dockerfile
```

-	Layers:
	-	`sha256:fff0c79b6617bada32062564279ba2c4c61cab0f5d7fb8bcdb5ac4e87f9f393c`  
		Last Modified: Sat, 13 Dec 2025 03:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:71a0b301e07cfb3145b58f5e33589420b2f0e643d9376d35097d4d402673c64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126466294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e849666bdf05465f46c218af24544c6a84be85d4505f05f1a67f2439df655afb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:48 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:22 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbf8f000eac737bf318d60725474e05cf5bb1d57c289c8f1a9fc5a087446bbb`  
		Last Modified: Fri, 12 Dec 2025 23:04:10 GMT  
		Size: 7.6 MB (7597999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c0b74efc53c5a11551937b3c0ac0e558dda2c21c713a42b1a8c90c83e929a`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26fc85eb088676c2237ad1410f2d06bf4167acef7e7573aa468e85f49ee8`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 17.6 MB (17552135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c0880b371ae9def4a59c648a03dc32de73c939a82863ed46189b5d3c1b26`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 21.5 MB (21454919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dfae8792ac984c5843e7a75359342e09ed6b06094284d3d9afef64ef8d37`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 10.2 MB (10188515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c8dcf60105513f337a71a7a302174c703f2ac4b01eca1a6976550cabbc9cb`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078bbc407a642525a8ecd8f3f56ec5f42ea4276b7984629db0dada8b0ecf69c`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091878b07b4fafc28f7778946a2e29d096eb34042255686f44fcadaea5d597`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e785e66500d9f73341d04a0d0fe01a7ca6a4ce3d3b9288e82242bc725426b`  
		Last Modified: Fri, 12 Dec 2025 23:10:40 GMT  
		Size: 6.6 MB (6570882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928ed8314751e2e9eaeabdc972d4af1311ab6177479d3b6f80a5539231796da7`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9abf1ec541ec0b256d5eab59239d0b754ddab5d999b8dc430585b6f948e604e`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233d3deeb4102367ed1ec89b7ef2fc760d574be2fc7fedd4ea2e4108be9aba6`  
		Last Modified: Fri, 12 Dec 2025 23:10:45 GMT  
		Size: 59.7 MB (59727126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b55b2d0cde4acdec0d0647c16445382a856fdacd9c1cd5fdf7116a5f96dbb4`  
		Last Modified: Fri, 12 Dec 2025 23:10:50 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603edd3336b192e57264b4a135254f9b4dc1a5761163fe26d86596342fe422de`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:0c9b638681007c9d6737a03cc64eac228cfd924c10100f3189602dd4d65d73bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70074d9836671bcf71409a77556f876fa92be1526c11bc44cf503e7077324561`

```dockerfile
```

-	Layers:
	-	`sha256:18a5d28b03d244c5685e86038be1cc676b25e374d481bfba7ced9ce1023ebe95`  
		Last Modified: Sat, 13 Dec 2025 03:07:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ae8fb276f238b912024b6b5805e3e244f0919648b835cf7a1ad0c1b791638ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126321327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b51d82ca438a87cf78f035539342acb921ff3b8a7c5c316c5dd827b52838dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1f8bb5ac9908d8a2f05285d5bafaaa09c4639ad5ec575f506b7f94eb9b027`  
		Last Modified: Fri, 12 Dec 2025 23:09:43 GMT  
		Size: 7.2 MB (7211487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07fdd52b461065d91e16e325ebe1351e98a49811bfe1953d3ffe9d71f66976`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 101.3 KB (101259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d775131bce9a8efbc68a01168997189db83ec2f6764633a853bb6c4013ba98b9`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1bdb364f96a9e042c2a09900dea9f490b2fd714dc314a9b36df5e470baa327`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 58.4 MB (58430278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039982dd10164d6a2e84e3eba3fd37ce736fbfcb0f9e03881c7ba02615b5c87`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22468ff67dbfccb6e8991c334fe5d9d379c964a9ecfe16c05d804125837727f8`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:3c36eabf6e66c492c055fbc625e84d44c47a923d35e2f46f5d13f8c90174aca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae5563a6811d6d3cc3a1e6303828b71d9608a6a4fc125183d83423348c5f2a6`

```dockerfile
```

-	Layers:
	-	`sha256:f88b5a51b8c8deb7c3b298f4e2252c16a18f817fb711be330fa64e81a65284e0`  
		Last Modified: Sat, 13 Dec 2025 03:07:37 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1.3-cli`

```console
$ docker pull docker@sha256:fef89d736d81ca03bb9bac2fabdc7bbf5f0b1485a708c94028225cb8623d1084
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

### `docker:29.1.3-cli` - linux; amd64

```console
$ docker pull docker@sha256:460bd54747e38686f19906b2c7871d7a24159b2149fab3d2576d5cfd201cad73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64715034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4453f9079883af7ee6a02d1d59e76df1c5254647118c2fcd31dad73a7868a2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:18efc4ebd9cdbdf6b6ce77046066d86d2ca19db8332ee23cf54e560fbc3731bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76513174b1ca50e674ed0be90a756d3e124b07462362dbb3baab908e1537cb85`

```dockerfile
```

-	Layers:
	-	`sha256:7a2736719c9b6d24bbb2e67120ddc54c6a898296084a245f781f6e63d2158f2a`  
		Last Modified: Sat, 13 Dec 2025 00:07:29 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ed3d4022bcc3b84bda70aaae6c5f5fc5fcfe3c166b59a310eb546de5b1b93419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61106920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95404e10bb74578f403ba9578c56111c25597aa98a33490d2ea3bc7ac17c48b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:01:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:01:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:01:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:01:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:01:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:01:06 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a442d3375c6cf3a0d64cab9a5657f13a2ad79d715217080e57d4091d88c4324`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 8.3 MB (8301082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d2ff8b4dcb5e27c0a3ebecc8f29e07008e917fc5a5a7a6dfeece3f50f8613`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf22d2b96392d2b3c9f1cb454ed14bc66a1dfdef830883f46ed5613c0133d4`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 17.6 MB (17563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be201cbc63828006213cbca3a3f8b91138447829d70553ea57b47fb7b36316`  
		Last Modified: Fri, 12 Dec 2025 23:01:28 GMT  
		Size: 21.5 MB (21476558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e492ed6855e1816d78b7edbd4cdc38ef0cb81d978dfc857129d58d22c754fa`  
		Last Modified: Fri, 12 Dec 2025 23:01:25 GMT  
		Size: 10.2 MB (10195786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50a36847c59872394550e672e167266ae450d58950ec050895f9a2b8b650e3`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836b06438ad83afcbbb80d394f9a68dc224a96dbc3f7446ef31113fbd4fc107`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844bcb311c659e5cab12e879fb055dd4d63aaca8e759553df1c68ad8f8572a0`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:050b2baec8a743beab976d109ade8bbd2255f907abf6ed7c521825f031ebfb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8711322ffdbfc1512d835bdbb3d1aab5d63286fc0edb80507d74fd721e7093`

```dockerfile
```

-	Layers:
	-	`sha256:3462d33a19054d0414ea3eb7bdc0b282352efc598442d721e9c2f5e3e7af653d`  
		Last Modified: Sat, 13 Dec 2025 00:07:32 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:7b6ba4909381a6b3ca8380db56b5e0566e94241d29ad12196b4871bcd0751e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60074186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273d97076d24ffa898e7608f96246fe2f9c6a75ca258cfa233e728c2a3d00b89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbf8f000eac737bf318d60725474e05cf5bb1d57c289c8f1a9fc5a087446bbb`  
		Last Modified: Fri, 12 Dec 2025 23:04:10 GMT  
		Size: 7.6 MB (7597999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c0b74efc53c5a11551937b3c0ac0e558dda2c21c713a42b1a8c90c83e929a`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26fc85eb088676c2237ad1410f2d06bf4167acef7e7573aa468e85f49ee8`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 17.6 MB (17552135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c0880b371ae9def4a59c648a03dc32de73c939a82863ed46189b5d3c1b26`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 21.5 MB (21454919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dfae8792ac984c5843e7a75359342e09ed6b06094284d3d9afef64ef8d37`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 10.2 MB (10188515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c8dcf60105513f337a71a7a302174c703f2ac4b01eca1a6976550cabbc9cb`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078bbc407a642525a8ecd8f3f56ec5f42ea4276b7984629db0dada8b0ecf69c`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091878b07b4fafc28f7778946a2e29d096eb34042255686f44fcadaea5d597`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2cd5fe33035b9b245d7633d313b6c10663c4b4a15539e1049ed543ae30b0895b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0eafce598b67ac57b3e56ed0966055137da7f5a73489083c1c5a72c6e7febc`

```dockerfile
```

-	Layers:
	-	`sha256:5453b680a91095b07fa3308adfcd6460856cd978700e2fcac203bbcd490a8b4c`  
		Last Modified: Sat, 13 Dec 2025 00:07:35 GMT  
		Size: 38.2 KB (38220 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cd7a8fb27fb7769bd1e99c859cd81b6b5907a48159fe0c5978d36dac92832ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60572305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9fc8e3c559250bb84f436eb83db1fca5000b54667762710ed0053847f4df6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:3fc751e1389e0e81e12e5a50e51cd4c8c9f09bc6f5c22868892d33f362494bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d129b4abe449d1af4183719346aec5b3c50a1a8a0a42844f5299279d54a22a`

```dockerfile
```

-	Layers:
	-	`sha256:847c010774232d19f586d313e7adf4e52cf76fbf7d80543c31098ce2d449ddbc`  
		Last Modified: Sat, 13 Dec 2025 00:08:01 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1.3-cli-alpine3.23`

```console
$ docker pull docker@sha256:fef89d736d81ca03bb9bac2fabdc7bbf5f0b1485a708c94028225cb8623d1084
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

### `docker:29.1.3-cli-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:460bd54747e38686f19906b2c7871d7a24159b2149fab3d2576d5cfd201cad73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64715034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4453f9079883af7ee6a02d1d59e76df1c5254647118c2fcd31dad73a7868a2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:18efc4ebd9cdbdf6b6ce77046066d86d2ca19db8332ee23cf54e560fbc3731bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76513174b1ca50e674ed0be90a756d3e124b07462362dbb3baab908e1537cb85`

```dockerfile
```

-	Layers:
	-	`sha256:7a2736719c9b6d24bbb2e67120ddc54c6a898296084a245f781f6e63d2158f2a`  
		Last Modified: Sat, 13 Dec 2025 00:07:29 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-cli-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:ed3d4022bcc3b84bda70aaae6c5f5fc5fcfe3c166b59a310eb546de5b1b93419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61106920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95404e10bb74578f403ba9578c56111c25597aa98a33490d2ea3bc7ac17c48b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:01:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:01:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:01:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:01:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:01:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:01:06 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a442d3375c6cf3a0d64cab9a5657f13a2ad79d715217080e57d4091d88c4324`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 8.3 MB (8301082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d2ff8b4dcb5e27c0a3ebecc8f29e07008e917fc5a5a7a6dfeece3f50f8613`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf22d2b96392d2b3c9f1cb454ed14bc66a1dfdef830883f46ed5613c0133d4`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 17.6 MB (17563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be201cbc63828006213cbca3a3f8b91138447829d70553ea57b47fb7b36316`  
		Last Modified: Fri, 12 Dec 2025 23:01:28 GMT  
		Size: 21.5 MB (21476558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e492ed6855e1816d78b7edbd4cdc38ef0cb81d978dfc857129d58d22c754fa`  
		Last Modified: Fri, 12 Dec 2025 23:01:25 GMT  
		Size: 10.2 MB (10195786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50a36847c59872394550e672e167266ae450d58950ec050895f9a2b8b650e3`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836b06438ad83afcbbb80d394f9a68dc224a96dbc3f7446ef31113fbd4fc107`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844bcb311c659e5cab12e879fb055dd4d63aaca8e759553df1c68ad8f8572a0`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:050b2baec8a743beab976d109ade8bbd2255f907abf6ed7c521825f031ebfb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8711322ffdbfc1512d835bdbb3d1aab5d63286fc0edb80507d74fd721e7093`

```dockerfile
```

-	Layers:
	-	`sha256:3462d33a19054d0414ea3eb7bdc0b282352efc598442d721e9c2f5e3e7af653d`  
		Last Modified: Sat, 13 Dec 2025 00:07:32 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-cli-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:7b6ba4909381a6b3ca8380db56b5e0566e94241d29ad12196b4871bcd0751e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60074186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273d97076d24ffa898e7608f96246fe2f9c6a75ca258cfa233e728c2a3d00b89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbf8f000eac737bf318d60725474e05cf5bb1d57c289c8f1a9fc5a087446bbb`  
		Last Modified: Fri, 12 Dec 2025 23:04:10 GMT  
		Size: 7.6 MB (7597999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c0b74efc53c5a11551937b3c0ac0e558dda2c21c713a42b1a8c90c83e929a`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26fc85eb088676c2237ad1410f2d06bf4167acef7e7573aa468e85f49ee8`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 17.6 MB (17552135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c0880b371ae9def4a59c648a03dc32de73c939a82863ed46189b5d3c1b26`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 21.5 MB (21454919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dfae8792ac984c5843e7a75359342e09ed6b06094284d3d9afef64ef8d37`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 10.2 MB (10188515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c8dcf60105513f337a71a7a302174c703f2ac4b01eca1a6976550cabbc9cb`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078bbc407a642525a8ecd8f3f56ec5f42ea4276b7984629db0dada8b0ecf69c`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091878b07b4fafc28f7778946a2e29d096eb34042255686f44fcadaea5d597`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:2cd5fe33035b9b245d7633d313b6c10663c4b4a15539e1049ed543ae30b0895b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0eafce598b67ac57b3e56ed0966055137da7f5a73489083c1c5a72c6e7febc`

```dockerfile
```

-	Layers:
	-	`sha256:5453b680a91095b07fa3308adfcd6460856cd978700e2fcac203bbcd490a8b4c`  
		Last Modified: Sat, 13 Dec 2025 00:07:35 GMT  
		Size: 38.2 KB (38220 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-cli-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cd7a8fb27fb7769bd1e99c859cd81b6b5907a48159fe0c5978d36dac92832ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60572305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9fc8e3c559250bb84f436eb83db1fca5000b54667762710ed0053847f4df6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:3fc751e1389e0e81e12e5a50e51cd4c8c9f09bc6f5c22868892d33f362494bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d129b4abe449d1af4183719346aec5b3c50a1a8a0a42844f5299279d54a22a`

```dockerfile
```

-	Layers:
	-	`sha256:847c010774232d19f586d313e7adf4e52cf76fbf7d80543c31098ce2d449ddbc`  
		Last Modified: Sat, 13 Dec 2025 00:08:01 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1.3-dind`

```console
$ docker pull docker@sha256:7370a6c49b7e708fb969b422dffe6cdd78a9f0ff5b3bfba0e0cddce736c49eaf
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

### `docker:29.1.3-dind` - linux; amd64

```console
$ docker pull docker@sha256:614db3c0aa1f5a2fe91d4bbbb0df8190c5d233d6ad55aa0f285c29f54227f7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136136542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8274856237f1b49083c42adab01ae804b00b8eeddb621e75b53e8c7a18657249`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:14 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6395790a96f25fe9ae60e8642bb53dc32742cc2a952240e2430c727343070f94`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 6.9 MB (6932404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0e7dad2234067bcdefdfbe8a95f9d27a127e90c2547a0b535e998e62492f9`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 92.5 KB (92451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d2dd2748ca8b7279cc840f1717a591f741f79ca77fccc303369e23381404e`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be03fb08c790242db2d11f5c8abd1e27779400315ae4bebf6812421eb196f424`  
		Last Modified: Fri, 12 Dec 2025 23:10:36 GMT  
		Size: 64.4 MB (64390653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969ded5ab7c174111a0938c32df0c859eae02e11a1f03b285260d4e52ada118`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15928226105bb78669d71594057c0a40684760f66de44e473fe4559e048a1fc4`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d872ccf708c0c6cf248b60f3628d4f6c144e2b9b28d7249d5e99349e036598bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2e79926af9c2cfd84fb6eaa06ee2a235ee5389bbc8f0c528a68c05c925f98c`

```dockerfile
```

-	Layers:
	-	`sha256:dfa8b777c70191bcd2b044ff54627b657daadee8f5c1dfcae039cb25aa6d9e66`  
		Last Modified: Sat, 13 Dec 2025 03:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:e290522631fba31e8ef320a62d0efe0f7bd279c504aacea1b231502c56c75d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128368324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52adaa135524f86585c09c3b6ea713da7b19764a9bb3853687c4410ff4057193`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:01:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:01:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:01:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:01:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:01:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:01:06 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:29 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:29 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:29 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a442d3375c6cf3a0d64cab9a5657f13a2ad79d715217080e57d4091d88c4324`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 8.3 MB (8301082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d2ff8b4dcb5e27c0a3ebecc8f29e07008e917fc5a5a7a6dfeece3f50f8613`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf22d2b96392d2b3c9f1cb454ed14bc66a1dfdef830883f46ed5613c0133d4`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 17.6 MB (17563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be201cbc63828006213cbca3a3f8b91138447829d70553ea57b47fb7b36316`  
		Last Modified: Fri, 12 Dec 2025 23:01:28 GMT  
		Size: 21.5 MB (21476558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e492ed6855e1816d78b7edbd4cdc38ef0cb81d978dfc857129d58d22c754fa`  
		Last Modified: Fri, 12 Dec 2025 23:01:25 GMT  
		Size: 10.2 MB (10195786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50a36847c59872394550e672e167266ae450d58950ec050895f9a2b8b650e3`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836b06438ad83afcbbb80d394f9a68dc224a96dbc3f7446ef31113fbd4fc107`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844bcb311c659e5cab12e879fb055dd4d63aaca8e759553df1c68ad8f8572a0`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f78a51ea72b486ea303cfe9a35e0936165e64f6c1ce623050f1bbc03783827e`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 7.3 MB (7269237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150a1e8e9e07769ffd55ede4c3ebe7b37a7d4a52e59841483c2f1dc104a73cd`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 91.7 KB (91744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d880baf4277f9d0addd5734ad6cd8ef5e32b361ae8196dffbee590ccd63e28c2`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba95d05539ea20cd2ad894c3b01011b5412ac30470cf2067be3a4de6893fb49`  
		Last Modified: Fri, 12 Dec 2025 23:09:51 GMT  
		Size: 59.9 MB (59894425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d365292960a46a15ee408a118f8ed3443f9de61abacc32b1e1c93ca107c203b`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad152b473b5d59ed3116b07b37f35d4bc0fc85aa8364882c610816bea229f3bf`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:c70c7dcb7dfdb1cc89722c4c1299406e1924186e972fd94deb54abbd1052301a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bec62c6dbaf983fd287f9991784c3219e307aceca7be3d32fe32b63d7b2187f`

```dockerfile
```

-	Layers:
	-	`sha256:fff0c79b6617bada32062564279ba2c4c61cab0f5d7fb8bcdb5ac4e87f9f393c`  
		Last Modified: Sat, 13 Dec 2025 03:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:71a0b301e07cfb3145b58f5e33589420b2f0e643d9376d35097d4d402673c64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126466294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e849666bdf05465f46c218af24544c6a84be85d4505f05f1a67f2439df655afb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:48 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:22 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbf8f000eac737bf318d60725474e05cf5bb1d57c289c8f1a9fc5a087446bbb`  
		Last Modified: Fri, 12 Dec 2025 23:04:10 GMT  
		Size: 7.6 MB (7597999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c0b74efc53c5a11551937b3c0ac0e558dda2c21c713a42b1a8c90c83e929a`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26fc85eb088676c2237ad1410f2d06bf4167acef7e7573aa468e85f49ee8`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 17.6 MB (17552135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c0880b371ae9def4a59c648a03dc32de73c939a82863ed46189b5d3c1b26`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 21.5 MB (21454919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dfae8792ac984c5843e7a75359342e09ed6b06094284d3d9afef64ef8d37`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 10.2 MB (10188515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c8dcf60105513f337a71a7a302174c703f2ac4b01eca1a6976550cabbc9cb`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078bbc407a642525a8ecd8f3f56ec5f42ea4276b7984629db0dada8b0ecf69c`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091878b07b4fafc28f7778946a2e29d096eb34042255686f44fcadaea5d597`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e785e66500d9f73341d04a0d0fe01a7ca6a4ce3d3b9288e82242bc725426b`  
		Last Modified: Fri, 12 Dec 2025 23:10:40 GMT  
		Size: 6.6 MB (6570882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928ed8314751e2e9eaeabdc972d4af1311ab6177479d3b6f80a5539231796da7`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9abf1ec541ec0b256d5eab59239d0b754ddab5d999b8dc430585b6f948e604e`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233d3deeb4102367ed1ec89b7ef2fc760d574be2fc7fedd4ea2e4108be9aba6`  
		Last Modified: Fri, 12 Dec 2025 23:10:45 GMT  
		Size: 59.7 MB (59727126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b55b2d0cde4acdec0d0647c16445382a856fdacd9c1cd5fdf7116a5f96dbb4`  
		Last Modified: Fri, 12 Dec 2025 23:10:50 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603edd3336b192e57264b4a135254f9b4dc1a5761163fe26d86596342fe422de`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0c9b638681007c9d6737a03cc64eac228cfd924c10100f3189602dd4d65d73bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70074d9836671bcf71409a77556f876fa92be1526c11bc44cf503e7077324561`

```dockerfile
```

-	Layers:
	-	`sha256:18a5d28b03d244c5685e86038be1cc676b25e374d481bfba7ced9ce1023ebe95`  
		Last Modified: Sat, 13 Dec 2025 03:07:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ae8fb276f238b912024b6b5805e3e244f0919648b835cf7a1ad0c1b791638ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126321327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b51d82ca438a87cf78f035539342acb921ff3b8a7c5c316c5dd827b52838dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1f8bb5ac9908d8a2f05285d5bafaaa09c4639ad5ec575f506b7f94eb9b027`  
		Last Modified: Fri, 12 Dec 2025 23:09:43 GMT  
		Size: 7.2 MB (7211487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07fdd52b461065d91e16e325ebe1351e98a49811bfe1953d3ffe9d71f66976`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 101.3 KB (101259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d775131bce9a8efbc68a01168997189db83ec2f6764633a853bb6c4013ba98b9`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1bdb364f96a9e042c2a09900dea9f490b2fd714dc314a9b36df5e470baa327`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 58.4 MB (58430278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039982dd10164d6a2e84e3eba3fd37ce736fbfcb0f9e03881c7ba02615b5c87`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22468ff67dbfccb6e8991c334fe5d9d379c964a9ecfe16c05d804125837727f8`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3c36eabf6e66c492c055fbc625e84d44c47a923d35e2f46f5d13f8c90174aca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae5563a6811d6d3cc3a1e6303828b71d9608a6a4fc125183d83423348c5f2a6`

```dockerfile
```

-	Layers:
	-	`sha256:f88b5a51b8c8deb7c3b298f4e2252c16a18f817fb711be330fa64e81a65284e0`  
		Last Modified: Sat, 13 Dec 2025 03:07:37 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1.3-dind-alpine3.23`

```console
$ docker pull docker@sha256:7370a6c49b7e708fb969b422dffe6cdd78a9f0ff5b3bfba0e0cddce736c49eaf
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

### `docker:29.1.3-dind-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:614db3c0aa1f5a2fe91d4bbbb0df8190c5d233d6ad55aa0f285c29f54227f7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136136542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8274856237f1b49083c42adab01ae804b00b8eeddb621e75b53e8c7a18657249`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:14 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6395790a96f25fe9ae60e8642bb53dc32742cc2a952240e2430c727343070f94`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 6.9 MB (6932404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0e7dad2234067bcdefdfbe8a95f9d27a127e90c2547a0b535e998e62492f9`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 92.5 KB (92451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d2dd2748ca8b7279cc840f1717a591f741f79ca77fccc303369e23381404e`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be03fb08c790242db2d11f5c8abd1e27779400315ae4bebf6812421eb196f424`  
		Last Modified: Fri, 12 Dec 2025 23:10:36 GMT  
		Size: 64.4 MB (64390653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969ded5ab7c174111a0938c32df0c859eae02e11a1f03b285260d4e52ada118`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15928226105bb78669d71594057c0a40684760f66de44e473fe4559e048a1fc4`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:d872ccf708c0c6cf248b60f3628d4f6c144e2b9b28d7249d5e99349e036598bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2e79926af9c2cfd84fb6eaa06ee2a235ee5389bbc8f0c528a68c05c925f98c`

```dockerfile
```

-	Layers:
	-	`sha256:dfa8b777c70191bcd2b044ff54627b657daadee8f5c1dfcae039cb25aa6d9e66`  
		Last Modified: Sat, 13 Dec 2025 03:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-dind-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:e290522631fba31e8ef320a62d0efe0f7bd279c504aacea1b231502c56c75d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128368324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52adaa135524f86585c09c3b6ea713da7b19764a9bb3853687c4410ff4057193`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:01:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:01:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:01:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:01:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:01:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:01:06 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:29 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:29 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:29 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a442d3375c6cf3a0d64cab9a5657f13a2ad79d715217080e57d4091d88c4324`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 8.3 MB (8301082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d2ff8b4dcb5e27c0a3ebecc8f29e07008e917fc5a5a7a6dfeece3f50f8613`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf22d2b96392d2b3c9f1cb454ed14bc66a1dfdef830883f46ed5613c0133d4`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 17.6 MB (17563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be201cbc63828006213cbca3a3f8b91138447829d70553ea57b47fb7b36316`  
		Last Modified: Fri, 12 Dec 2025 23:01:28 GMT  
		Size: 21.5 MB (21476558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e492ed6855e1816d78b7edbd4cdc38ef0cb81d978dfc857129d58d22c754fa`  
		Last Modified: Fri, 12 Dec 2025 23:01:25 GMT  
		Size: 10.2 MB (10195786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50a36847c59872394550e672e167266ae450d58950ec050895f9a2b8b650e3`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836b06438ad83afcbbb80d394f9a68dc224a96dbc3f7446ef31113fbd4fc107`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844bcb311c659e5cab12e879fb055dd4d63aaca8e759553df1c68ad8f8572a0`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f78a51ea72b486ea303cfe9a35e0936165e64f6c1ce623050f1bbc03783827e`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 7.3 MB (7269237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150a1e8e9e07769ffd55ede4c3ebe7b37a7d4a52e59841483c2f1dc104a73cd`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 91.7 KB (91744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d880baf4277f9d0addd5734ad6cd8ef5e32b361ae8196dffbee590ccd63e28c2`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba95d05539ea20cd2ad894c3b01011b5412ac30470cf2067be3a4de6893fb49`  
		Last Modified: Fri, 12 Dec 2025 23:09:51 GMT  
		Size: 59.9 MB (59894425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d365292960a46a15ee408a118f8ed3443f9de61abacc32b1e1c93ca107c203b`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad152b473b5d59ed3116b07b37f35d4bc0fc85aa8364882c610816bea229f3bf`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:c70c7dcb7dfdb1cc89722c4c1299406e1924186e972fd94deb54abbd1052301a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bec62c6dbaf983fd287f9991784c3219e307aceca7be3d32fe32b63d7b2187f`

```dockerfile
```

-	Layers:
	-	`sha256:fff0c79b6617bada32062564279ba2c4c61cab0f5d7fb8bcdb5ac4e87f9f393c`  
		Last Modified: Sat, 13 Dec 2025 03:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-dind-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:71a0b301e07cfb3145b58f5e33589420b2f0e643d9376d35097d4d402673c64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126466294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e849666bdf05465f46c218af24544c6a84be85d4505f05f1a67f2439df655afb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:48 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:22 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbf8f000eac737bf318d60725474e05cf5bb1d57c289c8f1a9fc5a087446bbb`  
		Last Modified: Fri, 12 Dec 2025 23:04:10 GMT  
		Size: 7.6 MB (7597999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c0b74efc53c5a11551937b3c0ac0e558dda2c21c713a42b1a8c90c83e929a`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26fc85eb088676c2237ad1410f2d06bf4167acef7e7573aa468e85f49ee8`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 17.6 MB (17552135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c0880b371ae9def4a59c648a03dc32de73c939a82863ed46189b5d3c1b26`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 21.5 MB (21454919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dfae8792ac984c5843e7a75359342e09ed6b06094284d3d9afef64ef8d37`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 10.2 MB (10188515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c8dcf60105513f337a71a7a302174c703f2ac4b01eca1a6976550cabbc9cb`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078bbc407a642525a8ecd8f3f56ec5f42ea4276b7984629db0dada8b0ecf69c`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091878b07b4fafc28f7778946a2e29d096eb34042255686f44fcadaea5d597`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e785e66500d9f73341d04a0d0fe01a7ca6a4ce3d3b9288e82242bc725426b`  
		Last Modified: Fri, 12 Dec 2025 23:10:40 GMT  
		Size: 6.6 MB (6570882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928ed8314751e2e9eaeabdc972d4af1311ab6177479d3b6f80a5539231796da7`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9abf1ec541ec0b256d5eab59239d0b754ddab5d999b8dc430585b6f948e604e`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233d3deeb4102367ed1ec89b7ef2fc760d574be2fc7fedd4ea2e4108be9aba6`  
		Last Modified: Fri, 12 Dec 2025 23:10:45 GMT  
		Size: 59.7 MB (59727126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b55b2d0cde4acdec0d0647c16445382a856fdacd9c1cd5fdf7116a5f96dbb4`  
		Last Modified: Fri, 12 Dec 2025 23:10:50 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603edd3336b192e57264b4a135254f9b4dc1a5761163fe26d86596342fe422de`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:0c9b638681007c9d6737a03cc64eac228cfd924c10100f3189602dd4d65d73bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70074d9836671bcf71409a77556f876fa92be1526c11bc44cf503e7077324561`

```dockerfile
```

-	Layers:
	-	`sha256:18a5d28b03d244c5685e86038be1cc676b25e374d481bfba7ced9ce1023ebe95`  
		Last Modified: Sat, 13 Dec 2025 03:07:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-dind-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ae8fb276f238b912024b6b5805e3e244f0919648b835cf7a1ad0c1b791638ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126321327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b51d82ca438a87cf78f035539342acb921ff3b8a7c5c316c5dd827b52838dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1f8bb5ac9908d8a2f05285d5bafaaa09c4639ad5ec575f506b7f94eb9b027`  
		Last Modified: Fri, 12 Dec 2025 23:09:43 GMT  
		Size: 7.2 MB (7211487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07fdd52b461065d91e16e325ebe1351e98a49811bfe1953d3ffe9d71f66976`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 101.3 KB (101259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d775131bce9a8efbc68a01168997189db83ec2f6764633a853bb6c4013ba98b9`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1bdb364f96a9e042c2a09900dea9f490b2fd714dc314a9b36df5e470baa327`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 58.4 MB (58430278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039982dd10164d6a2e84e3eba3fd37ce736fbfcb0f9e03881c7ba02615b5c87`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22468ff67dbfccb6e8991c334fe5d9d379c964a9ecfe16c05d804125837727f8`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:3c36eabf6e66c492c055fbc625e84d44c47a923d35e2f46f5d13f8c90174aca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae5563a6811d6d3cc3a1e6303828b71d9608a6a4fc125183d83423348c5f2a6`

```dockerfile
```

-	Layers:
	-	`sha256:f88b5a51b8c8deb7c3b298f4e2252c16a18f817fb711be330fa64e81a65284e0`  
		Last Modified: Sat, 13 Dec 2025 03:07:37 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1.3-dind-rootless`

```console
$ docker pull docker@sha256:ac12412d8bc07bdbc71e1bd730572dc5010a5d2116987775b30f849d1268380e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.1.3-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:09950db32d89c1662f1970578f51562812eab9a3eb50feb7326519f7e5514235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156928803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17a49738c68db9b440e165269dc75f5f3e74a89e9a75426199cd466b0383cd6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:14 GMT
CMD []
# Sat, 13 Dec 2025 00:10:12 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 13 Dec 2025 00:10:12 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 13 Dec 2025 00:10:12 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 13 Dec 2025 00:10:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 13 Dec 2025 00:10:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 13 Dec 2025 00:10:13 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 13 Dec 2025 00:10:13 GMT
USER rootless
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6395790a96f25fe9ae60e8642bb53dc32742cc2a952240e2430c727343070f94`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 6.9 MB (6932404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0e7dad2234067bcdefdfbe8a95f9d27a127e90c2547a0b535e998e62492f9`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 92.5 KB (92451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d2dd2748ca8b7279cc840f1717a591f741f79ca77fccc303369e23381404e`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be03fb08c790242db2d11f5c8abd1e27779400315ae4bebf6812421eb196f424`  
		Last Modified: Fri, 12 Dec 2025 23:10:36 GMT  
		Size: 64.4 MB (64390653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969ded5ab7c174111a0938c32df0c859eae02e11a1f03b285260d4e52ada118`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15928226105bb78669d71594057c0a40684760f66de44e473fe4559e048a1fc4`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7efc67e74d7bff7198949770096adae0c34ad7c6a32faa6e3d0bab24e69da51`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 3.4 MB (3419931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0ea6cd17928c2035157de458119f33ee511ec1deee23008735895ce2472b79`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b30c307447754a05b3912b60fa4a43ebe6eb174bb107be0d85866ce5cf6d0b6`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab6e3723d2a693205fe1725bd19abcfbfd2ac1331a374d8b35b7897742941c5`  
		Last Modified: Sat, 13 Dec 2025 00:10:37 GMT  
		Size: 17.4 MB (17370991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7db2853efa7da1fc8d7b3143c0f861bdc77ee5a9cce03278ff21f1568ef69c5`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:336e04652a588e2ad4e195e403ef93c675ba97007c75e40a9efe962cb4f16bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd1e5b602cf458f135106fdc1b6bee98d42185597cd98c67410b6c1c42dc34f`

```dockerfile
```

-	Layers:
	-	`sha256:e3a762cb9f51fe6d372134b550c76079147291d858530a914cc826e7d8dbc1d9`  
		Last Modified: Sat, 13 Dec 2025 03:07:42 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1.3-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7deb6a567eeef7d5a72412f239f2170d024ede941b350b13f24ebf9abc29721e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147425780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229ad388f6f6b781e7a9b6825675f4deeb04ea90f1123729e79549a7b32b83ac`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:25 GMT
CMD []
# Sat, 13 Dec 2025 00:09:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 13 Dec 2025 00:09:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 13 Dec 2025 00:09:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 13 Dec 2025 00:10:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 13 Dec 2025 00:10:01 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 13 Dec 2025 00:10:01 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 13 Dec 2025 00:10:01 GMT
USER rootless
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1f8bb5ac9908d8a2f05285d5bafaaa09c4639ad5ec575f506b7f94eb9b027`  
		Last Modified: Fri, 12 Dec 2025 23:09:43 GMT  
		Size: 7.2 MB (7211487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07fdd52b461065d91e16e325ebe1351e98a49811bfe1953d3ffe9d71f66976`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 101.3 KB (101259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d775131bce9a8efbc68a01168997189db83ec2f6764633a853bb6c4013ba98b9`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1bdb364f96a9e042c2a09900dea9f490b2fd714dc314a9b36df5e470baa327`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 58.4 MB (58430278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039982dd10164d6a2e84e3eba3fd37ce736fbfcb0f9e03881c7ba02615b5c87`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22468ff67dbfccb6e8991c334fe5d9d379c964a9ecfe16c05d804125837727f8`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb2d13730b1a2b9437f55aa38844a2d4f3a41baff03b9ba200fd6c8e3640f65`  
		Last Modified: Sat, 13 Dec 2025 00:10:27 GMT  
		Size: 3.4 MB (3394382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c5eda520ed158582d67f72a42c82eef1d312c24f5fb51f16441c4772825971`  
		Last Modified: Sat, 13 Dec 2025 00:10:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05db2d742efc92d52e078c87f0af299e70fb014fbfaea3a18b757374eca9af`  
		Last Modified: Sat, 13 Dec 2025 00:10:27 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9af16ab409354af0d1a5b9a8dd6362e6886e59680f35e8fc253d99c504af99`  
		Last Modified: Sat, 13 Dec 2025 00:10:32 GMT  
		Size: 17.7 MB (17708729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffd4a2a8cc857d1398fdf583e20112730537572a29d8c9100512be073ec09d8`  
		Last Modified: Sat, 13 Dec 2025 00:10:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6eab544cd873580b808013fbe86c7cc254767cc99c60313d1cd9f4e5eccb9f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c814e243bbda6587996667fdd159361b2cc27f15e889e349a1976482785bda18`

```dockerfile
```

-	Layers:
	-	`sha256:3a3842cd2beb5724ad7a78418740bfd432103bce0f213347880883022e4a0094`  
		Last Modified: Sat, 13 Dec 2025 03:07:45 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1.3-windowsservercore`

```console
$ docker pull docker@sha256:24e3252850071e0729b50e765be6eb141aec202a2709217891272b9d2a8efb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `docker:29.1.3-windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:072f69cc9a1bc2cb016cd912ee5dcb075d0f2e73df576a46f98ddb1f3f8a4ea2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308280068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e356747fea9e9e69ddc2df399e0a31cb31c5c255da4f7f8ff52e08eef859a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Fri, 12 Dec 2025 23:51:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:51:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:51:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:33 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:51:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:43 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:51:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49db97996aeb50d6cc3bb59d05b2805a04f9a341f791d3bbf78f96c91ea6ea46`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e012252a5c78e6736aa02ede33d15956b820e11e10d32c0eed00f4ac4c0642ed`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 365.2 KB (365173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba990e6755d56a5110398c67645345164f3cb13a4f31f2c87cd0cf475b2fddc`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df48c7a2c9538324b83a4a6378f6ecbcf5c51d2b4c853c98b154d3d2e1fe23c`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9a30b43b8cff73e13f7e796431a6d59d40548fd5ed22e9f0f643554cffa66`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 19.4 MB (19430080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053e9422e23dca07aade3c64cf9355ecc9227c50dd075cde8a77bf5f588fdf07`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d53e5a50955843cf8df23bd9852867dc4e044732ab6a2c3dff445d30a03969`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6a3bffb040caaef43c930bcf019f71c62523c17c8c3aa21340ce83fd63c367`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5297cc0777d4cd44c02f2f373fa189394855ab3f6e99fb51e0e9b14dcbe7719`  
		Last Modified: Sat, 13 Dec 2025 00:10:41 GMT  
		Size: 23.9 MB (23916756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d343979aeb667bd44bc30f0385636c1525e1007c30d7a56b0c4b2929e986e3ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e484e796b3e881c2c53ab847de762b0acce3ce695452b588333031fd16f4722`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1d8d8a0183df8a67af7c17491af2ce9bcc2f1e5bed8a1b7337d9cc59d72a48`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e066997579a2dbc121185aac60816764e96c1cbce7d351630d1ae1a79062f7ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 11.4 MB (11435912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.1.3-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:6c63e74fbbe6a6853d2eed17e74a22a1f27caa6652d65e73237c8cdae1584560
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835158901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31a8d2106c0d362d41e18b340f4ce9fcb284d2750fd96d7010599996e10f95a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Fri, 12 Dec 2025 23:42:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:42:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:42:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:35 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:42:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:42:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a59061a4bd19a5f5104deac5c13f08378f0d057b550fa44336edd48c297a30`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d45f349269329c39cb7f626e581200a0cfd951639d64b460dc496e827a02d3`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 496.4 KB (496422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbbd38f48aebab5ee03921c61d62bc51aafa5296de9f243a1b119cb5b9b59e8`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38e962b0dcf2e2174265dd10ed886b4ac610012a54d0a165b374784dfbfaf5b`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b233205356122f2ba9d651e4d85f51b9efc8720271061a670c3d376808be4df`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 19.4 MB (19421634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4696a1bc6b20cc354eebea761ac5c3e7bee2e41055c2310c9e1efda5acac04cc`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8453a804e2b4641b89e10a12a6711adc2ed009fb0687ea447f9edc9d0ce9b9`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05197d8ed628728e4a93c7c6f52a0cafa2263039f4526e490b5f873167e1144`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b28a4909f7f0860e1395562cbebd921b09728397d7a533d1f7cd4b5d31e1671`  
		Last Modified: Fri, 12 Dec 2025 23:43:12 GMT  
		Size: 23.9 MB (23918113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926c23fb5c1c50e722a5b86e6ae921cd02d73d170dff76ff2af4910598654ae`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594a752382b75756d57cf29a40ab0bde12a567d548acf7cd83772f09c4a21930`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1087bd776bf52196852d02423f98f410d12929744cedd00d7c48c7c0b2113`  
		Last Modified: Fri, 12 Dec 2025 23:43:10 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e85bde05b43a43ab482a075807c5b38bbe7bf9b47871b3147d117cff05b772`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 11.4 MB (11431570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1.3-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c0c8ea04bc96a986cc33445b9d46d8a5607e447352d26cc9bd8c0a8845fca4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `docker:29.1.3-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:6c63e74fbbe6a6853d2eed17e74a22a1f27caa6652d65e73237c8cdae1584560
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835158901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31a8d2106c0d362d41e18b340f4ce9fcb284d2750fd96d7010599996e10f95a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Fri, 12 Dec 2025 23:42:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:42:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:42:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:35 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:42:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:42:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a59061a4bd19a5f5104deac5c13f08378f0d057b550fa44336edd48c297a30`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d45f349269329c39cb7f626e581200a0cfd951639d64b460dc496e827a02d3`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 496.4 KB (496422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbbd38f48aebab5ee03921c61d62bc51aafa5296de9f243a1b119cb5b9b59e8`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38e962b0dcf2e2174265dd10ed886b4ac610012a54d0a165b374784dfbfaf5b`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b233205356122f2ba9d651e4d85f51b9efc8720271061a670c3d376808be4df`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 19.4 MB (19421634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4696a1bc6b20cc354eebea761ac5c3e7bee2e41055c2310c9e1efda5acac04cc`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8453a804e2b4641b89e10a12a6711adc2ed009fb0687ea447f9edc9d0ce9b9`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05197d8ed628728e4a93c7c6f52a0cafa2263039f4526e490b5f873167e1144`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b28a4909f7f0860e1395562cbebd921b09728397d7a533d1f7cd4b5d31e1671`  
		Last Modified: Fri, 12 Dec 2025 23:43:12 GMT  
		Size: 23.9 MB (23918113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926c23fb5c1c50e722a5b86e6ae921cd02d73d170dff76ff2af4910598654ae`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594a752382b75756d57cf29a40ab0bde12a567d548acf7cd83772f09c4a21930`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1087bd776bf52196852d02423f98f410d12929744cedd00d7c48c7c0b2113`  
		Last Modified: Fri, 12 Dec 2025 23:43:10 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e85bde05b43a43ab482a075807c5b38bbe7bf9b47871b3147d117cff05b772`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 11.4 MB (11431570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1.3-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:f862456b5cfe6c2b259f159ae0b967e1a05ad2839c2798b3c9b755e2447508dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `docker:29.1.3-windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:072f69cc9a1bc2cb016cd912ee5dcb075d0f2e73df576a46f98ddb1f3f8a4ea2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308280068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e356747fea9e9e69ddc2df399e0a31cb31c5c255da4f7f8ff52e08eef859a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Fri, 12 Dec 2025 23:51:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:51:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:51:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:33 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:51:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:43 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:51:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49db97996aeb50d6cc3bb59d05b2805a04f9a341f791d3bbf78f96c91ea6ea46`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e012252a5c78e6736aa02ede33d15956b820e11e10d32c0eed00f4ac4c0642ed`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 365.2 KB (365173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba990e6755d56a5110398c67645345164f3cb13a4f31f2c87cd0cf475b2fddc`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df48c7a2c9538324b83a4a6378f6ecbcf5c51d2b4c853c98b154d3d2e1fe23c`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9a30b43b8cff73e13f7e796431a6d59d40548fd5ed22e9f0f643554cffa66`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 19.4 MB (19430080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053e9422e23dca07aade3c64cf9355ecc9227c50dd075cde8a77bf5f588fdf07`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d53e5a50955843cf8df23bd9852867dc4e044732ab6a2c3dff445d30a03969`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6a3bffb040caaef43c930bcf019f71c62523c17c8c3aa21340ce83fd63c367`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5297cc0777d4cd44c02f2f373fa189394855ab3f6e99fb51e0e9b14dcbe7719`  
		Last Modified: Sat, 13 Dec 2025 00:10:41 GMT  
		Size: 23.9 MB (23916756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d343979aeb667bd44bc30f0385636c1525e1007c30d7a56b0c4b2929e986e3ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e484e796b3e881c2c53ab847de762b0acce3ce695452b588333031fd16f4722`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1d8d8a0183df8a67af7c17491af2ce9bcc2f1e5bed8a1b7337d9cc59d72a48`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e066997579a2dbc121185aac60816764e96c1cbce7d351630d1ae1a79062f7ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 11.4 MB (11435912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:fef89d736d81ca03bb9bac2fabdc7bbf5f0b1485a708c94028225cb8623d1084
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
$ docker pull docker@sha256:460bd54747e38686f19906b2c7871d7a24159b2149fab3d2576d5cfd201cad73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64715034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4453f9079883af7ee6a02d1d59e76df1c5254647118c2fcd31dad73a7868a2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:18efc4ebd9cdbdf6b6ce77046066d86d2ca19db8332ee23cf54e560fbc3731bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76513174b1ca50e674ed0be90a756d3e124b07462362dbb3baab908e1537cb85`

```dockerfile
```

-	Layers:
	-	`sha256:7a2736719c9b6d24bbb2e67120ddc54c6a898296084a245f781f6e63d2158f2a`  
		Last Modified: Sat, 13 Dec 2025 00:07:29 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:ed3d4022bcc3b84bda70aaae6c5f5fc5fcfe3c166b59a310eb546de5b1b93419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61106920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95404e10bb74578f403ba9578c56111c25597aa98a33490d2ea3bc7ac17c48b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:01:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:01:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:01:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:01:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:01:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:01:06 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a442d3375c6cf3a0d64cab9a5657f13a2ad79d715217080e57d4091d88c4324`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 8.3 MB (8301082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d2ff8b4dcb5e27c0a3ebecc8f29e07008e917fc5a5a7a6dfeece3f50f8613`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf22d2b96392d2b3c9f1cb454ed14bc66a1dfdef830883f46ed5613c0133d4`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 17.6 MB (17563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be201cbc63828006213cbca3a3f8b91138447829d70553ea57b47fb7b36316`  
		Last Modified: Fri, 12 Dec 2025 23:01:28 GMT  
		Size: 21.5 MB (21476558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e492ed6855e1816d78b7edbd4cdc38ef0cb81d978dfc857129d58d22c754fa`  
		Last Modified: Fri, 12 Dec 2025 23:01:25 GMT  
		Size: 10.2 MB (10195786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50a36847c59872394550e672e167266ae450d58950ec050895f9a2b8b650e3`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836b06438ad83afcbbb80d394f9a68dc224a96dbc3f7446ef31113fbd4fc107`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844bcb311c659e5cab12e879fb055dd4d63aaca8e759553df1c68ad8f8572a0`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:050b2baec8a743beab976d109ade8bbd2255f907abf6ed7c521825f031ebfb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8711322ffdbfc1512d835bdbb3d1aab5d63286fc0edb80507d74fd721e7093`

```dockerfile
```

-	Layers:
	-	`sha256:3462d33a19054d0414ea3eb7bdc0b282352efc598442d721e9c2f5e3e7af653d`  
		Last Modified: Sat, 13 Dec 2025 00:07:32 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:7b6ba4909381a6b3ca8380db56b5e0566e94241d29ad12196b4871bcd0751e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60074186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273d97076d24ffa898e7608f96246fe2f9c6a75ca258cfa233e728c2a3d00b89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:48 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbf8f000eac737bf318d60725474e05cf5bb1d57c289c8f1a9fc5a087446bbb`  
		Last Modified: Fri, 12 Dec 2025 23:04:10 GMT  
		Size: 7.6 MB (7597999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c0b74efc53c5a11551937b3c0ac0e558dda2c21c713a42b1a8c90c83e929a`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26fc85eb088676c2237ad1410f2d06bf4167acef7e7573aa468e85f49ee8`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 17.6 MB (17552135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c0880b371ae9def4a59c648a03dc32de73c939a82863ed46189b5d3c1b26`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 21.5 MB (21454919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dfae8792ac984c5843e7a75359342e09ed6b06094284d3d9afef64ef8d37`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 10.2 MB (10188515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c8dcf60105513f337a71a7a302174c703f2ac4b01eca1a6976550cabbc9cb`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078bbc407a642525a8ecd8f3f56ec5f42ea4276b7984629db0dada8b0ecf69c`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091878b07b4fafc28f7778946a2e29d096eb34042255686f44fcadaea5d597`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:2cd5fe33035b9b245d7633d313b6c10663c4b4a15539e1049ed543ae30b0895b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0eafce598b67ac57b3e56ed0966055137da7f5a73489083c1c5a72c6e7febc`

```dockerfile
```

-	Layers:
	-	`sha256:5453b680a91095b07fa3308adfcd6460856cd978700e2fcac203bbcd490a8b4c`  
		Last Modified: Sat, 13 Dec 2025 00:07:35 GMT  
		Size: 38.2 KB (38220 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:cd7a8fb27fb7769bd1e99c859cd81b6b5907a48159fe0c5978d36dac92832ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60572305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9fc8e3c559250bb84f436eb83db1fca5000b54667762710ed0053847f4df6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:3fc751e1389e0e81e12e5a50e51cd4c8c9f09bc6f5c22868892d33f362494bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d129b4abe449d1af4183719346aec5b3c50a1a8a0a42844f5299279d54a22a`

```dockerfile
```

-	Layers:
	-	`sha256:847c010774232d19f586d313e7adf4e52cf76fbf7d80543c31098ce2d449ddbc`  
		Last Modified: Sat, 13 Dec 2025 00:08:01 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:7370a6c49b7e708fb969b422dffe6cdd78a9f0ff5b3bfba0e0cddce736c49eaf
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
$ docker pull docker@sha256:614db3c0aa1f5a2fe91d4bbbb0df8190c5d233d6ad55aa0f285c29f54227f7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136136542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8274856237f1b49083c42adab01ae804b00b8eeddb621e75b53e8c7a18657249`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:14 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6395790a96f25fe9ae60e8642bb53dc32742cc2a952240e2430c727343070f94`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 6.9 MB (6932404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0e7dad2234067bcdefdfbe8a95f9d27a127e90c2547a0b535e998e62492f9`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 92.5 KB (92451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d2dd2748ca8b7279cc840f1717a591f741f79ca77fccc303369e23381404e`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be03fb08c790242db2d11f5c8abd1e27779400315ae4bebf6812421eb196f424`  
		Last Modified: Fri, 12 Dec 2025 23:10:36 GMT  
		Size: 64.4 MB (64390653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969ded5ab7c174111a0938c32df0c859eae02e11a1f03b285260d4e52ada118`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15928226105bb78669d71594057c0a40684760f66de44e473fe4559e048a1fc4`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:d872ccf708c0c6cf248b60f3628d4f6c144e2b9b28d7249d5e99349e036598bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2e79926af9c2cfd84fb6eaa06ee2a235ee5389bbc8f0c528a68c05c925f98c`

```dockerfile
```

-	Layers:
	-	`sha256:dfa8b777c70191bcd2b044ff54627b657daadee8f5c1dfcae039cb25aa6d9e66`  
		Last Modified: Sat, 13 Dec 2025 03:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:e290522631fba31e8ef320a62d0efe0f7bd279c504aacea1b231502c56c75d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128368324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52adaa135524f86585c09c3b6ea713da7b19764a9bb3853687c4410ff4057193`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:01:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:01:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:01:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:01:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:01:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:01:06 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:29 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:29 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:29 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a442d3375c6cf3a0d64cab9a5657f13a2ad79d715217080e57d4091d88c4324`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 8.3 MB (8301082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d2ff8b4dcb5e27c0a3ebecc8f29e07008e917fc5a5a7a6dfeece3f50f8613`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf22d2b96392d2b3c9f1cb454ed14bc66a1dfdef830883f46ed5613c0133d4`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 17.6 MB (17563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be201cbc63828006213cbca3a3f8b91138447829d70553ea57b47fb7b36316`  
		Last Modified: Fri, 12 Dec 2025 23:01:28 GMT  
		Size: 21.5 MB (21476558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e492ed6855e1816d78b7edbd4cdc38ef0cb81d978dfc857129d58d22c754fa`  
		Last Modified: Fri, 12 Dec 2025 23:01:25 GMT  
		Size: 10.2 MB (10195786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50a36847c59872394550e672e167266ae450d58950ec050895f9a2b8b650e3`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836b06438ad83afcbbb80d394f9a68dc224a96dbc3f7446ef31113fbd4fc107`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844bcb311c659e5cab12e879fb055dd4d63aaca8e759553df1c68ad8f8572a0`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f78a51ea72b486ea303cfe9a35e0936165e64f6c1ce623050f1bbc03783827e`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 7.3 MB (7269237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150a1e8e9e07769ffd55ede4c3ebe7b37a7d4a52e59841483c2f1dc104a73cd`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 91.7 KB (91744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d880baf4277f9d0addd5734ad6cd8ef5e32b361ae8196dffbee590ccd63e28c2`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba95d05539ea20cd2ad894c3b01011b5412ac30470cf2067be3a4de6893fb49`  
		Last Modified: Fri, 12 Dec 2025 23:09:51 GMT  
		Size: 59.9 MB (59894425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d365292960a46a15ee408a118f8ed3443f9de61abacc32b1e1c93ca107c203b`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad152b473b5d59ed3116b07b37f35d4bc0fc85aa8364882c610816bea229f3bf`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:c70c7dcb7dfdb1cc89722c4c1299406e1924186e972fd94deb54abbd1052301a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bec62c6dbaf983fd287f9991784c3219e307aceca7be3d32fe32b63d7b2187f`

```dockerfile
```

-	Layers:
	-	`sha256:fff0c79b6617bada32062564279ba2c4c61cab0f5d7fb8bcdb5ac4e87f9f393c`  
		Last Modified: Sat, 13 Dec 2025 03:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:71a0b301e07cfb3145b58f5e33589420b2f0e643d9376d35097d4d402673c64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126466294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e849666bdf05465f46c218af24544c6a84be85d4505f05f1a67f2439df655afb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:48 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:22 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbf8f000eac737bf318d60725474e05cf5bb1d57c289c8f1a9fc5a087446bbb`  
		Last Modified: Fri, 12 Dec 2025 23:04:10 GMT  
		Size: 7.6 MB (7597999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c0b74efc53c5a11551937b3c0ac0e558dda2c21c713a42b1a8c90c83e929a`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26fc85eb088676c2237ad1410f2d06bf4167acef7e7573aa468e85f49ee8`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 17.6 MB (17552135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c0880b371ae9def4a59c648a03dc32de73c939a82863ed46189b5d3c1b26`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 21.5 MB (21454919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dfae8792ac984c5843e7a75359342e09ed6b06094284d3d9afef64ef8d37`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 10.2 MB (10188515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c8dcf60105513f337a71a7a302174c703f2ac4b01eca1a6976550cabbc9cb`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078bbc407a642525a8ecd8f3f56ec5f42ea4276b7984629db0dada8b0ecf69c`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091878b07b4fafc28f7778946a2e29d096eb34042255686f44fcadaea5d597`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e785e66500d9f73341d04a0d0fe01a7ca6a4ce3d3b9288e82242bc725426b`  
		Last Modified: Fri, 12 Dec 2025 23:10:40 GMT  
		Size: 6.6 MB (6570882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928ed8314751e2e9eaeabdc972d4af1311ab6177479d3b6f80a5539231796da7`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9abf1ec541ec0b256d5eab59239d0b754ddab5d999b8dc430585b6f948e604e`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233d3deeb4102367ed1ec89b7ef2fc760d574be2fc7fedd4ea2e4108be9aba6`  
		Last Modified: Fri, 12 Dec 2025 23:10:45 GMT  
		Size: 59.7 MB (59727126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b55b2d0cde4acdec0d0647c16445382a856fdacd9c1cd5fdf7116a5f96dbb4`  
		Last Modified: Fri, 12 Dec 2025 23:10:50 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603edd3336b192e57264b4a135254f9b4dc1a5761163fe26d86596342fe422de`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:0c9b638681007c9d6737a03cc64eac228cfd924c10100f3189602dd4d65d73bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70074d9836671bcf71409a77556f876fa92be1526c11bc44cf503e7077324561`

```dockerfile
```

-	Layers:
	-	`sha256:18a5d28b03d244c5685e86038be1cc676b25e374d481bfba7ced9ce1023ebe95`  
		Last Modified: Sat, 13 Dec 2025 03:07:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ae8fb276f238b912024b6b5805e3e244f0919648b835cf7a1ad0c1b791638ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126321327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b51d82ca438a87cf78f035539342acb921ff3b8a7c5c316c5dd827b52838dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1f8bb5ac9908d8a2f05285d5bafaaa09c4639ad5ec575f506b7f94eb9b027`  
		Last Modified: Fri, 12 Dec 2025 23:09:43 GMT  
		Size: 7.2 MB (7211487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07fdd52b461065d91e16e325ebe1351e98a49811bfe1953d3ffe9d71f66976`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 101.3 KB (101259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d775131bce9a8efbc68a01168997189db83ec2f6764633a853bb6c4013ba98b9`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1bdb364f96a9e042c2a09900dea9f490b2fd714dc314a9b36df5e470baa327`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 58.4 MB (58430278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039982dd10164d6a2e84e3eba3fd37ce736fbfcb0f9e03881c7ba02615b5c87`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22468ff67dbfccb6e8991c334fe5d9d379c964a9ecfe16c05d804125837727f8`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:3c36eabf6e66c492c055fbc625e84d44c47a923d35e2f46f5d13f8c90174aca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae5563a6811d6d3cc3a1e6303828b71d9608a6a4fc125183d83423348c5f2a6`

```dockerfile
```

-	Layers:
	-	`sha256:f88b5a51b8c8deb7c3b298f4e2252c16a18f817fb711be330fa64e81a65284e0`  
		Last Modified: Sat, 13 Dec 2025 03:07:37 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:ac12412d8bc07bdbc71e1bd730572dc5010a5d2116987775b30f849d1268380e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:09950db32d89c1662f1970578f51562812eab9a3eb50feb7326519f7e5514235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156928803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17a49738c68db9b440e165269dc75f5f3e74a89e9a75426199cd466b0383cd6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:14 GMT
CMD []
# Sat, 13 Dec 2025 00:10:12 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 13 Dec 2025 00:10:12 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 13 Dec 2025 00:10:12 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 13 Dec 2025 00:10:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 13 Dec 2025 00:10:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 13 Dec 2025 00:10:13 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 13 Dec 2025 00:10:13 GMT
USER rootless
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6395790a96f25fe9ae60e8642bb53dc32742cc2a952240e2430c727343070f94`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 6.9 MB (6932404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0e7dad2234067bcdefdfbe8a95f9d27a127e90c2547a0b535e998e62492f9`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 92.5 KB (92451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d2dd2748ca8b7279cc840f1717a591f741f79ca77fccc303369e23381404e`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be03fb08c790242db2d11f5c8abd1e27779400315ae4bebf6812421eb196f424`  
		Last Modified: Fri, 12 Dec 2025 23:10:36 GMT  
		Size: 64.4 MB (64390653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969ded5ab7c174111a0938c32df0c859eae02e11a1f03b285260d4e52ada118`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15928226105bb78669d71594057c0a40684760f66de44e473fe4559e048a1fc4`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7efc67e74d7bff7198949770096adae0c34ad7c6a32faa6e3d0bab24e69da51`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 3.4 MB (3419931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0ea6cd17928c2035157de458119f33ee511ec1deee23008735895ce2472b79`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b30c307447754a05b3912b60fa4a43ebe6eb174bb107be0d85866ce5cf6d0b6`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab6e3723d2a693205fe1725bd19abcfbfd2ac1331a374d8b35b7897742941c5`  
		Last Modified: Sat, 13 Dec 2025 00:10:37 GMT  
		Size: 17.4 MB (17370991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7db2853efa7da1fc8d7b3143c0f861bdc77ee5a9cce03278ff21f1568ef69c5`  
		Last Modified: Sat, 13 Dec 2025 00:10:35 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:336e04652a588e2ad4e195e403ef93c675ba97007c75e40a9efe962cb4f16bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd1e5b602cf458f135106fdc1b6bee98d42185597cd98c67410b6c1c42dc34f`

```dockerfile
```

-	Layers:
	-	`sha256:e3a762cb9f51fe6d372134b550c76079147291d858530a914cc826e7d8dbc1d9`  
		Last Modified: Sat, 13 Dec 2025 03:07:42 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7deb6a567eeef7d5a72412f239f2170d024ede941b350b13f24ebf9abc29721e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147425780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229ad388f6f6b781e7a9b6825675f4deeb04ea90f1123729e79549a7b32b83ac`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:25 GMT
CMD []
# Sat, 13 Dec 2025 00:09:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 13 Dec 2025 00:09:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 13 Dec 2025 00:09:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 13 Dec 2025 00:10:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 13 Dec 2025 00:10:01 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 13 Dec 2025 00:10:01 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 13 Dec 2025 00:10:01 GMT
USER rootless
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1f8bb5ac9908d8a2f05285d5bafaaa09c4639ad5ec575f506b7f94eb9b027`  
		Last Modified: Fri, 12 Dec 2025 23:09:43 GMT  
		Size: 7.2 MB (7211487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07fdd52b461065d91e16e325ebe1351e98a49811bfe1953d3ffe9d71f66976`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 101.3 KB (101259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d775131bce9a8efbc68a01168997189db83ec2f6764633a853bb6c4013ba98b9`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1bdb364f96a9e042c2a09900dea9f490b2fd714dc314a9b36df5e470baa327`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 58.4 MB (58430278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039982dd10164d6a2e84e3eba3fd37ce736fbfcb0f9e03881c7ba02615b5c87`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22468ff67dbfccb6e8991c334fe5d9d379c964a9ecfe16c05d804125837727f8`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb2d13730b1a2b9437f55aa38844a2d4f3a41baff03b9ba200fd6c8e3640f65`  
		Last Modified: Sat, 13 Dec 2025 00:10:27 GMT  
		Size: 3.4 MB (3394382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c5eda520ed158582d67f72a42c82eef1d312c24f5fb51f16441c4772825971`  
		Last Modified: Sat, 13 Dec 2025 00:10:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05db2d742efc92d52e078c87f0af299e70fb014fbfaea3a18b757374eca9af`  
		Last Modified: Sat, 13 Dec 2025 00:10:27 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9af16ab409354af0d1a5b9a8dd6362e6886e59680f35e8fc253d99c504af99`  
		Last Modified: Sat, 13 Dec 2025 00:10:32 GMT  
		Size: 17.7 MB (17708729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffd4a2a8cc857d1398fdf583e20112730537572a29d8c9100512be073ec09d8`  
		Last Modified: Sat, 13 Dec 2025 00:10:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6eab544cd873580b808013fbe86c7cc254767cc99c60313d1cd9f4e5eccb9f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c814e243bbda6587996667fdd159361b2cc27f15e889e349a1976482785bda18`

```dockerfile
```

-	Layers:
	-	`sha256:3a3842cd2beb5724ad7a78418740bfd432103bce0f213347880883022e4a0094`  
		Last Modified: Sat, 13 Dec 2025 03:07:45 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:7370a6c49b7e708fb969b422dffe6cdd78a9f0ff5b3bfba0e0cddce736c49eaf
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
$ docker pull docker@sha256:614db3c0aa1f5a2fe91d4bbbb0df8190c5d233d6ad55aa0f285c29f54227f7dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136136542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8274856237f1b49083c42adab01ae804b00b8eeddb621e75b53e8c7a18657249`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:37 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:38 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:00:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:00:40 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:00:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:00:41 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:00:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:00:42 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:00:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:00:42 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:12 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:14 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:14 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ed8c6ed98d2404de8d25ee331d19e421397ba4b1bae26436f8e7c534e2468`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 8.4 MB (8399222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b392bd67cfbded80bc603bd71d69afbd3f667fb107633e7e87930104e56f593d`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436cebc0ac3974288b1de6303ee63cac28644b4b2ecf5c327ee068d0fd65765`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 18.8 MB (18764413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfaaa0831573544888c2d625781794f454a3b4854285ac999ad55f5a0f82a6`  
		Last Modified: Fri, 12 Dec 2025 23:00:59 GMT  
		Size: 22.9 MB (22905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6eed2678361a18b81e161a9968aaac53ab6d9a19649fb712c23e8b4c3624b6`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 10.8 MB (10784448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f06bc095e3936bd9a6f91928a199e023b3d7c1c64c54c41f50820fa025e1a`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092c6280b8367dd4adaa422f03e6c1df6e1207496323c52d77fac2a61428397`  
		Last Modified: Fri, 12 Dec 2025 23:00:57 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f755eec0b602b9139519e1dede43ef7b62d133a7fcdc9559a67396af7679f8db`  
		Last Modified: Fri, 12 Dec 2025 23:00:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6395790a96f25fe9ae60e8642bb53dc32742cc2a952240e2430c727343070f94`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 6.9 MB (6932404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0e7dad2234067bcdefdfbe8a95f9d27a127e90c2547a0b535e998e62492f9`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 92.5 KB (92451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d2dd2748ca8b7279cc840f1717a591f741f79ca77fccc303369e23381404e`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be03fb08c790242db2d11f5c8abd1e27779400315ae4bebf6812421eb196f424`  
		Last Modified: Fri, 12 Dec 2025 23:10:36 GMT  
		Size: 64.4 MB (64390653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3969ded5ab7c174111a0938c32df0c859eae02e11a1f03b285260d4e52ada118`  
		Last Modified: Fri, 12 Dec 2025 23:10:33 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15928226105bb78669d71594057c0a40684760f66de44e473fe4559e048a1fc4`  
		Last Modified: Fri, 12 Dec 2025 23:10:32 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:d872ccf708c0c6cf248b60f3628d4f6c144e2b9b28d7249d5e99349e036598bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2e79926af9c2cfd84fb6eaa06ee2a235ee5389bbc8f0c528a68c05c925f98c`

```dockerfile
```

-	Layers:
	-	`sha256:dfa8b777c70191bcd2b044ff54627b657daadee8f5c1dfcae039cb25aa6d9e66`  
		Last Modified: Sat, 13 Dec 2025 03:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:e290522631fba31e8ef320a62d0efe0f7bd279c504aacea1b231502c56c75d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128368324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52adaa135524f86585c09c3b6ea713da7b19764a9bb3853687c4410ff4057193`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:00:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:00:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:01:02 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:01:02 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:01:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:01:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:01:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:01:06 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:01:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:01:06 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:24 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:29 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:29 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:29 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:29 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:29 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a442d3375c6cf3a0d64cab9a5657f13a2ad79d715217080e57d4091d88c4324`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 8.3 MB (8301082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d2ff8b4dcb5e27c0a3ebecc8f29e07008e917fc5a5a7a6dfeece3f50f8613`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaf22d2b96392d2b3c9f1cb454ed14bc66a1dfdef830883f46ed5613c0133d4`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 17.6 MB (17563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be201cbc63828006213cbca3a3f8b91138447829d70553ea57b47fb7b36316`  
		Last Modified: Fri, 12 Dec 2025 23:01:28 GMT  
		Size: 21.5 MB (21476558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e492ed6855e1816d78b7edbd4cdc38ef0cb81d978dfc857129d58d22c754fa`  
		Last Modified: Fri, 12 Dec 2025 23:01:25 GMT  
		Size: 10.2 MB (10195786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e50a36847c59872394550e672e167266ae450d58950ec050895f9a2b8b650e3`  
		Last Modified: Fri, 12 Dec 2025 23:01:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836b06438ad83afcbbb80d394f9a68dc224a96dbc3f7446ef31113fbd4fc107`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b844bcb311c659e5cab12e879fb055dd4d63aaca8e759553df1c68ad8f8572a0`  
		Last Modified: Fri, 12 Dec 2025 23:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f78a51ea72b486ea303cfe9a35e0936165e64f6c1ce623050f1bbc03783827e`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 7.3 MB (7269237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150a1e8e9e07769ffd55ede4c3ebe7b37a7d4a52e59841483c2f1dc104a73cd`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 91.7 KB (91744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d880baf4277f9d0addd5734ad6cd8ef5e32b361ae8196dffbee590ccd63e28c2`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba95d05539ea20cd2ad894c3b01011b5412ac30470cf2067be3a4de6893fb49`  
		Last Modified: Fri, 12 Dec 2025 23:09:51 GMT  
		Size: 59.9 MB (59894425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d365292960a46a15ee408a118f8ed3443f9de61abacc32b1e1c93ca107c203b`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad152b473b5d59ed3116b07b37f35d4bc0fc85aa8364882c610816bea229f3bf`  
		Last Modified: Fri, 12 Dec 2025 23:09:46 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:c70c7dcb7dfdb1cc89722c4c1299406e1924186e972fd94deb54abbd1052301a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bec62c6dbaf983fd287f9991784c3219e307aceca7be3d32fe32b63d7b2187f`

```dockerfile
```

-	Layers:
	-	`sha256:fff0c79b6617bada32062564279ba2c4c61cab0f5d7fb8bcdb5ac4e87f9f393c`  
		Last Modified: Sat, 13 Dec 2025 03:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:71a0b301e07cfb3145b58f5e33589420b2f0e643d9376d35097d4d402673c64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126466294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e849666bdf05465f46c218af24544c6a84be85d4505f05f1a67f2439df655afb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:44 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:47 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:48 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:48 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:10:19 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:10:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:10:22 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:10:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:10:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:10:22 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbf8f000eac737bf318d60725474e05cf5bb1d57c289c8f1a9fc5a087446bbb`  
		Last Modified: Fri, 12 Dec 2025 23:04:10 GMT  
		Size: 7.6 MB (7597999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c0b74efc53c5a11551937b3c0ac0e558dda2c21c713a42b1a8c90c83e929a`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d26fc85eb088676c2237ad1410f2d06bf4167acef7e7573aa468e85f49ee8`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 17.6 MB (17552135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f9c0880b371ae9def4a59c648a03dc32de73c939a82863ed46189b5d3c1b26`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 21.5 MB (21454919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56dfae8792ac984c5843e7a75359342e09ed6b06094284d3d9afef64ef8d37`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 10.2 MB (10188515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c8dcf60105513f337a71a7a302174c703f2ac4b01eca1a6976550cabbc9cb`  
		Last Modified: Fri, 12 Dec 2025 23:04:04 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5078bbc407a642525a8ecd8f3f56ec5f42ea4276b7984629db0dada8b0ecf69c`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51091878b07b4fafc28f7778946a2e29d096eb34042255686f44fcadaea5d597`  
		Last Modified: Fri, 12 Dec 2025 23:04:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e785e66500d9f73341d04a0d0fe01a7ca6a4ce3d3b9288e82242bc725426b`  
		Last Modified: Fri, 12 Dec 2025 23:10:40 GMT  
		Size: 6.6 MB (6570882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928ed8314751e2e9eaeabdc972d4af1311ab6177479d3b6f80a5539231796da7`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 88.1 KB (88101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9abf1ec541ec0b256d5eab59239d0b754ddab5d999b8dc430585b6f948e604e`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233d3deeb4102367ed1ec89b7ef2fc760d574be2fc7fedd4ea2e4108be9aba6`  
		Last Modified: Fri, 12 Dec 2025 23:10:45 GMT  
		Size: 59.7 MB (59727126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b55b2d0cde4acdec0d0647c16445382a856fdacd9c1cd5fdf7116a5f96dbb4`  
		Last Modified: Fri, 12 Dec 2025 23:10:50 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603edd3336b192e57264b4a135254f9b4dc1a5761163fe26d86596342fe422de`  
		Last Modified: Fri, 12 Dec 2025 23:10:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:0c9b638681007c9d6737a03cc64eac228cfd924c10100f3189602dd4d65d73bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70074d9836671bcf71409a77556f876fa92be1526c11bc44cf503e7077324561`

```dockerfile
```

-	Layers:
	-	`sha256:18a5d28b03d244c5685e86038be1cc676b25e374d481bfba7ced9ce1023ebe95`  
		Last Modified: Sat, 13 Dec 2025 03:07:35 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ae8fb276f238b912024b6b5805e3e244f0919648b835cf7a1ad0c1b791638ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126321327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b51d82ca438a87cf78f035539342acb921ff3b8a7c5c316c5dd827b52838dba`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Dec 2025 23:03:20 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 12 Dec 2025 23:03:20 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:03:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 12 Dec 2025 23:03:23 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:03:24 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:03:24 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 12 Dec 2025 23:03:25 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 12 Dec 2025 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Dec 2025 23:03:25 GMT
CMD ["sh"]
# Fri, 12 Dec 2025 23:09:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 12 Dec 2025 23:09:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 12 Dec 2025 23:09:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Dec 2025 23:09:25 GMT
VOLUME [/var/lib/docker]
# Fri, 12 Dec 2025 23:09:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 12 Dec 2025 23:09:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 12 Dec 2025 23:09:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913956074c40562de1c9f07a0805cf4a0051709def8efea7dca321f0b579fc4`  
		Last Modified: Fri, 12 Dec 2025 23:03:47 GMT  
		Size: 8.5 MB (8453489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e12cc29c990b88541c0f02c0080c2693ba2ddb7ca89e193f585615a82a68be`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6088b3e3a871e63b060e2ffc732ca21a1de229f03dbefa5a748d6d4aa77d83`  
		Last Modified: Fri, 12 Dec 2025 23:03:42 GMT  
		Size: 17.3 MB (17337704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d0e7f4db6f6bd5fa6a463586ca1d63dee296a1965791536c8e815e858c91ea`  
		Last Modified: Fri, 12 Dec 2025 23:03:40 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce23931b532c773ccd0c9c89ab8476c0d0875895c9eeb9a47c5f0ecc1081995f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 9.9 MB (9938702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c286d7cb026f710041a2a3b8c7c1cf739af7d667994c104d210851408d3b2f`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9573c85100de2c026352b8716746dcdb238f7d63ec9c40a66fc42fefb53e723`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d642624667876441edb900437c766c69a6e5c8e505c852299931efda4b3765`  
		Last Modified: Fri, 12 Dec 2025 23:03:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d1f8bb5ac9908d8a2f05285d5bafaaa09c4639ad5ec575f506b7f94eb9b027`  
		Last Modified: Fri, 12 Dec 2025 23:09:43 GMT  
		Size: 7.2 MB (7211487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be07fdd52b461065d91e16e325ebe1351e98a49811bfe1953d3ffe9d71f66976`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 101.3 KB (101259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d775131bce9a8efbc68a01168997189db83ec2f6764633a853bb6c4013ba98b9`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1bdb364f96a9e042c2a09900dea9f490b2fd714dc314a9b36df5e470baa327`  
		Last Modified: Fri, 12 Dec 2025 23:09:47 GMT  
		Size: 58.4 MB (58430278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a039982dd10164d6a2e84e3eba3fd37ce736fbfcb0f9e03881c7ba02615b5c87`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22468ff67dbfccb6e8991c334fe5d9d379c964a9ecfe16c05d804125837727f8`  
		Last Modified: Fri, 12 Dec 2025 23:09:42 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:3c36eabf6e66c492c055fbc625e84d44c47a923d35e2f46f5d13f8c90174aca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae5563a6811d6d3cc3a1e6303828b71d9608a6a4fc125183d83423348c5f2a6`

```dockerfile
```

-	Layers:
	-	`sha256:f88b5a51b8c8deb7c3b298f4e2252c16a18f817fb711be330fa64e81a65284e0`  
		Last Modified: Sat, 13 Dec 2025 03:07:37 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:24e3252850071e0729b50e765be6eb141aec202a2709217891272b9d2a8efb7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `docker:windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:072f69cc9a1bc2cb016cd912ee5dcb075d0f2e73df576a46f98ddb1f3f8a4ea2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308280068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e356747fea9e9e69ddc2df399e0a31cb31c5c255da4f7f8ff52e08eef859a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Fri, 12 Dec 2025 23:51:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:51:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:51:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:33 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:51:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:43 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:51:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49db97996aeb50d6cc3bb59d05b2805a04f9a341f791d3bbf78f96c91ea6ea46`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e012252a5c78e6736aa02ede33d15956b820e11e10d32c0eed00f4ac4c0642ed`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 365.2 KB (365173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba990e6755d56a5110398c67645345164f3cb13a4f31f2c87cd0cf475b2fddc`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df48c7a2c9538324b83a4a6378f6ecbcf5c51d2b4c853c98b154d3d2e1fe23c`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9a30b43b8cff73e13f7e796431a6d59d40548fd5ed22e9f0f643554cffa66`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 19.4 MB (19430080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053e9422e23dca07aade3c64cf9355ecc9227c50dd075cde8a77bf5f588fdf07`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d53e5a50955843cf8df23bd9852867dc4e044732ab6a2c3dff445d30a03969`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6a3bffb040caaef43c930bcf019f71c62523c17c8c3aa21340ce83fd63c367`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5297cc0777d4cd44c02f2f373fa189394855ab3f6e99fb51e0e9b14dcbe7719`  
		Last Modified: Sat, 13 Dec 2025 00:10:41 GMT  
		Size: 23.9 MB (23916756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d343979aeb667bd44bc30f0385636c1525e1007c30d7a56b0c4b2929e986e3ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e484e796b3e881c2c53ab847de762b0acce3ce695452b588333031fd16f4722`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1d8d8a0183df8a67af7c17491af2ce9bcc2f1e5bed8a1b7337d9cc59d72a48`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e066997579a2dbc121185aac60816764e96c1cbce7d351630d1ae1a79062f7ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 11.4 MB (11435912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:6c63e74fbbe6a6853d2eed17e74a22a1f27caa6652d65e73237c8cdae1584560
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835158901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31a8d2106c0d362d41e18b340f4ce9fcb284d2750fd96d7010599996e10f95a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Fri, 12 Dec 2025 23:42:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:42:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:42:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:35 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:42:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:42:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a59061a4bd19a5f5104deac5c13f08378f0d057b550fa44336edd48c297a30`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d45f349269329c39cb7f626e581200a0cfd951639d64b460dc496e827a02d3`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 496.4 KB (496422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbbd38f48aebab5ee03921c61d62bc51aafa5296de9f243a1b119cb5b9b59e8`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38e962b0dcf2e2174265dd10ed886b4ac610012a54d0a165b374784dfbfaf5b`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b233205356122f2ba9d651e4d85f51b9efc8720271061a670c3d376808be4df`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 19.4 MB (19421634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4696a1bc6b20cc354eebea761ac5c3e7bee2e41055c2310c9e1efda5acac04cc`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8453a804e2b4641b89e10a12a6711adc2ed009fb0687ea447f9edc9d0ce9b9`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05197d8ed628728e4a93c7c6f52a0cafa2263039f4526e490b5f873167e1144`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b28a4909f7f0860e1395562cbebd921b09728397d7a533d1f7cd4b5d31e1671`  
		Last Modified: Fri, 12 Dec 2025 23:43:12 GMT  
		Size: 23.9 MB (23918113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926c23fb5c1c50e722a5b86e6ae921cd02d73d170dff76ff2af4910598654ae`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594a752382b75756d57cf29a40ab0bde12a567d548acf7cd83772f09c4a21930`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1087bd776bf52196852d02423f98f410d12929744cedd00d7c48c7c0b2113`  
		Last Modified: Fri, 12 Dec 2025 23:43:10 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e85bde05b43a43ab482a075807c5b38bbe7bf9b47871b3147d117cff05b772`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 11.4 MB (11431570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c0c8ea04bc96a986cc33445b9d46d8a5607e447352d26cc9bd8c0a8845fca4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:6c63e74fbbe6a6853d2eed17e74a22a1f27caa6652d65e73237c8cdae1584560
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835158901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31a8d2106c0d362d41e18b340f4ce9fcb284d2750fd96d7010599996e10f95a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Fri, 12 Dec 2025 23:42:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:42:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:42:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:42:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:35 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:42:36 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:42:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:42:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:42:45 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:42:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a59061a4bd19a5f5104deac5c13f08378f0d057b550fa44336edd48c297a30`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d45f349269329c39cb7f626e581200a0cfd951639d64b460dc496e827a02d3`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 496.4 KB (496422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbbd38f48aebab5ee03921c61d62bc51aafa5296de9f243a1b119cb5b9b59e8`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38e962b0dcf2e2174265dd10ed886b4ac610012a54d0a165b374784dfbfaf5b`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b233205356122f2ba9d651e4d85f51b9efc8720271061a670c3d376808be4df`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 19.4 MB (19421634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4696a1bc6b20cc354eebea761ac5c3e7bee2e41055c2310c9e1efda5acac04cc`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8453a804e2b4641b89e10a12a6711adc2ed009fb0687ea447f9edc9d0ce9b9`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05197d8ed628728e4a93c7c6f52a0cafa2263039f4526e490b5f873167e1144`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b28a4909f7f0860e1395562cbebd921b09728397d7a533d1f7cd4b5d31e1671`  
		Last Modified: Fri, 12 Dec 2025 23:43:12 GMT  
		Size: 23.9 MB (23918113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926c23fb5c1c50e722a5b86e6ae921cd02d73d170dff76ff2af4910598654ae`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594a752382b75756d57cf29a40ab0bde12a567d548acf7cd83772f09c4a21930`  
		Last Modified: Fri, 12 Dec 2025 23:43:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1087bd776bf52196852d02423f98f410d12929744cedd00d7c48c7c0b2113`  
		Last Modified: Fri, 12 Dec 2025 23:43:10 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e85bde05b43a43ab482a075807c5b38bbe7bf9b47871b3147d117cff05b772`  
		Last Modified: Fri, 12 Dec 2025 23:43:11 GMT  
		Size: 11.4 MB (11431570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:f862456b5cfe6c2b259f159ae0b967e1a05ad2839c2798b3c9b755e2447508dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:072f69cc9a1bc2cb016cd912ee5dcb075d0f2e73df576a46f98ddb1f3f8a4ea2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308280068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e356747fea9e9e69ddc2df399e0a31cb31c5c255da4f7f8ff52e08eef859a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Fri, 12 Dec 2025 23:51:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Dec 2025 23:51:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_VERSION=29.1.3
# Fri, 12 Dec 2025 23:51:23 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.3.zip
# Fri, 12 Dec 2025 23:51:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:33 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Fri, 12 Dec 2025 23:51:34 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Fri, 12 Dec 2025 23:51:43 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 12 Dec 2025 23:51:43 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Fri, 12 Dec 2025 23:51:44 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Fri, 12 Dec 2025 23:51:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49db97996aeb50d6cc3bb59d05b2805a04f9a341f791d3bbf78f96c91ea6ea46`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e012252a5c78e6736aa02ede33d15956b820e11e10d32c0eed00f4ac4c0642ed`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 365.2 KB (365173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba990e6755d56a5110398c67645345164f3cb13a4f31f2c87cd0cf475b2fddc`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df48c7a2c9538324b83a4a6378f6ecbcf5c51d2b4c853c98b154d3d2e1fe23c`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f9a30b43b8cff73e13f7e796431a6d59d40548fd5ed22e9f0f643554cffa66`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 19.4 MB (19430080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053e9422e23dca07aade3c64cf9355ecc9227c50dd075cde8a77bf5f588fdf07`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d53e5a50955843cf8df23bd9852867dc4e044732ab6a2c3dff445d30a03969`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6a3bffb040caaef43c930bcf019f71c62523c17c8c3aa21340ce83fd63c367`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5297cc0777d4cd44c02f2f373fa189394855ab3f6e99fb51e0e9b14dcbe7719`  
		Last Modified: Sat, 13 Dec 2025 00:10:41 GMT  
		Size: 23.9 MB (23916756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d343979aeb667bd44bc30f0385636c1525e1007c30d7a56b0c4b2929e986e3ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e484e796b3e881c2c53ab847de762b0acce3ce695452b588333031fd16f4722`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1d8d8a0183df8a67af7c17491af2ce9bcc2f1e5bed8a1b7337d9cc59d72a48`  
		Last Modified: Sat, 13 Dec 2025 00:10:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e066997579a2dbc121185aac60816764e96c1cbce7d351630d1ae1a79062f7ff`  
		Last Modified: Sat, 13 Dec 2025 00:10:40 GMT  
		Size: 11.4 MB (11435912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
