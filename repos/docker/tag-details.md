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
$ docker pull docker@sha256:40916fb078cdd27640d069bba401324a15a06d3ecbd8895048122c8d321f43f8
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
$ docker pull docker@sha256:967468c0be954e3a0d4bc31310e196a5a8d1adda607b0be11056d4d1badd6587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136137253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad869b62b5c060fe1594ae7fd17228cbc7468da180d9192bd8d59c1b17c896b3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:12:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:12:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:12:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:12:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:12:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:12:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:12:38 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:17 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9948ae9a3223520d912ab66de5d55ae24d29c808a510d02ab8cefd00f6af1`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 8.4 MB (8399334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b09731169ba7df8d96a4bb9a1a6ab3d4c1560d30cc4429e0e0180131ccaf7c9`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22939237c954384f47f26a89ee0dd27d44805625e73797e594c00dfe4f40b97a`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 18.8 MB (18763825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb36afae27f4bbcb70ff6c2154f9a0c7e0e5aeb479254c14e3d97743d63765d`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 22.9 MB (22905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf52db4eb6dc458063c42a6e1ccff1a420fc8ca9c6054305aa393dcb100491`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 10.8 MB (10784455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0739e6c04d86d46c4bbd27f2c6aeddd85de220909f633494d0d453f69475e1f`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33287860d4ed49c1e91d9f437b63622f4a717e826b7d3aa4d3cc847adfbd85fe`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8131e857b4a01669f532d44efd02dc2eced5ae48d3eeaee6272747a38064919`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ceb3774725100b39cc84625299eaf7a38cd9350fc52d2bb092d2261483b6b`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 6.9 MB (6932412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb61cbf781bf1ad1f584b29991a24c4ad159bb77066a66dfbc69d0530c956bd`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 92.4 KB (92445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f614095489d33530a88164a8c28f37b2d4905f0b80d0d6b55f20aaadfd70949`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebf1832bba38f06f167c58af841378ce16e956f5bbf93fac3890ad9c28c8cbf`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 64.4 MB (64391839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40879250d388c3438681a3fcb4c0dfd255a9608c7640fef9336b0e41182e1f96`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e36d8cddb77fc04b3f2ce2f905702ec5fa87992d2042e8c67f1270e0a00d47`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:f9bb7ce8788987c53f7376c978032c32bd32ceb0a11d3922bd1f30e83a330420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488001f5e00c1d96abaa4ef21598a7cb0c85dcdc849cc938a582649148cbfa1f`

```dockerfile
```

-	Layers:
	-	`sha256:f4371bf22d65b61f21247586c39a31945ff88f568ae5663039cabcbb9a800af7`  
		Last Modified: Thu, 04 Dec 2025 06:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:414cac80b8731cec0ba7269b2401349a90593d66af7a0861ec3c7d0198f4f25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128364231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab64be5a5da0cbe0bcc502e6958aa17939272152b190069d69458ac92d5ce4bd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:18:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:18:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:18:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:18:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:18:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:18:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:18:46 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:14:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:14:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:14:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:14:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:14:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:14:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:14:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:14:14 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af6abcf03c4d2a46ff1f3cf4e321bc7993d4d20b17f12f99d466b39b3555298`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 8.3 MB (8301067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb792a943c4d38855261216162c97e27587aa936e4de5451eeda4d170348a07`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309aa1d961beedab5a903eed7b199a7f3cf448a9ad0d235f989735bce0000963`  
		Last Modified: Thu, 04 Dec 2025 01:19:02 GMT  
		Size: 17.6 MB (17560675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136294917ec3532038026ad3f18199c6aff9e645109302b3c9fdc832bf5dd82`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 21.5 MB (21476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e0b74dd96a21e6b38324422ba118ccd940a01d181d09275193f948ebd543d2`  
		Last Modified: Thu, 04 Dec 2025 01:19:00 GMT  
		Size: 10.2 MB (10195783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48a193c8f7c9fb004babea7c82efc513b5196991d924daf956f6881012fec3`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86d05610e4cf2f79db6d09c9b4c2c8944991a0da701d442726824c5daf33ae`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ebf88cb27a0d9b7e72386749701cbb0df6c753c53caa647578e1151c9f6e0`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2889ceaea16d005f911037ba1943baa11fca8f5499572f26e08d1623571b0fca`  
		Last Modified: Thu, 04 Dec 2025 02:14:36 GMT  
		Size: 7.3 MB (7269170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a951be59abc423fe14ab9e8f769c4aab51ee15004ef9b7cccad5f65451fb56`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 91.7 KB (91736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e9ad64722f26f00125e9b549b06d40a727849d2f9550dc66a6533d89ebf8fa`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31cd3ee01e94bb58480e2a72b8f3677d9457fa9a26aa6f8b63431dbc313074e`  
		Last Modified: Thu, 04 Dec 2025 02:14:43 GMT  
		Size: 59.9 MB (59893205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0159762f19a8b9a93c9555ca6508e536ae2ffa5221f1f7fe2517b25edb26c7df`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b0105e4b3b66292b7fa5025b925cfea155b39007901429ba1dad2b3064ee51`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:ab05258dcfbb29e603677ce44f578d475223727587324270624d8ea011d7ccda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20281852242edf20349d07841d8bc88fc25a406146000e725cf15a381d07094a`

```dockerfile
```

-	Layers:
	-	`sha256:e799d064fde967b53c6149a5df7009511ddce4ce4274868ee730661a6eeb37be`  
		Last Modified: Thu, 04 Dec 2025 06:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:0541f6653d52b64dd6cd2d3d726aee9bca91947de8a574f57303b4f1636a14f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126462847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209da4e636036ccbab56e97d822d0ab39a923aa5572a22674e75a74493b686c2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:17:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:17:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:17:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:17:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:17:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:17:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:17:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:17:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:17:29 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:09:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:09:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:09:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:09:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:09:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:09:21 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab67aee2b47b20a25046ed73de706bd5a80ad82192c27db420a65cfa5fb17cb`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 7.6 MB (7598018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860397c02592909361c994060954f1d684dc0366a2df922a3fe521f02a6b6b2`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ddf54b4c1a081004e3eb1cd154ca1c1cc7e169e416c1ebb9fb23b872919a4d`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 17.6 MB (17550083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645b95707890af1cad5443377a3d8bba32e3701d1f59ee629bd3a1598e45b63`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 21.5 MB (21454910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d968e842fbfa0f7d8d14048d776e945449a586f5772cf04dc12753e58629d9`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 10.2 MB (10188525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9482495d52b3d32ead0b4c76816259e750cf45944ac6a48937ed5de349bc73b`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862303f1e616b7c4e5debf343f489e54323b1d7e8d897d6bbcf9951c6fb125e7`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581b42590dfec33aa271798a0fdbb5fb080fa6137a58beb89183e43d609cc24`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef35268d1c5043e126a7b2b7cccba9910ba866f3721d67bc80d8768966a3202`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 6.6 MB (6570913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6110fc79c7e532c554cef8b106c77e384dffc4dbe8ff453044efb95611640865`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 88.1 KB (88108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eebdb0a3d24aad8069039ec36bba107f65570fd4460d47f5c5bc29bd7ab18c9`  
		Last Modified: Thu, 04 Dec 2025 02:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ff8b61a42ac17a9147133f9cfb9f005cc5a7597c4fbe27bd8305f307f0413a`  
		Last Modified: Thu, 04 Dec 2025 02:09:51 GMT  
		Size: 59.7 MB (59725679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5721cb1c43ef63e8c0bce0addcaa897e3b41d32fe7bf88c8020981f6cf24833f`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ef0da11c43d1593fd48c517bb7f91d37aba3bdf335ba6c03da014da92736e`  
		Last Modified: Thu, 04 Dec 2025 02:09:42 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:5ac10dc71cf0cc09125a924469cb4aecc84840796fde5d9d0342a0baee3f5507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37587e9d82c759400bbe91d7affa6d8bed70364b85068a5dceef5c381a8f048a`

```dockerfile
```

-	Layers:
	-	`sha256:a20dd7c4bd39660f77009db4c78ecbaf59987f8c583b5a69d876f11f05d0da6e`  
		Last Modified: Thu, 04 Dec 2025 06:07:37 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:835173465724c55bedd93b72bdb6724104693472836d4354236bd9f87ccc6e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126316862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1db13432a7537ebc347611396429d42295ceb944903b73ab7ed6ca66a7d24ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:14:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:14:01 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf7527ac3d38e2b3f6d1176cd286fb31e55896c8724ba176b4d4958e4075db2`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 8.5 MB (8453465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4639c90abf56c9e413f2f2d2c096aefc19cf619ba9f5b28d891218b96ce733`  
		Last Modified: Thu, 04 Dec 2025 01:14:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc4c4bdc3b3639f19fd743ed949e35d8d7164a53fa32494422b203bbc675f5`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 17.3 MB (17334885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787c5406b3fa1fc1c5f4ee10e3f972d710de70beb323a67ceb5aa62273f8aa2`  
		Last Modified: Thu, 04 Dec 2025 01:14:22 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772518255e899b197408165167764a4d01d2b1098d6b40716fe91444be12a43c`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 9.9 MB (9938698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa62af1a24bf51d9a4d39915667786eb279e97dab96543236a409060be26a4`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a485df48fa9519df08360fc32bc48f54c3e8645b16565c58654267487f7bff`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e420e20b91d5cf88de9d2f64e34c09ebf8fa77ab2147c66fe59fbc546b08a64`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4ec7220c3f61f31eba0afab7f6e4defe2bc8ce778302f7ccbe98325fbc2`  
		Last Modified: Thu, 04 Dec 2025 02:12:44 GMT  
		Size: 7.2 MB (7211504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216239cfaa66c6158aaee65ef2d3ce737384d2ee872d2a74d4ae2f0178284e69`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 101.3 KB (101256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba097afc00e56a014d7ba0d623f39b67a2e68e4d622113752ce9e9e03e2308f9`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0c46a299f22b7f8f78c049709892e1660352aa8fe591e54e27030774b69e3d`  
		Last Modified: Thu, 04 Dec 2025 02:12:47 GMT  
		Size: 58.4 MB (58428644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c271f430dfb557ed996372a070b01fc71fd92aa464beb69530d45a33dd887b`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3583ad88ca4d8e567b11ce83128811bc0c359cfa889e192896e0942686282598`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:1d3c36d88728fafa4708e5ffc1a34ae3be9c093b4668b882bd3f9b2808df9f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c9de27527effa797f1e73c2627b71d4d65243f3429a0fff7dd7a42d9601934`

```dockerfile
```

-	Layers:
	-	`sha256:467e80fb00d99af46899eed546c4f3c351297a1b14166825411e06dcbb6f39e2`  
		Last Modified: Thu, 04 Dec 2025 06:07:40 GMT  
		Size: 34.8 KB (34775 bytes)  
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
$ docker pull docker@sha256:40916fb078cdd27640d069bba401324a15a06d3ecbd8895048122c8d321f43f8
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
$ docker pull docker@sha256:967468c0be954e3a0d4bc31310e196a5a8d1adda607b0be11056d4d1badd6587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136137253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad869b62b5c060fe1594ae7fd17228cbc7468da180d9192bd8d59c1b17c896b3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:12:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:12:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:12:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:12:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:12:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:12:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:12:38 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:17 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9948ae9a3223520d912ab66de5d55ae24d29c808a510d02ab8cefd00f6af1`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 8.4 MB (8399334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b09731169ba7df8d96a4bb9a1a6ab3d4c1560d30cc4429e0e0180131ccaf7c9`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22939237c954384f47f26a89ee0dd27d44805625e73797e594c00dfe4f40b97a`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 18.8 MB (18763825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb36afae27f4bbcb70ff6c2154f9a0c7e0e5aeb479254c14e3d97743d63765d`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 22.9 MB (22905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf52db4eb6dc458063c42a6e1ccff1a420fc8ca9c6054305aa393dcb100491`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 10.8 MB (10784455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0739e6c04d86d46c4bbd27f2c6aeddd85de220909f633494d0d453f69475e1f`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33287860d4ed49c1e91d9f437b63622f4a717e826b7d3aa4d3cc847adfbd85fe`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8131e857b4a01669f532d44efd02dc2eced5ae48d3eeaee6272747a38064919`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ceb3774725100b39cc84625299eaf7a38cd9350fc52d2bb092d2261483b6b`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 6.9 MB (6932412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb61cbf781bf1ad1f584b29991a24c4ad159bb77066a66dfbc69d0530c956bd`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 92.4 KB (92445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f614095489d33530a88164a8c28f37b2d4905f0b80d0d6b55f20aaadfd70949`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebf1832bba38f06f167c58af841378ce16e956f5bbf93fac3890ad9c28c8cbf`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 64.4 MB (64391839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40879250d388c3438681a3fcb4c0dfd255a9608c7640fef9336b0e41182e1f96`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e36d8cddb77fc04b3f2ce2f905702ec5fa87992d2042e8c67f1270e0a00d47`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f9bb7ce8788987c53f7376c978032c32bd32ceb0a11d3922bd1f30e83a330420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488001f5e00c1d96abaa4ef21598a7cb0c85dcdc849cc938a582649148cbfa1f`

```dockerfile
```

-	Layers:
	-	`sha256:f4371bf22d65b61f21247586c39a31945ff88f568ae5663039cabcbb9a800af7`  
		Last Modified: Thu, 04 Dec 2025 06:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:414cac80b8731cec0ba7269b2401349a90593d66af7a0861ec3c7d0198f4f25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128364231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab64be5a5da0cbe0bcc502e6958aa17939272152b190069d69458ac92d5ce4bd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:18:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:18:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:18:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:18:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:18:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:18:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:18:46 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:14:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:14:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:14:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:14:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:14:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:14:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:14:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:14:14 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af6abcf03c4d2a46ff1f3cf4e321bc7993d4d20b17f12f99d466b39b3555298`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 8.3 MB (8301067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb792a943c4d38855261216162c97e27587aa936e4de5451eeda4d170348a07`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309aa1d961beedab5a903eed7b199a7f3cf448a9ad0d235f989735bce0000963`  
		Last Modified: Thu, 04 Dec 2025 01:19:02 GMT  
		Size: 17.6 MB (17560675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136294917ec3532038026ad3f18199c6aff9e645109302b3c9fdc832bf5dd82`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 21.5 MB (21476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e0b74dd96a21e6b38324422ba118ccd940a01d181d09275193f948ebd543d2`  
		Last Modified: Thu, 04 Dec 2025 01:19:00 GMT  
		Size: 10.2 MB (10195783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48a193c8f7c9fb004babea7c82efc513b5196991d924daf956f6881012fec3`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86d05610e4cf2f79db6d09c9b4c2c8944991a0da701d442726824c5daf33ae`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ebf88cb27a0d9b7e72386749701cbb0df6c753c53caa647578e1151c9f6e0`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2889ceaea16d005f911037ba1943baa11fca8f5499572f26e08d1623571b0fca`  
		Last Modified: Thu, 04 Dec 2025 02:14:36 GMT  
		Size: 7.3 MB (7269170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a951be59abc423fe14ab9e8f769c4aab51ee15004ef9b7cccad5f65451fb56`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 91.7 KB (91736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e9ad64722f26f00125e9b549b06d40a727849d2f9550dc66a6533d89ebf8fa`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31cd3ee01e94bb58480e2a72b8f3677d9457fa9a26aa6f8b63431dbc313074e`  
		Last Modified: Thu, 04 Dec 2025 02:14:43 GMT  
		Size: 59.9 MB (59893205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0159762f19a8b9a93c9555ca6508e536ae2ffa5221f1f7fe2517b25edb26c7df`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b0105e4b3b66292b7fa5025b925cfea155b39007901429ba1dad2b3064ee51`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ab05258dcfbb29e603677ce44f578d475223727587324270624d8ea011d7ccda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20281852242edf20349d07841d8bc88fc25a406146000e725cf15a381d07094a`

```dockerfile
```

-	Layers:
	-	`sha256:e799d064fde967b53c6149a5df7009511ddce4ce4274868ee730661a6eeb37be`  
		Last Modified: Thu, 04 Dec 2025 06:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:0541f6653d52b64dd6cd2d3d726aee9bca91947de8a574f57303b4f1636a14f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126462847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209da4e636036ccbab56e97d822d0ab39a923aa5572a22674e75a74493b686c2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:17:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:17:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:17:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:17:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:17:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:17:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:17:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:17:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:17:29 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:09:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:09:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:09:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:09:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:09:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:09:21 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab67aee2b47b20a25046ed73de706bd5a80ad82192c27db420a65cfa5fb17cb`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 7.6 MB (7598018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860397c02592909361c994060954f1d684dc0366a2df922a3fe521f02a6b6b2`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ddf54b4c1a081004e3eb1cd154ca1c1cc7e169e416c1ebb9fb23b872919a4d`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 17.6 MB (17550083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645b95707890af1cad5443377a3d8bba32e3701d1f59ee629bd3a1598e45b63`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 21.5 MB (21454910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d968e842fbfa0f7d8d14048d776e945449a586f5772cf04dc12753e58629d9`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 10.2 MB (10188525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9482495d52b3d32ead0b4c76816259e750cf45944ac6a48937ed5de349bc73b`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862303f1e616b7c4e5debf343f489e54323b1d7e8d897d6bbcf9951c6fb125e7`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581b42590dfec33aa271798a0fdbb5fb080fa6137a58beb89183e43d609cc24`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef35268d1c5043e126a7b2b7cccba9910ba866f3721d67bc80d8768966a3202`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 6.6 MB (6570913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6110fc79c7e532c554cef8b106c77e384dffc4dbe8ff453044efb95611640865`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 88.1 KB (88108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eebdb0a3d24aad8069039ec36bba107f65570fd4460d47f5c5bc29bd7ab18c9`  
		Last Modified: Thu, 04 Dec 2025 02:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ff8b61a42ac17a9147133f9cfb9f005cc5a7597c4fbe27bd8305f307f0413a`  
		Last Modified: Thu, 04 Dec 2025 02:09:51 GMT  
		Size: 59.7 MB (59725679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5721cb1c43ef63e8c0bce0addcaa897e3b41d32fe7bf88c8020981f6cf24833f`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ef0da11c43d1593fd48c517bb7f91d37aba3bdf335ba6c03da014da92736e`  
		Last Modified: Thu, 04 Dec 2025 02:09:42 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5ac10dc71cf0cc09125a924469cb4aecc84840796fde5d9d0342a0baee3f5507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37587e9d82c759400bbe91d7affa6d8bed70364b85068a5dceef5c381a8f048a`

```dockerfile
```

-	Layers:
	-	`sha256:a20dd7c4bd39660f77009db4c78ecbaf59987f8c583b5a69d876f11f05d0da6e`  
		Last Modified: Thu, 04 Dec 2025 06:07:37 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:835173465724c55bedd93b72bdb6724104693472836d4354236bd9f87ccc6e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126316862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1db13432a7537ebc347611396429d42295ceb944903b73ab7ed6ca66a7d24ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:14:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:14:01 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf7527ac3d38e2b3f6d1176cd286fb31e55896c8724ba176b4d4958e4075db2`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 8.5 MB (8453465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4639c90abf56c9e413f2f2d2c096aefc19cf619ba9f5b28d891218b96ce733`  
		Last Modified: Thu, 04 Dec 2025 01:14:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc4c4bdc3b3639f19fd743ed949e35d8d7164a53fa32494422b203bbc675f5`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 17.3 MB (17334885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787c5406b3fa1fc1c5f4ee10e3f972d710de70beb323a67ceb5aa62273f8aa2`  
		Last Modified: Thu, 04 Dec 2025 01:14:22 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772518255e899b197408165167764a4d01d2b1098d6b40716fe91444be12a43c`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 9.9 MB (9938698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa62af1a24bf51d9a4d39915667786eb279e97dab96543236a409060be26a4`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a485df48fa9519df08360fc32bc48f54c3e8645b16565c58654267487f7bff`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e420e20b91d5cf88de9d2f64e34c09ebf8fa77ab2147c66fe59fbc546b08a64`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4ec7220c3f61f31eba0afab7f6e4defe2bc8ce778302f7ccbe98325fbc2`  
		Last Modified: Thu, 04 Dec 2025 02:12:44 GMT  
		Size: 7.2 MB (7211504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216239cfaa66c6158aaee65ef2d3ce737384d2ee872d2a74d4ae2f0178284e69`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 101.3 KB (101256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba097afc00e56a014d7ba0d623f39b67a2e68e4d622113752ce9e9e03e2308f9`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0c46a299f22b7f8f78c049709892e1660352aa8fe591e54e27030774b69e3d`  
		Last Modified: Thu, 04 Dec 2025 02:12:47 GMT  
		Size: 58.4 MB (58428644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c271f430dfb557ed996372a070b01fc71fd92aa464beb69530d45a33dd887b`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3583ad88ca4d8e567b11ce83128811bc0c359cfa889e192896e0942686282598`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1d3c36d88728fafa4708e5ffc1a34ae3be9c093b4668b882bd3f9b2808df9f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c9de27527effa797f1e73c2627b71d4d65243f3429a0fff7dd7a42d9601934`

```dockerfile
```

-	Layers:
	-	`sha256:467e80fb00d99af46899eed546c4f3c351297a1b14166825411e06dcbb6f39e2`  
		Last Modified: Thu, 04 Dec 2025 06:07:40 GMT  
		Size: 34.8 KB (34775 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:574a3f2f9fdbffa4c8e8f9741a8c04c6609d29b344338a46ec4d54f218e28e7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:56a7635e08b58bc1c764f0646e484b480a37c0c9209e42d7a1324d426d58d996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156929499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7044c07accbc2c2fec49490a3d5822690d721f4af5e2ab2dc96ca8ff23017d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:12:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:12:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:12:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:12:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:12:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:12:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:12:38 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:17 GMT
CMD []
# Thu, 04 Dec 2025 03:13:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 03:13:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 03:13:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 03:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 03:14:00 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 03:14:00 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 03:14:00 GMT
USER rootless
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9948ae9a3223520d912ab66de5d55ae24d29c808a510d02ab8cefd00f6af1`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 8.4 MB (8399334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b09731169ba7df8d96a4bb9a1a6ab3d4c1560d30cc4429e0e0180131ccaf7c9`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22939237c954384f47f26a89ee0dd27d44805625e73797e594c00dfe4f40b97a`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 18.8 MB (18763825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb36afae27f4bbcb70ff6c2154f9a0c7e0e5aeb479254c14e3d97743d63765d`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 22.9 MB (22905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf52db4eb6dc458063c42a6e1ccff1a420fc8ca9c6054305aa393dcb100491`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 10.8 MB (10784455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0739e6c04d86d46c4bbd27f2c6aeddd85de220909f633494d0d453f69475e1f`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33287860d4ed49c1e91d9f437b63622f4a717e826b7d3aa4d3cc847adfbd85fe`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8131e857b4a01669f532d44efd02dc2eced5ae48d3eeaee6272747a38064919`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ceb3774725100b39cc84625299eaf7a38cd9350fc52d2bb092d2261483b6b`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 6.9 MB (6932412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb61cbf781bf1ad1f584b29991a24c4ad159bb77066a66dfbc69d0530c956bd`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 92.4 KB (92445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f614095489d33530a88164a8c28f37b2d4905f0b80d0d6b55f20aaadfd70949`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebf1832bba38f06f167c58af841378ce16e956f5bbf93fac3890ad9c28c8cbf`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 64.4 MB (64391839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40879250d388c3438681a3fcb4c0dfd255a9608c7640fef9336b0e41182e1f96`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e36d8cddb77fc04b3f2ce2f905702ec5fa87992d2042e8c67f1270e0a00d47`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a640eb35a6502db5190bb0bb8deb619d9f050e7f3017b5819cd9f2f0730ace`  
		Last Modified: Thu, 04 Dec 2025 03:14:13 GMT  
		Size: 3.4 MB (3419922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c74d1c60153ac02bd4eff5325e6fa1887d79239e7ad25ebdc10daa3c737ebc3`  
		Last Modified: Thu, 04 Dec 2025 03:14:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a3f3709fe2bfb65daceaff5bc768a8c46c12b429dd51f6d836deb949f69ed2`  
		Last Modified: Thu, 04 Dec 2025 03:14:12 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea03eb9631ccce3547d2b98ccbae68940b4b27ee68a0023d8e85f3d03571811a`  
		Last Modified: Thu, 04 Dec 2025 03:14:14 GMT  
		Size: 17.4 MB (17370982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659d25d3e0c3b4f79f1ab84cd3383ac7c5ad40ad0d1257e746bf9a598056a773`  
		Last Modified: Thu, 04 Dec 2025 03:14:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3088595ddea0c377ad4a6d825a1e599bfc51c5179c762016f33e84f70f146281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a9ecfe6ee5edd280120c6ed90cc853e67a271da14fafa84d4a83ebd3a8847a`

```dockerfile
```

-	Layers:
	-	`sha256:c0e983a660428ca0287998fc28bc7373babd47a24229c324b828df8b14da19b3`  
		Last Modified: Thu, 04 Dec 2025 06:07:42 GMT  
		Size: 30.6 KB (30588 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6b25832ef4e2c960f75ab279a6595d37461cd3d5b27f92661b2b383e0ccd0dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147421264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a897cb5a9ae1c74a08c6011f4a8f635e8179c79bc7fc616545a1c57af41bb8a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:14:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:14:01 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:25 GMT
CMD []
# Thu, 04 Dec 2025 03:12:48 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 03:12:48 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 03:12:49 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 03:12:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 03:12:49 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 03:12:49 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 03:12:49 GMT
USER rootless
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf7527ac3d38e2b3f6d1176cd286fb31e55896c8724ba176b4d4958e4075db2`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 8.5 MB (8453465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4639c90abf56c9e413f2f2d2c096aefc19cf619ba9f5b28d891218b96ce733`  
		Last Modified: Thu, 04 Dec 2025 01:14:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc4c4bdc3b3639f19fd743ed949e35d8d7164a53fa32494422b203bbc675f5`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 17.3 MB (17334885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787c5406b3fa1fc1c5f4ee10e3f972d710de70beb323a67ceb5aa62273f8aa2`  
		Last Modified: Thu, 04 Dec 2025 01:14:22 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772518255e899b197408165167764a4d01d2b1098d6b40716fe91444be12a43c`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 9.9 MB (9938698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa62af1a24bf51d9a4d39915667786eb279e97dab96543236a409060be26a4`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a485df48fa9519df08360fc32bc48f54c3e8645b16565c58654267487f7bff`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e420e20b91d5cf88de9d2f64e34c09ebf8fa77ab2147c66fe59fbc546b08a64`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4ec7220c3f61f31eba0afab7f6e4defe2bc8ce778302f7ccbe98325fbc2`  
		Last Modified: Thu, 04 Dec 2025 02:12:44 GMT  
		Size: 7.2 MB (7211504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216239cfaa66c6158aaee65ef2d3ce737384d2ee872d2a74d4ae2f0178284e69`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 101.3 KB (101256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba097afc00e56a014d7ba0d623f39b67a2e68e4d622113752ce9e9e03e2308f9`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0c46a299f22b7f8f78c049709892e1660352aa8fe591e54e27030774b69e3d`  
		Last Modified: Thu, 04 Dec 2025 02:12:47 GMT  
		Size: 58.4 MB (58428644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c271f430dfb557ed996372a070b01fc71fd92aa464beb69530d45a33dd887b`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3583ad88ca4d8e567b11ce83128811bc0c359cfa889e192896e0942686282598`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d2bb7e9b7fe1cdb8d2b60423b41081687236d166de8ff04449219e1a8c151a`  
		Last Modified: Thu, 04 Dec 2025 03:13:10 GMT  
		Size: 3.4 MB (3394320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7b242fa22ee707972d86134a53d0a0f6a7d76efffa79ebfd4df747a3b7a5da`  
		Last Modified: Thu, 04 Dec 2025 03:13:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd4bac04225138ca50ef4363daee9293867ae4b0ce79f6b2dbad7b96a89d653`  
		Last Modified: Thu, 04 Dec 2025 03:13:10 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b4a984119cab953f09c8d619d346a43cbe48ff928ca031ad3d5908235b9412`  
		Last Modified: Thu, 04 Dec 2025 03:13:12 GMT  
		Size: 17.7 MB (17708737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db42e4847c0349ea6ed8a7f8941c38c153ae17691259ac6dbdb7c42b5027d309`  
		Last Modified: Thu, 04 Dec 2025 03:13:10 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2d4ae8ad4ca57769cf93f6dd3546eb767e4c9854641b08f4d8b9bd7c6e3bdd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97d97a6ee675067883e76b4653acfb23b19eeafd22f3ca54d975bfd1f94eec1`

```dockerfile
```

-	Layers:
	-	`sha256:953c88b79af11583ed0f510cfa7ce6fd408413d33ba382b397097f3992a54073`  
		Last Modified: Thu, 04 Dec 2025 06:07:54 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:67d857e9b0274e9c3bedbcba525dce2fa9133df508d67717e9e7e2950bec1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:d4dc0559c90e51495ababe507d0d4e412494de5b91e422af6c3cc68d924b6993
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308219283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74124bda75304cdae09598bcf1e2092ec876a2ff90459600c44773c77af4e38d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:32:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:33:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:33:11 GMT
ENV DOCKER_VERSION=29.1.2
# Tue, 09 Dec 2025 20:33:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Tue, 09 Dec 2025 20:33:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:33:21 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 09 Dec 2025 20:33:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 09 Dec 2025 20:33:22 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 09 Dec 2025 20:33:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:33:30 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Tue, 09 Dec 2025 20:33:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Tue, 09 Dec 2025 20:33:31 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Tue, 09 Dec 2025 20:33:37 GMT
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
	-	`sha256:a2fe319ee30340452819276b474d727c837b38b988cffead971ab498342327a0`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b497a39ebb57933272167001f136723338e9978c27a3ed3fc07cf559cfd3c6f6`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 350.8 KB (350799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba80a26db457c47c0c692c8edd53e3254f9208f569053d10b37fa20f3ee9f61`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc370eb16492f352f81a2fa60f8184a7e193436d6c1065bd341f1619fbe6f11a`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d799e6d8eae30a8d932238e5b2096f89536fbc820e6ebdceb023b76a49adc791`  
		Last Modified: Tue, 09 Dec 2025 20:42:56 GMT  
		Size: 19.4 MB (19412389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efba57425bf6d57f35db21a956148c7011ffe7bcc7c7f39cc164b5d64926733c`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1253688da912cc57db2a544ae99548889bdf183dd7c78430e465bd428049e1fe`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b592805a7d17afbafc77f7ff035bce675f05e30b44c04a43a3a4f7f58ea1a8`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8416f9beb18ad66ba7343e899211ea306550a6eb4222148da2703ca450658f72`  
		Last Modified: Tue, 09 Dec 2025 20:42:57 GMT  
		Size: 23.9 MB (23901643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051c1994c45a3c345cd3977217d9d617df96a809c20fa15edbb9f5f87b484c93`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a185b6b64f2626043248cb47685a0d9c80e8ba4e4bcafca01544e3321473ac2a`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d79da57493f446b6263f59eda6b9554b1b88318bb230873d2e371050f55d0dc`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361a34870d5fab376e491284c214f936b58ee5031797aee97d0411a7f6269c02`  
		Last Modified: Tue, 09 Dec 2025 20:42:55 GMT  
		Size: 11.4 MB (11422280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:895cf5abcd8b5c61241aba2dd46c1dfd3d0ae29324f35730e0c05a23d6bd0cb9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835132397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f5a3f08a73b3091edff5dba7b7b84491fdc8c6ea4263706f1af48bde068687`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:29:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:29:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:29:34 GMT
ENV DOCKER_VERSION=29.1.2
# Tue, 09 Dec 2025 20:29:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Tue, 09 Dec 2025 20:29:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:29:48 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 09 Dec 2025 20:29:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 09 Dec 2025 20:29:50 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 09 Dec 2025 20:30:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Tue, 09 Dec 2025 20:30:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Tue, 09 Dec 2025 20:30:09 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Tue, 09 Dec 2025 20:30:20 GMT
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
	-	`sha256:9dac22ca67391bc67ae059bdc6b4fe7cfa91d0dd9f198a7a4a48d1208814e923`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043349e15d735002fd555e4be32832770828589a651eae11f6cf3f2d02ad4b4e`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 488.7 KB (488734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0fb93b3fcc9496a612d74204ac287360ea57a3a26361271104c86be97334`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea35c40b9971e81debd25b3b9ba90709cdd71ad966066d98d4ef47f7ef1eaa74`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868c903082601f929e25172b2414f102a42725f192ad9fd0edda66b432253e2f`  
		Last Modified: Tue, 09 Dec 2025 20:37:36 GMT  
		Size: 19.4 MB (19412413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3cf58d9086ad644440d4cd0239041b6305aceaeee9f403302a36428940da55`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b32043b05c27d4f3be96d052d081c4c79b08a4d493ba5737e2814bf8698c0d9`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c50ed9458936b4b0976ddb6a0aa490c6a3a101279aa9cf908ea25110d348fd`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f549308f1773171323e5c688a1a6ffb5c50c95638f3ad4d039147527e46a3a8a`  
		Last Modified: Tue, 09 Dec 2025 20:37:36 GMT  
		Size: 23.9 MB (23912184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38406868117ff3519bb0788d7047ec66dfa6834a044d57d8182b6d146b3160e`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd122a724ea56e0e9207b97122512081dd96d6795b3e61063cef71d5a12e001`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530aa0c39c848502a74b0e0aeea5d02325c53752e036d70f6be87168e64e92ea`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7727d6e218b2e69fbc73769cf1761c3f84c1884e76186c74a315eaf7ac866ba`  
		Last Modified: Tue, 09 Dec 2025 20:37:35 GMT  
		Size: 11.4 MB (11427927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f1da8d96a13c6d2f5c2c77394c41baa60cba07f4323fb4c5a10c042d18dc0591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:895cf5abcd8b5c61241aba2dd46c1dfd3d0ae29324f35730e0c05a23d6bd0cb9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835132397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f5a3f08a73b3091edff5dba7b7b84491fdc8c6ea4263706f1af48bde068687`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:29:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:29:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:29:34 GMT
ENV DOCKER_VERSION=29.1.2
# Tue, 09 Dec 2025 20:29:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Tue, 09 Dec 2025 20:29:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:29:48 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 09 Dec 2025 20:29:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 09 Dec 2025 20:29:50 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 09 Dec 2025 20:30:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Tue, 09 Dec 2025 20:30:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Tue, 09 Dec 2025 20:30:09 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Tue, 09 Dec 2025 20:30:20 GMT
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
	-	`sha256:9dac22ca67391bc67ae059bdc6b4fe7cfa91d0dd9f198a7a4a48d1208814e923`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043349e15d735002fd555e4be32832770828589a651eae11f6cf3f2d02ad4b4e`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 488.7 KB (488734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0fb93b3fcc9496a612d74204ac287360ea57a3a26361271104c86be97334`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea35c40b9971e81debd25b3b9ba90709cdd71ad966066d98d4ef47f7ef1eaa74`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868c903082601f929e25172b2414f102a42725f192ad9fd0edda66b432253e2f`  
		Last Modified: Tue, 09 Dec 2025 20:37:36 GMT  
		Size: 19.4 MB (19412413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3cf58d9086ad644440d4cd0239041b6305aceaeee9f403302a36428940da55`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b32043b05c27d4f3be96d052d081c4c79b08a4d493ba5737e2814bf8698c0d9`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c50ed9458936b4b0976ddb6a0aa490c6a3a101279aa9cf908ea25110d348fd`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f549308f1773171323e5c688a1a6ffb5c50c95638f3ad4d039147527e46a3a8a`  
		Last Modified: Tue, 09 Dec 2025 20:37:36 GMT  
		Size: 23.9 MB (23912184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38406868117ff3519bb0788d7047ec66dfa6834a044d57d8182b6d146b3160e`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd122a724ea56e0e9207b97122512081dd96d6795b3e61063cef71d5a12e001`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530aa0c39c848502a74b0e0aeea5d02325c53752e036d70f6be87168e64e92ea`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7727d6e218b2e69fbc73769cf1761c3f84c1884e76186c74a315eaf7ac866ba`  
		Last Modified: Tue, 09 Dec 2025 20:37:35 GMT  
		Size: 11.4 MB (11427927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:55c65e84a8de249a5b8a74df2f4e07f150d558869a7fbef2e356c66caa4c4c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:d4dc0559c90e51495ababe507d0d4e412494de5b91e422af6c3cc68d924b6993
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308219283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74124bda75304cdae09598bcf1e2092ec876a2ff90459600c44773c77af4e38d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:32:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:33:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:33:11 GMT
ENV DOCKER_VERSION=29.1.2
# Tue, 09 Dec 2025 20:33:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Tue, 09 Dec 2025 20:33:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:33:21 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 09 Dec 2025 20:33:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 09 Dec 2025 20:33:22 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 09 Dec 2025 20:33:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:33:30 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Tue, 09 Dec 2025 20:33:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Tue, 09 Dec 2025 20:33:31 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Tue, 09 Dec 2025 20:33:37 GMT
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
	-	`sha256:a2fe319ee30340452819276b474d727c837b38b988cffead971ab498342327a0`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b497a39ebb57933272167001f136723338e9978c27a3ed3fc07cf559cfd3c6f6`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 350.8 KB (350799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba80a26db457c47c0c692c8edd53e3254f9208f569053d10b37fa20f3ee9f61`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc370eb16492f352f81a2fa60f8184a7e193436d6c1065bd341f1619fbe6f11a`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d799e6d8eae30a8d932238e5b2096f89536fbc820e6ebdceb023b76a49adc791`  
		Last Modified: Tue, 09 Dec 2025 20:42:56 GMT  
		Size: 19.4 MB (19412389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efba57425bf6d57f35db21a956148c7011ffe7bcc7c7f39cc164b5d64926733c`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1253688da912cc57db2a544ae99548889bdf183dd7c78430e465bd428049e1fe`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b592805a7d17afbafc77f7ff035bce675f05e30b44c04a43a3a4f7f58ea1a8`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8416f9beb18ad66ba7343e899211ea306550a6eb4222148da2703ca450658f72`  
		Last Modified: Tue, 09 Dec 2025 20:42:57 GMT  
		Size: 23.9 MB (23901643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051c1994c45a3c345cd3977217d9d617df96a809c20fa15edbb9f5f87b484c93`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a185b6b64f2626043248cb47685a0d9c80e8ba4e4bcafca01544e3321473ac2a`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d79da57493f446b6263f59eda6b9554b1b88318bb230873d2e371050f55d0dc`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361a34870d5fab376e491284c214f936b58ee5031797aee97d0411a7f6269c02`  
		Last Modified: Tue, 09 Dec 2025 20:42:55 GMT  
		Size: 11.4 MB (11422280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1`

```console
$ docker pull docker@sha256:40916fb078cdd27640d069bba401324a15a06d3ecbd8895048122c8d321f43f8
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
$ docker pull docker@sha256:967468c0be954e3a0d4bc31310e196a5a8d1adda607b0be11056d4d1badd6587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136137253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad869b62b5c060fe1594ae7fd17228cbc7468da180d9192bd8d59c1b17c896b3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:12:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:12:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:12:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:12:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:12:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:12:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:12:38 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:17 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9948ae9a3223520d912ab66de5d55ae24d29c808a510d02ab8cefd00f6af1`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 8.4 MB (8399334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b09731169ba7df8d96a4bb9a1a6ab3d4c1560d30cc4429e0e0180131ccaf7c9`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22939237c954384f47f26a89ee0dd27d44805625e73797e594c00dfe4f40b97a`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 18.8 MB (18763825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb36afae27f4bbcb70ff6c2154f9a0c7e0e5aeb479254c14e3d97743d63765d`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 22.9 MB (22905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf52db4eb6dc458063c42a6e1ccff1a420fc8ca9c6054305aa393dcb100491`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 10.8 MB (10784455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0739e6c04d86d46c4bbd27f2c6aeddd85de220909f633494d0d453f69475e1f`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33287860d4ed49c1e91d9f437b63622f4a717e826b7d3aa4d3cc847adfbd85fe`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8131e857b4a01669f532d44efd02dc2eced5ae48d3eeaee6272747a38064919`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ceb3774725100b39cc84625299eaf7a38cd9350fc52d2bb092d2261483b6b`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 6.9 MB (6932412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb61cbf781bf1ad1f584b29991a24c4ad159bb77066a66dfbc69d0530c956bd`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 92.4 KB (92445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f614095489d33530a88164a8c28f37b2d4905f0b80d0d6b55f20aaadfd70949`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebf1832bba38f06f167c58af841378ce16e956f5bbf93fac3890ad9c28c8cbf`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 64.4 MB (64391839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40879250d388c3438681a3fcb4c0dfd255a9608c7640fef9336b0e41182e1f96`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e36d8cddb77fc04b3f2ce2f905702ec5fa87992d2042e8c67f1270e0a00d47`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:f9bb7ce8788987c53f7376c978032c32bd32ceb0a11d3922bd1f30e83a330420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488001f5e00c1d96abaa4ef21598a7cb0c85dcdc849cc938a582649148cbfa1f`

```dockerfile
```

-	Layers:
	-	`sha256:f4371bf22d65b61f21247586c39a31945ff88f568ae5663039cabcbb9a800af7`  
		Last Modified: Thu, 04 Dec 2025 06:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:414cac80b8731cec0ba7269b2401349a90593d66af7a0861ec3c7d0198f4f25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128364231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab64be5a5da0cbe0bcc502e6958aa17939272152b190069d69458ac92d5ce4bd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:18:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:18:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:18:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:18:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:18:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:18:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:18:46 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:14:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:14:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:14:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:14:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:14:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:14:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:14:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:14:14 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af6abcf03c4d2a46ff1f3cf4e321bc7993d4d20b17f12f99d466b39b3555298`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 8.3 MB (8301067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb792a943c4d38855261216162c97e27587aa936e4de5451eeda4d170348a07`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309aa1d961beedab5a903eed7b199a7f3cf448a9ad0d235f989735bce0000963`  
		Last Modified: Thu, 04 Dec 2025 01:19:02 GMT  
		Size: 17.6 MB (17560675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136294917ec3532038026ad3f18199c6aff9e645109302b3c9fdc832bf5dd82`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 21.5 MB (21476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e0b74dd96a21e6b38324422ba118ccd940a01d181d09275193f948ebd543d2`  
		Last Modified: Thu, 04 Dec 2025 01:19:00 GMT  
		Size: 10.2 MB (10195783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48a193c8f7c9fb004babea7c82efc513b5196991d924daf956f6881012fec3`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86d05610e4cf2f79db6d09c9b4c2c8944991a0da701d442726824c5daf33ae`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ebf88cb27a0d9b7e72386749701cbb0df6c753c53caa647578e1151c9f6e0`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2889ceaea16d005f911037ba1943baa11fca8f5499572f26e08d1623571b0fca`  
		Last Modified: Thu, 04 Dec 2025 02:14:36 GMT  
		Size: 7.3 MB (7269170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a951be59abc423fe14ab9e8f769c4aab51ee15004ef9b7cccad5f65451fb56`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 91.7 KB (91736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e9ad64722f26f00125e9b549b06d40a727849d2f9550dc66a6533d89ebf8fa`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31cd3ee01e94bb58480e2a72b8f3677d9457fa9a26aa6f8b63431dbc313074e`  
		Last Modified: Thu, 04 Dec 2025 02:14:43 GMT  
		Size: 59.9 MB (59893205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0159762f19a8b9a93c9555ca6508e536ae2ffa5221f1f7fe2517b25edb26c7df`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b0105e4b3b66292b7fa5025b925cfea155b39007901429ba1dad2b3064ee51`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:ab05258dcfbb29e603677ce44f578d475223727587324270624d8ea011d7ccda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20281852242edf20349d07841d8bc88fc25a406146000e725cf15a381d07094a`

```dockerfile
```

-	Layers:
	-	`sha256:e799d064fde967b53c6149a5df7009511ddce4ce4274868ee730661a6eeb37be`  
		Last Modified: Thu, 04 Dec 2025 06:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:0541f6653d52b64dd6cd2d3d726aee9bca91947de8a574f57303b4f1636a14f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126462847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209da4e636036ccbab56e97d822d0ab39a923aa5572a22674e75a74493b686c2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:17:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:17:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:17:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:17:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:17:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:17:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:17:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:17:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:17:29 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:09:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:09:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:09:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:09:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:09:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:09:21 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab67aee2b47b20a25046ed73de706bd5a80ad82192c27db420a65cfa5fb17cb`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 7.6 MB (7598018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860397c02592909361c994060954f1d684dc0366a2df922a3fe521f02a6b6b2`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ddf54b4c1a081004e3eb1cd154ca1c1cc7e169e416c1ebb9fb23b872919a4d`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 17.6 MB (17550083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645b95707890af1cad5443377a3d8bba32e3701d1f59ee629bd3a1598e45b63`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 21.5 MB (21454910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d968e842fbfa0f7d8d14048d776e945449a586f5772cf04dc12753e58629d9`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 10.2 MB (10188525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9482495d52b3d32ead0b4c76816259e750cf45944ac6a48937ed5de349bc73b`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862303f1e616b7c4e5debf343f489e54323b1d7e8d897d6bbcf9951c6fb125e7`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581b42590dfec33aa271798a0fdbb5fb080fa6137a58beb89183e43d609cc24`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef35268d1c5043e126a7b2b7cccba9910ba866f3721d67bc80d8768966a3202`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 6.6 MB (6570913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6110fc79c7e532c554cef8b106c77e384dffc4dbe8ff453044efb95611640865`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 88.1 KB (88108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eebdb0a3d24aad8069039ec36bba107f65570fd4460d47f5c5bc29bd7ab18c9`  
		Last Modified: Thu, 04 Dec 2025 02:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ff8b61a42ac17a9147133f9cfb9f005cc5a7597c4fbe27bd8305f307f0413a`  
		Last Modified: Thu, 04 Dec 2025 02:09:51 GMT  
		Size: 59.7 MB (59725679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5721cb1c43ef63e8c0bce0addcaa897e3b41d32fe7bf88c8020981f6cf24833f`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ef0da11c43d1593fd48c517bb7f91d37aba3bdf335ba6c03da014da92736e`  
		Last Modified: Thu, 04 Dec 2025 02:09:42 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:5ac10dc71cf0cc09125a924469cb4aecc84840796fde5d9d0342a0baee3f5507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37587e9d82c759400bbe91d7affa6d8bed70364b85068a5dceef5c381a8f048a`

```dockerfile
```

-	Layers:
	-	`sha256:a20dd7c4bd39660f77009db4c78ecbaf59987f8c583b5a69d876f11f05d0da6e`  
		Last Modified: Thu, 04 Dec 2025 06:07:37 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:835173465724c55bedd93b72bdb6724104693472836d4354236bd9f87ccc6e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126316862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1db13432a7537ebc347611396429d42295ceb944903b73ab7ed6ca66a7d24ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:14:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:14:01 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf7527ac3d38e2b3f6d1176cd286fb31e55896c8724ba176b4d4958e4075db2`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 8.5 MB (8453465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4639c90abf56c9e413f2f2d2c096aefc19cf619ba9f5b28d891218b96ce733`  
		Last Modified: Thu, 04 Dec 2025 01:14:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc4c4bdc3b3639f19fd743ed949e35d8d7164a53fa32494422b203bbc675f5`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 17.3 MB (17334885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787c5406b3fa1fc1c5f4ee10e3f972d710de70beb323a67ceb5aa62273f8aa2`  
		Last Modified: Thu, 04 Dec 2025 01:14:22 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772518255e899b197408165167764a4d01d2b1098d6b40716fe91444be12a43c`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 9.9 MB (9938698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa62af1a24bf51d9a4d39915667786eb279e97dab96543236a409060be26a4`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a485df48fa9519df08360fc32bc48f54c3e8645b16565c58654267487f7bff`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e420e20b91d5cf88de9d2f64e34c09ebf8fa77ab2147c66fe59fbc546b08a64`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4ec7220c3f61f31eba0afab7f6e4defe2bc8ce778302f7ccbe98325fbc2`  
		Last Modified: Thu, 04 Dec 2025 02:12:44 GMT  
		Size: 7.2 MB (7211504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216239cfaa66c6158aaee65ef2d3ce737384d2ee872d2a74d4ae2f0178284e69`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 101.3 KB (101256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba097afc00e56a014d7ba0d623f39b67a2e68e4d622113752ce9e9e03e2308f9`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0c46a299f22b7f8f78c049709892e1660352aa8fe591e54e27030774b69e3d`  
		Last Modified: Thu, 04 Dec 2025 02:12:47 GMT  
		Size: 58.4 MB (58428644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c271f430dfb557ed996372a070b01fc71fd92aa464beb69530d45a33dd887b`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3583ad88ca4d8e567b11ce83128811bc0c359cfa889e192896e0942686282598`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1` - unknown; unknown

```console
$ docker pull docker@sha256:1d3c36d88728fafa4708e5ffc1a34ae3be9c093b4668b882bd3f9b2808df9f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c9de27527effa797f1e73c2627b71d4d65243f3429a0fff7dd7a42d9601934`

```dockerfile
```

-	Layers:
	-	`sha256:467e80fb00d99af46899eed546c4f3c351297a1b14166825411e06dcbb6f39e2`  
		Last Modified: Thu, 04 Dec 2025 06:07:40 GMT  
		Size: 34.8 KB (34775 bytes)  
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
$ docker pull docker@sha256:40916fb078cdd27640d069bba401324a15a06d3ecbd8895048122c8d321f43f8
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
$ docker pull docker@sha256:967468c0be954e3a0d4bc31310e196a5a8d1adda607b0be11056d4d1badd6587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136137253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad869b62b5c060fe1594ae7fd17228cbc7468da180d9192bd8d59c1b17c896b3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:12:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:12:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:12:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:12:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:12:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:12:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:12:38 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:17 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9948ae9a3223520d912ab66de5d55ae24d29c808a510d02ab8cefd00f6af1`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 8.4 MB (8399334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b09731169ba7df8d96a4bb9a1a6ab3d4c1560d30cc4429e0e0180131ccaf7c9`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22939237c954384f47f26a89ee0dd27d44805625e73797e594c00dfe4f40b97a`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 18.8 MB (18763825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb36afae27f4bbcb70ff6c2154f9a0c7e0e5aeb479254c14e3d97743d63765d`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 22.9 MB (22905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf52db4eb6dc458063c42a6e1ccff1a420fc8ca9c6054305aa393dcb100491`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 10.8 MB (10784455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0739e6c04d86d46c4bbd27f2c6aeddd85de220909f633494d0d453f69475e1f`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33287860d4ed49c1e91d9f437b63622f4a717e826b7d3aa4d3cc847adfbd85fe`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8131e857b4a01669f532d44efd02dc2eced5ae48d3eeaee6272747a38064919`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ceb3774725100b39cc84625299eaf7a38cd9350fc52d2bb092d2261483b6b`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 6.9 MB (6932412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb61cbf781bf1ad1f584b29991a24c4ad159bb77066a66dfbc69d0530c956bd`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 92.4 KB (92445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f614095489d33530a88164a8c28f37b2d4905f0b80d0d6b55f20aaadfd70949`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebf1832bba38f06f167c58af841378ce16e956f5bbf93fac3890ad9c28c8cbf`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 64.4 MB (64391839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40879250d388c3438681a3fcb4c0dfd255a9608c7640fef9336b0e41182e1f96`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e36d8cddb77fc04b3f2ce2f905702ec5fa87992d2042e8c67f1270e0a00d47`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f9bb7ce8788987c53f7376c978032c32bd32ceb0a11d3922bd1f30e83a330420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488001f5e00c1d96abaa4ef21598a7cb0c85dcdc849cc938a582649148cbfa1f`

```dockerfile
```

-	Layers:
	-	`sha256:f4371bf22d65b61f21247586c39a31945ff88f568ae5663039cabcbb9a800af7`  
		Last Modified: Thu, 04 Dec 2025 06:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:414cac80b8731cec0ba7269b2401349a90593d66af7a0861ec3c7d0198f4f25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128364231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab64be5a5da0cbe0bcc502e6958aa17939272152b190069d69458ac92d5ce4bd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:18:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:18:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:18:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:18:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:18:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:18:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:18:46 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:14:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:14:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:14:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:14:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:14:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:14:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:14:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:14:14 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af6abcf03c4d2a46ff1f3cf4e321bc7993d4d20b17f12f99d466b39b3555298`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 8.3 MB (8301067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb792a943c4d38855261216162c97e27587aa936e4de5451eeda4d170348a07`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309aa1d961beedab5a903eed7b199a7f3cf448a9ad0d235f989735bce0000963`  
		Last Modified: Thu, 04 Dec 2025 01:19:02 GMT  
		Size: 17.6 MB (17560675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136294917ec3532038026ad3f18199c6aff9e645109302b3c9fdc832bf5dd82`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 21.5 MB (21476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e0b74dd96a21e6b38324422ba118ccd940a01d181d09275193f948ebd543d2`  
		Last Modified: Thu, 04 Dec 2025 01:19:00 GMT  
		Size: 10.2 MB (10195783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48a193c8f7c9fb004babea7c82efc513b5196991d924daf956f6881012fec3`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86d05610e4cf2f79db6d09c9b4c2c8944991a0da701d442726824c5daf33ae`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ebf88cb27a0d9b7e72386749701cbb0df6c753c53caa647578e1151c9f6e0`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2889ceaea16d005f911037ba1943baa11fca8f5499572f26e08d1623571b0fca`  
		Last Modified: Thu, 04 Dec 2025 02:14:36 GMT  
		Size: 7.3 MB (7269170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a951be59abc423fe14ab9e8f769c4aab51ee15004ef9b7cccad5f65451fb56`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 91.7 KB (91736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e9ad64722f26f00125e9b549b06d40a727849d2f9550dc66a6533d89ebf8fa`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31cd3ee01e94bb58480e2a72b8f3677d9457fa9a26aa6f8b63431dbc313074e`  
		Last Modified: Thu, 04 Dec 2025 02:14:43 GMT  
		Size: 59.9 MB (59893205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0159762f19a8b9a93c9555ca6508e536ae2ffa5221f1f7fe2517b25edb26c7df`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b0105e4b3b66292b7fa5025b925cfea155b39007901429ba1dad2b3064ee51`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ab05258dcfbb29e603677ce44f578d475223727587324270624d8ea011d7ccda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20281852242edf20349d07841d8bc88fc25a406146000e725cf15a381d07094a`

```dockerfile
```

-	Layers:
	-	`sha256:e799d064fde967b53c6149a5df7009511ddce4ce4274868ee730661a6eeb37be`  
		Last Modified: Thu, 04 Dec 2025 06:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:0541f6653d52b64dd6cd2d3d726aee9bca91947de8a574f57303b4f1636a14f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126462847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209da4e636036ccbab56e97d822d0ab39a923aa5572a22674e75a74493b686c2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:17:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:17:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:17:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:17:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:17:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:17:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:17:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:17:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:17:29 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:09:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:09:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:09:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:09:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:09:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:09:21 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab67aee2b47b20a25046ed73de706bd5a80ad82192c27db420a65cfa5fb17cb`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 7.6 MB (7598018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860397c02592909361c994060954f1d684dc0366a2df922a3fe521f02a6b6b2`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ddf54b4c1a081004e3eb1cd154ca1c1cc7e169e416c1ebb9fb23b872919a4d`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 17.6 MB (17550083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645b95707890af1cad5443377a3d8bba32e3701d1f59ee629bd3a1598e45b63`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 21.5 MB (21454910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d968e842fbfa0f7d8d14048d776e945449a586f5772cf04dc12753e58629d9`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 10.2 MB (10188525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9482495d52b3d32ead0b4c76816259e750cf45944ac6a48937ed5de349bc73b`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862303f1e616b7c4e5debf343f489e54323b1d7e8d897d6bbcf9951c6fb125e7`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581b42590dfec33aa271798a0fdbb5fb080fa6137a58beb89183e43d609cc24`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef35268d1c5043e126a7b2b7cccba9910ba866f3721d67bc80d8768966a3202`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 6.6 MB (6570913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6110fc79c7e532c554cef8b106c77e384dffc4dbe8ff453044efb95611640865`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 88.1 KB (88108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eebdb0a3d24aad8069039ec36bba107f65570fd4460d47f5c5bc29bd7ab18c9`  
		Last Modified: Thu, 04 Dec 2025 02:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ff8b61a42ac17a9147133f9cfb9f005cc5a7597c4fbe27bd8305f307f0413a`  
		Last Modified: Thu, 04 Dec 2025 02:09:51 GMT  
		Size: 59.7 MB (59725679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5721cb1c43ef63e8c0bce0addcaa897e3b41d32fe7bf88c8020981f6cf24833f`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ef0da11c43d1593fd48c517bb7f91d37aba3bdf335ba6c03da014da92736e`  
		Last Modified: Thu, 04 Dec 2025 02:09:42 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5ac10dc71cf0cc09125a924469cb4aecc84840796fde5d9d0342a0baee3f5507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37587e9d82c759400bbe91d7affa6d8bed70364b85068a5dceef5c381a8f048a`

```dockerfile
```

-	Layers:
	-	`sha256:a20dd7c4bd39660f77009db4c78ecbaf59987f8c583b5a69d876f11f05d0da6e`  
		Last Modified: Thu, 04 Dec 2025 06:07:37 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:835173465724c55bedd93b72bdb6724104693472836d4354236bd9f87ccc6e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126316862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1db13432a7537ebc347611396429d42295ceb944903b73ab7ed6ca66a7d24ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:14:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:14:01 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf7527ac3d38e2b3f6d1176cd286fb31e55896c8724ba176b4d4958e4075db2`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 8.5 MB (8453465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4639c90abf56c9e413f2f2d2c096aefc19cf619ba9f5b28d891218b96ce733`  
		Last Modified: Thu, 04 Dec 2025 01:14:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc4c4bdc3b3639f19fd743ed949e35d8d7164a53fa32494422b203bbc675f5`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 17.3 MB (17334885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787c5406b3fa1fc1c5f4ee10e3f972d710de70beb323a67ceb5aa62273f8aa2`  
		Last Modified: Thu, 04 Dec 2025 01:14:22 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772518255e899b197408165167764a4d01d2b1098d6b40716fe91444be12a43c`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 9.9 MB (9938698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa62af1a24bf51d9a4d39915667786eb279e97dab96543236a409060be26a4`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a485df48fa9519df08360fc32bc48f54c3e8645b16565c58654267487f7bff`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e420e20b91d5cf88de9d2f64e34c09ebf8fa77ab2147c66fe59fbc546b08a64`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4ec7220c3f61f31eba0afab7f6e4defe2bc8ce778302f7ccbe98325fbc2`  
		Last Modified: Thu, 04 Dec 2025 02:12:44 GMT  
		Size: 7.2 MB (7211504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216239cfaa66c6158aaee65ef2d3ce737384d2ee872d2a74d4ae2f0178284e69`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 101.3 KB (101256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba097afc00e56a014d7ba0d623f39b67a2e68e4d622113752ce9e9e03e2308f9`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0c46a299f22b7f8f78c049709892e1660352aa8fe591e54e27030774b69e3d`  
		Last Modified: Thu, 04 Dec 2025 02:12:47 GMT  
		Size: 58.4 MB (58428644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c271f430dfb557ed996372a070b01fc71fd92aa464beb69530d45a33dd887b`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3583ad88ca4d8e567b11ce83128811bc0c359cfa889e192896e0942686282598`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1d3c36d88728fafa4708e5ffc1a34ae3be9c093b4668b882bd3f9b2808df9f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c9de27527effa797f1e73c2627b71d4d65243f3429a0fff7dd7a42d9601934`

```dockerfile
```

-	Layers:
	-	`sha256:467e80fb00d99af46899eed546c4f3c351297a1b14166825411e06dcbb6f39e2`  
		Last Modified: Thu, 04 Dec 2025 06:07:40 GMT  
		Size: 34.8 KB (34775 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1-dind-rootless`

```console
$ docker pull docker@sha256:574a3f2f9fdbffa4c8e8f9741a8c04c6609d29b344338a46ec4d54f218e28e7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:56a7635e08b58bc1c764f0646e484b480a37c0c9209e42d7a1324d426d58d996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156929499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7044c07accbc2c2fec49490a3d5822690d721f4af5e2ab2dc96ca8ff23017d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:12:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:12:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:12:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:12:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:12:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:12:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:12:38 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:17 GMT
CMD []
# Thu, 04 Dec 2025 03:13:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 03:13:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 03:13:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 03:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 03:14:00 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 03:14:00 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 03:14:00 GMT
USER rootless
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9948ae9a3223520d912ab66de5d55ae24d29c808a510d02ab8cefd00f6af1`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 8.4 MB (8399334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b09731169ba7df8d96a4bb9a1a6ab3d4c1560d30cc4429e0e0180131ccaf7c9`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22939237c954384f47f26a89ee0dd27d44805625e73797e594c00dfe4f40b97a`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 18.8 MB (18763825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb36afae27f4bbcb70ff6c2154f9a0c7e0e5aeb479254c14e3d97743d63765d`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 22.9 MB (22905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf52db4eb6dc458063c42a6e1ccff1a420fc8ca9c6054305aa393dcb100491`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 10.8 MB (10784455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0739e6c04d86d46c4bbd27f2c6aeddd85de220909f633494d0d453f69475e1f`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33287860d4ed49c1e91d9f437b63622f4a717e826b7d3aa4d3cc847adfbd85fe`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8131e857b4a01669f532d44efd02dc2eced5ae48d3eeaee6272747a38064919`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ceb3774725100b39cc84625299eaf7a38cd9350fc52d2bb092d2261483b6b`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 6.9 MB (6932412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb61cbf781bf1ad1f584b29991a24c4ad159bb77066a66dfbc69d0530c956bd`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 92.4 KB (92445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f614095489d33530a88164a8c28f37b2d4905f0b80d0d6b55f20aaadfd70949`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebf1832bba38f06f167c58af841378ce16e956f5bbf93fac3890ad9c28c8cbf`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 64.4 MB (64391839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40879250d388c3438681a3fcb4c0dfd255a9608c7640fef9336b0e41182e1f96`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e36d8cddb77fc04b3f2ce2f905702ec5fa87992d2042e8c67f1270e0a00d47`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a640eb35a6502db5190bb0bb8deb619d9f050e7f3017b5819cd9f2f0730ace`  
		Last Modified: Thu, 04 Dec 2025 03:14:13 GMT  
		Size: 3.4 MB (3419922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c74d1c60153ac02bd4eff5325e6fa1887d79239e7ad25ebdc10daa3c737ebc3`  
		Last Modified: Thu, 04 Dec 2025 03:14:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a3f3709fe2bfb65daceaff5bc768a8c46c12b429dd51f6d836deb949f69ed2`  
		Last Modified: Thu, 04 Dec 2025 03:14:12 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea03eb9631ccce3547d2b98ccbae68940b4b27ee68a0023d8e85f3d03571811a`  
		Last Modified: Thu, 04 Dec 2025 03:14:14 GMT  
		Size: 17.4 MB (17370982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659d25d3e0c3b4f79f1ab84cd3383ac7c5ad40ad0d1257e746bf9a598056a773`  
		Last Modified: Thu, 04 Dec 2025 03:14:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3088595ddea0c377ad4a6d825a1e599bfc51c5179c762016f33e84f70f146281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a9ecfe6ee5edd280120c6ed90cc853e67a271da14fafa84d4a83ebd3a8847a`

```dockerfile
```

-	Layers:
	-	`sha256:c0e983a660428ca0287998fc28bc7373babd47a24229c324b828df8b14da19b3`  
		Last Modified: Thu, 04 Dec 2025 06:07:42 GMT  
		Size: 30.6 KB (30588 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6b25832ef4e2c960f75ab279a6595d37461cd3d5b27f92661b2b383e0ccd0dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147421264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a897cb5a9ae1c74a08c6011f4a8f635e8179c79bc7fc616545a1c57af41bb8a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:14:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:14:01 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:25 GMT
CMD []
# Thu, 04 Dec 2025 03:12:48 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 03:12:48 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 03:12:49 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 03:12:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 03:12:49 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 03:12:49 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 03:12:49 GMT
USER rootless
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf7527ac3d38e2b3f6d1176cd286fb31e55896c8724ba176b4d4958e4075db2`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 8.5 MB (8453465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4639c90abf56c9e413f2f2d2c096aefc19cf619ba9f5b28d891218b96ce733`  
		Last Modified: Thu, 04 Dec 2025 01:14:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc4c4bdc3b3639f19fd743ed949e35d8d7164a53fa32494422b203bbc675f5`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 17.3 MB (17334885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787c5406b3fa1fc1c5f4ee10e3f972d710de70beb323a67ceb5aa62273f8aa2`  
		Last Modified: Thu, 04 Dec 2025 01:14:22 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772518255e899b197408165167764a4d01d2b1098d6b40716fe91444be12a43c`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 9.9 MB (9938698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa62af1a24bf51d9a4d39915667786eb279e97dab96543236a409060be26a4`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a485df48fa9519df08360fc32bc48f54c3e8645b16565c58654267487f7bff`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e420e20b91d5cf88de9d2f64e34c09ebf8fa77ab2147c66fe59fbc546b08a64`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4ec7220c3f61f31eba0afab7f6e4defe2bc8ce778302f7ccbe98325fbc2`  
		Last Modified: Thu, 04 Dec 2025 02:12:44 GMT  
		Size: 7.2 MB (7211504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216239cfaa66c6158aaee65ef2d3ce737384d2ee872d2a74d4ae2f0178284e69`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 101.3 KB (101256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba097afc00e56a014d7ba0d623f39b67a2e68e4d622113752ce9e9e03e2308f9`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0c46a299f22b7f8f78c049709892e1660352aa8fe591e54e27030774b69e3d`  
		Last Modified: Thu, 04 Dec 2025 02:12:47 GMT  
		Size: 58.4 MB (58428644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c271f430dfb557ed996372a070b01fc71fd92aa464beb69530d45a33dd887b`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3583ad88ca4d8e567b11ce83128811bc0c359cfa889e192896e0942686282598`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d2bb7e9b7fe1cdb8d2b60423b41081687236d166de8ff04449219e1a8c151a`  
		Last Modified: Thu, 04 Dec 2025 03:13:10 GMT  
		Size: 3.4 MB (3394320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7b242fa22ee707972d86134a53d0a0f6a7d76efffa79ebfd4df747a3b7a5da`  
		Last Modified: Thu, 04 Dec 2025 03:13:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd4bac04225138ca50ef4363daee9293867ae4b0ce79f6b2dbad7b96a89d653`  
		Last Modified: Thu, 04 Dec 2025 03:13:10 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b4a984119cab953f09c8d619d346a43cbe48ff928ca031ad3d5908235b9412`  
		Last Modified: Thu, 04 Dec 2025 03:13:12 GMT  
		Size: 17.7 MB (17708737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db42e4847c0349ea6ed8a7f8941c38c153ae17691259ac6dbdb7c42b5027d309`  
		Last Modified: Thu, 04 Dec 2025 03:13:10 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2d4ae8ad4ca57769cf93f6dd3546eb767e4c9854641b08f4d8b9bd7c6e3bdd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97d97a6ee675067883e76b4653acfb23b19eeafd22f3ca54d975bfd1f94eec1`

```dockerfile
```

-	Layers:
	-	`sha256:953c88b79af11583ed0f510cfa7ce6fd408413d33ba382b397097f3992a54073`  
		Last Modified: Thu, 04 Dec 2025 06:07:54 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.1-windowsservercore`

```console
$ docker pull docker@sha256:67d857e9b0274e9c3bedbcba525dce2fa9133df508d67717e9e7e2950bec1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `docker:29.1-windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:d4dc0559c90e51495ababe507d0d4e412494de5b91e422af6c3cc68d924b6993
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308219283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74124bda75304cdae09598bcf1e2092ec876a2ff90459600c44773c77af4e38d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:32:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:33:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:33:11 GMT
ENV DOCKER_VERSION=29.1.2
# Tue, 09 Dec 2025 20:33:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Tue, 09 Dec 2025 20:33:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:33:21 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 09 Dec 2025 20:33:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 09 Dec 2025 20:33:22 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 09 Dec 2025 20:33:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:33:30 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Tue, 09 Dec 2025 20:33:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Tue, 09 Dec 2025 20:33:31 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Tue, 09 Dec 2025 20:33:37 GMT
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
	-	`sha256:a2fe319ee30340452819276b474d727c837b38b988cffead971ab498342327a0`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b497a39ebb57933272167001f136723338e9978c27a3ed3fc07cf559cfd3c6f6`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 350.8 KB (350799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba80a26db457c47c0c692c8edd53e3254f9208f569053d10b37fa20f3ee9f61`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc370eb16492f352f81a2fa60f8184a7e193436d6c1065bd341f1619fbe6f11a`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d799e6d8eae30a8d932238e5b2096f89536fbc820e6ebdceb023b76a49adc791`  
		Last Modified: Tue, 09 Dec 2025 20:42:56 GMT  
		Size: 19.4 MB (19412389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efba57425bf6d57f35db21a956148c7011ffe7bcc7c7f39cc164b5d64926733c`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1253688da912cc57db2a544ae99548889bdf183dd7c78430e465bd428049e1fe`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b592805a7d17afbafc77f7ff035bce675f05e30b44c04a43a3a4f7f58ea1a8`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8416f9beb18ad66ba7343e899211ea306550a6eb4222148da2703ca450658f72`  
		Last Modified: Tue, 09 Dec 2025 20:42:57 GMT  
		Size: 23.9 MB (23901643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051c1994c45a3c345cd3977217d9d617df96a809c20fa15edbb9f5f87b484c93`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a185b6b64f2626043248cb47685a0d9c80e8ba4e4bcafca01544e3321473ac2a`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d79da57493f446b6263f59eda6b9554b1b88318bb230873d2e371050f55d0dc`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361a34870d5fab376e491284c214f936b58ee5031797aee97d0411a7f6269c02`  
		Last Modified: Tue, 09 Dec 2025 20:42:55 GMT  
		Size: 11.4 MB (11422280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.1-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:895cf5abcd8b5c61241aba2dd46c1dfd3d0ae29324f35730e0c05a23d6bd0cb9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835132397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f5a3f08a73b3091edff5dba7b7b84491fdc8c6ea4263706f1af48bde068687`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:29:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:29:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:29:34 GMT
ENV DOCKER_VERSION=29.1.2
# Tue, 09 Dec 2025 20:29:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Tue, 09 Dec 2025 20:29:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:29:48 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 09 Dec 2025 20:29:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 09 Dec 2025 20:29:50 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 09 Dec 2025 20:30:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Tue, 09 Dec 2025 20:30:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Tue, 09 Dec 2025 20:30:09 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Tue, 09 Dec 2025 20:30:20 GMT
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
	-	`sha256:9dac22ca67391bc67ae059bdc6b4fe7cfa91d0dd9f198a7a4a48d1208814e923`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043349e15d735002fd555e4be32832770828589a651eae11f6cf3f2d02ad4b4e`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 488.7 KB (488734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0fb93b3fcc9496a612d74204ac287360ea57a3a26361271104c86be97334`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea35c40b9971e81debd25b3b9ba90709cdd71ad966066d98d4ef47f7ef1eaa74`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868c903082601f929e25172b2414f102a42725f192ad9fd0edda66b432253e2f`  
		Last Modified: Tue, 09 Dec 2025 20:37:36 GMT  
		Size: 19.4 MB (19412413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3cf58d9086ad644440d4cd0239041b6305aceaeee9f403302a36428940da55`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b32043b05c27d4f3be96d052d081c4c79b08a4d493ba5737e2814bf8698c0d9`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c50ed9458936b4b0976ddb6a0aa490c6a3a101279aa9cf908ea25110d348fd`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f549308f1773171323e5c688a1a6ffb5c50c95638f3ad4d039147527e46a3a8a`  
		Last Modified: Tue, 09 Dec 2025 20:37:36 GMT  
		Size: 23.9 MB (23912184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38406868117ff3519bb0788d7047ec66dfa6834a044d57d8182b6d146b3160e`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd122a724ea56e0e9207b97122512081dd96d6795b3e61063cef71d5a12e001`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530aa0c39c848502a74b0e0aeea5d02325c53752e036d70f6be87168e64e92ea`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7727d6e218b2e69fbc73769cf1761c3f84c1884e76186c74a315eaf7ac866ba`  
		Last Modified: Tue, 09 Dec 2025 20:37:35 GMT  
		Size: 11.4 MB (11427927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f1da8d96a13c6d2f5c2c77394c41baa60cba07f4323fb4c5a10c042d18dc0591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `docker:29.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:895cf5abcd8b5c61241aba2dd46c1dfd3d0ae29324f35730e0c05a23d6bd0cb9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835132397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f5a3f08a73b3091edff5dba7b7b84491fdc8c6ea4263706f1af48bde068687`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:29:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:29:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:29:34 GMT
ENV DOCKER_VERSION=29.1.2
# Tue, 09 Dec 2025 20:29:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Tue, 09 Dec 2025 20:29:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:29:48 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 09 Dec 2025 20:29:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 09 Dec 2025 20:29:50 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 09 Dec 2025 20:30:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Tue, 09 Dec 2025 20:30:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Tue, 09 Dec 2025 20:30:09 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Tue, 09 Dec 2025 20:30:20 GMT
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
	-	`sha256:9dac22ca67391bc67ae059bdc6b4fe7cfa91d0dd9f198a7a4a48d1208814e923`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043349e15d735002fd555e4be32832770828589a651eae11f6cf3f2d02ad4b4e`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 488.7 KB (488734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0fb93b3fcc9496a612d74204ac287360ea57a3a26361271104c86be97334`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea35c40b9971e81debd25b3b9ba90709cdd71ad966066d98d4ef47f7ef1eaa74`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868c903082601f929e25172b2414f102a42725f192ad9fd0edda66b432253e2f`  
		Last Modified: Tue, 09 Dec 2025 20:37:36 GMT  
		Size: 19.4 MB (19412413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3cf58d9086ad644440d4cd0239041b6305aceaeee9f403302a36428940da55`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b32043b05c27d4f3be96d052d081c4c79b08a4d493ba5737e2814bf8698c0d9`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c50ed9458936b4b0976ddb6a0aa490c6a3a101279aa9cf908ea25110d348fd`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f549308f1773171323e5c688a1a6ffb5c50c95638f3ad4d039147527e46a3a8a`  
		Last Modified: Tue, 09 Dec 2025 20:37:36 GMT  
		Size: 23.9 MB (23912184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38406868117ff3519bb0788d7047ec66dfa6834a044d57d8182b6d146b3160e`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd122a724ea56e0e9207b97122512081dd96d6795b3e61063cef71d5a12e001`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530aa0c39c848502a74b0e0aeea5d02325c53752e036d70f6be87168e64e92ea`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7727d6e218b2e69fbc73769cf1761c3f84c1884e76186c74a315eaf7ac866ba`  
		Last Modified: Tue, 09 Dec 2025 20:37:35 GMT  
		Size: 11.4 MB (11427927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:55c65e84a8de249a5b8a74df2f4e07f150d558869a7fbef2e356c66caa4c4c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `docker:29.1-windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:d4dc0559c90e51495ababe507d0d4e412494de5b91e422af6c3cc68d924b6993
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308219283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74124bda75304cdae09598bcf1e2092ec876a2ff90459600c44773c77af4e38d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:32:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:33:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:33:11 GMT
ENV DOCKER_VERSION=29.1.2
# Tue, 09 Dec 2025 20:33:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Tue, 09 Dec 2025 20:33:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:33:21 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 09 Dec 2025 20:33:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 09 Dec 2025 20:33:22 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 09 Dec 2025 20:33:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:33:30 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Tue, 09 Dec 2025 20:33:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Tue, 09 Dec 2025 20:33:31 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Tue, 09 Dec 2025 20:33:37 GMT
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
	-	`sha256:a2fe319ee30340452819276b474d727c837b38b988cffead971ab498342327a0`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b497a39ebb57933272167001f136723338e9978c27a3ed3fc07cf559cfd3c6f6`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 350.8 KB (350799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba80a26db457c47c0c692c8edd53e3254f9208f569053d10b37fa20f3ee9f61`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc370eb16492f352f81a2fa60f8184a7e193436d6c1065bd341f1619fbe6f11a`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d799e6d8eae30a8d932238e5b2096f89536fbc820e6ebdceb023b76a49adc791`  
		Last Modified: Tue, 09 Dec 2025 20:42:56 GMT  
		Size: 19.4 MB (19412389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efba57425bf6d57f35db21a956148c7011ffe7bcc7c7f39cc164b5d64926733c`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1253688da912cc57db2a544ae99548889bdf183dd7c78430e465bd428049e1fe`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b592805a7d17afbafc77f7ff035bce675f05e30b44c04a43a3a4f7f58ea1a8`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8416f9beb18ad66ba7343e899211ea306550a6eb4222148da2703ca450658f72`  
		Last Modified: Tue, 09 Dec 2025 20:42:57 GMT  
		Size: 23.9 MB (23901643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051c1994c45a3c345cd3977217d9d617df96a809c20fa15edbb9f5f87b484c93`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a185b6b64f2626043248cb47685a0d9c80e8ba4e4bcafca01544e3321473ac2a`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d79da57493f446b6263f59eda6b9554b1b88318bb230873d2e371050f55d0dc`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361a34870d5fab376e491284c214f936b58ee5031797aee97d0411a7f6269c02`  
		Last Modified: Tue, 09 Dec 2025 20:42:55 GMT  
		Size: 11.4 MB (11422280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.1.3`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.1.3-alpine3.23`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

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
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.1.3-dind-alpine3.23`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.1.3-dind-rootless`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.1.3-windowsservercore`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.1.3-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `docker:29.1.3-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

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
$ docker pull docker@sha256:40916fb078cdd27640d069bba401324a15a06d3ecbd8895048122c8d321f43f8
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
$ docker pull docker@sha256:967468c0be954e3a0d4bc31310e196a5a8d1adda607b0be11056d4d1badd6587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136137253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad869b62b5c060fe1594ae7fd17228cbc7468da180d9192bd8d59c1b17c896b3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:12:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:12:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:12:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:12:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:12:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:12:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:12:38 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:17 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9948ae9a3223520d912ab66de5d55ae24d29c808a510d02ab8cefd00f6af1`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 8.4 MB (8399334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b09731169ba7df8d96a4bb9a1a6ab3d4c1560d30cc4429e0e0180131ccaf7c9`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22939237c954384f47f26a89ee0dd27d44805625e73797e594c00dfe4f40b97a`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 18.8 MB (18763825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb36afae27f4bbcb70ff6c2154f9a0c7e0e5aeb479254c14e3d97743d63765d`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 22.9 MB (22905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf52db4eb6dc458063c42a6e1ccff1a420fc8ca9c6054305aa393dcb100491`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 10.8 MB (10784455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0739e6c04d86d46c4bbd27f2c6aeddd85de220909f633494d0d453f69475e1f`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33287860d4ed49c1e91d9f437b63622f4a717e826b7d3aa4d3cc847adfbd85fe`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8131e857b4a01669f532d44efd02dc2eced5ae48d3eeaee6272747a38064919`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ceb3774725100b39cc84625299eaf7a38cd9350fc52d2bb092d2261483b6b`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 6.9 MB (6932412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb61cbf781bf1ad1f584b29991a24c4ad159bb77066a66dfbc69d0530c956bd`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 92.4 KB (92445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f614095489d33530a88164a8c28f37b2d4905f0b80d0d6b55f20aaadfd70949`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebf1832bba38f06f167c58af841378ce16e956f5bbf93fac3890ad9c28c8cbf`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 64.4 MB (64391839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40879250d388c3438681a3fcb4c0dfd255a9608c7640fef9336b0e41182e1f96`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e36d8cddb77fc04b3f2ce2f905702ec5fa87992d2042e8c67f1270e0a00d47`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:f9bb7ce8788987c53f7376c978032c32bd32ceb0a11d3922bd1f30e83a330420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488001f5e00c1d96abaa4ef21598a7cb0c85dcdc849cc938a582649148cbfa1f`

```dockerfile
```

-	Layers:
	-	`sha256:f4371bf22d65b61f21247586c39a31945ff88f568ae5663039cabcbb9a800af7`  
		Last Modified: Thu, 04 Dec 2025 06:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:414cac80b8731cec0ba7269b2401349a90593d66af7a0861ec3c7d0198f4f25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128364231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab64be5a5da0cbe0bcc502e6958aa17939272152b190069d69458ac92d5ce4bd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:18:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:18:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:18:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:18:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:18:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:18:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:18:46 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:14:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:14:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:14:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:14:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:14:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:14:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:14:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:14:14 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af6abcf03c4d2a46ff1f3cf4e321bc7993d4d20b17f12f99d466b39b3555298`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 8.3 MB (8301067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb792a943c4d38855261216162c97e27587aa936e4de5451eeda4d170348a07`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309aa1d961beedab5a903eed7b199a7f3cf448a9ad0d235f989735bce0000963`  
		Last Modified: Thu, 04 Dec 2025 01:19:02 GMT  
		Size: 17.6 MB (17560675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136294917ec3532038026ad3f18199c6aff9e645109302b3c9fdc832bf5dd82`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 21.5 MB (21476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e0b74dd96a21e6b38324422ba118ccd940a01d181d09275193f948ebd543d2`  
		Last Modified: Thu, 04 Dec 2025 01:19:00 GMT  
		Size: 10.2 MB (10195783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48a193c8f7c9fb004babea7c82efc513b5196991d924daf956f6881012fec3`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86d05610e4cf2f79db6d09c9b4c2c8944991a0da701d442726824c5daf33ae`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ebf88cb27a0d9b7e72386749701cbb0df6c753c53caa647578e1151c9f6e0`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2889ceaea16d005f911037ba1943baa11fca8f5499572f26e08d1623571b0fca`  
		Last Modified: Thu, 04 Dec 2025 02:14:36 GMT  
		Size: 7.3 MB (7269170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a951be59abc423fe14ab9e8f769c4aab51ee15004ef9b7cccad5f65451fb56`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 91.7 KB (91736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e9ad64722f26f00125e9b549b06d40a727849d2f9550dc66a6533d89ebf8fa`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31cd3ee01e94bb58480e2a72b8f3677d9457fa9a26aa6f8b63431dbc313074e`  
		Last Modified: Thu, 04 Dec 2025 02:14:43 GMT  
		Size: 59.9 MB (59893205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0159762f19a8b9a93c9555ca6508e536ae2ffa5221f1f7fe2517b25edb26c7df`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b0105e4b3b66292b7fa5025b925cfea155b39007901429ba1dad2b3064ee51`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:ab05258dcfbb29e603677ce44f578d475223727587324270624d8ea011d7ccda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20281852242edf20349d07841d8bc88fc25a406146000e725cf15a381d07094a`

```dockerfile
```

-	Layers:
	-	`sha256:e799d064fde967b53c6149a5df7009511ddce4ce4274868ee730661a6eeb37be`  
		Last Modified: Thu, 04 Dec 2025 06:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:0541f6653d52b64dd6cd2d3d726aee9bca91947de8a574f57303b4f1636a14f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126462847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209da4e636036ccbab56e97d822d0ab39a923aa5572a22674e75a74493b686c2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:17:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:17:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:17:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:17:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:17:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:17:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:17:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:17:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:17:29 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:09:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:09:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:09:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:09:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:09:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:09:21 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab67aee2b47b20a25046ed73de706bd5a80ad82192c27db420a65cfa5fb17cb`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 7.6 MB (7598018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860397c02592909361c994060954f1d684dc0366a2df922a3fe521f02a6b6b2`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ddf54b4c1a081004e3eb1cd154ca1c1cc7e169e416c1ebb9fb23b872919a4d`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 17.6 MB (17550083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645b95707890af1cad5443377a3d8bba32e3701d1f59ee629bd3a1598e45b63`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 21.5 MB (21454910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d968e842fbfa0f7d8d14048d776e945449a586f5772cf04dc12753e58629d9`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 10.2 MB (10188525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9482495d52b3d32ead0b4c76816259e750cf45944ac6a48937ed5de349bc73b`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862303f1e616b7c4e5debf343f489e54323b1d7e8d897d6bbcf9951c6fb125e7`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581b42590dfec33aa271798a0fdbb5fb080fa6137a58beb89183e43d609cc24`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef35268d1c5043e126a7b2b7cccba9910ba866f3721d67bc80d8768966a3202`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 6.6 MB (6570913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6110fc79c7e532c554cef8b106c77e384dffc4dbe8ff453044efb95611640865`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 88.1 KB (88108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eebdb0a3d24aad8069039ec36bba107f65570fd4460d47f5c5bc29bd7ab18c9`  
		Last Modified: Thu, 04 Dec 2025 02:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ff8b61a42ac17a9147133f9cfb9f005cc5a7597c4fbe27bd8305f307f0413a`  
		Last Modified: Thu, 04 Dec 2025 02:09:51 GMT  
		Size: 59.7 MB (59725679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5721cb1c43ef63e8c0bce0addcaa897e3b41d32fe7bf88c8020981f6cf24833f`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ef0da11c43d1593fd48c517bb7f91d37aba3bdf335ba6c03da014da92736e`  
		Last Modified: Thu, 04 Dec 2025 02:09:42 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:5ac10dc71cf0cc09125a924469cb4aecc84840796fde5d9d0342a0baee3f5507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37587e9d82c759400bbe91d7affa6d8bed70364b85068a5dceef5c381a8f048a`

```dockerfile
```

-	Layers:
	-	`sha256:a20dd7c4bd39660f77009db4c78ecbaf59987f8c583b5a69d876f11f05d0da6e`  
		Last Modified: Thu, 04 Dec 2025 06:07:37 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:835173465724c55bedd93b72bdb6724104693472836d4354236bd9f87ccc6e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126316862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1db13432a7537ebc347611396429d42295ceb944903b73ab7ed6ca66a7d24ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:14:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:14:01 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf7527ac3d38e2b3f6d1176cd286fb31e55896c8724ba176b4d4958e4075db2`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 8.5 MB (8453465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4639c90abf56c9e413f2f2d2c096aefc19cf619ba9f5b28d891218b96ce733`  
		Last Modified: Thu, 04 Dec 2025 01:14:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc4c4bdc3b3639f19fd743ed949e35d8d7164a53fa32494422b203bbc675f5`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 17.3 MB (17334885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787c5406b3fa1fc1c5f4ee10e3f972d710de70beb323a67ceb5aa62273f8aa2`  
		Last Modified: Thu, 04 Dec 2025 01:14:22 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772518255e899b197408165167764a4d01d2b1098d6b40716fe91444be12a43c`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 9.9 MB (9938698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa62af1a24bf51d9a4d39915667786eb279e97dab96543236a409060be26a4`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a485df48fa9519df08360fc32bc48f54c3e8645b16565c58654267487f7bff`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e420e20b91d5cf88de9d2f64e34c09ebf8fa77ab2147c66fe59fbc546b08a64`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4ec7220c3f61f31eba0afab7f6e4defe2bc8ce778302f7ccbe98325fbc2`  
		Last Modified: Thu, 04 Dec 2025 02:12:44 GMT  
		Size: 7.2 MB (7211504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216239cfaa66c6158aaee65ef2d3ce737384d2ee872d2a74d4ae2f0178284e69`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 101.3 KB (101256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba097afc00e56a014d7ba0d623f39b67a2e68e4d622113752ce9e9e03e2308f9`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0c46a299f22b7f8f78c049709892e1660352aa8fe591e54e27030774b69e3d`  
		Last Modified: Thu, 04 Dec 2025 02:12:47 GMT  
		Size: 58.4 MB (58428644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c271f430dfb557ed996372a070b01fc71fd92aa464beb69530d45a33dd887b`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3583ad88ca4d8e567b11ce83128811bc0c359cfa889e192896e0942686282598`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:1d3c36d88728fafa4708e5ffc1a34ae3be9c093b4668b882bd3f9b2808df9f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c9de27527effa797f1e73c2627b71d4d65243f3429a0fff7dd7a42d9601934`

```dockerfile
```

-	Layers:
	-	`sha256:467e80fb00d99af46899eed546c4f3c351297a1b14166825411e06dcbb6f39e2`  
		Last Modified: Thu, 04 Dec 2025 06:07:40 GMT  
		Size: 34.8 KB (34775 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:574a3f2f9fdbffa4c8e8f9741a8c04c6609d29b344338a46ec4d54f218e28e7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:56a7635e08b58bc1c764f0646e484b480a37c0c9209e42d7a1324d426d58d996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156929499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7044c07accbc2c2fec49490a3d5822690d721f4af5e2ab2dc96ca8ff23017d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:12:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:12:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:12:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:12:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:12:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:12:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:12:38 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:17 GMT
CMD []
# Thu, 04 Dec 2025 03:13:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 03:13:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 03:13:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 03:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 03:14:00 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 03:14:00 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 03:14:00 GMT
USER rootless
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9948ae9a3223520d912ab66de5d55ae24d29c808a510d02ab8cefd00f6af1`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 8.4 MB (8399334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b09731169ba7df8d96a4bb9a1a6ab3d4c1560d30cc4429e0e0180131ccaf7c9`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22939237c954384f47f26a89ee0dd27d44805625e73797e594c00dfe4f40b97a`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 18.8 MB (18763825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb36afae27f4bbcb70ff6c2154f9a0c7e0e5aeb479254c14e3d97743d63765d`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 22.9 MB (22905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf52db4eb6dc458063c42a6e1ccff1a420fc8ca9c6054305aa393dcb100491`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 10.8 MB (10784455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0739e6c04d86d46c4bbd27f2c6aeddd85de220909f633494d0d453f69475e1f`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33287860d4ed49c1e91d9f437b63622f4a717e826b7d3aa4d3cc847adfbd85fe`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8131e857b4a01669f532d44efd02dc2eced5ae48d3eeaee6272747a38064919`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ceb3774725100b39cc84625299eaf7a38cd9350fc52d2bb092d2261483b6b`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 6.9 MB (6932412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb61cbf781bf1ad1f584b29991a24c4ad159bb77066a66dfbc69d0530c956bd`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 92.4 KB (92445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f614095489d33530a88164a8c28f37b2d4905f0b80d0d6b55f20aaadfd70949`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebf1832bba38f06f167c58af841378ce16e956f5bbf93fac3890ad9c28c8cbf`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 64.4 MB (64391839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40879250d388c3438681a3fcb4c0dfd255a9608c7640fef9336b0e41182e1f96`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e36d8cddb77fc04b3f2ce2f905702ec5fa87992d2042e8c67f1270e0a00d47`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a640eb35a6502db5190bb0bb8deb619d9f050e7f3017b5819cd9f2f0730ace`  
		Last Modified: Thu, 04 Dec 2025 03:14:13 GMT  
		Size: 3.4 MB (3419922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c74d1c60153ac02bd4eff5325e6fa1887d79239e7ad25ebdc10daa3c737ebc3`  
		Last Modified: Thu, 04 Dec 2025 03:14:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a3f3709fe2bfb65daceaff5bc768a8c46c12b429dd51f6d836deb949f69ed2`  
		Last Modified: Thu, 04 Dec 2025 03:14:12 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea03eb9631ccce3547d2b98ccbae68940b4b27ee68a0023d8e85f3d03571811a`  
		Last Modified: Thu, 04 Dec 2025 03:14:14 GMT  
		Size: 17.4 MB (17370982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659d25d3e0c3b4f79f1ab84cd3383ac7c5ad40ad0d1257e746bf9a598056a773`  
		Last Modified: Thu, 04 Dec 2025 03:14:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3088595ddea0c377ad4a6d825a1e599bfc51c5179c762016f33e84f70f146281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a9ecfe6ee5edd280120c6ed90cc853e67a271da14fafa84d4a83ebd3a8847a`

```dockerfile
```

-	Layers:
	-	`sha256:c0e983a660428ca0287998fc28bc7373babd47a24229c324b828df8b14da19b3`  
		Last Modified: Thu, 04 Dec 2025 06:07:42 GMT  
		Size: 30.6 KB (30588 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:6b25832ef4e2c960f75ab279a6595d37461cd3d5b27f92661b2b383e0ccd0dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147421264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a897cb5a9ae1c74a08c6011f4a8f635e8179c79bc7fc616545a1c57af41bb8a6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:14:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:14:01 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:25 GMT
CMD []
# Thu, 04 Dec 2025 03:12:48 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Thu, 04 Dec 2025 03:12:48 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Dec 2025 03:12:49 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 03:12:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Dec 2025 03:12:49 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Dec 2025 03:12:49 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Dec 2025 03:12:49 GMT
USER rootless
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf7527ac3d38e2b3f6d1176cd286fb31e55896c8724ba176b4d4958e4075db2`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 8.5 MB (8453465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4639c90abf56c9e413f2f2d2c096aefc19cf619ba9f5b28d891218b96ce733`  
		Last Modified: Thu, 04 Dec 2025 01:14:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc4c4bdc3b3639f19fd743ed949e35d8d7164a53fa32494422b203bbc675f5`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 17.3 MB (17334885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787c5406b3fa1fc1c5f4ee10e3f972d710de70beb323a67ceb5aa62273f8aa2`  
		Last Modified: Thu, 04 Dec 2025 01:14:22 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772518255e899b197408165167764a4d01d2b1098d6b40716fe91444be12a43c`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 9.9 MB (9938698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa62af1a24bf51d9a4d39915667786eb279e97dab96543236a409060be26a4`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a485df48fa9519df08360fc32bc48f54c3e8645b16565c58654267487f7bff`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e420e20b91d5cf88de9d2f64e34c09ebf8fa77ab2147c66fe59fbc546b08a64`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4ec7220c3f61f31eba0afab7f6e4defe2bc8ce778302f7ccbe98325fbc2`  
		Last Modified: Thu, 04 Dec 2025 02:12:44 GMT  
		Size: 7.2 MB (7211504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216239cfaa66c6158aaee65ef2d3ce737384d2ee872d2a74d4ae2f0178284e69`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 101.3 KB (101256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba097afc00e56a014d7ba0d623f39b67a2e68e4d622113752ce9e9e03e2308f9`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0c46a299f22b7f8f78c049709892e1660352aa8fe591e54e27030774b69e3d`  
		Last Modified: Thu, 04 Dec 2025 02:12:47 GMT  
		Size: 58.4 MB (58428644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c271f430dfb557ed996372a070b01fc71fd92aa464beb69530d45a33dd887b`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3583ad88ca4d8e567b11ce83128811bc0c359cfa889e192896e0942686282598`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d2bb7e9b7fe1cdb8d2b60423b41081687236d166de8ff04449219e1a8c151a`  
		Last Modified: Thu, 04 Dec 2025 03:13:10 GMT  
		Size: 3.4 MB (3394320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7b242fa22ee707972d86134a53d0a0f6a7d76efffa79ebfd4df747a3b7a5da`  
		Last Modified: Thu, 04 Dec 2025 03:13:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd4bac04225138ca50ef4363daee9293867ae4b0ce79f6b2dbad7b96a89d653`  
		Last Modified: Thu, 04 Dec 2025 03:13:10 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b4a984119cab953f09c8d619d346a43cbe48ff928ca031ad3d5908235b9412`  
		Last Modified: Thu, 04 Dec 2025 03:13:12 GMT  
		Size: 17.7 MB (17708737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db42e4847c0349ea6ed8a7f8941c38c153ae17691259ac6dbdb7c42b5027d309`  
		Last Modified: Thu, 04 Dec 2025 03:13:10 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2d4ae8ad4ca57769cf93f6dd3546eb767e4c9854641b08f4d8b9bd7c6e3bdd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97d97a6ee675067883e76b4653acfb23b19eeafd22f3ca54d975bfd1f94eec1`

```dockerfile
```

-	Layers:
	-	`sha256:953c88b79af11583ed0f510cfa7ce6fd408413d33ba382b397097f3992a54073`  
		Last Modified: Thu, 04 Dec 2025 06:07:54 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:40916fb078cdd27640d069bba401324a15a06d3ecbd8895048122c8d321f43f8
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
$ docker pull docker@sha256:967468c0be954e3a0d4bc31310e196a5a8d1adda607b0be11056d4d1badd6587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136137253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad869b62b5c060fe1594ae7fd17228cbc7468da180d9192bd8d59c1b17c896b3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:12:34 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:12:34 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:12:36 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:12:36 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:12:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:12:37 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:12:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:12:38 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:12:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:12:38 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:17 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:17 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:17 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:17 GMT
CMD []
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d9948ae9a3223520d912ab66de5d55ae24d29c808a510d02ab8cefd00f6af1`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 8.4 MB (8399334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b09731169ba7df8d96a4bb9a1a6ab3d4c1560d30cc4429e0e0180131ccaf7c9`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22939237c954384f47f26a89ee0dd27d44805625e73797e594c00dfe4f40b97a`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 18.8 MB (18763825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb36afae27f4bbcb70ff6c2154f9a0c7e0e5aeb479254c14e3d97743d63765d`  
		Last Modified: Thu, 04 Dec 2025 01:12:55 GMT  
		Size: 22.9 MB (22905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cf52db4eb6dc458063c42a6e1ccff1a420fc8ca9c6054305aa393dcb100491`  
		Last Modified: Thu, 04 Dec 2025 01:12:54 GMT  
		Size: 10.8 MB (10784455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0739e6c04d86d46c4bbd27f2c6aeddd85de220909f633494d0d453f69475e1f`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33287860d4ed49c1e91d9f437b63622f4a717e826b7d3aa4d3cc847adfbd85fe`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8131e857b4a01669f532d44efd02dc2eced5ae48d3eeaee6272747a38064919`  
		Last Modified: Thu, 04 Dec 2025 01:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82ceb3774725100b39cc84625299eaf7a38cd9350fc52d2bb092d2261483b6b`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 6.9 MB (6932412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb61cbf781bf1ad1f584b29991a24c4ad159bb77066a66dfbc69d0530c956bd`  
		Last Modified: Thu, 04 Dec 2025 02:12:38 GMT  
		Size: 92.4 KB (92445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f614095489d33530a88164a8c28f37b2d4905f0b80d0d6b55f20aaadfd70949`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebf1832bba38f06f167c58af841378ce16e956f5bbf93fac3890ad9c28c8cbf`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 64.4 MB (64391839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40879250d388c3438681a3fcb4c0dfd255a9608c7640fef9336b0e41182e1f96`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e36d8cddb77fc04b3f2ce2f905702ec5fa87992d2042e8c67f1270e0a00d47`  
		Last Modified: Thu, 04 Dec 2025 02:12:39 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:f9bb7ce8788987c53f7376c978032c32bd32ceb0a11d3922bd1f30e83a330420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488001f5e00c1d96abaa4ef21598a7cb0c85dcdc849cc938a582649148cbfa1f`

```dockerfile
```

-	Layers:
	-	`sha256:f4371bf22d65b61f21247586c39a31945ff88f568ae5663039cabcbb9a800af7`  
		Last Modified: Thu, 04 Dec 2025 06:07:29 GMT  
		Size: 34.5 KB (34541 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:414cac80b8731cec0ba7269b2401349a90593d66af7a0861ec3c7d0198f4f25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128364231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab64be5a5da0cbe0bcc502e6958aa17939272152b190069d69458ac92d5ce4bd`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:18:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:18:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:18:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:18:42 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:18:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:18:44 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:18:45 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:18:45 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:18:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:18:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:18:46 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:14:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:14:10 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:14:10 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:14:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:14:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:14:14 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:14:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:14:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:14:14 GMT
CMD []
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af6abcf03c4d2a46ff1f3cf4e321bc7993d4d20b17f12f99d466b39b3555298`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 8.3 MB (8301067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb792a943c4d38855261216162c97e27587aa936e4de5451eeda4d170348a07`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309aa1d961beedab5a903eed7b199a7f3cf448a9ad0d235f989735bce0000963`  
		Last Modified: Thu, 04 Dec 2025 01:19:02 GMT  
		Size: 17.6 MB (17560675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b136294917ec3532038026ad3f18199c6aff9e645109302b3c9fdc832bf5dd82`  
		Last Modified: Thu, 04 Dec 2025 01:19:01 GMT  
		Size: 21.5 MB (21476553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e0b74dd96a21e6b38324422ba118ccd940a01d181d09275193f948ebd543d2`  
		Last Modified: Thu, 04 Dec 2025 01:19:00 GMT  
		Size: 10.2 MB (10195783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da48a193c8f7c9fb004babea7c82efc513b5196991d924daf956f6881012fec3`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86d05610e4cf2f79db6d09c9b4c2c8944991a0da701d442726824c5daf33ae`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ebf88cb27a0d9b7e72386749701cbb0df6c753c53caa647578e1151c9f6e0`  
		Last Modified: Thu, 04 Dec 2025 01:18:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2889ceaea16d005f911037ba1943baa11fca8f5499572f26e08d1623571b0fca`  
		Last Modified: Thu, 04 Dec 2025 02:14:36 GMT  
		Size: 7.3 MB (7269170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a951be59abc423fe14ab9e8f769c4aab51ee15004ef9b7cccad5f65451fb56`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 91.7 KB (91736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e9ad64722f26f00125e9b549b06d40a727849d2f9550dc66a6533d89ebf8fa`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31cd3ee01e94bb58480e2a72b8f3677d9457fa9a26aa6f8b63431dbc313074e`  
		Last Modified: Thu, 04 Dec 2025 02:14:43 GMT  
		Size: 59.9 MB (59893205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0159762f19a8b9a93c9555ca6508e536ae2ffa5221f1f7fe2517b25edb26c7df`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b0105e4b3b66292b7fa5025b925cfea155b39007901429ba1dad2b3064ee51`  
		Last Modified: Thu, 04 Dec 2025 02:14:35 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:ab05258dcfbb29e603677ce44f578d475223727587324270624d8ea011d7ccda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20281852242edf20349d07841d8bc88fc25a406146000e725cf15a381d07094a`

```dockerfile
```

-	Layers:
	-	`sha256:e799d064fde967b53c6149a5df7009511ddce4ce4274868ee730661a6eeb37be`  
		Last Modified: Thu, 04 Dec 2025 06:07:32 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:0541f6653d52b64dd6cd2d3d726aee9bca91947de8a574f57303b4f1636a14f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126462847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209da4e636036ccbab56e97d822d0ab39a923aa5572a22674e75a74493b686c2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:17:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:17:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:17:24 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:17:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:17:26 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:17:28 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:17:28 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:17:29 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:17:29 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:17:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:17:29 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:09:16 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:09:18 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:09:18 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:09:21 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:09:21 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:09:21 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:09:21 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:09:21 GMT
CMD []
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab67aee2b47b20a25046ed73de706bd5a80ad82192c27db420a65cfa5fb17cb`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 7.6 MB (7598018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860397c02592909361c994060954f1d684dc0366a2df922a3fe521f02a6b6b2`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ddf54b4c1a081004e3eb1cd154ca1c1cc7e169e416c1ebb9fb23b872919a4d`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 17.6 MB (17550083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1645b95707890af1cad5443377a3d8bba32e3701d1f59ee629bd3a1598e45b63`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 21.5 MB (21454910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d968e842fbfa0f7d8d14048d776e945449a586f5772cf04dc12753e58629d9`  
		Last Modified: Thu, 04 Dec 2025 01:17:45 GMT  
		Size: 10.2 MB (10188525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9482495d52b3d32ead0b4c76816259e750cf45944ac6a48937ed5de349bc73b`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862303f1e616b7c4e5debf343f489e54323b1d7e8d897d6bbcf9951c6fb125e7`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581b42590dfec33aa271798a0fdbb5fb080fa6137a58beb89183e43d609cc24`  
		Last Modified: Thu, 04 Dec 2025 01:17:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef35268d1c5043e126a7b2b7cccba9910ba866f3721d67bc80d8768966a3202`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 6.6 MB (6570913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6110fc79c7e532c554cef8b106c77e384dffc4dbe8ff453044efb95611640865`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 88.1 KB (88108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eebdb0a3d24aad8069039ec36bba107f65570fd4460d47f5c5bc29bd7ab18c9`  
		Last Modified: Thu, 04 Dec 2025 02:09:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ff8b61a42ac17a9147133f9cfb9f005cc5a7597c4fbe27bd8305f307f0413a`  
		Last Modified: Thu, 04 Dec 2025 02:09:51 GMT  
		Size: 59.7 MB (59725679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5721cb1c43ef63e8c0bce0addcaa897e3b41d32fe7bf88c8020981f6cf24833f`  
		Last Modified: Thu, 04 Dec 2025 02:09:43 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ef0da11c43d1593fd48c517bb7f91d37aba3bdf335ba6c03da014da92736e`  
		Last Modified: Thu, 04 Dec 2025 02:09:42 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:5ac10dc71cf0cc09125a924469cb4aecc84840796fde5d9d0342a0baee3f5507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37587e9d82c759400bbe91d7affa6d8bed70364b85068a5dceef5c381a8f048a`

```dockerfile
```

-	Layers:
	-	`sha256:a20dd7c4bd39660f77009db4c78ecbaf59987f8c583b5a69d876f11f05d0da6e`  
		Last Modified: Thu, 04 Dec 2025 06:07:37 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:835173465724c55bedd93b72bdb6724104693472836d4354236bd9f87ccc6e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126316862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1db13432a7537ebc347611396429d42295ceb944903b73ab7ed6ca66a7d24ee`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 01:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Dec 2025 01:13:57 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_VERSION=29.1.2
# Thu, 04 Dec 2025 01:14:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Dec 2025 01:14:00 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Thu, 04 Dec 2025 01:14:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Dec 2025 01:14:01 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Dec 2025 01:14:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 01:14:01 GMT
CMD ["sh"]
# Thu, 04 Dec 2025 02:12:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Dec 2025 02:12:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Thu, 04 Dec 2025 02:12:25 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 02:12:25 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Dec 2025 02:12:25 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Dec 2025 02:12:25 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Dec 2025 02:12:25 GMT
CMD []
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf7527ac3d38e2b3f6d1176cd286fb31e55896c8724ba176b4d4958e4075db2`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 8.5 MB (8453465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4639c90abf56c9e413f2f2d2c096aefc19cf619ba9f5b28d891218b96ce733`  
		Last Modified: Thu, 04 Dec 2025 01:14:19 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bc4c4bdc3b3639f19fd743ed949e35d8d7164a53fa32494422b203bbc675f5`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 17.3 MB (17334885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8787c5406b3fa1fc1c5f4ee10e3f972d710de70beb323a67ceb5aa62273f8aa2`  
		Last Modified: Thu, 04 Dec 2025 01:14:22 GMT  
		Size: 20.6 MB (20645073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772518255e899b197408165167764a4d01d2b1098d6b40716fe91444be12a43c`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 9.9 MB (9938698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa62af1a24bf51d9a4d39915667786eb279e97dab96543236a409060be26a4`  
		Last Modified: Thu, 04 Dec 2025 01:14:20 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a485df48fa9519df08360fc32bc48f54c3e8645b16565c58654267487f7bff`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e420e20b91d5cf88de9d2f64e34c09ebf8fa77ab2147c66fe59fbc546b08a64`  
		Last Modified: Thu, 04 Dec 2025 01:14:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7662c4ec7220c3f61f31eba0afab7f6e4defe2bc8ce778302f7ccbe98325fbc2`  
		Last Modified: Thu, 04 Dec 2025 02:12:44 GMT  
		Size: 7.2 MB (7211504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216239cfaa66c6158aaee65ef2d3ce737384d2ee872d2a74d4ae2f0178284e69`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 101.3 KB (101256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba097afc00e56a014d7ba0d623f39b67a2e68e4d622113752ce9e9e03e2308f9`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0c46a299f22b7f8f78c049709892e1660352aa8fe591e54e27030774b69e3d`  
		Last Modified: Thu, 04 Dec 2025 02:12:47 GMT  
		Size: 58.4 MB (58428644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c271f430dfb557ed996372a070b01fc71fd92aa464beb69530d45a33dd887b`  
		Last Modified: Thu, 04 Dec 2025 02:12:43 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3583ad88ca4d8e567b11ce83128811bc0c359cfa889e192896e0942686282598`  
		Last Modified: Thu, 04 Dec 2025 02:12:42 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:1d3c36d88728fafa4708e5ffc1a34ae3be9c093b4668b882bd3f9b2808df9f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c9de27527effa797f1e73c2627b71d4d65243f3429a0fff7dd7a42d9601934`

```dockerfile
```

-	Layers:
	-	`sha256:467e80fb00d99af46899eed546c4f3c351297a1b14166825411e06dcbb6f39e2`  
		Last Modified: Thu, 04 Dec 2025 06:07:40 GMT  
		Size: 34.8 KB (34775 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:67d857e9b0274e9c3bedbcba525dce2fa9133df508d67717e9e7e2950bec1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `docker:windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:d4dc0559c90e51495ababe507d0d4e412494de5b91e422af6c3cc68d924b6993
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308219283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74124bda75304cdae09598bcf1e2092ec876a2ff90459600c44773c77af4e38d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:32:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:33:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:33:11 GMT
ENV DOCKER_VERSION=29.1.2
# Tue, 09 Dec 2025 20:33:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Tue, 09 Dec 2025 20:33:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:33:21 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 09 Dec 2025 20:33:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 09 Dec 2025 20:33:22 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 09 Dec 2025 20:33:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:33:30 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Tue, 09 Dec 2025 20:33:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Tue, 09 Dec 2025 20:33:31 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Tue, 09 Dec 2025 20:33:37 GMT
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
	-	`sha256:a2fe319ee30340452819276b474d727c837b38b988cffead971ab498342327a0`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b497a39ebb57933272167001f136723338e9978c27a3ed3fc07cf559cfd3c6f6`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 350.8 KB (350799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba80a26db457c47c0c692c8edd53e3254f9208f569053d10b37fa20f3ee9f61`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc370eb16492f352f81a2fa60f8184a7e193436d6c1065bd341f1619fbe6f11a`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d799e6d8eae30a8d932238e5b2096f89536fbc820e6ebdceb023b76a49adc791`  
		Last Modified: Tue, 09 Dec 2025 20:42:56 GMT  
		Size: 19.4 MB (19412389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efba57425bf6d57f35db21a956148c7011ffe7bcc7c7f39cc164b5d64926733c`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1253688da912cc57db2a544ae99548889bdf183dd7c78430e465bd428049e1fe`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b592805a7d17afbafc77f7ff035bce675f05e30b44c04a43a3a4f7f58ea1a8`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8416f9beb18ad66ba7343e899211ea306550a6eb4222148da2703ca450658f72`  
		Last Modified: Tue, 09 Dec 2025 20:42:57 GMT  
		Size: 23.9 MB (23901643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051c1994c45a3c345cd3977217d9d617df96a809c20fa15edbb9f5f87b484c93`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a185b6b64f2626043248cb47685a0d9c80e8ba4e4bcafca01544e3321473ac2a`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d79da57493f446b6263f59eda6b9554b1b88318bb230873d2e371050f55d0dc`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361a34870d5fab376e491284c214f936b58ee5031797aee97d0411a7f6269c02`  
		Last Modified: Tue, 09 Dec 2025 20:42:55 GMT  
		Size: 11.4 MB (11422280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:895cf5abcd8b5c61241aba2dd46c1dfd3d0ae29324f35730e0c05a23d6bd0cb9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835132397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f5a3f08a73b3091edff5dba7b7b84491fdc8c6ea4263706f1af48bde068687`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:29:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:29:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:29:34 GMT
ENV DOCKER_VERSION=29.1.2
# Tue, 09 Dec 2025 20:29:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Tue, 09 Dec 2025 20:29:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:29:48 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 09 Dec 2025 20:29:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 09 Dec 2025 20:29:50 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 09 Dec 2025 20:30:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Tue, 09 Dec 2025 20:30:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Tue, 09 Dec 2025 20:30:09 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Tue, 09 Dec 2025 20:30:20 GMT
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
	-	`sha256:9dac22ca67391bc67ae059bdc6b4fe7cfa91d0dd9f198a7a4a48d1208814e923`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043349e15d735002fd555e4be32832770828589a651eae11f6cf3f2d02ad4b4e`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 488.7 KB (488734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0fb93b3fcc9496a612d74204ac287360ea57a3a26361271104c86be97334`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea35c40b9971e81debd25b3b9ba90709cdd71ad966066d98d4ef47f7ef1eaa74`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868c903082601f929e25172b2414f102a42725f192ad9fd0edda66b432253e2f`  
		Last Modified: Tue, 09 Dec 2025 20:37:36 GMT  
		Size: 19.4 MB (19412413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3cf58d9086ad644440d4cd0239041b6305aceaeee9f403302a36428940da55`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b32043b05c27d4f3be96d052d081c4c79b08a4d493ba5737e2814bf8698c0d9`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c50ed9458936b4b0976ddb6a0aa490c6a3a101279aa9cf908ea25110d348fd`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f549308f1773171323e5c688a1a6ffb5c50c95638f3ad4d039147527e46a3a8a`  
		Last Modified: Tue, 09 Dec 2025 20:37:36 GMT  
		Size: 23.9 MB (23912184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38406868117ff3519bb0788d7047ec66dfa6834a044d57d8182b6d146b3160e`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd122a724ea56e0e9207b97122512081dd96d6795b3e61063cef71d5a12e001`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530aa0c39c848502a74b0e0aeea5d02325c53752e036d70f6be87168e64e92ea`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7727d6e218b2e69fbc73769cf1761c3f84c1884e76186c74a315eaf7ac866ba`  
		Last Modified: Tue, 09 Dec 2025 20:37:35 GMT  
		Size: 11.4 MB (11427927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f1da8d96a13c6d2f5c2c77394c41baa60cba07f4323fb4c5a10c042d18dc0591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:895cf5abcd8b5c61241aba2dd46c1dfd3d0ae29324f35730e0c05a23d6bd0cb9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835132397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f5a3f08a73b3091edff5dba7b7b84491fdc8c6ea4263706f1af48bde068687`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:29:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:29:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:29:34 GMT
ENV DOCKER_VERSION=29.1.2
# Tue, 09 Dec 2025 20:29:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Tue, 09 Dec 2025 20:29:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:29:48 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 09 Dec 2025 20:29:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 09 Dec 2025 20:29:50 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 09 Dec 2025 20:30:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:30:08 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Tue, 09 Dec 2025 20:30:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Tue, 09 Dec 2025 20:30:09 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Tue, 09 Dec 2025 20:30:20 GMT
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
	-	`sha256:9dac22ca67391bc67ae059bdc6b4fe7cfa91d0dd9f198a7a4a48d1208814e923`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043349e15d735002fd555e4be32832770828589a651eae11f6cf3f2d02ad4b4e`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 488.7 KB (488734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236b0fb93b3fcc9496a612d74204ac287360ea57a3a26361271104c86be97334`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea35c40b9971e81debd25b3b9ba90709cdd71ad966066d98d4ef47f7ef1eaa74`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868c903082601f929e25172b2414f102a42725f192ad9fd0edda66b432253e2f`  
		Last Modified: Tue, 09 Dec 2025 20:37:36 GMT  
		Size: 19.4 MB (19412413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3cf58d9086ad644440d4cd0239041b6305aceaeee9f403302a36428940da55`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b32043b05c27d4f3be96d052d081c4c79b08a4d493ba5737e2814bf8698c0d9`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c50ed9458936b4b0976ddb6a0aa490c6a3a101279aa9cf908ea25110d348fd`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f549308f1773171323e5c688a1a6ffb5c50c95638f3ad4d039147527e46a3a8a`  
		Last Modified: Tue, 09 Dec 2025 20:37:36 GMT  
		Size: 23.9 MB (23912184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38406868117ff3519bb0788d7047ec66dfa6834a044d57d8182b6d146b3160e`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd122a724ea56e0e9207b97122512081dd96d6795b3e61063cef71d5a12e001`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530aa0c39c848502a74b0e0aeea5d02325c53752e036d70f6be87168e64e92ea`  
		Last Modified: Tue, 09 Dec 2025 20:37:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7727d6e218b2e69fbc73769cf1761c3f84c1884e76186c74a315eaf7ac866ba`  
		Last Modified: Tue, 09 Dec 2025 20:37:35 GMT  
		Size: 11.4 MB (11427927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:55c65e84a8de249a5b8a74df2f4e07f150d558869a7fbef2e356c66caa4c4c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull docker@sha256:d4dc0559c90e51495ababe507d0d4e412494de5b91e422af6c3cc68d924b6993
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3308219283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74124bda75304cdae09598bcf1e2092ec876a2ff90459600c44773c77af4e38d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:32:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:33:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:33:11 GMT
ENV DOCKER_VERSION=29.1.2
# Tue, 09 Dec 2025 20:33:12 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.1.2.zip
# Tue, 09 Dec 2025 20:33:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:33:21 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Tue, 09 Dec 2025 20:33:22 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Tue, 09 Dec 2025 20:33:22 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Tue, 09 Dec 2025 20:33:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:33:30 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Tue, 09 Dec 2025 20:33:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Tue, 09 Dec 2025 20:33:31 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Tue, 09 Dec 2025 20:33:37 GMT
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
	-	`sha256:a2fe319ee30340452819276b474d727c837b38b988cffead971ab498342327a0`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b497a39ebb57933272167001f136723338e9978c27a3ed3fc07cf559cfd3c6f6`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 350.8 KB (350799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba80a26db457c47c0c692c8edd53e3254f9208f569053d10b37fa20f3ee9f61`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc370eb16492f352f81a2fa60f8184a7e193436d6c1065bd341f1619fbe6f11a`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d799e6d8eae30a8d932238e5b2096f89536fbc820e6ebdceb023b76a49adc791`  
		Last Modified: Tue, 09 Dec 2025 20:42:56 GMT  
		Size: 19.4 MB (19412389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efba57425bf6d57f35db21a956148c7011ffe7bcc7c7f39cc164b5d64926733c`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1253688da912cc57db2a544ae99548889bdf183dd7c78430e465bd428049e1fe`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b592805a7d17afbafc77f7ff035bce675f05e30b44c04a43a3a4f7f58ea1a8`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8416f9beb18ad66ba7343e899211ea306550a6eb4222148da2703ca450658f72`  
		Last Modified: Tue, 09 Dec 2025 20:42:57 GMT  
		Size: 23.9 MB (23901643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051c1994c45a3c345cd3977217d9d617df96a809c20fa15edbb9f5f87b484c93`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a185b6b64f2626043248cb47685a0d9c80e8ba4e4bcafca01544e3321473ac2a`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d79da57493f446b6263f59eda6b9554b1b88318bb230873d2e371050f55d0dc`  
		Last Modified: Tue, 09 Dec 2025 20:42:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361a34870d5fab376e491284c214f936b58ee5031797aee97d0411a7f6269c02`  
		Last Modified: Tue, 09 Dec 2025 20:42:55 GMT  
		Size: 11.4 MB (11422280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
