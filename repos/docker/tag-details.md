<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:28`](#docker28)
-	[`docker:28-cli`](#docker28-cli)
-	[`docker:28-dind`](#docker28-dind)
-	[`docker:28-dind-rootless`](#docker28-dind-rootless)
-	[`docker:28-windowsservercore`](#docker28-windowsservercore)
-	[`docker:28-windowsservercore-ltsc2022`](#docker28-windowsservercore-ltsc2022)
-	[`docker:28-windowsservercore-ltsc2025`](#docker28-windowsservercore-ltsc2025)
-	[`docker:28.3`](#docker283)
-	[`docker:28.3-cli`](#docker283-cli)
-	[`docker:28.3-dind`](#docker283-dind)
-	[`docker:28.3-dind-rootless`](#docker283-dind-rootless)
-	[`docker:28.3-windowsservercore`](#docker283-windowsservercore)
-	[`docker:28.3-windowsservercore-ltsc2022`](#docker283-windowsservercore-ltsc2022)
-	[`docker:28.3-windowsservercore-ltsc2025`](#docker283-windowsservercore-ltsc2025)
-	[`docker:28.3.3`](#docker2833)
-	[`docker:28.3.3-alpine3.22`](#docker2833-alpine322)
-	[`docker:28.3.3-cli`](#docker2833-cli)
-	[`docker:28.3.3-cli-alpine3.22`](#docker2833-cli-alpine322)
-	[`docker:28.3.3-dind`](#docker2833-dind)
-	[`docker:28.3.3-dind-alpine3.22`](#docker2833-dind-alpine322)
-	[`docker:28.3.3-dind-rootless`](#docker2833-dind-rootless)
-	[`docker:28.3.3-windowsservercore`](#docker2833-windowsservercore)
-	[`docker:28.3.3-windowsservercore-ltsc2022`](#docker2833-windowsservercore-ltsc2022)
-	[`docker:28.3.3-windowsservercore-ltsc2025`](#docker2833-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

```console
$ docker pull docker@sha256:c0872aae4791ff427e6eda52769afa04f17b5cf756f8267e0d52774c99d5c9de
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

### `docker:28` - linux; amd64

```console
$ docker pull docker@sha256:acf2e2d09cedf21fa8f27bb0962674e33e159c744c152b248f1f7f43623ccd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145400826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a8bf985f76be7345c0c827c568db287ccb4dfad919a4693488224e3644fb0c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8791499fa9bdef98d7e3a188725e48e8c8dba0180702d559340747beef3519c`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 6.9 MB (6905701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fadee7df1b34bce659502e94099411a4bcea4f3b4b5703acdea29f43f10435d`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 90.2 KB (90225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585c63523750cbc3e625b48e735c70327c58c50817730a4f0ccfa5bca404699a`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ef36d1f42ecc72cee33f9b3630df040c2b3c0129388095caa52aa65663b6b`  
		Last Modified: Tue, 29 Jul 2025 17:08:29 GMT  
		Size: 62.5 MB (62516136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa56a13dffa7d647581a8133c12b84570ac763f9c5a281a0762d56e2cf50c5`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae60b320044d4dddd57522c6c3ddcd806948664e3b77e4b4f3dfdbcbb154bb`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:b07ec0abd0eacbbb7a5caff69421dcf417d11e841cd6c39914c6350ec8ead6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3b72142c672a9277787f2a650dfe1c3d5ec96a77d3dfb1b30ee99fd35cfbbb`

```dockerfile
```

-	Layers:
	-	`sha256:810146a77372683cd7bd8b4e79c73015f3d7c76c01b681379c962de5166e83d5`  
		Last Modified: Tue, 29 Jul 2025 20:07:23 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:1f082418e60bfdc41615178f3338a57e008be9e54a0a088bdaf7639e6440aa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136481510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b903ce9efae22aff353f3b148f4b81543338dda7c191abe851759db185d55660`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f822c2573de7e9c67a5c71e3631064c5bcc0ea4209e1599a17c1acfeaaf1af`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 18.5 MB (18451848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd472c4b566302d5ccb09e4bc30d193d93f2127195f039fcc1e4c2e6384fd1`  
		Last Modified: Tue, 29 Jul 2025 16:50:49 GMT  
		Size: 20.6 MB (20568606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e39b3b275050311240d86f4184b92738124227ab91074f2d543353027e9ee`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 20.2 MB (20183248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fcfc43ab15c1da7e48f821e25c54c51d723b64684b20d2a4b4edff8e04dcc3`  
		Last Modified: Tue, 29 Jul 2025 16:50:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563338bb8fe09f3e62c3a07902962cba52ef8de211de1bda00ead94befe4d6c6`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d5bc334980f311595207402ce2300f8a11e1e71eb800bd573dcdfcbbb7383`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44f5f22ffde31d78b179f8cd7410f20820e06caf28efa9a65355c29b1e2b10b`  
		Last Modified: Thu, 07 Aug 2025 16:57:01 GMT  
		Size: 7.2 MB (7230142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebba53fb812598805b6fc21226a04919f3781430ba936808b0f59d133c00e80`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 89.8 KB (89806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e516ec65aa3324f86b97988d15e6abcbe2d2cd5aa91eaa93c11d0119f0016b85`  
		Last Modified: Thu, 07 Aug 2025 16:57:00 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036456d63ef0cf8b17f84e9d6b0243b01f469739b1a7f24cfe71c25d87b89496`  
		Last Modified: Thu, 07 Aug 2025 16:57:05 GMT  
		Size: 58.3 MB (58345094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909c6394356186a1784dad76416d85e70821a8a0efdf5b9bc6084f7f4cad6dbc`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2bfa6563e19d5b6bf2937e08f7af0eeeef31f1d0da970fbb37bdc678a99e81`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:caf190c0124eba00b01a8690ce7a05f806d0cf5ba34877fdf387e41444f3aeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b22a0c050d02e7164da7a016f4a9e2934ce69b7b45be19137f526a4c3cd0a4b`

```dockerfile
```

-	Layers:
	-	`sha256:c8c17618f747eab2415d91d988104c720915211836b105288567df5c8ca9f095`  
		Last Modified: Thu, 07 Aug 2025 17:07:28 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:0e5e5db93aa3e8af23c2189c2f949f41637e51178bf775ddff251f72743345f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134624627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a94d5bea77d233423c8ec637c7ec3d4ae66c22b1a4f9b58c44d6a5b9084ae0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fda06620cb3acbe8d29e62b35edf4eab73bd1796050a544bac974a28f5fd99`  
		Last Modified: Tue, 29 Jul 2025 17:13:20 GMT  
		Size: 18.4 MB (18441097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab513f15d8a635f59bcbe656922221d344bfc6c7d6c78e0b69a118c025c543b5`  
		Last Modified: Tue, 29 Jul 2025 17:13:21 GMT  
		Size: 20.5 MB (20548892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ff39cd4cd7f51997cb5ef915890dd813cd17afa5822471bc9fcf70b903121`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 20.2 MB (20166234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb6e886463cf3968d42871b95c8d48e815d647d699e9512783a2ef44fa0f64`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672297f80502d6989f94397992684d739879955ca812c635d7d02bbd1c82ba0`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269088758c4eb6e7275e58a86756108338d7e30a284edf53331fca7f4a88b0a5`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df050d7dc2c286cb6eb89f5f6074f0e2050b5647fac156e97e954bb586e0c977`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 6.5 MB (6538354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfde1691582119bdf48b4b13b8ec970dc7ea3fee792a9dcb2e806abbbb6939e`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 86.2 KB (86243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea99a75781859a140708f0f46a3c77bf434229b777a07580312f1f7051f87f50`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6cd3c5f53aed54fbcbdee772d968d063922cdb9ccaaf39af1ed46362650de`  
		Last Modified: Thu, 07 Aug 2025 14:58:09 GMT  
		Size: 58.2 MB (58186632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d193787930eddbb555cddea45342d37ec90697f6a1189dbe0103604b619f5ca`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfc61f65df60ef9b0388537e5876063cd37269cde97577fbb9cdc488230afe0`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:9c2557085ad68b5571b358134d36f2754b98a3ecb6882d6fd39a108e7180b090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522da17433e7ff04443725fdae9470d541ce7b230974c06928d9b00072a85a37`

```dockerfile
```

-	Layers:
	-	`sha256:67874486df4d385d50d3bcfc818bc8427ee8992e7228812841386fcb4f9dc903`  
		Last Modified: Thu, 07 Aug 2025 17:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:88bf2ba4673e2963049952ad60d46389e6d2be3d31f0f4d1d69c55e0712d22a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136102855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0680e652cec44e947fd5401c80526cad1e184420cc2645f6399d102127e5bbf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f90fb8179789820d09ee62a252a0b5d2007f1e6a0116dc93cef396028b74`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 7.1 MB (7140514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e7ada02315c507aa603b515c8af64560c37e3b0c3e1ae602c926a39f0e193`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 99.3 KB (99312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0bce22e68e3e822e795bdd12fcda8fe4d3374269c9031570e52e4989e30cc`  
		Last Modified: Tue, 29 Jul 2025 17:07:42 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94302614c7eb1b832998ebf0e2a380369fcc6c23e0fa4bab8669b02665af8558`  
		Last Modified: Tue, 29 Jul 2025 17:07:38 GMT  
		Size: 57.5 MB (57464791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6fb8714059d9cacf4db01465f092fa2bfbaebc073ecf76e620e3776406896`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d9a1a1a08782f599a9be2fe288ef0cbd4aa9a049d7b515137cf06ff00f2ba`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:9e688304c06587ce1c71a3409b301f476dc1fd9b67ee40cf659e180e174582d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878a9b4d22bd08a4e39e541ae7b4ca75ac8e62370ac53573fa18a05338573ec4`

```dockerfile
```

-	Layers:
	-	`sha256:e0a4c2285c0b8b2afc33b86867190ce402deccb8def5a4573f617737a1c16087`  
		Last Modified: Tue, 29 Jul 2025 20:07:33 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:d87c674b7f01043207f1badc6e86e1f8bc33a90981c2f31f3e0f57c1ecb0c5cc
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

### `docker:28-cli` - linux; amd64

```console
$ docker pull docker@sha256:e47e07b4616ad120a5e3812a315c0adb0a80d17eb19c979271dd3b16416226bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75882770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef97129ecf899446838ff807b2d675d8a1e30f2dac9af363534872b88f7b3def`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:019dbf214cb0eaa7943816f0cc580437ccae2ef546bf1bcff82e5b51ab2ca91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86120028f5d4320014588ac17e4563c14713f8a385d8e192c8229475f8ff6c35`

```dockerfile
```

-	Layers:
	-	`sha256:13645690d79e822200fb314c8947b0437ed272113942e70c5e93b9215ac0c449`  
		Last Modified: Tue, 29 Jul 2025 17:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:8f845ca7eb3d2dab949a1321d7ba195c8f690a89eb313190e35c32687d2a507b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70810451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b83d2189eeff2d9c339890963393fb464d80828d8b043a20894478fe3ffee1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f822c2573de7e9c67a5c71e3631064c5bcc0ea4209e1599a17c1acfeaaf1af`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 18.5 MB (18451848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd472c4b566302d5ccb09e4bc30d193d93f2127195f039fcc1e4c2e6384fd1`  
		Last Modified: Tue, 29 Jul 2025 16:50:49 GMT  
		Size: 20.6 MB (20568606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e39b3b275050311240d86f4184b92738124227ab91074f2d543353027e9ee`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 20.2 MB (20183248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fcfc43ab15c1da7e48f821e25c54c51d723b64684b20d2a4b4edff8e04dcc3`  
		Last Modified: Tue, 29 Jul 2025 16:50:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563338bb8fe09f3e62c3a07902962cba52ef8de211de1bda00ead94befe4d6c6`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d5bc334980f311595207402ce2300f8a11e1e71eb800bd573dcdfcbbb7383`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f1537ca07297772da32b2e246c50c1dea5ebad32ae760a9b9b7ccb94eaad29c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f65333c983620826c8527af4e58d432a3ee0ae31df3f9b51352442ccfdf7595`

```dockerfile
```

-	Layers:
	-	`sha256:b1609329088ee42b557625a4e309152f4ae582a5feb24069e6b4ac2a02371377`  
		Last Modified: Tue, 29 Jul 2025 17:07:26 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:c63fc02e3bb2c71c1e39d9618770900f16aeccddb8d13a517c16752f113a7fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69807384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c236c8ccc2e365a65223161398d002ebd5f6d7a8499070bd805ec062050a149f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fda06620cb3acbe8d29e62b35edf4eab73bd1796050a544bac974a28f5fd99`  
		Last Modified: Tue, 29 Jul 2025 17:13:20 GMT  
		Size: 18.4 MB (18441097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab513f15d8a635f59bcbe656922221d344bfc6c7d6c78e0b69a118c025c543b5`  
		Last Modified: Tue, 29 Jul 2025 17:13:21 GMT  
		Size: 20.5 MB (20548892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ff39cd4cd7f51997cb5ef915890dd813cd17afa5822471bc9fcf70b903121`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 20.2 MB (20166234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb6e886463cf3968d42871b95c8d48e815d647d699e9512783a2ef44fa0f64`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672297f80502d6989f94397992684d739879955ca812c635d7d02bbd1c82ba0`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269088758c4eb6e7275e58a86756108338d7e30a284edf53331fca7f4a88b0a5`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:324a1f85dda8d36fcd3250fec9cca2ed582c781a8c5ebfded37a04ac8840aa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82360f4e5611e16371e1b1bf406b68e64ff5640d3207b215c35251543cc4956`

```dockerfile
```

-	Layers:
	-	`sha256:3ffc99fef904d345817e2028615cef8ce8299be6c0754569973a322b26a2cad5`  
		Last Modified: Tue, 29 Jul 2025 20:07:33 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2b6312fd57e7b24ffae3ace014357496da75c7d3b7bd15455987364d5805999c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71392240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324b3c32e29caad939b212c3d18aa70ad98a23579154b2254f63b19284e09046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b00a03f6a893ff05072a6aec1f14baab706cadb23df8f3472eca7a730139ff6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c33d99fbb568b26e841daf1694e071995a07b8dd92bbc7c1414abe997adbc70`

```dockerfile
```

-	Layers:
	-	`sha256:278de4bd27c29d5f7783b8e9211f0b5596e91aab67d37d191bd0e5df0b2a41e9`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:c0872aae4791ff427e6eda52769afa04f17b5cf756f8267e0d52774c99d5c9de
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

### `docker:28-dind` - linux; amd64

```console
$ docker pull docker@sha256:acf2e2d09cedf21fa8f27bb0962674e33e159c744c152b248f1f7f43623ccd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145400826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a8bf985f76be7345c0c827c568db287ccb4dfad919a4693488224e3644fb0c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8791499fa9bdef98d7e3a188725e48e8c8dba0180702d559340747beef3519c`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 6.9 MB (6905701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fadee7df1b34bce659502e94099411a4bcea4f3b4b5703acdea29f43f10435d`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 90.2 KB (90225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585c63523750cbc3e625b48e735c70327c58c50817730a4f0ccfa5bca404699a`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ef36d1f42ecc72cee33f9b3630df040c2b3c0129388095caa52aa65663b6b`  
		Last Modified: Tue, 29 Jul 2025 17:08:29 GMT  
		Size: 62.5 MB (62516136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa56a13dffa7d647581a8133c12b84570ac763f9c5a281a0762d56e2cf50c5`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae60b320044d4dddd57522c6c3ddcd806948664e3b77e4b4f3dfdbcbb154bb`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b07ec0abd0eacbbb7a5caff69421dcf417d11e841cd6c39914c6350ec8ead6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3b72142c672a9277787f2a650dfe1c3d5ec96a77d3dfb1b30ee99fd35cfbbb`

```dockerfile
```

-	Layers:
	-	`sha256:810146a77372683cd7bd8b4e79c73015f3d7c76c01b681379c962de5166e83d5`  
		Last Modified: Tue, 29 Jul 2025 20:07:23 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1f082418e60bfdc41615178f3338a57e008be9e54a0a088bdaf7639e6440aa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136481510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b903ce9efae22aff353f3b148f4b81543338dda7c191abe851759db185d55660`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f822c2573de7e9c67a5c71e3631064c5bcc0ea4209e1599a17c1acfeaaf1af`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 18.5 MB (18451848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd472c4b566302d5ccb09e4bc30d193d93f2127195f039fcc1e4c2e6384fd1`  
		Last Modified: Tue, 29 Jul 2025 16:50:49 GMT  
		Size: 20.6 MB (20568606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e39b3b275050311240d86f4184b92738124227ab91074f2d543353027e9ee`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 20.2 MB (20183248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fcfc43ab15c1da7e48f821e25c54c51d723b64684b20d2a4b4edff8e04dcc3`  
		Last Modified: Tue, 29 Jul 2025 16:50:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563338bb8fe09f3e62c3a07902962cba52ef8de211de1bda00ead94befe4d6c6`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d5bc334980f311595207402ce2300f8a11e1e71eb800bd573dcdfcbbb7383`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44f5f22ffde31d78b179f8cd7410f20820e06caf28efa9a65355c29b1e2b10b`  
		Last Modified: Thu, 07 Aug 2025 16:57:01 GMT  
		Size: 7.2 MB (7230142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebba53fb812598805b6fc21226a04919f3781430ba936808b0f59d133c00e80`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 89.8 KB (89806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e516ec65aa3324f86b97988d15e6abcbe2d2cd5aa91eaa93c11d0119f0016b85`  
		Last Modified: Thu, 07 Aug 2025 16:57:00 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036456d63ef0cf8b17f84e9d6b0243b01f469739b1a7f24cfe71c25d87b89496`  
		Last Modified: Thu, 07 Aug 2025 16:57:05 GMT  
		Size: 58.3 MB (58345094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909c6394356186a1784dad76416d85e70821a8a0efdf5b9bc6084f7f4cad6dbc`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2bfa6563e19d5b6bf2937e08f7af0eeeef31f1d0da970fbb37bdc678a99e81`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:caf190c0124eba00b01a8690ce7a05f806d0cf5ba34877fdf387e41444f3aeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b22a0c050d02e7164da7a016f4a9e2934ce69b7b45be19137f526a4c3cd0a4b`

```dockerfile
```

-	Layers:
	-	`sha256:c8c17618f747eab2415d91d988104c720915211836b105288567df5c8ca9f095`  
		Last Modified: Thu, 07 Aug 2025 17:07:28 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:0e5e5db93aa3e8af23c2189c2f949f41637e51178bf775ddff251f72743345f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134624627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a94d5bea77d233423c8ec637c7ec3d4ae66c22b1a4f9b58c44d6a5b9084ae0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fda06620cb3acbe8d29e62b35edf4eab73bd1796050a544bac974a28f5fd99`  
		Last Modified: Tue, 29 Jul 2025 17:13:20 GMT  
		Size: 18.4 MB (18441097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab513f15d8a635f59bcbe656922221d344bfc6c7d6c78e0b69a118c025c543b5`  
		Last Modified: Tue, 29 Jul 2025 17:13:21 GMT  
		Size: 20.5 MB (20548892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ff39cd4cd7f51997cb5ef915890dd813cd17afa5822471bc9fcf70b903121`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 20.2 MB (20166234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb6e886463cf3968d42871b95c8d48e815d647d699e9512783a2ef44fa0f64`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672297f80502d6989f94397992684d739879955ca812c635d7d02bbd1c82ba0`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269088758c4eb6e7275e58a86756108338d7e30a284edf53331fca7f4a88b0a5`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df050d7dc2c286cb6eb89f5f6074f0e2050b5647fac156e97e954bb586e0c977`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 6.5 MB (6538354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfde1691582119bdf48b4b13b8ec970dc7ea3fee792a9dcb2e806abbbb6939e`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 86.2 KB (86243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea99a75781859a140708f0f46a3c77bf434229b777a07580312f1f7051f87f50`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6cd3c5f53aed54fbcbdee772d968d063922cdb9ccaaf39af1ed46362650de`  
		Last Modified: Thu, 07 Aug 2025 14:58:09 GMT  
		Size: 58.2 MB (58186632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d193787930eddbb555cddea45342d37ec90697f6a1189dbe0103604b619f5ca`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfc61f65df60ef9b0388537e5876063cd37269cde97577fbb9cdc488230afe0`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9c2557085ad68b5571b358134d36f2754b98a3ecb6882d6fd39a108e7180b090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522da17433e7ff04443725fdae9470d541ce7b230974c06928d9b00072a85a37`

```dockerfile
```

-	Layers:
	-	`sha256:67874486df4d385d50d3bcfc818bc8427ee8992e7228812841386fcb4f9dc903`  
		Last Modified: Thu, 07 Aug 2025 17:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:88bf2ba4673e2963049952ad60d46389e6d2be3d31f0f4d1d69c55e0712d22a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136102855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0680e652cec44e947fd5401c80526cad1e184420cc2645f6399d102127e5bbf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f90fb8179789820d09ee62a252a0b5d2007f1e6a0116dc93cef396028b74`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 7.1 MB (7140514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e7ada02315c507aa603b515c8af64560c37e3b0c3e1ae602c926a39f0e193`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 99.3 KB (99312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0bce22e68e3e822e795bdd12fcda8fe4d3374269c9031570e52e4989e30cc`  
		Last Modified: Tue, 29 Jul 2025 17:07:42 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94302614c7eb1b832998ebf0e2a380369fcc6c23e0fa4bab8669b02665af8558`  
		Last Modified: Tue, 29 Jul 2025 17:07:38 GMT  
		Size: 57.5 MB (57464791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6fb8714059d9cacf4db01465f092fa2bfbaebc073ecf76e620e3776406896`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d9a1a1a08782f599a9be2fe288ef0cbd4aa9a049d7b515137cf06ff00f2ba`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9e688304c06587ce1c71a3409b301f476dc1fd9b67ee40cf659e180e174582d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878a9b4d22bd08a4e39e541ae7b4ca75ac8e62370ac53573fa18a05338573ec4`

```dockerfile
```

-	Layers:
	-	`sha256:e0a4c2285c0b8b2afc33b86867190ce402deccb8def5a4573f617737a1c16087`  
		Last Modified: Tue, 29 Jul 2025 20:07:33 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:0fa4819d7978945b730c21fafb4b795bba05e486ceae04fbf1871a920082f2a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e039e40debc22c3cab8f5bee7f63b70c559c55b940f60a12dca61d2b9d28b096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166384612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e02ef5f5cabe9695528ed4a1d27d7c4ff5b08b682d29a752bf84acdb8150f9b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8791499fa9bdef98d7e3a188725e48e8c8dba0180702d559340747beef3519c`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 6.9 MB (6905701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fadee7df1b34bce659502e94099411a4bcea4f3b4b5703acdea29f43f10435d`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 90.2 KB (90225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585c63523750cbc3e625b48e735c70327c58c50817730a4f0ccfa5bca404699a`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ef36d1f42ecc72cee33f9b3630df040c2b3c0129388095caa52aa65663b6b`  
		Last Modified: Tue, 29 Jul 2025 17:08:29 GMT  
		Size: 62.5 MB (62516136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa56a13dffa7d647581a8133c12b84570ac763f9c5a281a0762d56e2cf50c5`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae60b320044d4dddd57522c6c3ddcd806948664e3b77e4b4f3dfdbcbb154bb`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3287871b8ca8572ddc7e051c61124c5d7b8d170b4afa30990972ecc32d2b1ece`  
		Last Modified: Tue, 29 Jul 2025 18:08:07 GMT  
		Size: 3.4 MB (3398338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c461874a9c04227f0bb239173b4ada58d4db9ae8822f866bf3869a0a112547`  
		Last Modified: Tue, 29 Jul 2025 18:08:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e93b4300a29b1f4578589daaa971b85425d6933fc13a844fad5d06e910ad23`  
		Last Modified: Tue, 29 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7016b5b02df5fdd9973630f913712193bc9276e47e3ac3eec14c29e694a4ff7`  
		Last Modified: Tue, 29 Jul 2025 18:08:10 GMT  
		Size: 17.6 MB (17584103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed2e953d4988003d64d426d269de70faa9c883a584158b5051029ea4f95a5cd`  
		Last Modified: Tue, 29 Jul 2025 18:08:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d3dd8c5f4e079aa9cc4a9deb31657fac070b425f2c95fc433839bd1fd9d1ff37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320768a07adb0a8b788d5f39c7d266fb5f45092252fa70bf78fa0767a653d068`

```dockerfile
```

-	Layers:
	-	`sha256:0222f5bf30363b640dfe6720d68d54f7f37a192fef439f4610ffae517243dc33`  
		Last Modified: Tue, 29 Jul 2025 20:07:40 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:412f7ef33b757bf61e5a858aee1d37534d091731e94701e1c0b3c448902c4f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157509962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6709bbcb068f2c6e78025d69110cc5eec100dda035be262877ece8e79dc47bf8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f90fb8179789820d09ee62a252a0b5d2007f1e6a0116dc93cef396028b74`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 7.1 MB (7140514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e7ada02315c507aa603b515c8af64560c37e3b0c3e1ae602c926a39f0e193`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 99.3 KB (99312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0bce22e68e3e822e795bdd12fcda8fe4d3374269c9031570e52e4989e30cc`  
		Last Modified: Tue, 29 Jul 2025 17:07:42 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94302614c7eb1b832998ebf0e2a380369fcc6c23e0fa4bab8669b02665af8558`  
		Last Modified: Tue, 29 Jul 2025 17:07:38 GMT  
		Size: 57.5 MB (57464791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6fb8714059d9cacf4db01465f092fa2bfbaebc073ecf76e620e3776406896`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d9a1a1a08782f599a9be2fe288ef0cbd4aa9a049d7b515137cf06ff00f2ba`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de9b74ceab4068500d9e2bd01dfbe28d9de34020baf094c75a035f0e91dfe1c`  
		Last Modified: Tue, 29 Jul 2025 18:46:21 GMT  
		Size: 3.4 MB (3389783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e12d9582745618468bfbb94957b902ef8680c42836cd87af3abf1575c781300`  
		Last Modified: Tue, 29 Jul 2025 18:07:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137bbfcf556b45f0503de2e6587e5b717626e5aa84a74c48aaf42e25dc3748cd`  
		Last Modified: Tue, 29 Jul 2025 18:07:16 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c805ba216a001613d2cdde121482c9dd36550a2e1ecd0ca969822c07c6531448`  
		Last Modified: Tue, 29 Jul 2025 18:07:17 GMT  
		Size: 18.0 MB (18015980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3570e64b17160d03028caf56f4281afdaa55b29f7ef12727e24e0f2eab4a94`  
		Last Modified: Tue, 29 Jul 2025 18:07:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:5eb8f2deebe35b46795fecf8b10896f8a18edb8d193d4c729422528a3d65dccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7798353e96b504dbfbcc6f16bb93a06387185b9fb064ccfa7cef1c08283dc9a5`

```dockerfile
```

-	Layers:
	-	`sha256:9bbdf146cca0e581ca098844347a2e1a7a0d50fe603ae68b979d28455fb9e345`  
		Last Modified: Tue, 29 Jul 2025 20:07:44 GMT  
		Size: 30.8 KB (30801 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:32d6e626f79e39b5cc83a10d4fcc2fd8f090cf2052298b7081c073d05d6788b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fce944f1be9964c27dffe70ea4e05f43906e5c35d7f1d1f319ea241e6ff7766b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565385109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e16746b5d96d8f01c428a46027b16342e56a3f351d9e94cc23c4884e182a23`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:26:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:27:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:06 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:27:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:27:16 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:27:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d49ded649af742ac4e8aff9b2beba88841a34f5ac3c9cad1b2cbbb85a8a1741`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4901ee3ae2f2d3da5d2455d57c8497cdcd54fa3981e3eced30f632522080c987`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 356.9 KB (356904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cce2887577005a99bc013670c90c46c419da33c604d06b159d5a10bf40d3cb`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d727c7396ced4e810c63f727df20e45e76ebd1775b108e32a902fac6b6478076`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcfd1f605909b895b191bbc1dce66175acc45a5add136bc5a0ae4f36ecd8989`  
		Last Modified: Tue, 12 Aug 2025 20:31:31 GMT  
		Size: 20.8 MB (20837962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e6ab5bf2d2d618100a885f27c393467212c0570eaa7ea84e6ea8219e5dc291`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b884b8cda3f7df7bffd4252d58e7d9152d914e0d920161dfc1b2bbf477829d45`  
		Last Modified: Tue, 12 Aug 2025 20:31:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7094f59558defd3124f897718f374e4c7adb853752582ba8e4f3684c14b3e16a`  
		Last Modified: Tue, 12 Aug 2025 20:31:14 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7051fc3fd3e4df1ca961e28ab2cd07384069c0c2872b4680f672075663b48034`  
		Last Modified: Tue, 12 Aug 2025 20:31:20 GMT  
		Size: 23.0 MB (22953510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a709cde7693b4592561374d3dddec696b50b1a107e69458552265acbbf21459e`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d45050aa1c7e9ea58879bcb46bbf075e263acc49748dcd9a19068713b52e59`  
		Last Modified: Tue, 12 Aug 2025 20:31:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31e15e6414199a0fa232b38e3b810fa3806c10634d77fbde8642407b62f90f1`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4abea89efff9a4dcaee678846541ee7471b0d5e13f11a1ffd50c601da438141`  
		Last Modified: Tue, 12 Aug 2025 20:31:21 GMT  
		Size: 22.4 MB (22394336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:b08584be840c5fffd7d99e62ab49eae4c3f6636a8843cce35a5bd1067720e0ab
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348189021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732e79d977df1d9edff845acd89fee0b2122dfd3500338862d0c073f12710e29`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:25:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:06 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:26:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:26:19 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:26:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:26:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:26:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:26:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37ee622e1d3856c0f56d0e073b50e34ad5239aa1e8a0d7b93f11fb38230099f`  
		Last Modified: Tue, 12 Aug 2025 20:28:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04848d212a98717392544afa4ddeeef71992d66bba2d6eef616660649835eece`  
		Last Modified: Tue, 12 Aug 2025 20:28:14 GMT  
		Size: 346.1 KB (346147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e3cc07ce8c5cb86d5dd9907546bc97af931be4eef1e23a908c40d2ab28a68`  
		Last Modified: Tue, 12 Aug 2025 20:51:41 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188521c2085d7c3dbbbae5485b4fc383b0516ff6e9a27a023df6aca63dbb7459`  
		Last Modified: Tue, 12 Aug 2025 20:51:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581d2a99a5e27e493c9517fcb5d27c165f5696ad1d8f08f568d60eee1e8d6fcc`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 20.8 MB (20826824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e88f9f3cb2e7be25dbdc4626eb3bcbc619924d0c61d64356d2d7a8e3fc4a661`  
		Last Modified: Tue, 12 Aug 2025 20:51:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70bf9f40001314e26858770cf903764c3dc5e0c1278e072fa7daf620846745`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6079589750abcc6d3eb81778c4a2837ea2dc0467112980d886173696e4c9df`  
		Last Modified: Tue, 12 Aug 2025 20:51:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65174c16d8c061f85019c62493afae8d5db2f56e1a831a94c02db515515626d`  
		Last Modified: Tue, 12 Aug 2025 20:51:50 GMT  
		Size: 22.9 MB (22937256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728f806f53c767bd20bb97653fa5b5e3016a8e4af213a950135d9105930ac520`  
		Last Modified: Tue, 12 Aug 2025 20:51:48 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b5ab841f285aa2a8a9238b3c57bede8d2a91a3763c0f584275508deefcbdf5`  
		Last Modified: Tue, 12 Aug 2025 20:51:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae017706cc10313aa38b24d9c7c4dc2901f7f1ea62598f22aa0639e40d14cba0`  
		Last Modified: Tue, 12 Aug 2025 20:51:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bac6b791dfaef6e7c36ef93b178cc273d730b229d9112ceadede006ad1bc0a6`  
		Last Modified: Tue, 12 Aug 2025 20:51:56 GMT  
		Size: 22.4 MB (22375244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:7a3b2e07b931434a99cd7f00343a6fd5b6a618598e9cc4746313aaca3de5aaa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:b08584be840c5fffd7d99e62ab49eae4c3f6636a8843cce35a5bd1067720e0ab
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348189021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732e79d977df1d9edff845acd89fee0b2122dfd3500338862d0c073f12710e29`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:25:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:06 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:26:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:26:19 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:26:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:26:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:26:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:26:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37ee622e1d3856c0f56d0e073b50e34ad5239aa1e8a0d7b93f11fb38230099f`  
		Last Modified: Tue, 12 Aug 2025 20:28:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04848d212a98717392544afa4ddeeef71992d66bba2d6eef616660649835eece`  
		Last Modified: Tue, 12 Aug 2025 20:28:14 GMT  
		Size: 346.1 KB (346147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e3cc07ce8c5cb86d5dd9907546bc97af931be4eef1e23a908c40d2ab28a68`  
		Last Modified: Tue, 12 Aug 2025 20:51:41 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188521c2085d7c3dbbbae5485b4fc383b0516ff6e9a27a023df6aca63dbb7459`  
		Last Modified: Tue, 12 Aug 2025 20:51:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581d2a99a5e27e493c9517fcb5d27c165f5696ad1d8f08f568d60eee1e8d6fcc`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 20.8 MB (20826824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e88f9f3cb2e7be25dbdc4626eb3bcbc619924d0c61d64356d2d7a8e3fc4a661`  
		Last Modified: Tue, 12 Aug 2025 20:51:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70bf9f40001314e26858770cf903764c3dc5e0c1278e072fa7daf620846745`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6079589750abcc6d3eb81778c4a2837ea2dc0467112980d886173696e4c9df`  
		Last Modified: Tue, 12 Aug 2025 20:51:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65174c16d8c061f85019c62493afae8d5db2f56e1a831a94c02db515515626d`  
		Last Modified: Tue, 12 Aug 2025 20:51:50 GMT  
		Size: 22.9 MB (22937256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728f806f53c767bd20bb97653fa5b5e3016a8e4af213a950135d9105930ac520`  
		Last Modified: Tue, 12 Aug 2025 20:51:48 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b5ab841f285aa2a8a9238b3c57bede8d2a91a3763c0f584275508deefcbdf5`  
		Last Modified: Tue, 12 Aug 2025 20:51:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae017706cc10313aa38b24d9c7c4dc2901f7f1ea62598f22aa0639e40d14cba0`  
		Last Modified: Tue, 12 Aug 2025 20:51:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bac6b791dfaef6e7c36ef93b178cc273d730b229d9112ceadede006ad1bc0a6`  
		Last Modified: Tue, 12 Aug 2025 20:51:56 GMT  
		Size: 22.4 MB (22375244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a188802ccb2fc99331e286bf343b9ad5721c2fcf498565d8a6990f9642e3f046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fce944f1be9964c27dffe70ea4e05f43906e5c35d7f1d1f319ea241e6ff7766b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565385109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e16746b5d96d8f01c428a46027b16342e56a3f351d9e94cc23c4884e182a23`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:26:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:27:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:06 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:27:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:27:16 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:27:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d49ded649af742ac4e8aff9b2beba88841a34f5ac3c9cad1b2cbbb85a8a1741`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4901ee3ae2f2d3da5d2455d57c8497cdcd54fa3981e3eced30f632522080c987`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 356.9 KB (356904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cce2887577005a99bc013670c90c46c419da33c604d06b159d5a10bf40d3cb`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d727c7396ced4e810c63f727df20e45e76ebd1775b108e32a902fac6b6478076`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcfd1f605909b895b191bbc1dce66175acc45a5add136bc5a0ae4f36ecd8989`  
		Last Modified: Tue, 12 Aug 2025 20:31:31 GMT  
		Size: 20.8 MB (20837962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e6ab5bf2d2d618100a885f27c393467212c0570eaa7ea84e6ea8219e5dc291`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b884b8cda3f7df7bffd4252d58e7d9152d914e0d920161dfc1b2bbf477829d45`  
		Last Modified: Tue, 12 Aug 2025 20:31:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7094f59558defd3124f897718f374e4c7adb853752582ba8e4f3684c14b3e16a`  
		Last Modified: Tue, 12 Aug 2025 20:31:14 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7051fc3fd3e4df1ca961e28ab2cd07384069c0c2872b4680f672075663b48034`  
		Last Modified: Tue, 12 Aug 2025 20:31:20 GMT  
		Size: 23.0 MB (22953510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a709cde7693b4592561374d3dddec696b50b1a107e69458552265acbbf21459e`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d45050aa1c7e9ea58879bcb46bbf075e263acc49748dcd9a19068713b52e59`  
		Last Modified: Tue, 12 Aug 2025 20:31:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31e15e6414199a0fa232b38e3b810fa3806c10634d77fbde8642407b62f90f1`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4abea89efff9a4dcaee678846541ee7471b0d5e13f11a1ffd50c601da438141`  
		Last Modified: Tue, 12 Aug 2025 20:31:21 GMT  
		Size: 22.4 MB (22394336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3`

```console
$ docker pull docker@sha256:c0872aae4791ff427e6eda52769afa04f17b5cf756f8267e0d52774c99d5c9de
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

### `docker:28.3` - linux; amd64

```console
$ docker pull docker@sha256:acf2e2d09cedf21fa8f27bb0962674e33e159c744c152b248f1f7f43623ccd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145400826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a8bf985f76be7345c0c827c568db287ccb4dfad919a4693488224e3644fb0c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8791499fa9bdef98d7e3a188725e48e8c8dba0180702d559340747beef3519c`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 6.9 MB (6905701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fadee7df1b34bce659502e94099411a4bcea4f3b4b5703acdea29f43f10435d`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 90.2 KB (90225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585c63523750cbc3e625b48e735c70327c58c50817730a4f0ccfa5bca404699a`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ef36d1f42ecc72cee33f9b3630df040c2b3c0129388095caa52aa65663b6b`  
		Last Modified: Tue, 29 Jul 2025 17:08:29 GMT  
		Size: 62.5 MB (62516136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa56a13dffa7d647581a8133c12b84570ac763f9c5a281a0762d56e2cf50c5`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae60b320044d4dddd57522c6c3ddcd806948664e3b77e4b4f3dfdbcbb154bb`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:b07ec0abd0eacbbb7a5caff69421dcf417d11e841cd6c39914c6350ec8ead6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3b72142c672a9277787f2a650dfe1c3d5ec96a77d3dfb1b30ee99fd35cfbbb`

```dockerfile
```

-	Layers:
	-	`sha256:810146a77372683cd7bd8b4e79c73015f3d7c76c01b681379c962de5166e83d5`  
		Last Modified: Tue, 29 Jul 2025 20:07:23 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3` - linux; arm variant v6

```console
$ docker pull docker@sha256:1f082418e60bfdc41615178f3338a57e008be9e54a0a088bdaf7639e6440aa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136481510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b903ce9efae22aff353f3b148f4b81543338dda7c191abe851759db185d55660`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f822c2573de7e9c67a5c71e3631064c5bcc0ea4209e1599a17c1acfeaaf1af`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 18.5 MB (18451848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd472c4b566302d5ccb09e4bc30d193d93f2127195f039fcc1e4c2e6384fd1`  
		Last Modified: Tue, 29 Jul 2025 16:50:49 GMT  
		Size: 20.6 MB (20568606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e39b3b275050311240d86f4184b92738124227ab91074f2d543353027e9ee`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 20.2 MB (20183248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fcfc43ab15c1da7e48f821e25c54c51d723b64684b20d2a4b4edff8e04dcc3`  
		Last Modified: Tue, 29 Jul 2025 16:50:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563338bb8fe09f3e62c3a07902962cba52ef8de211de1bda00ead94befe4d6c6`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d5bc334980f311595207402ce2300f8a11e1e71eb800bd573dcdfcbbb7383`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44f5f22ffde31d78b179f8cd7410f20820e06caf28efa9a65355c29b1e2b10b`  
		Last Modified: Thu, 07 Aug 2025 16:57:01 GMT  
		Size: 7.2 MB (7230142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebba53fb812598805b6fc21226a04919f3781430ba936808b0f59d133c00e80`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 89.8 KB (89806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e516ec65aa3324f86b97988d15e6abcbe2d2cd5aa91eaa93c11d0119f0016b85`  
		Last Modified: Thu, 07 Aug 2025 16:57:00 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036456d63ef0cf8b17f84e9d6b0243b01f469739b1a7f24cfe71c25d87b89496`  
		Last Modified: Thu, 07 Aug 2025 16:57:05 GMT  
		Size: 58.3 MB (58345094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909c6394356186a1784dad76416d85e70821a8a0efdf5b9bc6084f7f4cad6dbc`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2bfa6563e19d5b6bf2937e08f7af0eeeef31f1d0da970fbb37bdc678a99e81`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:caf190c0124eba00b01a8690ce7a05f806d0cf5ba34877fdf387e41444f3aeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b22a0c050d02e7164da7a016f4a9e2934ce69b7b45be19137f526a4c3cd0a4b`

```dockerfile
```

-	Layers:
	-	`sha256:c8c17618f747eab2415d91d988104c720915211836b105288567df5c8ca9f095`  
		Last Modified: Thu, 07 Aug 2025 17:07:28 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3` - linux; arm variant v7

```console
$ docker pull docker@sha256:0e5e5db93aa3e8af23c2189c2f949f41637e51178bf775ddff251f72743345f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134624627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a94d5bea77d233423c8ec637c7ec3d4ae66c22b1a4f9b58c44d6a5b9084ae0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fda06620cb3acbe8d29e62b35edf4eab73bd1796050a544bac974a28f5fd99`  
		Last Modified: Tue, 29 Jul 2025 17:13:20 GMT  
		Size: 18.4 MB (18441097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab513f15d8a635f59bcbe656922221d344bfc6c7d6c78e0b69a118c025c543b5`  
		Last Modified: Tue, 29 Jul 2025 17:13:21 GMT  
		Size: 20.5 MB (20548892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ff39cd4cd7f51997cb5ef915890dd813cd17afa5822471bc9fcf70b903121`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 20.2 MB (20166234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb6e886463cf3968d42871b95c8d48e815d647d699e9512783a2ef44fa0f64`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672297f80502d6989f94397992684d739879955ca812c635d7d02bbd1c82ba0`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269088758c4eb6e7275e58a86756108338d7e30a284edf53331fca7f4a88b0a5`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df050d7dc2c286cb6eb89f5f6074f0e2050b5647fac156e97e954bb586e0c977`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 6.5 MB (6538354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfde1691582119bdf48b4b13b8ec970dc7ea3fee792a9dcb2e806abbbb6939e`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 86.2 KB (86243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea99a75781859a140708f0f46a3c77bf434229b777a07580312f1f7051f87f50`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6cd3c5f53aed54fbcbdee772d968d063922cdb9ccaaf39af1ed46362650de`  
		Last Modified: Thu, 07 Aug 2025 14:58:09 GMT  
		Size: 58.2 MB (58186632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d193787930eddbb555cddea45342d37ec90697f6a1189dbe0103604b619f5ca`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfc61f65df60ef9b0388537e5876063cd37269cde97577fbb9cdc488230afe0`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:9c2557085ad68b5571b358134d36f2754b98a3ecb6882d6fd39a108e7180b090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522da17433e7ff04443725fdae9470d541ce7b230974c06928d9b00072a85a37`

```dockerfile
```

-	Layers:
	-	`sha256:67874486df4d385d50d3bcfc818bc8427ee8992e7228812841386fcb4f9dc903`  
		Last Modified: Thu, 07 Aug 2025 17:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:88bf2ba4673e2963049952ad60d46389e6d2be3d31f0f4d1d69c55e0712d22a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136102855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0680e652cec44e947fd5401c80526cad1e184420cc2645f6399d102127e5bbf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f90fb8179789820d09ee62a252a0b5d2007f1e6a0116dc93cef396028b74`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 7.1 MB (7140514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e7ada02315c507aa603b515c8af64560c37e3b0c3e1ae602c926a39f0e193`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 99.3 KB (99312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0bce22e68e3e822e795bdd12fcda8fe4d3374269c9031570e52e4989e30cc`  
		Last Modified: Tue, 29 Jul 2025 17:07:42 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94302614c7eb1b832998ebf0e2a380369fcc6c23e0fa4bab8669b02665af8558`  
		Last Modified: Tue, 29 Jul 2025 17:07:38 GMT  
		Size: 57.5 MB (57464791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6fb8714059d9cacf4db01465f092fa2bfbaebc073ecf76e620e3776406896`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d9a1a1a08782f599a9be2fe288ef0cbd4aa9a049d7b515137cf06ff00f2ba`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:9e688304c06587ce1c71a3409b301f476dc1fd9b67ee40cf659e180e174582d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878a9b4d22bd08a4e39e541ae7b4ca75ac8e62370ac53573fa18a05338573ec4`

```dockerfile
```

-	Layers:
	-	`sha256:e0a4c2285c0b8b2afc33b86867190ce402deccb8def5a4573f617737a1c16087`  
		Last Modified: Tue, 29 Jul 2025 20:07:33 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-cli`

```console
$ docker pull docker@sha256:d87c674b7f01043207f1badc6e86e1f8bc33a90981c2f31f3e0f57c1ecb0c5cc
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

### `docker:28.3-cli` - linux; amd64

```console
$ docker pull docker@sha256:e47e07b4616ad120a5e3812a315c0adb0a80d17eb19c979271dd3b16416226bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75882770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef97129ecf899446838ff807b2d675d8a1e30f2dac9af363534872b88f7b3def`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:019dbf214cb0eaa7943816f0cc580437ccae2ef546bf1bcff82e5b51ab2ca91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86120028f5d4320014588ac17e4563c14713f8a385d8e192c8229475f8ff6c35`

```dockerfile
```

-	Layers:
	-	`sha256:13645690d79e822200fb314c8947b0437ed272113942e70c5e93b9215ac0c449`  
		Last Modified: Tue, 29 Jul 2025 17:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:8f845ca7eb3d2dab949a1321d7ba195c8f690a89eb313190e35c32687d2a507b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70810451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b83d2189eeff2d9c339890963393fb464d80828d8b043a20894478fe3ffee1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f822c2573de7e9c67a5c71e3631064c5bcc0ea4209e1599a17c1acfeaaf1af`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 18.5 MB (18451848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd472c4b566302d5ccb09e4bc30d193d93f2127195f039fcc1e4c2e6384fd1`  
		Last Modified: Tue, 29 Jul 2025 16:50:49 GMT  
		Size: 20.6 MB (20568606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e39b3b275050311240d86f4184b92738124227ab91074f2d543353027e9ee`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 20.2 MB (20183248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fcfc43ab15c1da7e48f821e25c54c51d723b64684b20d2a4b4edff8e04dcc3`  
		Last Modified: Tue, 29 Jul 2025 16:50:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563338bb8fe09f3e62c3a07902962cba52ef8de211de1bda00ead94befe4d6c6`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d5bc334980f311595207402ce2300f8a11e1e71eb800bd573dcdfcbbb7383`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f1537ca07297772da32b2e246c50c1dea5ebad32ae760a9b9b7ccb94eaad29c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f65333c983620826c8527af4e58d432a3ee0ae31df3f9b51352442ccfdf7595`

```dockerfile
```

-	Layers:
	-	`sha256:b1609329088ee42b557625a4e309152f4ae582a5feb24069e6b4ac2a02371377`  
		Last Modified: Tue, 29 Jul 2025 17:07:26 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:c63fc02e3bb2c71c1e39d9618770900f16aeccddb8d13a517c16752f113a7fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69807384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c236c8ccc2e365a65223161398d002ebd5f6d7a8499070bd805ec062050a149f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fda06620cb3acbe8d29e62b35edf4eab73bd1796050a544bac974a28f5fd99`  
		Last Modified: Tue, 29 Jul 2025 17:13:20 GMT  
		Size: 18.4 MB (18441097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab513f15d8a635f59bcbe656922221d344bfc6c7d6c78e0b69a118c025c543b5`  
		Last Modified: Tue, 29 Jul 2025 17:13:21 GMT  
		Size: 20.5 MB (20548892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ff39cd4cd7f51997cb5ef915890dd813cd17afa5822471bc9fcf70b903121`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 20.2 MB (20166234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb6e886463cf3968d42871b95c8d48e815d647d699e9512783a2ef44fa0f64`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672297f80502d6989f94397992684d739879955ca812c635d7d02bbd1c82ba0`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269088758c4eb6e7275e58a86756108338d7e30a284edf53331fca7f4a88b0a5`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:324a1f85dda8d36fcd3250fec9cca2ed582c781a8c5ebfded37a04ac8840aa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82360f4e5611e16371e1b1bf406b68e64ff5640d3207b215c35251543cc4956`

```dockerfile
```

-	Layers:
	-	`sha256:3ffc99fef904d345817e2028615cef8ce8299be6c0754569973a322b26a2cad5`  
		Last Modified: Tue, 29 Jul 2025 20:07:33 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2b6312fd57e7b24ffae3ace014357496da75c7d3b7bd15455987364d5805999c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71392240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324b3c32e29caad939b212c3d18aa70ad98a23579154b2254f63b19284e09046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b00a03f6a893ff05072a6aec1f14baab706cadb23df8f3472eca7a730139ff6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c33d99fbb568b26e841daf1694e071995a07b8dd92bbc7c1414abe997adbc70`

```dockerfile
```

-	Layers:
	-	`sha256:278de4bd27c29d5f7783b8e9211f0b5596e91aab67d37d191bd0e5df0b2a41e9`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-dind`

```console
$ docker pull docker@sha256:c0872aae4791ff427e6eda52769afa04f17b5cf756f8267e0d52774c99d5c9de
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

### `docker:28.3-dind` - linux; amd64

```console
$ docker pull docker@sha256:acf2e2d09cedf21fa8f27bb0962674e33e159c744c152b248f1f7f43623ccd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145400826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a8bf985f76be7345c0c827c568db287ccb4dfad919a4693488224e3644fb0c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8791499fa9bdef98d7e3a188725e48e8c8dba0180702d559340747beef3519c`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 6.9 MB (6905701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fadee7df1b34bce659502e94099411a4bcea4f3b4b5703acdea29f43f10435d`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 90.2 KB (90225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585c63523750cbc3e625b48e735c70327c58c50817730a4f0ccfa5bca404699a`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ef36d1f42ecc72cee33f9b3630df040c2b3c0129388095caa52aa65663b6b`  
		Last Modified: Tue, 29 Jul 2025 17:08:29 GMT  
		Size: 62.5 MB (62516136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa56a13dffa7d647581a8133c12b84570ac763f9c5a281a0762d56e2cf50c5`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae60b320044d4dddd57522c6c3ddcd806948664e3b77e4b4f3dfdbcbb154bb`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b07ec0abd0eacbbb7a5caff69421dcf417d11e841cd6c39914c6350ec8ead6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3b72142c672a9277787f2a650dfe1c3d5ec96a77d3dfb1b30ee99fd35cfbbb`

```dockerfile
```

-	Layers:
	-	`sha256:810146a77372683cd7bd8b4e79c73015f3d7c76c01b681379c962de5166e83d5`  
		Last Modified: Tue, 29 Jul 2025 20:07:23 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1f082418e60bfdc41615178f3338a57e008be9e54a0a088bdaf7639e6440aa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136481510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b903ce9efae22aff353f3b148f4b81543338dda7c191abe851759db185d55660`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f822c2573de7e9c67a5c71e3631064c5bcc0ea4209e1599a17c1acfeaaf1af`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 18.5 MB (18451848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd472c4b566302d5ccb09e4bc30d193d93f2127195f039fcc1e4c2e6384fd1`  
		Last Modified: Tue, 29 Jul 2025 16:50:49 GMT  
		Size: 20.6 MB (20568606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e39b3b275050311240d86f4184b92738124227ab91074f2d543353027e9ee`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 20.2 MB (20183248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fcfc43ab15c1da7e48f821e25c54c51d723b64684b20d2a4b4edff8e04dcc3`  
		Last Modified: Tue, 29 Jul 2025 16:50:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563338bb8fe09f3e62c3a07902962cba52ef8de211de1bda00ead94befe4d6c6`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d5bc334980f311595207402ce2300f8a11e1e71eb800bd573dcdfcbbb7383`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44f5f22ffde31d78b179f8cd7410f20820e06caf28efa9a65355c29b1e2b10b`  
		Last Modified: Thu, 07 Aug 2025 16:57:01 GMT  
		Size: 7.2 MB (7230142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebba53fb812598805b6fc21226a04919f3781430ba936808b0f59d133c00e80`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 89.8 KB (89806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e516ec65aa3324f86b97988d15e6abcbe2d2cd5aa91eaa93c11d0119f0016b85`  
		Last Modified: Thu, 07 Aug 2025 16:57:00 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036456d63ef0cf8b17f84e9d6b0243b01f469739b1a7f24cfe71c25d87b89496`  
		Last Modified: Thu, 07 Aug 2025 16:57:05 GMT  
		Size: 58.3 MB (58345094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909c6394356186a1784dad76416d85e70821a8a0efdf5b9bc6084f7f4cad6dbc`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2bfa6563e19d5b6bf2937e08f7af0eeeef31f1d0da970fbb37bdc678a99e81`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:caf190c0124eba00b01a8690ce7a05f806d0cf5ba34877fdf387e41444f3aeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b22a0c050d02e7164da7a016f4a9e2934ce69b7b45be19137f526a4c3cd0a4b`

```dockerfile
```

-	Layers:
	-	`sha256:c8c17618f747eab2415d91d988104c720915211836b105288567df5c8ca9f095`  
		Last Modified: Thu, 07 Aug 2025 17:07:28 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:0e5e5db93aa3e8af23c2189c2f949f41637e51178bf775ddff251f72743345f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134624627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a94d5bea77d233423c8ec637c7ec3d4ae66c22b1a4f9b58c44d6a5b9084ae0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fda06620cb3acbe8d29e62b35edf4eab73bd1796050a544bac974a28f5fd99`  
		Last Modified: Tue, 29 Jul 2025 17:13:20 GMT  
		Size: 18.4 MB (18441097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab513f15d8a635f59bcbe656922221d344bfc6c7d6c78e0b69a118c025c543b5`  
		Last Modified: Tue, 29 Jul 2025 17:13:21 GMT  
		Size: 20.5 MB (20548892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ff39cd4cd7f51997cb5ef915890dd813cd17afa5822471bc9fcf70b903121`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 20.2 MB (20166234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb6e886463cf3968d42871b95c8d48e815d647d699e9512783a2ef44fa0f64`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672297f80502d6989f94397992684d739879955ca812c635d7d02bbd1c82ba0`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269088758c4eb6e7275e58a86756108338d7e30a284edf53331fca7f4a88b0a5`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df050d7dc2c286cb6eb89f5f6074f0e2050b5647fac156e97e954bb586e0c977`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 6.5 MB (6538354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfde1691582119bdf48b4b13b8ec970dc7ea3fee792a9dcb2e806abbbb6939e`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 86.2 KB (86243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea99a75781859a140708f0f46a3c77bf434229b777a07580312f1f7051f87f50`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6cd3c5f53aed54fbcbdee772d968d063922cdb9ccaaf39af1ed46362650de`  
		Last Modified: Thu, 07 Aug 2025 14:58:09 GMT  
		Size: 58.2 MB (58186632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d193787930eddbb555cddea45342d37ec90697f6a1189dbe0103604b619f5ca`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfc61f65df60ef9b0388537e5876063cd37269cde97577fbb9cdc488230afe0`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9c2557085ad68b5571b358134d36f2754b98a3ecb6882d6fd39a108e7180b090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522da17433e7ff04443725fdae9470d541ce7b230974c06928d9b00072a85a37`

```dockerfile
```

-	Layers:
	-	`sha256:67874486df4d385d50d3bcfc818bc8427ee8992e7228812841386fcb4f9dc903`  
		Last Modified: Thu, 07 Aug 2025 17:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:88bf2ba4673e2963049952ad60d46389e6d2be3d31f0f4d1d69c55e0712d22a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136102855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0680e652cec44e947fd5401c80526cad1e184420cc2645f6399d102127e5bbf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f90fb8179789820d09ee62a252a0b5d2007f1e6a0116dc93cef396028b74`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 7.1 MB (7140514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e7ada02315c507aa603b515c8af64560c37e3b0c3e1ae602c926a39f0e193`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 99.3 KB (99312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0bce22e68e3e822e795bdd12fcda8fe4d3374269c9031570e52e4989e30cc`  
		Last Modified: Tue, 29 Jul 2025 17:07:42 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94302614c7eb1b832998ebf0e2a380369fcc6c23e0fa4bab8669b02665af8558`  
		Last Modified: Tue, 29 Jul 2025 17:07:38 GMT  
		Size: 57.5 MB (57464791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6fb8714059d9cacf4db01465f092fa2bfbaebc073ecf76e620e3776406896`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d9a1a1a08782f599a9be2fe288ef0cbd4aa9a049d7b515137cf06ff00f2ba`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9e688304c06587ce1c71a3409b301f476dc1fd9b67ee40cf659e180e174582d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878a9b4d22bd08a4e39e541ae7b4ca75ac8e62370ac53573fa18a05338573ec4`

```dockerfile
```

-	Layers:
	-	`sha256:e0a4c2285c0b8b2afc33b86867190ce402deccb8def5a4573f617737a1c16087`  
		Last Modified: Tue, 29 Jul 2025 20:07:33 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-dind-rootless`

```console
$ docker pull docker@sha256:0fa4819d7978945b730c21fafb4b795bba05e486ceae04fbf1871a920082f2a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.3-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e039e40debc22c3cab8f5bee7f63b70c559c55b940f60a12dca61d2b9d28b096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166384612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e02ef5f5cabe9695528ed4a1d27d7c4ff5b08b682d29a752bf84acdb8150f9b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8791499fa9bdef98d7e3a188725e48e8c8dba0180702d559340747beef3519c`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 6.9 MB (6905701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fadee7df1b34bce659502e94099411a4bcea4f3b4b5703acdea29f43f10435d`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 90.2 KB (90225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585c63523750cbc3e625b48e735c70327c58c50817730a4f0ccfa5bca404699a`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ef36d1f42ecc72cee33f9b3630df040c2b3c0129388095caa52aa65663b6b`  
		Last Modified: Tue, 29 Jul 2025 17:08:29 GMT  
		Size: 62.5 MB (62516136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa56a13dffa7d647581a8133c12b84570ac763f9c5a281a0762d56e2cf50c5`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae60b320044d4dddd57522c6c3ddcd806948664e3b77e4b4f3dfdbcbb154bb`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3287871b8ca8572ddc7e051c61124c5d7b8d170b4afa30990972ecc32d2b1ece`  
		Last Modified: Tue, 29 Jul 2025 18:08:07 GMT  
		Size: 3.4 MB (3398338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c461874a9c04227f0bb239173b4ada58d4db9ae8822f866bf3869a0a112547`  
		Last Modified: Tue, 29 Jul 2025 18:08:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e93b4300a29b1f4578589daaa971b85425d6933fc13a844fad5d06e910ad23`  
		Last Modified: Tue, 29 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7016b5b02df5fdd9973630f913712193bc9276e47e3ac3eec14c29e694a4ff7`  
		Last Modified: Tue, 29 Jul 2025 18:08:10 GMT  
		Size: 17.6 MB (17584103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed2e953d4988003d64d426d269de70faa9c883a584158b5051029ea4f95a5cd`  
		Last Modified: Tue, 29 Jul 2025 18:08:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d3dd8c5f4e079aa9cc4a9deb31657fac070b425f2c95fc433839bd1fd9d1ff37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320768a07adb0a8b788d5f39c7d266fb5f45092252fa70bf78fa0767a653d068`

```dockerfile
```

-	Layers:
	-	`sha256:0222f5bf30363b640dfe6720d68d54f7f37a192fef439f4610ffae517243dc33`  
		Last Modified: Tue, 29 Jul 2025 20:07:40 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:412f7ef33b757bf61e5a858aee1d37534d091731e94701e1c0b3c448902c4f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157509962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6709bbcb068f2c6e78025d69110cc5eec100dda035be262877ece8e79dc47bf8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f90fb8179789820d09ee62a252a0b5d2007f1e6a0116dc93cef396028b74`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 7.1 MB (7140514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e7ada02315c507aa603b515c8af64560c37e3b0c3e1ae602c926a39f0e193`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 99.3 KB (99312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0bce22e68e3e822e795bdd12fcda8fe4d3374269c9031570e52e4989e30cc`  
		Last Modified: Tue, 29 Jul 2025 17:07:42 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94302614c7eb1b832998ebf0e2a380369fcc6c23e0fa4bab8669b02665af8558`  
		Last Modified: Tue, 29 Jul 2025 17:07:38 GMT  
		Size: 57.5 MB (57464791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6fb8714059d9cacf4db01465f092fa2bfbaebc073ecf76e620e3776406896`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d9a1a1a08782f599a9be2fe288ef0cbd4aa9a049d7b515137cf06ff00f2ba`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de9b74ceab4068500d9e2bd01dfbe28d9de34020baf094c75a035f0e91dfe1c`  
		Last Modified: Tue, 29 Jul 2025 18:46:21 GMT  
		Size: 3.4 MB (3389783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e12d9582745618468bfbb94957b902ef8680c42836cd87af3abf1575c781300`  
		Last Modified: Tue, 29 Jul 2025 18:07:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137bbfcf556b45f0503de2e6587e5b717626e5aa84a74c48aaf42e25dc3748cd`  
		Last Modified: Tue, 29 Jul 2025 18:07:16 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c805ba216a001613d2cdde121482c9dd36550a2e1ecd0ca969822c07c6531448`  
		Last Modified: Tue, 29 Jul 2025 18:07:17 GMT  
		Size: 18.0 MB (18015980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3570e64b17160d03028caf56f4281afdaa55b29f7ef12727e24e0f2eab4a94`  
		Last Modified: Tue, 29 Jul 2025 18:07:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:5eb8f2deebe35b46795fecf8b10896f8a18edb8d193d4c729422528a3d65dccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7798353e96b504dbfbcc6f16bb93a06387185b9fb064ccfa7cef1c08283dc9a5`

```dockerfile
```

-	Layers:
	-	`sha256:9bbdf146cca0e581ca098844347a2e1a7a0d50fe603ae68b979d28455fb9e345`  
		Last Modified: Tue, 29 Jul 2025 20:07:44 GMT  
		Size: 30.8 KB (30801 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-windowsservercore`

```console
$ docker pull docker@sha256:32d6e626f79e39b5cc83a10d4fcc2fd8f090cf2052298b7081c073d05d6788b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `docker:28.3-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fce944f1be9964c27dffe70ea4e05f43906e5c35d7f1d1f319ea241e6ff7766b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565385109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e16746b5d96d8f01c428a46027b16342e56a3f351d9e94cc23c4884e182a23`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:26:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:27:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:06 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:27:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:27:16 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:27:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d49ded649af742ac4e8aff9b2beba88841a34f5ac3c9cad1b2cbbb85a8a1741`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4901ee3ae2f2d3da5d2455d57c8497cdcd54fa3981e3eced30f632522080c987`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 356.9 KB (356904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cce2887577005a99bc013670c90c46c419da33c604d06b159d5a10bf40d3cb`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d727c7396ced4e810c63f727df20e45e76ebd1775b108e32a902fac6b6478076`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcfd1f605909b895b191bbc1dce66175acc45a5add136bc5a0ae4f36ecd8989`  
		Last Modified: Tue, 12 Aug 2025 20:31:31 GMT  
		Size: 20.8 MB (20837962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e6ab5bf2d2d618100a885f27c393467212c0570eaa7ea84e6ea8219e5dc291`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b884b8cda3f7df7bffd4252d58e7d9152d914e0d920161dfc1b2bbf477829d45`  
		Last Modified: Tue, 12 Aug 2025 20:31:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7094f59558defd3124f897718f374e4c7adb853752582ba8e4f3684c14b3e16a`  
		Last Modified: Tue, 12 Aug 2025 20:31:14 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7051fc3fd3e4df1ca961e28ab2cd07384069c0c2872b4680f672075663b48034`  
		Last Modified: Tue, 12 Aug 2025 20:31:20 GMT  
		Size: 23.0 MB (22953510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a709cde7693b4592561374d3dddec696b50b1a107e69458552265acbbf21459e`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d45050aa1c7e9ea58879bcb46bbf075e263acc49748dcd9a19068713b52e59`  
		Last Modified: Tue, 12 Aug 2025 20:31:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31e15e6414199a0fa232b38e3b810fa3806c10634d77fbde8642407b62f90f1`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4abea89efff9a4dcaee678846541ee7471b0d5e13f11a1ffd50c601da438141`  
		Last Modified: Tue, 12 Aug 2025 20:31:21 GMT  
		Size: 22.4 MB (22394336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.3-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:b08584be840c5fffd7d99e62ab49eae4c3f6636a8843cce35a5bd1067720e0ab
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348189021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732e79d977df1d9edff845acd89fee0b2122dfd3500338862d0c073f12710e29`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:25:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:06 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:26:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:26:19 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:26:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:26:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:26:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:26:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37ee622e1d3856c0f56d0e073b50e34ad5239aa1e8a0d7b93f11fb38230099f`  
		Last Modified: Tue, 12 Aug 2025 20:28:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04848d212a98717392544afa4ddeeef71992d66bba2d6eef616660649835eece`  
		Last Modified: Tue, 12 Aug 2025 20:28:14 GMT  
		Size: 346.1 KB (346147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e3cc07ce8c5cb86d5dd9907546bc97af931be4eef1e23a908c40d2ab28a68`  
		Last Modified: Tue, 12 Aug 2025 20:51:41 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188521c2085d7c3dbbbae5485b4fc383b0516ff6e9a27a023df6aca63dbb7459`  
		Last Modified: Tue, 12 Aug 2025 20:51:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581d2a99a5e27e493c9517fcb5d27c165f5696ad1d8f08f568d60eee1e8d6fcc`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 20.8 MB (20826824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e88f9f3cb2e7be25dbdc4626eb3bcbc619924d0c61d64356d2d7a8e3fc4a661`  
		Last Modified: Tue, 12 Aug 2025 20:51:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70bf9f40001314e26858770cf903764c3dc5e0c1278e072fa7daf620846745`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6079589750abcc6d3eb81778c4a2837ea2dc0467112980d886173696e4c9df`  
		Last Modified: Tue, 12 Aug 2025 20:51:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65174c16d8c061f85019c62493afae8d5db2f56e1a831a94c02db515515626d`  
		Last Modified: Tue, 12 Aug 2025 20:51:50 GMT  
		Size: 22.9 MB (22937256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728f806f53c767bd20bb97653fa5b5e3016a8e4af213a950135d9105930ac520`  
		Last Modified: Tue, 12 Aug 2025 20:51:48 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b5ab841f285aa2a8a9238b3c57bede8d2a91a3763c0f584275508deefcbdf5`  
		Last Modified: Tue, 12 Aug 2025 20:51:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae017706cc10313aa38b24d9c7c4dc2901f7f1ea62598f22aa0639e40d14cba0`  
		Last Modified: Tue, 12 Aug 2025 20:51:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bac6b791dfaef6e7c36ef93b178cc273d730b229d9112ceadede006ad1bc0a6`  
		Last Modified: Tue, 12 Aug 2025 20:51:56 GMT  
		Size: 22.4 MB (22375244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:7a3b2e07b931434a99cd7f00343a6fd5b6a618598e9cc4746313aaca3de5aaa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `docker:28.3-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:b08584be840c5fffd7d99e62ab49eae4c3f6636a8843cce35a5bd1067720e0ab
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348189021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732e79d977df1d9edff845acd89fee0b2122dfd3500338862d0c073f12710e29`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:25:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:06 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:26:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:26:19 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:26:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:26:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:26:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:26:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37ee622e1d3856c0f56d0e073b50e34ad5239aa1e8a0d7b93f11fb38230099f`  
		Last Modified: Tue, 12 Aug 2025 20:28:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04848d212a98717392544afa4ddeeef71992d66bba2d6eef616660649835eece`  
		Last Modified: Tue, 12 Aug 2025 20:28:14 GMT  
		Size: 346.1 KB (346147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e3cc07ce8c5cb86d5dd9907546bc97af931be4eef1e23a908c40d2ab28a68`  
		Last Modified: Tue, 12 Aug 2025 20:51:41 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188521c2085d7c3dbbbae5485b4fc383b0516ff6e9a27a023df6aca63dbb7459`  
		Last Modified: Tue, 12 Aug 2025 20:51:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581d2a99a5e27e493c9517fcb5d27c165f5696ad1d8f08f568d60eee1e8d6fcc`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 20.8 MB (20826824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e88f9f3cb2e7be25dbdc4626eb3bcbc619924d0c61d64356d2d7a8e3fc4a661`  
		Last Modified: Tue, 12 Aug 2025 20:51:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70bf9f40001314e26858770cf903764c3dc5e0c1278e072fa7daf620846745`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6079589750abcc6d3eb81778c4a2837ea2dc0467112980d886173696e4c9df`  
		Last Modified: Tue, 12 Aug 2025 20:51:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65174c16d8c061f85019c62493afae8d5db2f56e1a831a94c02db515515626d`  
		Last Modified: Tue, 12 Aug 2025 20:51:50 GMT  
		Size: 22.9 MB (22937256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728f806f53c767bd20bb97653fa5b5e3016a8e4af213a950135d9105930ac520`  
		Last Modified: Tue, 12 Aug 2025 20:51:48 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b5ab841f285aa2a8a9238b3c57bede8d2a91a3763c0f584275508deefcbdf5`  
		Last Modified: Tue, 12 Aug 2025 20:51:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae017706cc10313aa38b24d9c7c4dc2901f7f1ea62598f22aa0639e40d14cba0`  
		Last Modified: Tue, 12 Aug 2025 20:51:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bac6b791dfaef6e7c36ef93b178cc273d730b229d9112ceadede006ad1bc0a6`  
		Last Modified: Tue, 12 Aug 2025 20:51:56 GMT  
		Size: 22.4 MB (22375244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a188802ccb2fc99331e286bf343b9ad5721c2fcf498565d8a6990f9642e3f046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `docker:28.3-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fce944f1be9964c27dffe70ea4e05f43906e5c35d7f1d1f319ea241e6ff7766b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565385109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e16746b5d96d8f01c428a46027b16342e56a3f351d9e94cc23c4884e182a23`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:26:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:27:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:06 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:27:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:27:16 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:27:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d49ded649af742ac4e8aff9b2beba88841a34f5ac3c9cad1b2cbbb85a8a1741`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4901ee3ae2f2d3da5d2455d57c8497cdcd54fa3981e3eced30f632522080c987`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 356.9 KB (356904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cce2887577005a99bc013670c90c46c419da33c604d06b159d5a10bf40d3cb`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d727c7396ced4e810c63f727df20e45e76ebd1775b108e32a902fac6b6478076`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcfd1f605909b895b191bbc1dce66175acc45a5add136bc5a0ae4f36ecd8989`  
		Last Modified: Tue, 12 Aug 2025 20:31:31 GMT  
		Size: 20.8 MB (20837962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e6ab5bf2d2d618100a885f27c393467212c0570eaa7ea84e6ea8219e5dc291`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b884b8cda3f7df7bffd4252d58e7d9152d914e0d920161dfc1b2bbf477829d45`  
		Last Modified: Tue, 12 Aug 2025 20:31:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7094f59558defd3124f897718f374e4c7adb853752582ba8e4f3684c14b3e16a`  
		Last Modified: Tue, 12 Aug 2025 20:31:14 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7051fc3fd3e4df1ca961e28ab2cd07384069c0c2872b4680f672075663b48034`  
		Last Modified: Tue, 12 Aug 2025 20:31:20 GMT  
		Size: 23.0 MB (22953510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a709cde7693b4592561374d3dddec696b50b1a107e69458552265acbbf21459e`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d45050aa1c7e9ea58879bcb46bbf075e263acc49748dcd9a19068713b52e59`  
		Last Modified: Tue, 12 Aug 2025 20:31:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31e15e6414199a0fa232b38e3b810fa3806c10634d77fbde8642407b62f90f1`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4abea89efff9a4dcaee678846541ee7471b0d5e13f11a1ffd50c601da438141`  
		Last Modified: Tue, 12 Aug 2025 20:31:21 GMT  
		Size: 22.4 MB (22394336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3.3`

```console
$ docker pull docker@sha256:c0872aae4791ff427e6eda52769afa04f17b5cf756f8267e0d52774c99d5c9de
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

### `docker:28.3.3` - linux; amd64

```console
$ docker pull docker@sha256:acf2e2d09cedf21fa8f27bb0962674e33e159c744c152b248f1f7f43623ccd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145400826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a8bf985f76be7345c0c827c568db287ccb4dfad919a4693488224e3644fb0c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8791499fa9bdef98d7e3a188725e48e8c8dba0180702d559340747beef3519c`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 6.9 MB (6905701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fadee7df1b34bce659502e94099411a4bcea4f3b4b5703acdea29f43f10435d`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 90.2 KB (90225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585c63523750cbc3e625b48e735c70327c58c50817730a4f0ccfa5bca404699a`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ef36d1f42ecc72cee33f9b3630df040c2b3c0129388095caa52aa65663b6b`  
		Last Modified: Tue, 29 Jul 2025 17:08:29 GMT  
		Size: 62.5 MB (62516136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa56a13dffa7d647581a8133c12b84570ac763f9c5a281a0762d56e2cf50c5`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae60b320044d4dddd57522c6c3ddcd806948664e3b77e4b4f3dfdbcbb154bb`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3` - unknown; unknown

```console
$ docker pull docker@sha256:b07ec0abd0eacbbb7a5caff69421dcf417d11e841cd6c39914c6350ec8ead6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3b72142c672a9277787f2a650dfe1c3d5ec96a77d3dfb1b30ee99fd35cfbbb`

```dockerfile
```

-	Layers:
	-	`sha256:810146a77372683cd7bd8b4e79c73015f3d7c76c01b681379c962de5166e83d5`  
		Last Modified: Tue, 29 Jul 2025 20:07:23 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3` - linux; arm variant v6

```console
$ docker pull docker@sha256:1f082418e60bfdc41615178f3338a57e008be9e54a0a088bdaf7639e6440aa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136481510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b903ce9efae22aff353f3b148f4b81543338dda7c191abe851759db185d55660`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f822c2573de7e9c67a5c71e3631064c5bcc0ea4209e1599a17c1acfeaaf1af`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 18.5 MB (18451848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd472c4b566302d5ccb09e4bc30d193d93f2127195f039fcc1e4c2e6384fd1`  
		Last Modified: Tue, 29 Jul 2025 16:50:49 GMT  
		Size: 20.6 MB (20568606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e39b3b275050311240d86f4184b92738124227ab91074f2d543353027e9ee`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 20.2 MB (20183248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fcfc43ab15c1da7e48f821e25c54c51d723b64684b20d2a4b4edff8e04dcc3`  
		Last Modified: Tue, 29 Jul 2025 16:50:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563338bb8fe09f3e62c3a07902962cba52ef8de211de1bda00ead94befe4d6c6`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d5bc334980f311595207402ce2300f8a11e1e71eb800bd573dcdfcbbb7383`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44f5f22ffde31d78b179f8cd7410f20820e06caf28efa9a65355c29b1e2b10b`  
		Last Modified: Thu, 07 Aug 2025 16:57:01 GMT  
		Size: 7.2 MB (7230142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebba53fb812598805b6fc21226a04919f3781430ba936808b0f59d133c00e80`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 89.8 KB (89806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e516ec65aa3324f86b97988d15e6abcbe2d2cd5aa91eaa93c11d0119f0016b85`  
		Last Modified: Thu, 07 Aug 2025 16:57:00 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036456d63ef0cf8b17f84e9d6b0243b01f469739b1a7f24cfe71c25d87b89496`  
		Last Modified: Thu, 07 Aug 2025 16:57:05 GMT  
		Size: 58.3 MB (58345094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909c6394356186a1784dad76416d85e70821a8a0efdf5b9bc6084f7f4cad6dbc`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2bfa6563e19d5b6bf2937e08f7af0eeeef31f1d0da970fbb37bdc678a99e81`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3` - unknown; unknown

```console
$ docker pull docker@sha256:caf190c0124eba00b01a8690ce7a05f806d0cf5ba34877fdf387e41444f3aeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b22a0c050d02e7164da7a016f4a9e2934ce69b7b45be19137f526a4c3cd0a4b`

```dockerfile
```

-	Layers:
	-	`sha256:c8c17618f747eab2415d91d988104c720915211836b105288567df5c8ca9f095`  
		Last Modified: Thu, 07 Aug 2025 17:07:28 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3` - linux; arm variant v7

```console
$ docker pull docker@sha256:0e5e5db93aa3e8af23c2189c2f949f41637e51178bf775ddff251f72743345f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134624627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a94d5bea77d233423c8ec637c7ec3d4ae66c22b1a4f9b58c44d6a5b9084ae0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fda06620cb3acbe8d29e62b35edf4eab73bd1796050a544bac974a28f5fd99`  
		Last Modified: Tue, 29 Jul 2025 17:13:20 GMT  
		Size: 18.4 MB (18441097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab513f15d8a635f59bcbe656922221d344bfc6c7d6c78e0b69a118c025c543b5`  
		Last Modified: Tue, 29 Jul 2025 17:13:21 GMT  
		Size: 20.5 MB (20548892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ff39cd4cd7f51997cb5ef915890dd813cd17afa5822471bc9fcf70b903121`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 20.2 MB (20166234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb6e886463cf3968d42871b95c8d48e815d647d699e9512783a2ef44fa0f64`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672297f80502d6989f94397992684d739879955ca812c635d7d02bbd1c82ba0`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269088758c4eb6e7275e58a86756108338d7e30a284edf53331fca7f4a88b0a5`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df050d7dc2c286cb6eb89f5f6074f0e2050b5647fac156e97e954bb586e0c977`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 6.5 MB (6538354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfde1691582119bdf48b4b13b8ec970dc7ea3fee792a9dcb2e806abbbb6939e`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 86.2 KB (86243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea99a75781859a140708f0f46a3c77bf434229b777a07580312f1f7051f87f50`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6cd3c5f53aed54fbcbdee772d968d063922cdb9ccaaf39af1ed46362650de`  
		Last Modified: Thu, 07 Aug 2025 14:58:09 GMT  
		Size: 58.2 MB (58186632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d193787930eddbb555cddea45342d37ec90697f6a1189dbe0103604b619f5ca`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfc61f65df60ef9b0388537e5876063cd37269cde97577fbb9cdc488230afe0`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3` - unknown; unknown

```console
$ docker pull docker@sha256:9c2557085ad68b5571b358134d36f2754b98a3ecb6882d6fd39a108e7180b090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522da17433e7ff04443725fdae9470d541ce7b230974c06928d9b00072a85a37`

```dockerfile
```

-	Layers:
	-	`sha256:67874486df4d385d50d3bcfc818bc8427ee8992e7228812841386fcb4f9dc903`  
		Last Modified: Thu, 07 Aug 2025 17:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:88bf2ba4673e2963049952ad60d46389e6d2be3d31f0f4d1d69c55e0712d22a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136102855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0680e652cec44e947fd5401c80526cad1e184420cc2645f6399d102127e5bbf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f90fb8179789820d09ee62a252a0b5d2007f1e6a0116dc93cef396028b74`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 7.1 MB (7140514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e7ada02315c507aa603b515c8af64560c37e3b0c3e1ae602c926a39f0e193`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 99.3 KB (99312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0bce22e68e3e822e795bdd12fcda8fe4d3374269c9031570e52e4989e30cc`  
		Last Modified: Tue, 29 Jul 2025 17:07:42 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94302614c7eb1b832998ebf0e2a380369fcc6c23e0fa4bab8669b02665af8558`  
		Last Modified: Tue, 29 Jul 2025 17:07:38 GMT  
		Size: 57.5 MB (57464791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6fb8714059d9cacf4db01465f092fa2bfbaebc073ecf76e620e3776406896`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d9a1a1a08782f599a9be2fe288ef0cbd4aa9a049d7b515137cf06ff00f2ba`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3` - unknown; unknown

```console
$ docker pull docker@sha256:9e688304c06587ce1c71a3409b301f476dc1fd9b67ee40cf659e180e174582d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878a9b4d22bd08a4e39e541ae7b4ca75ac8e62370ac53573fa18a05338573ec4`

```dockerfile
```

-	Layers:
	-	`sha256:e0a4c2285c0b8b2afc33b86867190ce402deccb8def5a4573f617737a1c16087`  
		Last Modified: Tue, 29 Jul 2025 20:07:33 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.3-alpine3.22`

```console
$ docker pull docker@sha256:c0872aae4791ff427e6eda52769afa04f17b5cf756f8267e0d52774c99d5c9de
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

### `docker:28.3.3-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:acf2e2d09cedf21fa8f27bb0962674e33e159c744c152b248f1f7f43623ccd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145400826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a8bf985f76be7345c0c827c568db287ccb4dfad919a4693488224e3644fb0c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8791499fa9bdef98d7e3a188725e48e8c8dba0180702d559340747beef3519c`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 6.9 MB (6905701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fadee7df1b34bce659502e94099411a4bcea4f3b4b5703acdea29f43f10435d`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 90.2 KB (90225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585c63523750cbc3e625b48e735c70327c58c50817730a4f0ccfa5bca404699a`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ef36d1f42ecc72cee33f9b3630df040c2b3c0129388095caa52aa65663b6b`  
		Last Modified: Tue, 29 Jul 2025 17:08:29 GMT  
		Size: 62.5 MB (62516136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa56a13dffa7d647581a8133c12b84570ac763f9c5a281a0762d56e2cf50c5`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae60b320044d4dddd57522c6c3ddcd806948664e3b77e4b4f3dfdbcbb154bb`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:b07ec0abd0eacbbb7a5caff69421dcf417d11e841cd6c39914c6350ec8ead6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3b72142c672a9277787f2a650dfe1c3d5ec96a77d3dfb1b30ee99fd35cfbbb`

```dockerfile
```

-	Layers:
	-	`sha256:810146a77372683cd7bd8b4e79c73015f3d7c76c01b681379c962de5166e83d5`  
		Last Modified: Tue, 29 Jul 2025 20:07:23 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:1f082418e60bfdc41615178f3338a57e008be9e54a0a088bdaf7639e6440aa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136481510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b903ce9efae22aff353f3b148f4b81543338dda7c191abe851759db185d55660`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f822c2573de7e9c67a5c71e3631064c5bcc0ea4209e1599a17c1acfeaaf1af`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 18.5 MB (18451848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd472c4b566302d5ccb09e4bc30d193d93f2127195f039fcc1e4c2e6384fd1`  
		Last Modified: Tue, 29 Jul 2025 16:50:49 GMT  
		Size: 20.6 MB (20568606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e39b3b275050311240d86f4184b92738124227ab91074f2d543353027e9ee`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 20.2 MB (20183248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fcfc43ab15c1da7e48f821e25c54c51d723b64684b20d2a4b4edff8e04dcc3`  
		Last Modified: Tue, 29 Jul 2025 16:50:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563338bb8fe09f3e62c3a07902962cba52ef8de211de1bda00ead94befe4d6c6`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d5bc334980f311595207402ce2300f8a11e1e71eb800bd573dcdfcbbb7383`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44f5f22ffde31d78b179f8cd7410f20820e06caf28efa9a65355c29b1e2b10b`  
		Last Modified: Thu, 07 Aug 2025 16:57:01 GMT  
		Size: 7.2 MB (7230142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebba53fb812598805b6fc21226a04919f3781430ba936808b0f59d133c00e80`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 89.8 KB (89806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e516ec65aa3324f86b97988d15e6abcbe2d2cd5aa91eaa93c11d0119f0016b85`  
		Last Modified: Thu, 07 Aug 2025 16:57:00 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036456d63ef0cf8b17f84e9d6b0243b01f469739b1a7f24cfe71c25d87b89496`  
		Last Modified: Thu, 07 Aug 2025 16:57:05 GMT  
		Size: 58.3 MB (58345094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909c6394356186a1784dad76416d85e70821a8a0efdf5b9bc6084f7f4cad6dbc`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2bfa6563e19d5b6bf2937e08f7af0eeeef31f1d0da970fbb37bdc678a99e81`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:caf190c0124eba00b01a8690ce7a05f806d0cf5ba34877fdf387e41444f3aeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b22a0c050d02e7164da7a016f4a9e2934ce69b7b45be19137f526a4c3cd0a4b`

```dockerfile
```

-	Layers:
	-	`sha256:c8c17618f747eab2415d91d988104c720915211836b105288567df5c8ca9f095`  
		Last Modified: Thu, 07 Aug 2025 17:07:28 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:0e5e5db93aa3e8af23c2189c2f949f41637e51178bf775ddff251f72743345f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134624627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a94d5bea77d233423c8ec637c7ec3d4ae66c22b1a4f9b58c44d6a5b9084ae0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fda06620cb3acbe8d29e62b35edf4eab73bd1796050a544bac974a28f5fd99`  
		Last Modified: Tue, 29 Jul 2025 17:13:20 GMT  
		Size: 18.4 MB (18441097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab513f15d8a635f59bcbe656922221d344bfc6c7d6c78e0b69a118c025c543b5`  
		Last Modified: Tue, 29 Jul 2025 17:13:21 GMT  
		Size: 20.5 MB (20548892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ff39cd4cd7f51997cb5ef915890dd813cd17afa5822471bc9fcf70b903121`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 20.2 MB (20166234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb6e886463cf3968d42871b95c8d48e815d647d699e9512783a2ef44fa0f64`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672297f80502d6989f94397992684d739879955ca812c635d7d02bbd1c82ba0`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269088758c4eb6e7275e58a86756108338d7e30a284edf53331fca7f4a88b0a5`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df050d7dc2c286cb6eb89f5f6074f0e2050b5647fac156e97e954bb586e0c977`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 6.5 MB (6538354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfde1691582119bdf48b4b13b8ec970dc7ea3fee792a9dcb2e806abbbb6939e`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 86.2 KB (86243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea99a75781859a140708f0f46a3c77bf434229b777a07580312f1f7051f87f50`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6cd3c5f53aed54fbcbdee772d968d063922cdb9ccaaf39af1ed46362650de`  
		Last Modified: Thu, 07 Aug 2025 14:58:09 GMT  
		Size: 58.2 MB (58186632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d193787930eddbb555cddea45342d37ec90697f6a1189dbe0103604b619f5ca`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfc61f65df60ef9b0388537e5876063cd37269cde97577fbb9cdc488230afe0`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:9c2557085ad68b5571b358134d36f2754b98a3ecb6882d6fd39a108e7180b090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522da17433e7ff04443725fdae9470d541ce7b230974c06928d9b00072a85a37`

```dockerfile
```

-	Layers:
	-	`sha256:67874486df4d385d50d3bcfc818bc8427ee8992e7228812841386fcb4f9dc903`  
		Last Modified: Thu, 07 Aug 2025 17:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:88bf2ba4673e2963049952ad60d46389e6d2be3d31f0f4d1d69c55e0712d22a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136102855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0680e652cec44e947fd5401c80526cad1e184420cc2645f6399d102127e5bbf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f90fb8179789820d09ee62a252a0b5d2007f1e6a0116dc93cef396028b74`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 7.1 MB (7140514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e7ada02315c507aa603b515c8af64560c37e3b0c3e1ae602c926a39f0e193`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 99.3 KB (99312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0bce22e68e3e822e795bdd12fcda8fe4d3374269c9031570e52e4989e30cc`  
		Last Modified: Tue, 29 Jul 2025 17:07:42 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94302614c7eb1b832998ebf0e2a380369fcc6c23e0fa4bab8669b02665af8558`  
		Last Modified: Tue, 29 Jul 2025 17:07:38 GMT  
		Size: 57.5 MB (57464791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6fb8714059d9cacf4db01465f092fa2bfbaebc073ecf76e620e3776406896`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d9a1a1a08782f599a9be2fe288ef0cbd4aa9a049d7b515137cf06ff00f2ba`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:9e688304c06587ce1c71a3409b301f476dc1fd9b67ee40cf659e180e174582d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878a9b4d22bd08a4e39e541ae7b4ca75ac8e62370ac53573fa18a05338573ec4`

```dockerfile
```

-	Layers:
	-	`sha256:e0a4c2285c0b8b2afc33b86867190ce402deccb8def5a4573f617737a1c16087`  
		Last Modified: Tue, 29 Jul 2025 20:07:33 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.3-cli`

```console
$ docker pull docker@sha256:d87c674b7f01043207f1badc6e86e1f8bc33a90981c2f31f3e0f57c1ecb0c5cc
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

### `docker:28.3.3-cli` - linux; amd64

```console
$ docker pull docker@sha256:e47e07b4616ad120a5e3812a315c0adb0a80d17eb19c979271dd3b16416226bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75882770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef97129ecf899446838ff807b2d675d8a1e30f2dac9af363534872b88f7b3def`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:019dbf214cb0eaa7943816f0cc580437ccae2ef546bf1bcff82e5b51ab2ca91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86120028f5d4320014588ac17e4563c14713f8a385d8e192c8229475f8ff6c35`

```dockerfile
```

-	Layers:
	-	`sha256:13645690d79e822200fb314c8947b0437ed272113942e70c5e93b9215ac0c449`  
		Last Modified: Tue, 29 Jul 2025 17:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:8f845ca7eb3d2dab949a1321d7ba195c8f690a89eb313190e35c32687d2a507b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70810451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b83d2189eeff2d9c339890963393fb464d80828d8b043a20894478fe3ffee1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f822c2573de7e9c67a5c71e3631064c5bcc0ea4209e1599a17c1acfeaaf1af`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 18.5 MB (18451848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd472c4b566302d5ccb09e4bc30d193d93f2127195f039fcc1e4c2e6384fd1`  
		Last Modified: Tue, 29 Jul 2025 16:50:49 GMT  
		Size: 20.6 MB (20568606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e39b3b275050311240d86f4184b92738124227ab91074f2d543353027e9ee`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 20.2 MB (20183248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fcfc43ab15c1da7e48f821e25c54c51d723b64684b20d2a4b4edff8e04dcc3`  
		Last Modified: Tue, 29 Jul 2025 16:50:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563338bb8fe09f3e62c3a07902962cba52ef8de211de1bda00ead94befe4d6c6`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d5bc334980f311595207402ce2300f8a11e1e71eb800bd573dcdfcbbb7383`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f1537ca07297772da32b2e246c50c1dea5ebad32ae760a9b9b7ccb94eaad29c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f65333c983620826c8527af4e58d432a3ee0ae31df3f9b51352442ccfdf7595`

```dockerfile
```

-	Layers:
	-	`sha256:b1609329088ee42b557625a4e309152f4ae582a5feb24069e6b4ac2a02371377`  
		Last Modified: Tue, 29 Jul 2025 17:07:26 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:c63fc02e3bb2c71c1e39d9618770900f16aeccddb8d13a517c16752f113a7fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69807384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c236c8ccc2e365a65223161398d002ebd5f6d7a8499070bd805ec062050a149f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fda06620cb3acbe8d29e62b35edf4eab73bd1796050a544bac974a28f5fd99`  
		Last Modified: Tue, 29 Jul 2025 17:13:20 GMT  
		Size: 18.4 MB (18441097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab513f15d8a635f59bcbe656922221d344bfc6c7d6c78e0b69a118c025c543b5`  
		Last Modified: Tue, 29 Jul 2025 17:13:21 GMT  
		Size: 20.5 MB (20548892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ff39cd4cd7f51997cb5ef915890dd813cd17afa5822471bc9fcf70b903121`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 20.2 MB (20166234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb6e886463cf3968d42871b95c8d48e815d647d699e9512783a2ef44fa0f64`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672297f80502d6989f94397992684d739879955ca812c635d7d02bbd1c82ba0`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269088758c4eb6e7275e58a86756108338d7e30a284edf53331fca7f4a88b0a5`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:324a1f85dda8d36fcd3250fec9cca2ed582c781a8c5ebfded37a04ac8840aa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82360f4e5611e16371e1b1bf406b68e64ff5640d3207b215c35251543cc4956`

```dockerfile
```

-	Layers:
	-	`sha256:3ffc99fef904d345817e2028615cef8ce8299be6c0754569973a322b26a2cad5`  
		Last Modified: Tue, 29 Jul 2025 20:07:33 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2b6312fd57e7b24ffae3ace014357496da75c7d3b7bd15455987364d5805999c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71392240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324b3c32e29caad939b212c3d18aa70ad98a23579154b2254f63b19284e09046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:b00a03f6a893ff05072a6aec1f14baab706cadb23df8f3472eca7a730139ff6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c33d99fbb568b26e841daf1694e071995a07b8dd92bbc7c1414abe997adbc70`

```dockerfile
```

-	Layers:
	-	`sha256:278de4bd27c29d5f7783b8e9211f0b5596e91aab67d37d191bd0e5df0b2a41e9`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.3-cli-alpine3.22`

```console
$ docker pull docker@sha256:d87c674b7f01043207f1badc6e86e1f8bc33a90981c2f31f3e0f57c1ecb0c5cc
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

### `docker:28.3.3-cli-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:e47e07b4616ad120a5e3812a315c0adb0a80d17eb19c979271dd3b16416226bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75882770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef97129ecf899446838ff807b2d675d8a1e30f2dac9af363534872b88f7b3def`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:019dbf214cb0eaa7943816f0cc580437ccae2ef546bf1bcff82e5b51ab2ca91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86120028f5d4320014588ac17e4563c14713f8a385d8e192c8229475f8ff6c35`

```dockerfile
```

-	Layers:
	-	`sha256:13645690d79e822200fb314c8947b0437ed272113942e70c5e93b9215ac0c449`  
		Last Modified: Tue, 29 Jul 2025 17:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-cli-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:8f845ca7eb3d2dab949a1321d7ba195c8f690a89eb313190e35c32687d2a507b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70810451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b83d2189eeff2d9c339890963393fb464d80828d8b043a20894478fe3ffee1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f822c2573de7e9c67a5c71e3631064c5bcc0ea4209e1599a17c1acfeaaf1af`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 18.5 MB (18451848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd472c4b566302d5ccb09e4bc30d193d93f2127195f039fcc1e4c2e6384fd1`  
		Last Modified: Tue, 29 Jul 2025 16:50:49 GMT  
		Size: 20.6 MB (20568606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e39b3b275050311240d86f4184b92738124227ab91074f2d543353027e9ee`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 20.2 MB (20183248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fcfc43ab15c1da7e48f821e25c54c51d723b64684b20d2a4b4edff8e04dcc3`  
		Last Modified: Tue, 29 Jul 2025 16:50:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563338bb8fe09f3e62c3a07902962cba52ef8de211de1bda00ead94befe4d6c6`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d5bc334980f311595207402ce2300f8a11e1e71eb800bd573dcdfcbbb7383`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:f1537ca07297772da32b2e246c50c1dea5ebad32ae760a9b9b7ccb94eaad29c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f65333c983620826c8527af4e58d432a3ee0ae31df3f9b51352442ccfdf7595`

```dockerfile
```

-	Layers:
	-	`sha256:b1609329088ee42b557625a4e309152f4ae582a5feb24069e6b4ac2a02371377`  
		Last Modified: Tue, 29 Jul 2025 17:07:26 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-cli-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:c63fc02e3bb2c71c1e39d9618770900f16aeccddb8d13a517c16752f113a7fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69807384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c236c8ccc2e365a65223161398d002ebd5f6d7a8499070bd805ec062050a149f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fda06620cb3acbe8d29e62b35edf4eab73bd1796050a544bac974a28f5fd99`  
		Last Modified: Tue, 29 Jul 2025 17:13:20 GMT  
		Size: 18.4 MB (18441097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab513f15d8a635f59bcbe656922221d344bfc6c7d6c78e0b69a118c025c543b5`  
		Last Modified: Tue, 29 Jul 2025 17:13:21 GMT  
		Size: 20.5 MB (20548892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ff39cd4cd7f51997cb5ef915890dd813cd17afa5822471bc9fcf70b903121`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 20.2 MB (20166234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb6e886463cf3968d42871b95c8d48e815d647d699e9512783a2ef44fa0f64`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672297f80502d6989f94397992684d739879955ca812c635d7d02bbd1c82ba0`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269088758c4eb6e7275e58a86756108338d7e30a284edf53331fca7f4a88b0a5`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:324a1f85dda8d36fcd3250fec9cca2ed582c781a8c5ebfded37a04ac8840aa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82360f4e5611e16371e1b1bf406b68e64ff5640d3207b215c35251543cc4956`

```dockerfile
```

-	Layers:
	-	`sha256:3ffc99fef904d345817e2028615cef8ce8299be6c0754569973a322b26a2cad5`  
		Last Modified: Tue, 29 Jul 2025 20:07:33 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-cli-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2b6312fd57e7b24ffae3ace014357496da75c7d3b7bd15455987364d5805999c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71392240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324b3c32e29caad939b212c3d18aa70ad98a23579154b2254f63b19284e09046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:b00a03f6a893ff05072a6aec1f14baab706cadb23df8f3472eca7a730139ff6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c33d99fbb568b26e841daf1694e071995a07b8dd92bbc7c1414abe997adbc70`

```dockerfile
```

-	Layers:
	-	`sha256:278de4bd27c29d5f7783b8e9211f0b5596e91aab67d37d191bd0e5df0b2a41e9`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.3-dind`

```console
$ docker pull docker@sha256:c0872aae4791ff427e6eda52769afa04f17b5cf756f8267e0d52774c99d5c9de
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

### `docker:28.3.3-dind` - linux; amd64

```console
$ docker pull docker@sha256:acf2e2d09cedf21fa8f27bb0962674e33e159c744c152b248f1f7f43623ccd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145400826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a8bf985f76be7345c0c827c568db287ccb4dfad919a4693488224e3644fb0c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8791499fa9bdef98d7e3a188725e48e8c8dba0180702d559340747beef3519c`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 6.9 MB (6905701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fadee7df1b34bce659502e94099411a4bcea4f3b4b5703acdea29f43f10435d`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 90.2 KB (90225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585c63523750cbc3e625b48e735c70327c58c50817730a4f0ccfa5bca404699a`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ef36d1f42ecc72cee33f9b3630df040c2b3c0129388095caa52aa65663b6b`  
		Last Modified: Tue, 29 Jul 2025 17:08:29 GMT  
		Size: 62.5 MB (62516136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa56a13dffa7d647581a8133c12b84570ac763f9c5a281a0762d56e2cf50c5`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae60b320044d4dddd57522c6c3ddcd806948664e3b77e4b4f3dfdbcbb154bb`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b07ec0abd0eacbbb7a5caff69421dcf417d11e841cd6c39914c6350ec8ead6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3b72142c672a9277787f2a650dfe1c3d5ec96a77d3dfb1b30ee99fd35cfbbb`

```dockerfile
```

-	Layers:
	-	`sha256:810146a77372683cd7bd8b4e79c73015f3d7c76c01b681379c962de5166e83d5`  
		Last Modified: Tue, 29 Jul 2025 20:07:23 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1f082418e60bfdc41615178f3338a57e008be9e54a0a088bdaf7639e6440aa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136481510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b903ce9efae22aff353f3b148f4b81543338dda7c191abe851759db185d55660`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f822c2573de7e9c67a5c71e3631064c5bcc0ea4209e1599a17c1acfeaaf1af`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 18.5 MB (18451848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd472c4b566302d5ccb09e4bc30d193d93f2127195f039fcc1e4c2e6384fd1`  
		Last Modified: Tue, 29 Jul 2025 16:50:49 GMT  
		Size: 20.6 MB (20568606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e39b3b275050311240d86f4184b92738124227ab91074f2d543353027e9ee`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 20.2 MB (20183248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fcfc43ab15c1da7e48f821e25c54c51d723b64684b20d2a4b4edff8e04dcc3`  
		Last Modified: Tue, 29 Jul 2025 16:50:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563338bb8fe09f3e62c3a07902962cba52ef8de211de1bda00ead94befe4d6c6`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d5bc334980f311595207402ce2300f8a11e1e71eb800bd573dcdfcbbb7383`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44f5f22ffde31d78b179f8cd7410f20820e06caf28efa9a65355c29b1e2b10b`  
		Last Modified: Thu, 07 Aug 2025 16:57:01 GMT  
		Size: 7.2 MB (7230142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebba53fb812598805b6fc21226a04919f3781430ba936808b0f59d133c00e80`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 89.8 KB (89806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e516ec65aa3324f86b97988d15e6abcbe2d2cd5aa91eaa93c11d0119f0016b85`  
		Last Modified: Thu, 07 Aug 2025 16:57:00 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036456d63ef0cf8b17f84e9d6b0243b01f469739b1a7f24cfe71c25d87b89496`  
		Last Modified: Thu, 07 Aug 2025 16:57:05 GMT  
		Size: 58.3 MB (58345094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909c6394356186a1784dad76416d85e70821a8a0efdf5b9bc6084f7f4cad6dbc`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2bfa6563e19d5b6bf2937e08f7af0eeeef31f1d0da970fbb37bdc678a99e81`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:caf190c0124eba00b01a8690ce7a05f806d0cf5ba34877fdf387e41444f3aeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b22a0c050d02e7164da7a016f4a9e2934ce69b7b45be19137f526a4c3cd0a4b`

```dockerfile
```

-	Layers:
	-	`sha256:c8c17618f747eab2415d91d988104c720915211836b105288567df5c8ca9f095`  
		Last Modified: Thu, 07 Aug 2025 17:07:28 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:0e5e5db93aa3e8af23c2189c2f949f41637e51178bf775ddff251f72743345f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134624627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a94d5bea77d233423c8ec637c7ec3d4ae66c22b1a4f9b58c44d6a5b9084ae0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fda06620cb3acbe8d29e62b35edf4eab73bd1796050a544bac974a28f5fd99`  
		Last Modified: Tue, 29 Jul 2025 17:13:20 GMT  
		Size: 18.4 MB (18441097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab513f15d8a635f59bcbe656922221d344bfc6c7d6c78e0b69a118c025c543b5`  
		Last Modified: Tue, 29 Jul 2025 17:13:21 GMT  
		Size: 20.5 MB (20548892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ff39cd4cd7f51997cb5ef915890dd813cd17afa5822471bc9fcf70b903121`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 20.2 MB (20166234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb6e886463cf3968d42871b95c8d48e815d647d699e9512783a2ef44fa0f64`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672297f80502d6989f94397992684d739879955ca812c635d7d02bbd1c82ba0`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269088758c4eb6e7275e58a86756108338d7e30a284edf53331fca7f4a88b0a5`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df050d7dc2c286cb6eb89f5f6074f0e2050b5647fac156e97e954bb586e0c977`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 6.5 MB (6538354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfde1691582119bdf48b4b13b8ec970dc7ea3fee792a9dcb2e806abbbb6939e`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 86.2 KB (86243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea99a75781859a140708f0f46a3c77bf434229b777a07580312f1f7051f87f50`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6cd3c5f53aed54fbcbdee772d968d063922cdb9ccaaf39af1ed46362650de`  
		Last Modified: Thu, 07 Aug 2025 14:58:09 GMT  
		Size: 58.2 MB (58186632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d193787930eddbb555cddea45342d37ec90697f6a1189dbe0103604b619f5ca`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfc61f65df60ef9b0388537e5876063cd37269cde97577fbb9cdc488230afe0`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9c2557085ad68b5571b358134d36f2754b98a3ecb6882d6fd39a108e7180b090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522da17433e7ff04443725fdae9470d541ce7b230974c06928d9b00072a85a37`

```dockerfile
```

-	Layers:
	-	`sha256:67874486df4d385d50d3bcfc818bc8427ee8992e7228812841386fcb4f9dc903`  
		Last Modified: Thu, 07 Aug 2025 17:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:88bf2ba4673e2963049952ad60d46389e6d2be3d31f0f4d1d69c55e0712d22a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136102855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0680e652cec44e947fd5401c80526cad1e184420cc2645f6399d102127e5bbf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f90fb8179789820d09ee62a252a0b5d2007f1e6a0116dc93cef396028b74`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 7.1 MB (7140514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e7ada02315c507aa603b515c8af64560c37e3b0c3e1ae602c926a39f0e193`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 99.3 KB (99312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0bce22e68e3e822e795bdd12fcda8fe4d3374269c9031570e52e4989e30cc`  
		Last Modified: Tue, 29 Jul 2025 17:07:42 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94302614c7eb1b832998ebf0e2a380369fcc6c23e0fa4bab8669b02665af8558`  
		Last Modified: Tue, 29 Jul 2025 17:07:38 GMT  
		Size: 57.5 MB (57464791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6fb8714059d9cacf4db01465f092fa2bfbaebc073ecf76e620e3776406896`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d9a1a1a08782f599a9be2fe288ef0cbd4aa9a049d7b515137cf06ff00f2ba`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:9e688304c06587ce1c71a3409b301f476dc1fd9b67ee40cf659e180e174582d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878a9b4d22bd08a4e39e541ae7b4ca75ac8e62370ac53573fa18a05338573ec4`

```dockerfile
```

-	Layers:
	-	`sha256:e0a4c2285c0b8b2afc33b86867190ce402deccb8def5a4573f617737a1c16087`  
		Last Modified: Tue, 29 Jul 2025 20:07:33 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.3-dind-alpine3.22`

```console
$ docker pull docker@sha256:c0872aae4791ff427e6eda52769afa04f17b5cf756f8267e0d52774c99d5c9de
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

### `docker:28.3.3-dind-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:acf2e2d09cedf21fa8f27bb0962674e33e159c744c152b248f1f7f43623ccd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145400826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a8bf985f76be7345c0c827c568db287ccb4dfad919a4693488224e3644fb0c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8791499fa9bdef98d7e3a188725e48e8c8dba0180702d559340747beef3519c`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 6.9 MB (6905701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fadee7df1b34bce659502e94099411a4bcea4f3b4b5703acdea29f43f10435d`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 90.2 KB (90225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585c63523750cbc3e625b48e735c70327c58c50817730a4f0ccfa5bca404699a`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ef36d1f42ecc72cee33f9b3630df040c2b3c0129388095caa52aa65663b6b`  
		Last Modified: Tue, 29 Jul 2025 17:08:29 GMT  
		Size: 62.5 MB (62516136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa56a13dffa7d647581a8133c12b84570ac763f9c5a281a0762d56e2cf50c5`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae60b320044d4dddd57522c6c3ddcd806948664e3b77e4b4f3dfdbcbb154bb`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:b07ec0abd0eacbbb7a5caff69421dcf417d11e841cd6c39914c6350ec8ead6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3b72142c672a9277787f2a650dfe1c3d5ec96a77d3dfb1b30ee99fd35cfbbb`

```dockerfile
```

-	Layers:
	-	`sha256:810146a77372683cd7bd8b4e79c73015f3d7c76c01b681379c962de5166e83d5`  
		Last Modified: Tue, 29 Jul 2025 20:07:23 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-dind-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:1f082418e60bfdc41615178f3338a57e008be9e54a0a088bdaf7639e6440aa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136481510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b903ce9efae22aff353f3b148f4b81543338dda7c191abe851759db185d55660`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f822c2573de7e9c67a5c71e3631064c5bcc0ea4209e1599a17c1acfeaaf1af`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 18.5 MB (18451848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd472c4b566302d5ccb09e4bc30d193d93f2127195f039fcc1e4c2e6384fd1`  
		Last Modified: Tue, 29 Jul 2025 16:50:49 GMT  
		Size: 20.6 MB (20568606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e39b3b275050311240d86f4184b92738124227ab91074f2d543353027e9ee`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 20.2 MB (20183248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fcfc43ab15c1da7e48f821e25c54c51d723b64684b20d2a4b4edff8e04dcc3`  
		Last Modified: Tue, 29 Jul 2025 16:50:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563338bb8fe09f3e62c3a07902962cba52ef8de211de1bda00ead94befe4d6c6`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d5bc334980f311595207402ce2300f8a11e1e71eb800bd573dcdfcbbb7383`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44f5f22ffde31d78b179f8cd7410f20820e06caf28efa9a65355c29b1e2b10b`  
		Last Modified: Thu, 07 Aug 2025 16:57:01 GMT  
		Size: 7.2 MB (7230142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebba53fb812598805b6fc21226a04919f3781430ba936808b0f59d133c00e80`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 89.8 KB (89806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e516ec65aa3324f86b97988d15e6abcbe2d2cd5aa91eaa93c11d0119f0016b85`  
		Last Modified: Thu, 07 Aug 2025 16:57:00 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036456d63ef0cf8b17f84e9d6b0243b01f469739b1a7f24cfe71c25d87b89496`  
		Last Modified: Thu, 07 Aug 2025 16:57:05 GMT  
		Size: 58.3 MB (58345094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909c6394356186a1784dad76416d85e70821a8a0efdf5b9bc6084f7f4cad6dbc`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2bfa6563e19d5b6bf2937e08f7af0eeeef31f1d0da970fbb37bdc678a99e81`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:caf190c0124eba00b01a8690ce7a05f806d0cf5ba34877fdf387e41444f3aeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b22a0c050d02e7164da7a016f4a9e2934ce69b7b45be19137f526a4c3cd0a4b`

```dockerfile
```

-	Layers:
	-	`sha256:c8c17618f747eab2415d91d988104c720915211836b105288567df5c8ca9f095`  
		Last Modified: Thu, 07 Aug 2025 17:07:28 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-dind-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:0e5e5db93aa3e8af23c2189c2f949f41637e51178bf775ddff251f72743345f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134624627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a94d5bea77d233423c8ec637c7ec3d4ae66c22b1a4f9b58c44d6a5b9084ae0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fda06620cb3acbe8d29e62b35edf4eab73bd1796050a544bac974a28f5fd99`  
		Last Modified: Tue, 29 Jul 2025 17:13:20 GMT  
		Size: 18.4 MB (18441097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab513f15d8a635f59bcbe656922221d344bfc6c7d6c78e0b69a118c025c543b5`  
		Last Modified: Tue, 29 Jul 2025 17:13:21 GMT  
		Size: 20.5 MB (20548892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ff39cd4cd7f51997cb5ef915890dd813cd17afa5822471bc9fcf70b903121`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 20.2 MB (20166234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb6e886463cf3968d42871b95c8d48e815d647d699e9512783a2ef44fa0f64`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672297f80502d6989f94397992684d739879955ca812c635d7d02bbd1c82ba0`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269088758c4eb6e7275e58a86756108338d7e30a284edf53331fca7f4a88b0a5`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df050d7dc2c286cb6eb89f5f6074f0e2050b5647fac156e97e954bb586e0c977`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 6.5 MB (6538354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfde1691582119bdf48b4b13b8ec970dc7ea3fee792a9dcb2e806abbbb6939e`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 86.2 KB (86243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea99a75781859a140708f0f46a3c77bf434229b777a07580312f1f7051f87f50`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6cd3c5f53aed54fbcbdee772d968d063922cdb9ccaaf39af1ed46362650de`  
		Last Modified: Thu, 07 Aug 2025 14:58:09 GMT  
		Size: 58.2 MB (58186632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d193787930eddbb555cddea45342d37ec90697f6a1189dbe0103604b619f5ca`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfc61f65df60ef9b0388537e5876063cd37269cde97577fbb9cdc488230afe0`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:9c2557085ad68b5571b358134d36f2754b98a3ecb6882d6fd39a108e7180b090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522da17433e7ff04443725fdae9470d541ce7b230974c06928d9b00072a85a37`

```dockerfile
```

-	Layers:
	-	`sha256:67874486df4d385d50d3bcfc818bc8427ee8992e7228812841386fcb4f9dc903`  
		Last Modified: Thu, 07 Aug 2025 17:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-dind-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:88bf2ba4673e2963049952ad60d46389e6d2be3d31f0f4d1d69c55e0712d22a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136102855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0680e652cec44e947fd5401c80526cad1e184420cc2645f6399d102127e5bbf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f90fb8179789820d09ee62a252a0b5d2007f1e6a0116dc93cef396028b74`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 7.1 MB (7140514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e7ada02315c507aa603b515c8af64560c37e3b0c3e1ae602c926a39f0e193`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 99.3 KB (99312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0bce22e68e3e822e795bdd12fcda8fe4d3374269c9031570e52e4989e30cc`  
		Last Modified: Tue, 29 Jul 2025 17:07:42 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94302614c7eb1b832998ebf0e2a380369fcc6c23e0fa4bab8669b02665af8558`  
		Last Modified: Tue, 29 Jul 2025 17:07:38 GMT  
		Size: 57.5 MB (57464791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6fb8714059d9cacf4db01465f092fa2bfbaebc073ecf76e620e3776406896`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d9a1a1a08782f599a9be2fe288ef0cbd4aa9a049d7b515137cf06ff00f2ba`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:9e688304c06587ce1c71a3409b301f476dc1fd9b67ee40cf659e180e174582d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878a9b4d22bd08a4e39e541ae7b4ca75ac8e62370ac53573fa18a05338573ec4`

```dockerfile
```

-	Layers:
	-	`sha256:e0a4c2285c0b8b2afc33b86867190ce402deccb8def5a4573f617737a1c16087`  
		Last Modified: Tue, 29 Jul 2025 20:07:33 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.3-dind-rootless`

```console
$ docker pull docker@sha256:0fa4819d7978945b730c21fafb4b795bba05e486ceae04fbf1871a920082f2a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.3.3-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e039e40debc22c3cab8f5bee7f63b70c559c55b940f60a12dca61d2b9d28b096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166384612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e02ef5f5cabe9695528ed4a1d27d7c4ff5b08b682d29a752bf84acdb8150f9b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8791499fa9bdef98d7e3a188725e48e8c8dba0180702d559340747beef3519c`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 6.9 MB (6905701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fadee7df1b34bce659502e94099411a4bcea4f3b4b5703acdea29f43f10435d`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 90.2 KB (90225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585c63523750cbc3e625b48e735c70327c58c50817730a4f0ccfa5bca404699a`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ef36d1f42ecc72cee33f9b3630df040c2b3c0129388095caa52aa65663b6b`  
		Last Modified: Tue, 29 Jul 2025 17:08:29 GMT  
		Size: 62.5 MB (62516136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa56a13dffa7d647581a8133c12b84570ac763f9c5a281a0762d56e2cf50c5`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae60b320044d4dddd57522c6c3ddcd806948664e3b77e4b4f3dfdbcbb154bb`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3287871b8ca8572ddc7e051c61124c5d7b8d170b4afa30990972ecc32d2b1ece`  
		Last Modified: Tue, 29 Jul 2025 18:08:07 GMT  
		Size: 3.4 MB (3398338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c461874a9c04227f0bb239173b4ada58d4db9ae8822f866bf3869a0a112547`  
		Last Modified: Tue, 29 Jul 2025 18:08:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e93b4300a29b1f4578589daaa971b85425d6933fc13a844fad5d06e910ad23`  
		Last Modified: Tue, 29 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7016b5b02df5fdd9973630f913712193bc9276e47e3ac3eec14c29e694a4ff7`  
		Last Modified: Tue, 29 Jul 2025 18:08:10 GMT  
		Size: 17.6 MB (17584103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed2e953d4988003d64d426d269de70faa9c883a584158b5051029ea4f95a5cd`  
		Last Modified: Tue, 29 Jul 2025 18:08:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d3dd8c5f4e079aa9cc4a9deb31657fac070b425f2c95fc433839bd1fd9d1ff37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320768a07adb0a8b788d5f39c7d266fb5f45092252fa70bf78fa0767a653d068`

```dockerfile
```

-	Layers:
	-	`sha256:0222f5bf30363b640dfe6720d68d54f7f37a192fef439f4610ffae517243dc33`  
		Last Modified: Tue, 29 Jul 2025 20:07:40 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.3-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:412f7ef33b757bf61e5a858aee1d37534d091731e94701e1c0b3c448902c4f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157509962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6709bbcb068f2c6e78025d69110cc5eec100dda035be262877ece8e79dc47bf8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f90fb8179789820d09ee62a252a0b5d2007f1e6a0116dc93cef396028b74`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 7.1 MB (7140514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e7ada02315c507aa603b515c8af64560c37e3b0c3e1ae602c926a39f0e193`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 99.3 KB (99312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0bce22e68e3e822e795bdd12fcda8fe4d3374269c9031570e52e4989e30cc`  
		Last Modified: Tue, 29 Jul 2025 17:07:42 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94302614c7eb1b832998ebf0e2a380369fcc6c23e0fa4bab8669b02665af8558`  
		Last Modified: Tue, 29 Jul 2025 17:07:38 GMT  
		Size: 57.5 MB (57464791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6fb8714059d9cacf4db01465f092fa2bfbaebc073ecf76e620e3776406896`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d9a1a1a08782f599a9be2fe288ef0cbd4aa9a049d7b515137cf06ff00f2ba`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de9b74ceab4068500d9e2bd01dfbe28d9de34020baf094c75a035f0e91dfe1c`  
		Last Modified: Tue, 29 Jul 2025 18:46:21 GMT  
		Size: 3.4 MB (3389783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e12d9582745618468bfbb94957b902ef8680c42836cd87af3abf1575c781300`  
		Last Modified: Tue, 29 Jul 2025 18:07:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137bbfcf556b45f0503de2e6587e5b717626e5aa84a74c48aaf42e25dc3748cd`  
		Last Modified: Tue, 29 Jul 2025 18:07:16 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c805ba216a001613d2cdde121482c9dd36550a2e1ecd0ca969822c07c6531448`  
		Last Modified: Tue, 29 Jul 2025 18:07:17 GMT  
		Size: 18.0 MB (18015980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3570e64b17160d03028caf56f4281afdaa55b29f7ef12727e24e0f2eab4a94`  
		Last Modified: Tue, 29 Jul 2025 18:07:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:5eb8f2deebe35b46795fecf8b10896f8a18edb8d193d4c729422528a3d65dccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7798353e96b504dbfbcc6f16bb93a06387185b9fb064ccfa7cef1c08283dc9a5`

```dockerfile
```

-	Layers:
	-	`sha256:9bbdf146cca0e581ca098844347a2e1a7a0d50fe603ae68b979d28455fb9e345`  
		Last Modified: Tue, 29 Jul 2025 20:07:44 GMT  
		Size: 30.8 KB (30801 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.3-windowsservercore`

```console
$ docker pull docker@sha256:32d6e626f79e39b5cc83a10d4fcc2fd8f090cf2052298b7081c073d05d6788b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `docker:28.3.3-windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fce944f1be9964c27dffe70ea4e05f43906e5c35d7f1d1f319ea241e6ff7766b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565385109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e16746b5d96d8f01c428a46027b16342e56a3f351d9e94cc23c4884e182a23`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:26:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:27:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:06 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:27:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:27:16 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:27:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d49ded649af742ac4e8aff9b2beba88841a34f5ac3c9cad1b2cbbb85a8a1741`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4901ee3ae2f2d3da5d2455d57c8497cdcd54fa3981e3eced30f632522080c987`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 356.9 KB (356904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cce2887577005a99bc013670c90c46c419da33c604d06b159d5a10bf40d3cb`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d727c7396ced4e810c63f727df20e45e76ebd1775b108e32a902fac6b6478076`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcfd1f605909b895b191bbc1dce66175acc45a5add136bc5a0ae4f36ecd8989`  
		Last Modified: Tue, 12 Aug 2025 20:31:31 GMT  
		Size: 20.8 MB (20837962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e6ab5bf2d2d618100a885f27c393467212c0570eaa7ea84e6ea8219e5dc291`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b884b8cda3f7df7bffd4252d58e7d9152d914e0d920161dfc1b2bbf477829d45`  
		Last Modified: Tue, 12 Aug 2025 20:31:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7094f59558defd3124f897718f374e4c7adb853752582ba8e4f3684c14b3e16a`  
		Last Modified: Tue, 12 Aug 2025 20:31:14 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7051fc3fd3e4df1ca961e28ab2cd07384069c0c2872b4680f672075663b48034`  
		Last Modified: Tue, 12 Aug 2025 20:31:20 GMT  
		Size: 23.0 MB (22953510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a709cde7693b4592561374d3dddec696b50b1a107e69458552265acbbf21459e`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d45050aa1c7e9ea58879bcb46bbf075e263acc49748dcd9a19068713b52e59`  
		Last Modified: Tue, 12 Aug 2025 20:31:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31e15e6414199a0fa232b38e3b810fa3806c10634d77fbde8642407b62f90f1`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4abea89efff9a4dcaee678846541ee7471b0d5e13f11a1ffd50c601da438141`  
		Last Modified: Tue, 12 Aug 2025 20:31:21 GMT  
		Size: 22.4 MB (22394336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.3.3-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:b08584be840c5fffd7d99e62ab49eae4c3f6636a8843cce35a5bd1067720e0ab
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348189021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732e79d977df1d9edff845acd89fee0b2122dfd3500338862d0c073f12710e29`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:25:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:06 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:26:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:26:19 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:26:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:26:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:26:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:26:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37ee622e1d3856c0f56d0e073b50e34ad5239aa1e8a0d7b93f11fb38230099f`  
		Last Modified: Tue, 12 Aug 2025 20:28:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04848d212a98717392544afa4ddeeef71992d66bba2d6eef616660649835eece`  
		Last Modified: Tue, 12 Aug 2025 20:28:14 GMT  
		Size: 346.1 KB (346147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e3cc07ce8c5cb86d5dd9907546bc97af931be4eef1e23a908c40d2ab28a68`  
		Last Modified: Tue, 12 Aug 2025 20:51:41 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188521c2085d7c3dbbbae5485b4fc383b0516ff6e9a27a023df6aca63dbb7459`  
		Last Modified: Tue, 12 Aug 2025 20:51:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581d2a99a5e27e493c9517fcb5d27c165f5696ad1d8f08f568d60eee1e8d6fcc`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 20.8 MB (20826824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e88f9f3cb2e7be25dbdc4626eb3bcbc619924d0c61d64356d2d7a8e3fc4a661`  
		Last Modified: Tue, 12 Aug 2025 20:51:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70bf9f40001314e26858770cf903764c3dc5e0c1278e072fa7daf620846745`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6079589750abcc6d3eb81778c4a2837ea2dc0467112980d886173696e4c9df`  
		Last Modified: Tue, 12 Aug 2025 20:51:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65174c16d8c061f85019c62493afae8d5db2f56e1a831a94c02db515515626d`  
		Last Modified: Tue, 12 Aug 2025 20:51:50 GMT  
		Size: 22.9 MB (22937256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728f806f53c767bd20bb97653fa5b5e3016a8e4af213a950135d9105930ac520`  
		Last Modified: Tue, 12 Aug 2025 20:51:48 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b5ab841f285aa2a8a9238b3c57bede8d2a91a3763c0f584275508deefcbdf5`  
		Last Modified: Tue, 12 Aug 2025 20:51:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae017706cc10313aa38b24d9c7c4dc2901f7f1ea62598f22aa0639e40d14cba0`  
		Last Modified: Tue, 12 Aug 2025 20:51:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bac6b791dfaef6e7c36ef93b178cc273d730b229d9112ceadede006ad1bc0a6`  
		Last Modified: Tue, 12 Aug 2025 20:51:56 GMT  
		Size: 22.4 MB (22375244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3.3-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:7a3b2e07b931434a99cd7f00343a6fd5b6a618598e9cc4746313aaca3de5aaa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `docker:28.3.3-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:b08584be840c5fffd7d99e62ab49eae4c3f6636a8843cce35a5bd1067720e0ab
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348189021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732e79d977df1d9edff845acd89fee0b2122dfd3500338862d0c073f12710e29`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:25:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:06 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:26:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:26:19 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:26:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:26:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:26:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:26:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37ee622e1d3856c0f56d0e073b50e34ad5239aa1e8a0d7b93f11fb38230099f`  
		Last Modified: Tue, 12 Aug 2025 20:28:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04848d212a98717392544afa4ddeeef71992d66bba2d6eef616660649835eece`  
		Last Modified: Tue, 12 Aug 2025 20:28:14 GMT  
		Size: 346.1 KB (346147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e3cc07ce8c5cb86d5dd9907546bc97af931be4eef1e23a908c40d2ab28a68`  
		Last Modified: Tue, 12 Aug 2025 20:51:41 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188521c2085d7c3dbbbae5485b4fc383b0516ff6e9a27a023df6aca63dbb7459`  
		Last Modified: Tue, 12 Aug 2025 20:51:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581d2a99a5e27e493c9517fcb5d27c165f5696ad1d8f08f568d60eee1e8d6fcc`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 20.8 MB (20826824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e88f9f3cb2e7be25dbdc4626eb3bcbc619924d0c61d64356d2d7a8e3fc4a661`  
		Last Modified: Tue, 12 Aug 2025 20:51:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70bf9f40001314e26858770cf903764c3dc5e0c1278e072fa7daf620846745`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6079589750abcc6d3eb81778c4a2837ea2dc0467112980d886173696e4c9df`  
		Last Modified: Tue, 12 Aug 2025 20:51:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65174c16d8c061f85019c62493afae8d5db2f56e1a831a94c02db515515626d`  
		Last Modified: Tue, 12 Aug 2025 20:51:50 GMT  
		Size: 22.9 MB (22937256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728f806f53c767bd20bb97653fa5b5e3016a8e4af213a950135d9105930ac520`  
		Last Modified: Tue, 12 Aug 2025 20:51:48 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b5ab841f285aa2a8a9238b3c57bede8d2a91a3763c0f584275508deefcbdf5`  
		Last Modified: Tue, 12 Aug 2025 20:51:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae017706cc10313aa38b24d9c7c4dc2901f7f1ea62598f22aa0639e40d14cba0`  
		Last Modified: Tue, 12 Aug 2025 20:51:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bac6b791dfaef6e7c36ef93b178cc273d730b229d9112ceadede006ad1bc0a6`  
		Last Modified: Tue, 12 Aug 2025 20:51:56 GMT  
		Size: 22.4 MB (22375244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3.3-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a188802ccb2fc99331e286bf343b9ad5721c2fcf498565d8a6990f9642e3f046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `docker:28.3.3-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fce944f1be9964c27dffe70ea4e05f43906e5c35d7f1d1f319ea241e6ff7766b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565385109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e16746b5d96d8f01c428a46027b16342e56a3f351d9e94cc23c4884e182a23`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:26:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:27:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:06 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:27:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:27:16 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:27:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d49ded649af742ac4e8aff9b2beba88841a34f5ac3c9cad1b2cbbb85a8a1741`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4901ee3ae2f2d3da5d2455d57c8497cdcd54fa3981e3eced30f632522080c987`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 356.9 KB (356904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cce2887577005a99bc013670c90c46c419da33c604d06b159d5a10bf40d3cb`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d727c7396ced4e810c63f727df20e45e76ebd1775b108e32a902fac6b6478076`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcfd1f605909b895b191bbc1dce66175acc45a5add136bc5a0ae4f36ecd8989`  
		Last Modified: Tue, 12 Aug 2025 20:31:31 GMT  
		Size: 20.8 MB (20837962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e6ab5bf2d2d618100a885f27c393467212c0570eaa7ea84e6ea8219e5dc291`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b884b8cda3f7df7bffd4252d58e7d9152d914e0d920161dfc1b2bbf477829d45`  
		Last Modified: Tue, 12 Aug 2025 20:31:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7094f59558defd3124f897718f374e4c7adb853752582ba8e4f3684c14b3e16a`  
		Last Modified: Tue, 12 Aug 2025 20:31:14 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7051fc3fd3e4df1ca961e28ab2cd07384069c0c2872b4680f672075663b48034`  
		Last Modified: Tue, 12 Aug 2025 20:31:20 GMT  
		Size: 23.0 MB (22953510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a709cde7693b4592561374d3dddec696b50b1a107e69458552265acbbf21459e`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d45050aa1c7e9ea58879bcb46bbf075e263acc49748dcd9a19068713b52e59`  
		Last Modified: Tue, 12 Aug 2025 20:31:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31e15e6414199a0fa232b38e3b810fa3806c10634d77fbde8642407b62f90f1`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4abea89efff9a4dcaee678846541ee7471b0d5e13f11a1ffd50c601da438141`  
		Last Modified: Tue, 12 Aug 2025 20:31:21 GMT  
		Size: 22.4 MB (22394336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:d87c674b7f01043207f1badc6e86e1f8bc33a90981c2f31f3e0f57c1ecb0c5cc
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
$ docker pull docker@sha256:e47e07b4616ad120a5e3812a315c0adb0a80d17eb19c979271dd3b16416226bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75882770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef97129ecf899446838ff807b2d675d8a1e30f2dac9af363534872b88f7b3def`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:019dbf214cb0eaa7943816f0cc580437ccae2ef546bf1bcff82e5b51ab2ca91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86120028f5d4320014588ac17e4563c14713f8a385d8e192c8229475f8ff6c35`

```dockerfile
```

-	Layers:
	-	`sha256:13645690d79e822200fb314c8947b0437ed272113942e70c5e93b9215ac0c449`  
		Last Modified: Tue, 29 Jul 2025 17:07:43 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:8f845ca7eb3d2dab949a1321d7ba195c8f690a89eb313190e35c32687d2a507b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70810451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b83d2189eeff2d9c339890963393fb464d80828d8b043a20894478fe3ffee1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f822c2573de7e9c67a5c71e3631064c5bcc0ea4209e1599a17c1acfeaaf1af`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 18.5 MB (18451848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd472c4b566302d5ccb09e4bc30d193d93f2127195f039fcc1e4c2e6384fd1`  
		Last Modified: Tue, 29 Jul 2025 16:50:49 GMT  
		Size: 20.6 MB (20568606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e39b3b275050311240d86f4184b92738124227ab91074f2d543353027e9ee`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 20.2 MB (20183248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fcfc43ab15c1da7e48f821e25c54c51d723b64684b20d2a4b4edff8e04dcc3`  
		Last Modified: Tue, 29 Jul 2025 16:50:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563338bb8fe09f3e62c3a07902962cba52ef8de211de1bda00ead94befe4d6c6`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d5bc334980f311595207402ce2300f8a11e1e71eb800bd573dcdfcbbb7383`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:f1537ca07297772da32b2e246c50c1dea5ebad32ae760a9b9b7ccb94eaad29c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f65333c983620826c8527af4e58d432a3ee0ae31df3f9b51352442ccfdf7595`

```dockerfile
```

-	Layers:
	-	`sha256:b1609329088ee42b557625a4e309152f4ae582a5feb24069e6b4ac2a02371377`  
		Last Modified: Tue, 29 Jul 2025 17:07:26 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:c63fc02e3bb2c71c1e39d9618770900f16aeccddb8d13a517c16752f113a7fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69807384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c236c8ccc2e365a65223161398d002ebd5f6d7a8499070bd805ec062050a149f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fda06620cb3acbe8d29e62b35edf4eab73bd1796050a544bac974a28f5fd99`  
		Last Modified: Tue, 29 Jul 2025 17:13:20 GMT  
		Size: 18.4 MB (18441097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab513f15d8a635f59bcbe656922221d344bfc6c7d6c78e0b69a118c025c543b5`  
		Last Modified: Tue, 29 Jul 2025 17:13:21 GMT  
		Size: 20.5 MB (20548892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ff39cd4cd7f51997cb5ef915890dd813cd17afa5822471bc9fcf70b903121`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 20.2 MB (20166234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb6e886463cf3968d42871b95c8d48e815d647d699e9512783a2ef44fa0f64`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672297f80502d6989f94397992684d739879955ca812c635d7d02bbd1c82ba0`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269088758c4eb6e7275e58a86756108338d7e30a284edf53331fca7f4a88b0a5`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:324a1f85dda8d36fcd3250fec9cca2ed582c781a8c5ebfded37a04ac8840aa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82360f4e5611e16371e1b1bf406b68e64ff5640d3207b215c35251543cc4956`

```dockerfile
```

-	Layers:
	-	`sha256:3ffc99fef904d345817e2028615cef8ce8299be6c0754569973a322b26a2cad5`  
		Last Modified: Tue, 29 Jul 2025 20:07:33 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2b6312fd57e7b24ffae3ace014357496da75c7d3b7bd15455987364d5805999c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71392240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324b3c32e29caad939b212c3d18aa70ad98a23579154b2254f63b19284e09046`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:b00a03f6a893ff05072a6aec1f14baab706cadb23df8f3472eca7a730139ff6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c33d99fbb568b26e841daf1694e071995a07b8dd92bbc7c1414abe997adbc70`

```dockerfile
```

-	Layers:
	-	`sha256:278de4bd27c29d5f7783b8e9211f0b5596e91aab67d37d191bd0e5df0b2a41e9`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:c0872aae4791ff427e6eda52769afa04f17b5cf756f8267e0d52774c99d5c9de
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
$ docker pull docker@sha256:acf2e2d09cedf21fa8f27bb0962674e33e159c744c152b248f1f7f43623ccd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145400826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a8bf985f76be7345c0c827c568db287ccb4dfad919a4693488224e3644fb0c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8791499fa9bdef98d7e3a188725e48e8c8dba0180702d559340747beef3519c`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 6.9 MB (6905701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fadee7df1b34bce659502e94099411a4bcea4f3b4b5703acdea29f43f10435d`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 90.2 KB (90225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585c63523750cbc3e625b48e735c70327c58c50817730a4f0ccfa5bca404699a`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ef36d1f42ecc72cee33f9b3630df040c2b3c0129388095caa52aa65663b6b`  
		Last Modified: Tue, 29 Jul 2025 17:08:29 GMT  
		Size: 62.5 MB (62516136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa56a13dffa7d647581a8133c12b84570ac763f9c5a281a0762d56e2cf50c5`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae60b320044d4dddd57522c6c3ddcd806948664e3b77e4b4f3dfdbcbb154bb`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:b07ec0abd0eacbbb7a5caff69421dcf417d11e841cd6c39914c6350ec8ead6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3b72142c672a9277787f2a650dfe1c3d5ec96a77d3dfb1b30ee99fd35cfbbb`

```dockerfile
```

-	Layers:
	-	`sha256:810146a77372683cd7bd8b4e79c73015f3d7c76c01b681379c962de5166e83d5`  
		Last Modified: Tue, 29 Jul 2025 20:07:23 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:1f082418e60bfdc41615178f3338a57e008be9e54a0a088bdaf7639e6440aa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136481510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b903ce9efae22aff353f3b148f4b81543338dda7c191abe851759db185d55660`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f822c2573de7e9c67a5c71e3631064c5bcc0ea4209e1599a17c1acfeaaf1af`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 18.5 MB (18451848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd472c4b566302d5ccb09e4bc30d193d93f2127195f039fcc1e4c2e6384fd1`  
		Last Modified: Tue, 29 Jul 2025 16:50:49 GMT  
		Size: 20.6 MB (20568606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e39b3b275050311240d86f4184b92738124227ab91074f2d543353027e9ee`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 20.2 MB (20183248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fcfc43ab15c1da7e48f821e25c54c51d723b64684b20d2a4b4edff8e04dcc3`  
		Last Modified: Tue, 29 Jul 2025 16:50:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563338bb8fe09f3e62c3a07902962cba52ef8de211de1bda00ead94befe4d6c6`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d5bc334980f311595207402ce2300f8a11e1e71eb800bd573dcdfcbbb7383`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44f5f22ffde31d78b179f8cd7410f20820e06caf28efa9a65355c29b1e2b10b`  
		Last Modified: Thu, 07 Aug 2025 16:57:01 GMT  
		Size: 7.2 MB (7230142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebba53fb812598805b6fc21226a04919f3781430ba936808b0f59d133c00e80`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 89.8 KB (89806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e516ec65aa3324f86b97988d15e6abcbe2d2cd5aa91eaa93c11d0119f0016b85`  
		Last Modified: Thu, 07 Aug 2025 16:57:00 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036456d63ef0cf8b17f84e9d6b0243b01f469739b1a7f24cfe71c25d87b89496`  
		Last Modified: Thu, 07 Aug 2025 16:57:05 GMT  
		Size: 58.3 MB (58345094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909c6394356186a1784dad76416d85e70821a8a0efdf5b9bc6084f7f4cad6dbc`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2bfa6563e19d5b6bf2937e08f7af0eeeef31f1d0da970fbb37bdc678a99e81`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:caf190c0124eba00b01a8690ce7a05f806d0cf5ba34877fdf387e41444f3aeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b22a0c050d02e7164da7a016f4a9e2934ce69b7b45be19137f526a4c3cd0a4b`

```dockerfile
```

-	Layers:
	-	`sha256:c8c17618f747eab2415d91d988104c720915211836b105288567df5c8ca9f095`  
		Last Modified: Thu, 07 Aug 2025 17:07:28 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:0e5e5db93aa3e8af23c2189c2f949f41637e51178bf775ddff251f72743345f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134624627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a94d5bea77d233423c8ec637c7ec3d4ae66c22b1a4f9b58c44d6a5b9084ae0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fda06620cb3acbe8d29e62b35edf4eab73bd1796050a544bac974a28f5fd99`  
		Last Modified: Tue, 29 Jul 2025 17:13:20 GMT  
		Size: 18.4 MB (18441097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab513f15d8a635f59bcbe656922221d344bfc6c7d6c78e0b69a118c025c543b5`  
		Last Modified: Tue, 29 Jul 2025 17:13:21 GMT  
		Size: 20.5 MB (20548892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ff39cd4cd7f51997cb5ef915890dd813cd17afa5822471bc9fcf70b903121`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 20.2 MB (20166234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb6e886463cf3968d42871b95c8d48e815d647d699e9512783a2ef44fa0f64`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672297f80502d6989f94397992684d739879955ca812c635d7d02bbd1c82ba0`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269088758c4eb6e7275e58a86756108338d7e30a284edf53331fca7f4a88b0a5`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df050d7dc2c286cb6eb89f5f6074f0e2050b5647fac156e97e954bb586e0c977`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 6.5 MB (6538354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfde1691582119bdf48b4b13b8ec970dc7ea3fee792a9dcb2e806abbbb6939e`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 86.2 KB (86243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea99a75781859a140708f0f46a3c77bf434229b777a07580312f1f7051f87f50`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6cd3c5f53aed54fbcbdee772d968d063922cdb9ccaaf39af1ed46362650de`  
		Last Modified: Thu, 07 Aug 2025 14:58:09 GMT  
		Size: 58.2 MB (58186632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d193787930eddbb555cddea45342d37ec90697f6a1189dbe0103604b619f5ca`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfc61f65df60ef9b0388537e5876063cd37269cde97577fbb9cdc488230afe0`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:9c2557085ad68b5571b358134d36f2754b98a3ecb6882d6fd39a108e7180b090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522da17433e7ff04443725fdae9470d541ce7b230974c06928d9b00072a85a37`

```dockerfile
```

-	Layers:
	-	`sha256:67874486df4d385d50d3bcfc818bc8427ee8992e7228812841386fcb4f9dc903`  
		Last Modified: Thu, 07 Aug 2025 17:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:88bf2ba4673e2963049952ad60d46389e6d2be3d31f0f4d1d69c55e0712d22a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136102855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0680e652cec44e947fd5401c80526cad1e184420cc2645f6399d102127e5bbf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f90fb8179789820d09ee62a252a0b5d2007f1e6a0116dc93cef396028b74`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 7.1 MB (7140514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e7ada02315c507aa603b515c8af64560c37e3b0c3e1ae602c926a39f0e193`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 99.3 KB (99312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0bce22e68e3e822e795bdd12fcda8fe4d3374269c9031570e52e4989e30cc`  
		Last Modified: Tue, 29 Jul 2025 17:07:42 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94302614c7eb1b832998ebf0e2a380369fcc6c23e0fa4bab8669b02665af8558`  
		Last Modified: Tue, 29 Jul 2025 17:07:38 GMT  
		Size: 57.5 MB (57464791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6fb8714059d9cacf4db01465f092fa2bfbaebc073ecf76e620e3776406896`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d9a1a1a08782f599a9be2fe288ef0cbd4aa9a049d7b515137cf06ff00f2ba`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:9e688304c06587ce1c71a3409b301f476dc1fd9b67ee40cf659e180e174582d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878a9b4d22bd08a4e39e541ae7b4ca75ac8e62370ac53573fa18a05338573ec4`

```dockerfile
```

-	Layers:
	-	`sha256:e0a4c2285c0b8b2afc33b86867190ce402deccb8def5a4573f617737a1c16087`  
		Last Modified: Tue, 29 Jul 2025 20:07:33 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:0fa4819d7978945b730c21fafb4b795bba05e486ceae04fbf1871a920082f2a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:e039e40debc22c3cab8f5bee7f63b70c559c55b940f60a12dca61d2b9d28b096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166384612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e02ef5f5cabe9695528ed4a1d27d7c4ff5b08b682d29a752bf84acdb8150f9b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8791499fa9bdef98d7e3a188725e48e8c8dba0180702d559340747beef3519c`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 6.9 MB (6905701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fadee7df1b34bce659502e94099411a4bcea4f3b4b5703acdea29f43f10435d`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 90.2 KB (90225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585c63523750cbc3e625b48e735c70327c58c50817730a4f0ccfa5bca404699a`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ef36d1f42ecc72cee33f9b3630df040c2b3c0129388095caa52aa65663b6b`  
		Last Modified: Tue, 29 Jul 2025 17:08:29 GMT  
		Size: 62.5 MB (62516136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa56a13dffa7d647581a8133c12b84570ac763f9c5a281a0762d56e2cf50c5`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae60b320044d4dddd57522c6c3ddcd806948664e3b77e4b4f3dfdbcbb154bb`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3287871b8ca8572ddc7e051c61124c5d7b8d170b4afa30990972ecc32d2b1ece`  
		Last Modified: Tue, 29 Jul 2025 18:08:07 GMT  
		Size: 3.4 MB (3398338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c461874a9c04227f0bb239173b4ada58d4db9ae8822f866bf3869a0a112547`  
		Last Modified: Tue, 29 Jul 2025 18:08:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e93b4300a29b1f4578589daaa971b85425d6933fc13a844fad5d06e910ad23`  
		Last Modified: Tue, 29 Jul 2025 18:08:06 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7016b5b02df5fdd9973630f913712193bc9276e47e3ac3eec14c29e694a4ff7`  
		Last Modified: Tue, 29 Jul 2025 18:08:10 GMT  
		Size: 17.6 MB (17584103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed2e953d4988003d64d426d269de70faa9c883a584158b5051029ea4f95a5cd`  
		Last Modified: Tue, 29 Jul 2025 18:08:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d3dd8c5f4e079aa9cc4a9deb31657fac070b425f2c95fc433839bd1fd9d1ff37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320768a07adb0a8b788d5f39c7d266fb5f45092252fa70bf78fa0767a653d068`

```dockerfile
```

-	Layers:
	-	`sha256:0222f5bf30363b640dfe6720d68d54f7f37a192fef439f4610ffae517243dc33`  
		Last Modified: Tue, 29 Jul 2025 20:07:40 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:412f7ef33b757bf61e5a858aee1d37534d091731e94701e1c0b3c448902c4f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157509962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6709bbcb068f2c6e78025d69110cc5eec100dda035be262877ece8e79dc47bf8`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f90fb8179789820d09ee62a252a0b5d2007f1e6a0116dc93cef396028b74`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 7.1 MB (7140514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e7ada02315c507aa603b515c8af64560c37e3b0c3e1ae602c926a39f0e193`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 99.3 KB (99312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0bce22e68e3e822e795bdd12fcda8fe4d3374269c9031570e52e4989e30cc`  
		Last Modified: Tue, 29 Jul 2025 17:07:42 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94302614c7eb1b832998ebf0e2a380369fcc6c23e0fa4bab8669b02665af8558`  
		Last Modified: Tue, 29 Jul 2025 17:07:38 GMT  
		Size: 57.5 MB (57464791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6fb8714059d9cacf4db01465f092fa2bfbaebc073ecf76e620e3776406896`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d9a1a1a08782f599a9be2fe288ef0cbd4aa9a049d7b515137cf06ff00f2ba`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de9b74ceab4068500d9e2bd01dfbe28d9de34020baf094c75a035f0e91dfe1c`  
		Last Modified: Tue, 29 Jul 2025 18:46:21 GMT  
		Size: 3.4 MB (3389783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e12d9582745618468bfbb94957b902ef8680c42836cd87af3abf1575c781300`  
		Last Modified: Tue, 29 Jul 2025 18:07:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137bbfcf556b45f0503de2e6587e5b717626e5aa84a74c48aaf42e25dc3748cd`  
		Last Modified: Tue, 29 Jul 2025 18:07:16 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c805ba216a001613d2cdde121482c9dd36550a2e1ecd0ca969822c07c6531448`  
		Last Modified: Tue, 29 Jul 2025 18:07:17 GMT  
		Size: 18.0 MB (18015980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3570e64b17160d03028caf56f4281afdaa55b29f7ef12727e24e0f2eab4a94`  
		Last Modified: Tue, 29 Jul 2025 18:07:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:5eb8f2deebe35b46795fecf8b10896f8a18edb8d193d4c729422528a3d65dccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7798353e96b504dbfbcc6f16bb93a06387185b9fb064ccfa7cef1c08283dc9a5`

```dockerfile
```

-	Layers:
	-	`sha256:9bbdf146cca0e581ca098844347a2e1a7a0d50fe603ae68b979d28455fb9e345`  
		Last Modified: Tue, 29 Jul 2025 20:07:44 GMT  
		Size: 30.8 KB (30801 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:c0872aae4791ff427e6eda52769afa04f17b5cf756f8267e0d52774c99d5c9de
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
$ docker pull docker@sha256:acf2e2d09cedf21fa8f27bb0962674e33e159c744c152b248f1f7f43623ccd82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145400826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a8bf985f76be7345c0c827c568db287ccb4dfad919a4693488224e3644fb0c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ebeacb5069e0ef8d56ccb1434aba74d8b32eb24d4c40e8ce4292d7cbeb26de`  
		Last Modified: Tue, 29 Jul 2025 16:31:15 GMT  
		Size: 8.2 MB (8198118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c513a0a32cd63d199cf4b0acf40c8616dcef3bfd62843207ac008e9da80bf`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c23551ae3e5435972be063b594fd55a1397211c845621bf0b240da3581f2d`  
		Last Modified: Tue, 29 Jul 2025 16:31:18 GMT  
		Size: 20.5 MB (20469499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e2e8a4d1616149136a0af9eff1e4dc8355495243a182432a353e992d85dbf`  
		Last Modified: Tue, 29 Jul 2025 16:31:16 GMT  
		Size: 22.0 MB (21957234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102b158915f6747b88c1cd650daadc2fc149c11ea76b7f1daa3bc1e044be3e54`  
		Last Modified: Tue, 29 Jul 2025 16:31:17 GMT  
		Size: 21.5 MB (21456077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f5c9f196526fbb5e25d3ba912eb011d4ffa9573e4bf5e0d8811f1a579c3070`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de31166e21da29b3bdcef0295121e678fef4d5295284dea2cc7658ef7c6477d`  
		Last Modified: Tue, 29 Jul 2025 16:31:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45275556821f5f32c9c52099d801009f2d8de70a62cee232069e664a536adfc5`  
		Last Modified: Tue, 29 Jul 2025 16:31:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8791499fa9bdef98d7e3a188725e48e8c8dba0180702d559340747beef3519c`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 6.9 MB (6905701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fadee7df1b34bce659502e94099411a4bcea4f3b4b5703acdea29f43f10435d`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 90.2 KB (90225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585c63523750cbc3e625b48e735c70327c58c50817730a4f0ccfa5bca404699a`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66ef36d1f42ecc72cee33f9b3630df040c2b3c0129388095caa52aa65663b6b`  
		Last Modified: Tue, 29 Jul 2025 17:08:29 GMT  
		Size: 62.5 MB (62516136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa56a13dffa7d647581a8133c12b84570ac763f9c5a281a0762d56e2cf50c5`  
		Last Modified: Tue, 29 Jul 2025 17:08:20 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae60b320044d4dddd57522c6c3ddcd806948664e3b77e4b4f3dfdbcbb154bb`  
		Last Modified: Tue, 29 Jul 2025 17:08:21 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:b07ec0abd0eacbbb7a5caff69421dcf417d11e841cd6c39914c6350ec8ead6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3b72142c672a9277787f2a650dfe1c3d5ec96a77d3dfb1b30ee99fd35cfbbb`

```dockerfile
```

-	Layers:
	-	`sha256:810146a77372683cd7bd8b4e79c73015f3d7c76c01b681379c962de5166e83d5`  
		Last Modified: Tue, 29 Jul 2025 20:07:23 GMT  
		Size: 34.6 KB (34590 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:1f082418e60bfdc41615178f3338a57e008be9e54a0a088bdaf7639e6440aa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136481510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b903ce9efae22aff353f3b148f4b81543338dda7c191abe851759db185d55660`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e2e128338d7b57fe23c975f30ee044e5f34c140bb5105d91bb65870022d122`  
		Last Modified: Tue, 15 Jul 2025 19:25:48 GMT  
		Size: 8.1 MB (8103674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5fc805728e8696dc9feee5a1184d3347245d314ae226e2819063aefa98f7cb`  
		Last Modified: Tue, 15 Jul 2025 19:25:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f822c2573de7e9c67a5c71e3631064c5bcc0ea4209e1599a17c1acfeaaf1af`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 18.5 MB (18451848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fd472c4b566302d5ccb09e4bc30d193d93f2127195f039fcc1e4c2e6384fd1`  
		Last Modified: Tue, 29 Jul 2025 16:50:49 GMT  
		Size: 20.6 MB (20568606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550e39b3b275050311240d86f4184b92738124227ab91074f2d543353027e9ee`  
		Last Modified: Tue, 29 Jul 2025 16:50:50 GMT  
		Size: 20.2 MB (20183248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fcfc43ab15c1da7e48f821e25c54c51d723b64684b20d2a4b4edff8e04dcc3`  
		Last Modified: Tue, 29 Jul 2025 16:50:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563338bb8fe09f3e62c3a07902962cba52ef8de211de1bda00ead94befe4d6c6`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d5bc334980f311595207402ce2300f8a11e1e71eb800bd573dcdfcbbb7383`  
		Last Modified: Tue, 29 Jul 2025 16:50:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44f5f22ffde31d78b179f8cd7410f20820e06caf28efa9a65355c29b1e2b10b`  
		Last Modified: Thu, 07 Aug 2025 16:57:01 GMT  
		Size: 7.2 MB (7230142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebba53fb812598805b6fc21226a04919f3781430ba936808b0f59d133c00e80`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 89.8 KB (89806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e516ec65aa3324f86b97988d15e6abcbe2d2cd5aa91eaa93c11d0119f0016b85`  
		Last Modified: Thu, 07 Aug 2025 16:57:00 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036456d63ef0cf8b17f84e9d6b0243b01f469739b1a7f24cfe71c25d87b89496`  
		Last Modified: Thu, 07 Aug 2025 16:57:05 GMT  
		Size: 58.3 MB (58345094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909c6394356186a1784dad76416d85e70821a8a0efdf5b9bc6084f7f4cad6dbc`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2bfa6563e19d5b6bf2937e08f7af0eeeef31f1d0da970fbb37bdc678a99e81`  
		Last Modified: Thu, 07 Aug 2025 16:56:59 GMT  
		Size: 3.3 KB (3307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:caf190c0124eba00b01a8690ce7a05f806d0cf5ba34877fdf387e41444f3aeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b22a0c050d02e7164da7a016f4a9e2934ce69b7b45be19137f526a4c3cd0a4b`

```dockerfile
```

-	Layers:
	-	`sha256:c8c17618f747eab2415d91d988104c720915211836b105288567df5c8ca9f095`  
		Last Modified: Thu, 07 Aug 2025 17:07:28 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:0e5e5db93aa3e8af23c2189c2f949f41637e51178bf775ddff251f72743345f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134624627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a94d5bea77d233423c8ec637c7ec3d4ae66c22b1a4f9b58c44d6a5b9084ae0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba9d788a5b3b08a47d6e1c8e2daffd5e78ccc433a94f5a24ada8e6f5a1186f`  
		Last Modified: Tue, 22 Jul 2025 21:17:11 GMT  
		Size: 7.4 MB (7429958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802c8fa87e0b8a5c6fe53a29e741f385b211f0e5d77f552b54b18b9af0c6d6e`  
		Last Modified: Tue, 22 Jul 2025 21:17:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fda06620cb3acbe8d29e62b35edf4eab73bd1796050a544bac974a28f5fd99`  
		Last Modified: Tue, 29 Jul 2025 17:13:20 GMT  
		Size: 18.4 MB (18441097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab513f15d8a635f59bcbe656922221d344bfc6c7d6c78e0b69a118c025c543b5`  
		Last Modified: Tue, 29 Jul 2025 17:13:21 GMT  
		Size: 20.5 MB (20548892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6ff39cd4cd7f51997cb5ef915890dd813cd17afa5822471bc9fcf70b903121`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 20.2 MB (20166234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbb6e886463cf3968d42871b95c8d48e815d647d699e9512783a2ef44fa0f64`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672297f80502d6989f94397992684d739879955ca812c635d7d02bbd1c82ba0`  
		Last Modified: Tue, 29 Jul 2025 17:13:17 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269088758c4eb6e7275e58a86756108338d7e30a284edf53331fca7f4a88b0a5`  
		Last Modified: Tue, 29 Jul 2025 17:13:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df050d7dc2c286cb6eb89f5f6074f0e2050b5647fac156e97e954bb586e0c977`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 6.5 MB (6538354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfde1691582119bdf48b4b13b8ec970dc7ea3fee792a9dcb2e806abbbb6939e`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 86.2 KB (86243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea99a75781859a140708f0f46a3c77bf434229b777a07580312f1f7051f87f50`  
		Last Modified: Thu, 07 Aug 2025 14:57:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6cd3c5f53aed54fbcbdee772d968d063922cdb9ccaaf39af1ed46362650de`  
		Last Modified: Thu, 07 Aug 2025 14:58:09 GMT  
		Size: 58.2 MB (58186632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d193787930eddbb555cddea45342d37ec90697f6a1189dbe0103604b619f5ca`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfc61f65df60ef9b0388537e5876063cd37269cde97577fbb9cdc488230afe0`  
		Last Modified: Thu, 07 Aug 2025 14:57:54 GMT  
		Size: 3.3 KB (3305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:9c2557085ad68b5571b358134d36f2754b98a3ecb6882d6fd39a108e7180b090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522da17433e7ff04443725fdae9470d541ce7b230974c06928d9b00072a85a37`

```dockerfile
```

-	Layers:
	-	`sha256:67874486df4d385d50d3bcfc818bc8427ee8992e7228812841386fcb4f9dc903`  
		Last Modified: Thu, 07 Aug 2025 17:07:32 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:88bf2ba4673e2963049952ad60d46389e6d2be3d31f0f4d1d69c55e0712d22a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136102855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0680e652cec44e947fd5401c80526cad1e184420cc2645f6399d102127e5bbf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-amd64'; 			sha256='9451034b6ca5354e8bf88a2002a413aedabf110fd0f12ebb0b2f2cc241be8e41'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v6'; 			sha256='e9f89ed92231e937b380afc8f0105dc57e1fd5a3949a1545e863312706bf2947'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm-v7'; 			sha256='92fe156e22eabbb58fb6b44aa3c59c2c06a820b66913158ed209ef5e18abc356'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-arm64'; 			sha256='b610d3c24836b2e7fecab5ef2c9466239a0f0156993a0406ea58943b87bff918'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-ppc64le'; 			sha256='74a9c8856ef7e742b5193358b43c8dbea9dc739009e4894c840fdb0a9c746d0d'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-riscv64'; 			sha256='698496a08f9c008230e858c63590aeb44b4806df2d6f02cd0b382137ce9394c6'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.linux-s390x'; 			sha256='6b561cb99d105114484897a3bc3f105dead11d4c14f28ffbf0873ce7fd1fe2d6'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-x86_64'; 			sha256='a5ea28722d5da628b59226626f7d6c33c89a7ed19e39f750645925242044c9d2'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv6'; 			sha256='14a8a2fd5ca75cf87a9c33f79eea5b51701d3a2039387ae48440c9d78b2c83c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-armv7'; 			sha256='a97c785b148cf744e4f91835fa981dc93d6ced5132d42dab934947e33032af98'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-aarch64'; 			sha256='7b2627ed76f7dcb0d93f649f185af912372229b4c09762a3cd1db5be5255632b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-ppc64le'; 			sha256='a2c76f4ea8cbba5906cfe9e97fc67463ad954813dfbddf341bf5062c5c0c93ec'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-riscv64'; 			sha256='3e54325b4019398e058be3cd8589b9ecc98a1a97b7fe8f3280ee4e25281091e2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-linux-s390x'; 			sha256='87e75c7ffd019507c823c49d83fac62eda239e55544bb56d7707c817f52acc69'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Jul 2025 11:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD ["sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 29 Jul 2025 11:04:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Jul 2025 11:04:14 GMT
VOLUME [/var/lib/docker]
# Tue, 29 Jul 2025 11:04:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 29 Jul 2025 11:04:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 29 Jul 2025 11:04:14 GMT
CMD []
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9487516d0e58356ab15b8fbe63d29b661c0a84ce2ff65b1f4d0de103ff070b17`  
		Last Modified: Tue, 29 Jul 2025 16:34:57 GMT  
		Size: 8.2 MB (8217731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7713168c92823bb16f971238d19c4d2c361e695316a74ec0a62476adba6d80`  
		Last Modified: Tue, 29 Jul 2025 16:34:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4e4cf6c152c52d78c3f1211758db7774a799862f57329da229048bb250562c`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 19.3 MB (19271222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940b1d5537bde7e6795e3c64e66763223d358cfeee6013583da894e7c25cf8a`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 20.1 MB (20093507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96af51f1b4e79e29dc96db91ace3d21bd9b90d03153762c5c97a5838ee072dd7`  
		Last Modified: Tue, 29 Jul 2025 16:35:01 GMT  
		Size: 19.7 MB (19676873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a7373e89532fa8a92b1464b92890dc0210b0df6f04496c9837814439640fdc`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b54ee594d864701e3836e5c4c8b406c756a0f9cd6f4782b7dde5a4d535f4ee`  
		Last Modified: Tue, 29 Jul 2025 16:34:59 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5061f31fc63b54b156863fd0b86f70d5dd1aff89bd8ed1a3cc207393ef430da1`  
		Last Modified: Tue, 29 Jul 2025 16:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a4f90fb8179789820d09ee62a252a0b5d2007f1e6a0116dc93cef396028b74`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 7.1 MB (7140514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e7ada02315c507aa603b515c8af64560c37e3b0c3e1ae602c926a39f0e193`  
		Last Modified: Tue, 29 Jul 2025 17:07:32 GMT  
		Size: 99.3 KB (99312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b0bce22e68e3e822e795bdd12fcda8fe4d3374269c9031570e52e4989e30cc`  
		Last Modified: Tue, 29 Jul 2025 17:07:42 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94302614c7eb1b832998ebf0e2a380369fcc6c23e0fa4bab8669b02665af8558`  
		Last Modified: Tue, 29 Jul 2025 17:07:38 GMT  
		Size: 57.5 MB (57464791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6fb8714059d9cacf4db01465f092fa2bfbaebc073ecf76e620e3776406896`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d9a1a1a08782f599a9be2fe288ef0cbd4aa9a049d7b515137cf06ff00f2ba`  
		Last Modified: Tue, 29 Jul 2025 17:07:33 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:9e688304c06587ce1c71a3409b301f476dc1fd9b67ee40cf659e180e174582d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878a9b4d22bd08a4e39e541ae7b4ca75ac8e62370ac53573fa18a05338573ec4`

```dockerfile
```

-	Layers:
	-	`sha256:e0a4c2285c0b8b2afc33b86867190ce402deccb8def5a4573f617737a1c16087`  
		Last Modified: Tue, 29 Jul 2025 20:07:33 GMT  
		Size: 34.8 KB (34825 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:32d6e626f79e39b5cc83a10d4fcc2fd8f090cf2052298b7081c073d05d6788b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `docker:windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fce944f1be9964c27dffe70ea4e05f43906e5c35d7f1d1f319ea241e6ff7766b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565385109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e16746b5d96d8f01c428a46027b16342e56a3f351d9e94cc23c4884e182a23`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:26:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:27:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:06 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:27:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:27:16 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:27:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d49ded649af742ac4e8aff9b2beba88841a34f5ac3c9cad1b2cbbb85a8a1741`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4901ee3ae2f2d3da5d2455d57c8497cdcd54fa3981e3eced30f632522080c987`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 356.9 KB (356904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cce2887577005a99bc013670c90c46c419da33c604d06b159d5a10bf40d3cb`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d727c7396ced4e810c63f727df20e45e76ebd1775b108e32a902fac6b6478076`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcfd1f605909b895b191bbc1dce66175acc45a5add136bc5a0ae4f36ecd8989`  
		Last Modified: Tue, 12 Aug 2025 20:31:31 GMT  
		Size: 20.8 MB (20837962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e6ab5bf2d2d618100a885f27c393467212c0570eaa7ea84e6ea8219e5dc291`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b884b8cda3f7df7bffd4252d58e7d9152d914e0d920161dfc1b2bbf477829d45`  
		Last Modified: Tue, 12 Aug 2025 20:31:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7094f59558defd3124f897718f374e4c7adb853752582ba8e4f3684c14b3e16a`  
		Last Modified: Tue, 12 Aug 2025 20:31:14 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7051fc3fd3e4df1ca961e28ab2cd07384069c0c2872b4680f672075663b48034`  
		Last Modified: Tue, 12 Aug 2025 20:31:20 GMT  
		Size: 23.0 MB (22953510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a709cde7693b4592561374d3dddec696b50b1a107e69458552265acbbf21459e`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d45050aa1c7e9ea58879bcb46bbf075e263acc49748dcd9a19068713b52e59`  
		Last Modified: Tue, 12 Aug 2025 20:31:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31e15e6414199a0fa232b38e3b810fa3806c10634d77fbde8642407b62f90f1`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4abea89efff9a4dcaee678846541ee7471b0d5e13f11a1ffd50c601da438141`  
		Last Modified: Tue, 12 Aug 2025 20:31:21 GMT  
		Size: 22.4 MB (22394336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:b08584be840c5fffd7d99e62ab49eae4c3f6636a8843cce35a5bd1067720e0ab
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348189021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732e79d977df1d9edff845acd89fee0b2122dfd3500338862d0c073f12710e29`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:25:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:06 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:26:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:26:19 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:26:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:26:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:26:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:26:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37ee622e1d3856c0f56d0e073b50e34ad5239aa1e8a0d7b93f11fb38230099f`  
		Last Modified: Tue, 12 Aug 2025 20:28:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04848d212a98717392544afa4ddeeef71992d66bba2d6eef616660649835eece`  
		Last Modified: Tue, 12 Aug 2025 20:28:14 GMT  
		Size: 346.1 KB (346147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e3cc07ce8c5cb86d5dd9907546bc97af931be4eef1e23a908c40d2ab28a68`  
		Last Modified: Tue, 12 Aug 2025 20:51:41 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188521c2085d7c3dbbbae5485b4fc383b0516ff6e9a27a023df6aca63dbb7459`  
		Last Modified: Tue, 12 Aug 2025 20:51:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581d2a99a5e27e493c9517fcb5d27c165f5696ad1d8f08f568d60eee1e8d6fcc`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 20.8 MB (20826824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e88f9f3cb2e7be25dbdc4626eb3bcbc619924d0c61d64356d2d7a8e3fc4a661`  
		Last Modified: Tue, 12 Aug 2025 20:51:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70bf9f40001314e26858770cf903764c3dc5e0c1278e072fa7daf620846745`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6079589750abcc6d3eb81778c4a2837ea2dc0467112980d886173696e4c9df`  
		Last Modified: Tue, 12 Aug 2025 20:51:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65174c16d8c061f85019c62493afae8d5db2f56e1a831a94c02db515515626d`  
		Last Modified: Tue, 12 Aug 2025 20:51:50 GMT  
		Size: 22.9 MB (22937256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728f806f53c767bd20bb97653fa5b5e3016a8e4af213a950135d9105930ac520`  
		Last Modified: Tue, 12 Aug 2025 20:51:48 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b5ab841f285aa2a8a9238b3c57bede8d2a91a3763c0f584275508deefcbdf5`  
		Last Modified: Tue, 12 Aug 2025 20:51:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae017706cc10313aa38b24d9c7c4dc2901f7f1ea62598f22aa0639e40d14cba0`  
		Last Modified: Tue, 12 Aug 2025 20:51:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bac6b791dfaef6e7c36ef93b178cc273d730b229d9112ceadede006ad1bc0a6`  
		Last Modified: Tue, 12 Aug 2025 20:51:56 GMT  
		Size: 22.4 MB (22375244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:7a3b2e07b931434a99cd7f00343a6fd5b6a618598e9cc4746313aaca3de5aaa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull docker@sha256:b08584be840c5fffd7d99e62ab49eae4c3f6636a8843cce35a5bd1067720e0ab
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348189021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732e79d977df1d9edff845acd89fee0b2122dfd3500338862d0c073f12710e29`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:25:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:06 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:06 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:07 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:26:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:26:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:26:19 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:26:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:26:28 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:26:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:26:30 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:26:38 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37ee622e1d3856c0f56d0e073b50e34ad5239aa1e8a0d7b93f11fb38230099f`  
		Last Modified: Tue, 12 Aug 2025 20:28:12 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04848d212a98717392544afa4ddeeef71992d66bba2d6eef616660649835eece`  
		Last Modified: Tue, 12 Aug 2025 20:28:14 GMT  
		Size: 346.1 KB (346147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9e3cc07ce8c5cb86d5dd9907546bc97af931be4eef1e23a908c40d2ab28a68`  
		Last Modified: Tue, 12 Aug 2025 20:51:41 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188521c2085d7c3dbbbae5485b4fc383b0516ff6e9a27a023df6aca63dbb7459`  
		Last Modified: Tue, 12 Aug 2025 20:51:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581d2a99a5e27e493c9517fcb5d27c165f5696ad1d8f08f568d60eee1e8d6fcc`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 20.8 MB (20826824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e88f9f3cb2e7be25dbdc4626eb3bcbc619924d0c61d64356d2d7a8e3fc4a661`  
		Last Modified: Tue, 12 Aug 2025 20:51:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d70bf9f40001314e26858770cf903764c3dc5e0c1278e072fa7daf620846745`  
		Last Modified: Tue, 12 Aug 2025 20:51:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6079589750abcc6d3eb81778c4a2837ea2dc0467112980d886173696e4c9df`  
		Last Modified: Tue, 12 Aug 2025 20:51:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65174c16d8c061f85019c62493afae8d5db2f56e1a831a94c02db515515626d`  
		Last Modified: Tue, 12 Aug 2025 20:51:50 GMT  
		Size: 22.9 MB (22937256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728f806f53c767bd20bb97653fa5b5e3016a8e4af213a950135d9105930ac520`  
		Last Modified: Tue, 12 Aug 2025 20:51:48 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b5ab841f285aa2a8a9238b3c57bede8d2a91a3763c0f584275508deefcbdf5`  
		Last Modified: Tue, 12 Aug 2025 20:51:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae017706cc10313aa38b24d9c7c4dc2901f7f1ea62598f22aa0639e40d14cba0`  
		Last Modified: Tue, 12 Aug 2025 20:51:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bac6b791dfaef6e7c36ef93b178cc273d730b229d9112ceadede006ad1bc0a6`  
		Last Modified: Tue, 12 Aug 2025 20:51:56 GMT  
		Size: 22.4 MB (22375244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:a188802ccb2fc99331e286bf343b9ad5721c2fcf498565d8a6990f9642e3f046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:fce944f1be9964c27dffe70ea4e05f43906e5c35d7f1d1f319ea241e6ff7766b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565385109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e16746b5d96d8f01c428a46027b16342e56a3f351d9e94cc23c4884e182a23`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:26:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_VERSION=28.3.3
# Tue, 12 Aug 2025 20:26:57 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.3.zip
# Tue, 12 Aug 2025 20:27:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:06 GMT
ENV DOCKER_BUILDX_VERSION=0.26.1
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.26.1/buildx-v0.26.1.windows-amd64.exe
# Tue, 12 Aug 2025 20:27:07 GMT
ENV DOCKER_BUILDX_SHA256=7920bc77bdcad5d6bfb02e530ed67b8dfa550b77ae79e080ac4ee9424a75acea
# Tue, 12 Aug 2025 20:27:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.1
# Tue, 12 Aug 2025 20:27:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.1/docker-compose-windows-x86_64.exe
# Tue, 12 Aug 2025 20:27:16 GMT
ENV DOCKER_COMPOSE_SHA256=5e0ae2df1651c6bed38c5367d0d84d5169537ef5426b2ee32f34e4166233efa7
# Tue, 12 Aug 2025 20:27:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d49ded649af742ac4e8aff9b2beba88841a34f5ac3c9cad1b2cbbb85a8a1741`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4901ee3ae2f2d3da5d2455d57c8497cdcd54fa3981e3eced30f632522080c987`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 356.9 KB (356904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cce2887577005a99bc013670c90c46c419da33c604d06b159d5a10bf40d3cb`  
		Last Modified: Tue, 12 Aug 2025 20:31:08 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d727c7396ced4e810c63f727df20e45e76ebd1775b108e32a902fac6b6478076`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcfd1f605909b895b191bbc1dce66175acc45a5add136bc5a0ae4f36ecd8989`  
		Last Modified: Tue, 12 Aug 2025 20:31:31 GMT  
		Size: 20.8 MB (20837962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e6ab5bf2d2d618100a885f27c393467212c0570eaa7ea84e6ea8219e5dc291`  
		Last Modified: Tue, 12 Aug 2025 20:31:09 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b884b8cda3f7df7bffd4252d58e7d9152d914e0d920161dfc1b2bbf477829d45`  
		Last Modified: Tue, 12 Aug 2025 20:31:10 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7094f59558defd3124f897718f374e4c7adb853752582ba8e4f3684c14b3e16a`  
		Last Modified: Tue, 12 Aug 2025 20:31:14 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7051fc3fd3e4df1ca961e28ab2cd07384069c0c2872b4680f672075663b48034`  
		Last Modified: Tue, 12 Aug 2025 20:31:20 GMT  
		Size: 23.0 MB (22953510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a709cde7693b4592561374d3dddec696b50b1a107e69458552265acbbf21459e`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d45050aa1c7e9ea58879bcb46bbf075e263acc49748dcd9a19068713b52e59`  
		Last Modified: Tue, 12 Aug 2025 20:31:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31e15e6414199a0fa232b38e3b810fa3806c10634d77fbde8642407b62f90f1`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4abea89efff9a4dcaee678846541ee7471b0d5e13f11a1ffd50c601da438141`  
		Last Modified: Tue, 12 Aug 2025 20:31:21 GMT  
		Size: 22.4 MB (22394336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
