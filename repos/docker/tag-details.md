<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:29`](#docker29)
-	[`docker:29-cli`](#docker29-cli)
-	[`docker:29-dind`](#docker29-dind)
-	[`docker:29-dind-rootless`](#docker29-dind-rootless)
-	[`docker:29-windowsservercore`](#docker29-windowsservercore)
-	[`docker:29-windowsservercore-ltsc2022`](#docker29-windowsservercore-ltsc2022)
-	[`docker:29-windowsservercore-ltsc2025`](#docker29-windowsservercore-ltsc2025)
-	[`docker:29.2`](#docker292)
-	[`docker:29.2-cli`](#docker292-cli)
-	[`docker:29.2-dind`](#docker292-dind)
-	[`docker:29.2-dind-rootless`](#docker292-dind-rootless)
-	[`docker:29.2-windowsservercore`](#docker292-windowsservercore)
-	[`docker:29.2-windowsservercore-ltsc2022`](#docker292-windowsservercore-ltsc2022)
-	[`docker:29.2-windowsservercore-ltsc2025`](#docker292-windowsservercore-ltsc2025)
-	[`docker:29.2.1`](#docker2921)
-	[`docker:29.2.1-alpine3.23`](#docker2921-alpine323)
-	[`docker:29.2.1-cli`](#docker2921-cli)
-	[`docker:29.2.1-cli-alpine3.23`](#docker2921-cli-alpine323)
-	[`docker:29.2.1-dind`](#docker2921-dind)
-	[`docker:29.2.1-dind-alpine3.23`](#docker2921-dind-alpine323)
-	[`docker:29.2.1-dind-rootless`](#docker2921-dind-rootless)
-	[`docker:29.2.1-windowsservercore`](#docker2921-windowsservercore)
-	[`docker:29.2.1-windowsservercore-ltsc2022`](#docker2921-windowsservercore-ltsc2022)
-	[`docker:29.2.1-windowsservercore-ltsc2025`](#docker2921-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:29`

```console
$ docker pull docker@sha256:8bcbad4b45f0bff9d3e809d85a7ac589390f0be8acbc526850c998c35c1243fd
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
$ docker pull docker@sha256:2658fda9e8779b94ea1581f4d25214dac9ed144b407902842e5328cce8f861f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143806344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e53a1133dad326140cd3d234b76db232167ef01734e3b1a87cf3fbb1d18f2d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:14 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb3344ffbb9855e9e8c1fc885f05984fa42d8d5830e32df03e0d135ad8822e`  
		Last Modified: Tue, 03 Feb 2026 18:08:25 GMT  
		Size: 6.9 MB (6934690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678f9b57b1bc0e3be53c874c97da597f979a78c280ad71e6d7f63fcb8463911`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 92.5 KB (92473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b249709b45e2c9f5f73832f9cc1ec388f12b297e00d1171b7ce479df111ebd`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635e03777d6fa8913ee09d5abd54e7646e340b3aff6ce8ddff1d2e60f75e349`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 66.6 MB (66625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc6090a660e5dc2d63b3bcc09f50f8c36a471ae548571d43cf9b8a3cfe639c`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ebca63bb1cffa50e238c87876cbad00be5ca7084fa675f75225e8d1f03aeff`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:5ca42eff6ef7d7c05200966f252adae0b699ece5fb2f8466eda35d7b36a890ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7670efdca26f8b1bcc0b988fb4f653a6376650ea58b34a100363b082bc6523`

```dockerfile
```

-	Layers:
	-	`sha256:04d995c70a723b002243db02983e46f08e29912414c5e73133bdb721b3f1e9b7`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v6

```console
$ docker pull docker@sha256:96c65c13341f1bd361681f0e10d68a466cb31465af3505c4ab11bb7e57b9f9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135639255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f4d60d48216741f772b218962de8bd12f6b4376c9b7d2d61945efe7de8af09`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:09:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:09:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:09:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:09:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589acbf83b02aefe4b74c88258659fbc3cbc808bca02b74d70fc84c2d85c1f0`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 7.3 MB (7271674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a1dc2d0150cb7d0d0ac4db0350de2ace99ddecbf13ede3f0852e989bee562`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e501e8c157d2cb65e85d675f7f62265ad6bf5403fd2fd5a82159dd013df16`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8a975a5a8a2c7f276059ed5b82c8d8fe03e3aa5f19fe35bfef977eb73f836a`  
		Last Modified: Tue, 03 Feb 2026 18:09:30 GMT  
		Size: 62.0 MB (62034292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b27e1927e65ff11d65fde3dbf30388e85fcddba8f24f5ed68c9556c7029e7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bf263325fbcf53d5d385378f5e9d50ebe967b108a54c4e71e1a21748ca0b7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:6322cd1e6550fefe96c9648558e12551a32688528b16770636b40cfafa1a7518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38278b3e49b1412f16afef4b1389dd760ef2f1ec2117c02d9802fab93b7e0ec7`

```dockerfile
```

-	Layers:
	-	`sha256:b5e6e9bb35a96bbc52efdac8258e865ffa07b199e52e6c7be4fd1669bef4fce7`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm variant v7

```console
$ docker pull docker@sha256:a1db2279111145cbcf1396c93955b81f5f2b7de52b32c9ba4859d020f36634f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133723354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284b3692652e58ba18acc63cf8b6e821364031b866cb6682f085149f779ab4ff`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:07:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:07:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:07:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:07:04 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6779a50db6dd09992adc4b403d5daf31daa7cfc8adf6350317537c2e3a7cb5f`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 6.6 MB (6573016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6e53c40bcc58f48835cdaa63c5a7022c93ff9df8c7106f139ce37baca30b5e`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 88.1 KB (88141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bd2d3709e6dab534375a42fc15c6065df38f73068c92ef2e76522924c25b7a`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f50af2801e8d40ff49c6a156103e37cab62872a4a79327fa5b346cfb48b9b`  
		Last Modified: Tue, 03 Feb 2026 18:07:17 GMT  
		Size: 61.9 MB (61863352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee9b22d2befaca7304238ebc8fd562d677a8b437d7f1d379ff801be543a6907`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eec5ef5f0a11840b0e7853071f5ca12064018f7d0d47f6101de217d79f484c7`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:c34ad6a1f7894d31642f2ece3bc56bb40c89621d5aca9042df85276dd5d91299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865285598aa081a112650828c916096f6c9d5b691cf04fe2c1fffca77a8e3dd3`

```dockerfile
```

-	Layers:
	-	`sha256:d8d51afa4a991b6fb7cc8cb5be95ab133da93d9f134e00e385b69c869b6bce03`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b5b3b18d8bb9d62276afb346b9392a9ca59fbf21e878c28d1a7694c847c49b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133253666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a395c8fe40dc997f59712d6616f1f5de99e5b87bd8652b1015f377bca5e2d60f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:04 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cdc8e2ada368f406368ddbc1a30cf5004317fe0d34e871c30de45de04f5555`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 7.2 MB (7213157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aabb19b2db370ae221b4a8c35a937d4c3ef464ab61a5cc640f4edd0ad27c`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 101.3 KB (101293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec0ca68a54a0c48f91559e549030d59a6ea57fe11e8c8f336d71203e30d4b`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359ce5f20066df79a2c2f15dfc2e4327391b52123711b1b932ba423d19dcd9d`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 60.4 MB (60436023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c858b59040b5e0571d6565b1c252744394e5c91f3fc7666c081592746f8acff`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017336f8dfa381510251cf029e1e8b9068af186aec76d056f13f1bfd02c0cd3`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29` - unknown; unknown

```console
$ docker pull docker@sha256:a7811e3fe95592d83bd7ac50ab2e29193e551c1ef2f3174975161619ce5a7898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d4b79b678de90d818e106856c1da5f8f57a0df8d7bba87809610bef584af9e`

```dockerfile
```

-	Layers:
	-	`sha256:94845085a82ddc797095cf318c979066478d1a17fa05c408df973ec4c8f31fe3`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-cli`

```console
$ docker pull docker@sha256:1d6d751f1d68d1a5142c23c730ef5ecc976a8e050fa08c3cdb09f7e2e54a4439
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
$ docker pull docker@sha256:0c04277b44d1d448d40238faa142c2edf21d4a90dc0d61486c32056bbf11572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70148082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fa388e81d5f66d9d9ee840c5375a0801629a980c3d9657463257b2c863f324`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c1620c41ed6e739f033f9e98a5bba1cb95e1ea6a093197beb216823c8c93ce72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f4666aeb7f994fb855d5fb4b289608e198a0a0b59b25161f28433aeb36364`

```dockerfile
```

-	Layers:
	-	`sha256:19b63918903a6b77f5af72e60038c44df3a84e5a4563b3db3d54ef79567b8195`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:cf09d93cea103396a11b1b12c36c15b6b93d367c0c80cce733f00214c71c92e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66235505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4367f8d4a4b3fc3d463d69bca54b902b58d4792ccf8967224e2ec3dd7aa4afb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:fbcdf3246eea54b7103bc19f384cd3f454538bd499af80a1566455c68e652971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63de4e3179da9faef11522e19444ae1387215588371c787a0b6852c464dcd77`

```dockerfile
```

-	Layers:
	-	`sha256:97d51d656e276dcee240923733068124918a337234be2ffb56edcdb70a458855`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ba03aff6e89a96861c91cbe97855b49f31e816c782afaa8225043cb76f7ae372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65192844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985b778ba8e60d8ceaa28fed60316b7c31c5ff3e18d6afb37619d388a8da92b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:725c7ed6fedc0c78099cca969de9d894742913605a635c1d1ae732d243e1f9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2b7afca7a73cadfc121038f2cb596614c4eff15299359ccc0fe5915a333dfa`

```dockerfile
```

-	Layers:
	-	`sha256:9fd463f063b0e999eee86b191492b64c48293c00436e4b777db697007872a8d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2bef500bc870e9a4eef5ac67cf6fef451c072f77b7351b207d74a3463c80e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65497196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffbe99c0e2eadb1b2dd8830a3ecddedf95c08183d497287cb048586c0c94905`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-cli` - unknown; unknown

```console
$ docker pull docker@sha256:22956d1b0f85ed3aaf3fbd162a232fd08241684704dc328c469298a7a60f924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0c6c28d5d6436cdecdceb1ee544bccb64c7a75c45b13de36e354116226cab3`

```dockerfile
```

-	Layers:
	-	`sha256:0c689b61e422b3962e7df2e52b56054a4e453d576da33fd3b1d6f7dca26d06b6`  
		Last Modified: Tue, 03 Feb 2026 17:26:45 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind`

```console
$ docker pull docker@sha256:8bcbad4b45f0bff9d3e809d85a7ac589390f0be8acbc526850c998c35c1243fd
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
$ docker pull docker@sha256:2658fda9e8779b94ea1581f4d25214dac9ed144b407902842e5328cce8f861f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143806344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e53a1133dad326140cd3d234b76db232167ef01734e3b1a87cf3fbb1d18f2d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:14 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb3344ffbb9855e9e8c1fc885f05984fa42d8d5830e32df03e0d135ad8822e`  
		Last Modified: Tue, 03 Feb 2026 18:08:25 GMT  
		Size: 6.9 MB (6934690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678f9b57b1bc0e3be53c874c97da597f979a78c280ad71e6d7f63fcb8463911`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 92.5 KB (92473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b249709b45e2c9f5f73832f9cc1ec388f12b297e00d1171b7ce479df111ebd`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635e03777d6fa8913ee09d5abd54e7646e340b3aff6ce8ddff1d2e60f75e349`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 66.6 MB (66625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc6090a660e5dc2d63b3bcc09f50f8c36a471ae548571d43cf9b8a3cfe639c`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ebca63bb1cffa50e238c87876cbad00be5ca7084fa675f75225e8d1f03aeff`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5ca42eff6ef7d7c05200966f252adae0b699ece5fb2f8466eda35d7b36a890ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7670efdca26f8b1bcc0b988fb4f653a6376650ea58b34a100363b082bc6523`

```dockerfile
```

-	Layers:
	-	`sha256:04d995c70a723b002243db02983e46f08e29912414c5e73133bdb721b3f1e9b7`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:96c65c13341f1bd361681f0e10d68a466cb31465af3505c4ab11bb7e57b9f9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135639255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f4d60d48216741f772b218962de8bd12f6b4376c9b7d2d61945efe7de8af09`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:09:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:09:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:09:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:09:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589acbf83b02aefe4b74c88258659fbc3cbc808bca02b74d70fc84c2d85c1f0`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 7.3 MB (7271674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a1dc2d0150cb7d0d0ac4db0350de2ace99ddecbf13ede3f0852e989bee562`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e501e8c157d2cb65e85d675f7f62265ad6bf5403fd2fd5a82159dd013df16`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8a975a5a8a2c7f276059ed5b82c8d8fe03e3aa5f19fe35bfef977eb73f836a`  
		Last Modified: Tue, 03 Feb 2026 18:09:30 GMT  
		Size: 62.0 MB (62034292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b27e1927e65ff11d65fde3dbf30388e85fcddba8f24f5ed68c9556c7029e7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bf263325fbcf53d5d385378f5e9d50ebe967b108a54c4e71e1a21748ca0b7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6322cd1e6550fefe96c9648558e12551a32688528b16770636b40cfafa1a7518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38278b3e49b1412f16afef4b1389dd760ef2f1ec2117c02d9802fab93b7e0ec7`

```dockerfile
```

-	Layers:
	-	`sha256:b5e6e9bb35a96bbc52efdac8258e865ffa07b199e52e6c7be4fd1669bef4fce7`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:a1db2279111145cbcf1396c93955b81f5f2b7de52b32c9ba4859d020f36634f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133723354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284b3692652e58ba18acc63cf8b6e821364031b866cb6682f085149f779ab4ff`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:07:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:07:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:07:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:07:04 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6779a50db6dd09992adc4b403d5daf31daa7cfc8adf6350317537c2e3a7cb5f`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 6.6 MB (6573016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6e53c40bcc58f48835cdaa63c5a7022c93ff9df8c7106f139ce37baca30b5e`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 88.1 KB (88141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bd2d3709e6dab534375a42fc15c6065df38f73068c92ef2e76522924c25b7a`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f50af2801e8d40ff49c6a156103e37cab62872a4a79327fa5b346cfb48b9b`  
		Last Modified: Tue, 03 Feb 2026 18:07:17 GMT  
		Size: 61.9 MB (61863352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee9b22d2befaca7304238ebc8fd562d677a8b437d7f1d379ff801be543a6907`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eec5ef5f0a11840b0e7853071f5ca12064018f7d0d47f6101de217d79f484c7`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:c34ad6a1f7894d31642f2ece3bc56bb40c89621d5aca9042df85276dd5d91299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865285598aa081a112650828c916096f6c9d5b691cf04fe2c1fffca77a8e3dd3`

```dockerfile
```

-	Layers:
	-	`sha256:d8d51afa4a991b6fb7cc8cb5be95ab133da93d9f134e00e385b69c869b6bce03`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b5b3b18d8bb9d62276afb346b9392a9ca59fbf21e878c28d1a7694c847c49b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133253666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a395c8fe40dc997f59712d6616f1f5de99e5b87bd8652b1015f377bca5e2d60f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:04 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cdc8e2ada368f406368ddbc1a30cf5004317fe0d34e871c30de45de04f5555`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 7.2 MB (7213157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aabb19b2db370ae221b4a8c35a937d4c3ef464ab61a5cc640f4edd0ad27c`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 101.3 KB (101293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec0ca68a54a0c48f91559e549030d59a6ea57fe11e8c8f336d71203e30d4b`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359ce5f20066df79a2c2f15dfc2e4327391b52123711b1b932ba423d19dcd9d`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 60.4 MB (60436023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c858b59040b5e0571d6565b1c252744394e5c91f3fc7666c081592746f8acff`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017336f8dfa381510251cf029e1e8b9068af186aec76d056f13f1bfd02c0cd3`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a7811e3fe95592d83bd7ac50ab2e29193e551c1ef2f3174975161619ce5a7898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d4b79b678de90d818e106856c1da5f8f57a0df8d7bba87809610bef584af9e`

```dockerfile
```

-	Layers:
	-	`sha256:94845085a82ddc797095cf318c979066478d1a17fa05c408df973ec4c8f31fe3`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-dind-rootless`

```console
$ docker pull docker@sha256:68bb0d88ed4134f6cc41f04c62e5e49762051b16f628abf84db6f7c33994885c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:567ead5a15f1f97b9878eede0250d242c0ef27a19c0dd685d70c1c59e21d750c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164603487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e52a73bd06c9759bd4433c27b69afd58457bdb3174e0153ecf3089eea25736`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:14 GMT
CMD []
# Tue, 03 Feb 2026 18:56:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 03 Feb 2026 18:56:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 03 Feb 2026 18:56:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:56:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 03 Feb 2026 18:56:44 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 03 Feb 2026 18:56:44 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 03 Feb 2026 18:56:44 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb3344ffbb9855e9e8c1fc885f05984fa42d8d5830e32df03e0d135ad8822e`  
		Last Modified: Tue, 03 Feb 2026 18:08:25 GMT  
		Size: 6.9 MB (6934690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678f9b57b1bc0e3be53c874c97da597f979a78c280ad71e6d7f63fcb8463911`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 92.5 KB (92473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b249709b45e2c9f5f73832f9cc1ec388f12b297e00d1171b7ce479df111ebd`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635e03777d6fa8913ee09d5abd54e7646e340b3aff6ce8ddff1d2e60f75e349`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 66.6 MB (66625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc6090a660e5dc2d63b3bcc09f50f8c36a471ae548571d43cf9b8a3cfe639c`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ebca63bb1cffa50e238c87876cbad00be5ca7084fa675f75225e8d1f03aeff`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ae3e167984ddda59e327294c6376b950eea2c3ef31d27360612eac1daa1f0a`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 3.4 MB (3419941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d922f02e9320e8d0119111798e4061c241770bb012211f450efe2d517fd1a42a`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5687d1e84b0ee14d3c1995e61b0e4a68d506dd136ef95f02c8e2b6faaf863a33`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfdc02c4d88b47fb1008ea5191d51a35b34fca85278d2030e245268126bf6c8`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 17.4 MB (17375862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077f22d66325a95178fd420b08832727efb00c81b7c88dd48a131ccb5b1ce2d0`  
		Last Modified: Tue, 03 Feb 2026 18:56:51 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0d5c44c6470979f0c582d86f55d66e742e639e3a8fdc0a404c02021d4f43d416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e137c0f7f1699722fc735873de3ba73dd4cae21481ee991407f271300a01252`

```dockerfile
```

-	Layers:
	-	`sha256:ae18371d1afbd9ae2b2e2a148ace11a55c228a20017f500977180dec98bd30d8`  
		Last Modified: Tue, 03 Feb 2026 18:56:49 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c68e67b2934792c04cb7f598418b51467087009fcb45ca095e2b0e350705d699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154359925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b76823faed7a9fec13c67806e9f797ce9b03718d27e5e068ad293efc75410c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:04 GMT
CMD []
# Tue, 03 Feb 2026 18:55:45 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 03 Feb 2026 18:55:45 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 03 Feb 2026 18:55:45 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:55:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 03 Feb 2026 18:55:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 03 Feb 2026 18:55:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 03 Feb 2026 18:55:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cdc8e2ada368f406368ddbc1a30cf5004317fe0d34e871c30de45de04f5555`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 7.2 MB (7213157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aabb19b2db370ae221b4a8c35a937d4c3ef464ab61a5cc640f4edd0ad27c`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 101.3 KB (101293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec0ca68a54a0c48f91559e549030d59a6ea57fe11e8c8f336d71203e30d4b`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359ce5f20066df79a2c2f15dfc2e4327391b52123711b1b932ba423d19dcd9d`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 60.4 MB (60436023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c858b59040b5e0571d6565b1c252744394e5c91f3fc7666c081592746f8acff`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017336f8dfa381510251cf029e1e8b9068af186aec76d056f13f1bfd02c0cd3`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3efad4ea039a0085ac85140fdaff7b0901f77d844a3ced398908bed50280d3`  
		Last Modified: Tue, 03 Feb 2026 18:55:53 GMT  
		Size: 3.4 MB (3394383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad831014bf8990f5582f5d3e6722e27cfbba3529f3c04cfe9c6a949d88ac099d`  
		Last Modified: Tue, 03 Feb 2026 18:55:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fdeaa64fd5c21fb8b772c2d90c06e6775a9a4bb2843aced9f1875939c73f16`  
		Last Modified: Tue, 03 Feb 2026 18:55:52 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd2325131d24f7831871c339c38827915943cb61cb8728e71b867ad3ebd747e`  
		Last Modified: Tue, 03 Feb 2026 18:55:53 GMT  
		Size: 17.7 MB (17710536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29101bcbdf9cfd2edf02a50ce900b29e142538dd886a8ce77c5a95e1b429560e`  
		Last Modified: Tue, 03 Feb 2026 18:55:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c8832a8a4baba19861161896908a1fba0f16c66b34289e1d7587c4f6f4a2945d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3023e84e94ad559ac9f3b408469b4b362197ad68436d62ad001a7a64cb14b81c`

```dockerfile
```

-	Layers:
	-	`sha256:5b681b0886068572453781d5d67943bb963e404233a24ccd9b820c068524c523`  
		Last Modified: Tue, 03 Feb 2026 18:55:52 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:79cb1793605b4f2d7317cea6706862e4b002e6ace6375912bab555eebfdf6ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:315827d701f9fef8731fca2a65b1c5960422bfb5d0e6f335995310b4c2c2bf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:ed671d3152d0f57a459cd9f0838f7e48071ccef5c71ad1188693f4540f24cf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2`

```console
$ docker pull docker@sha256:8bcbad4b45f0bff9d3e809d85a7ac589390f0be8acbc526850c998c35c1243fd
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

### `docker:29.2` - linux; amd64

```console
$ docker pull docker@sha256:2658fda9e8779b94ea1581f4d25214dac9ed144b407902842e5328cce8f861f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143806344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e53a1133dad326140cd3d234b76db232167ef01734e3b1a87cf3fbb1d18f2d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:14 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb3344ffbb9855e9e8c1fc885f05984fa42d8d5830e32df03e0d135ad8822e`  
		Last Modified: Tue, 03 Feb 2026 18:08:25 GMT  
		Size: 6.9 MB (6934690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678f9b57b1bc0e3be53c874c97da597f979a78c280ad71e6d7f63fcb8463911`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 92.5 KB (92473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b249709b45e2c9f5f73832f9cc1ec388f12b297e00d1171b7ce479df111ebd`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635e03777d6fa8913ee09d5abd54e7646e340b3aff6ce8ddff1d2e60f75e349`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 66.6 MB (66625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc6090a660e5dc2d63b3bcc09f50f8c36a471ae548571d43cf9b8a3cfe639c`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ebca63bb1cffa50e238c87876cbad00be5ca7084fa675f75225e8d1f03aeff`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:5ca42eff6ef7d7c05200966f252adae0b699ece5fb2f8466eda35d7b36a890ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7670efdca26f8b1bcc0b988fb4f653a6376650ea58b34a100363b082bc6523`

```dockerfile
```

-	Layers:
	-	`sha256:04d995c70a723b002243db02983e46f08e29912414c5e73133bdb721b3f1e9b7`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2` - linux; arm variant v6

```console
$ docker pull docker@sha256:96c65c13341f1bd361681f0e10d68a466cb31465af3505c4ab11bb7e57b9f9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135639255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f4d60d48216741f772b218962de8bd12f6b4376c9b7d2d61945efe7de8af09`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:09:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:09:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:09:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:09:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589acbf83b02aefe4b74c88258659fbc3cbc808bca02b74d70fc84c2d85c1f0`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 7.3 MB (7271674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a1dc2d0150cb7d0d0ac4db0350de2ace99ddecbf13ede3f0852e989bee562`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e501e8c157d2cb65e85d675f7f62265ad6bf5403fd2fd5a82159dd013df16`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8a975a5a8a2c7f276059ed5b82c8d8fe03e3aa5f19fe35bfef977eb73f836a`  
		Last Modified: Tue, 03 Feb 2026 18:09:30 GMT  
		Size: 62.0 MB (62034292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b27e1927e65ff11d65fde3dbf30388e85fcddba8f24f5ed68c9556c7029e7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bf263325fbcf53d5d385378f5e9d50ebe967b108a54c4e71e1a21748ca0b7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:6322cd1e6550fefe96c9648558e12551a32688528b16770636b40cfafa1a7518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38278b3e49b1412f16afef4b1389dd760ef2f1ec2117c02d9802fab93b7e0ec7`

```dockerfile
```

-	Layers:
	-	`sha256:b5e6e9bb35a96bbc52efdac8258e865ffa07b199e52e6c7be4fd1669bef4fce7`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2` - linux; arm variant v7

```console
$ docker pull docker@sha256:a1db2279111145cbcf1396c93955b81f5f2b7de52b32c9ba4859d020f36634f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133723354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284b3692652e58ba18acc63cf8b6e821364031b866cb6682f085149f779ab4ff`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:07:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:07:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:07:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:07:04 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6779a50db6dd09992adc4b403d5daf31daa7cfc8adf6350317537c2e3a7cb5f`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 6.6 MB (6573016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6e53c40bcc58f48835cdaa63c5a7022c93ff9df8c7106f139ce37baca30b5e`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 88.1 KB (88141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bd2d3709e6dab534375a42fc15c6065df38f73068c92ef2e76522924c25b7a`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f50af2801e8d40ff49c6a156103e37cab62872a4a79327fa5b346cfb48b9b`  
		Last Modified: Tue, 03 Feb 2026 18:07:17 GMT  
		Size: 61.9 MB (61863352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee9b22d2befaca7304238ebc8fd562d677a8b437d7f1d379ff801be543a6907`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eec5ef5f0a11840b0e7853071f5ca12064018f7d0d47f6101de217d79f484c7`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:c34ad6a1f7894d31642f2ece3bc56bb40c89621d5aca9042df85276dd5d91299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865285598aa081a112650828c916096f6c9d5b691cf04fe2c1fffca77a8e3dd3`

```dockerfile
```

-	Layers:
	-	`sha256:d8d51afa4a991b6fb7cc8cb5be95ab133da93d9f134e00e385b69c869b6bce03`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b5b3b18d8bb9d62276afb346b9392a9ca59fbf21e878c28d1a7694c847c49b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133253666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a395c8fe40dc997f59712d6616f1f5de99e5b87bd8652b1015f377bca5e2d60f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:04 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cdc8e2ada368f406368ddbc1a30cf5004317fe0d34e871c30de45de04f5555`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 7.2 MB (7213157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aabb19b2db370ae221b4a8c35a937d4c3ef464ab61a5cc640f4edd0ad27c`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 101.3 KB (101293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec0ca68a54a0c48f91559e549030d59a6ea57fe11e8c8f336d71203e30d4b`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359ce5f20066df79a2c2f15dfc2e4327391b52123711b1b932ba423d19dcd9d`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 60.4 MB (60436023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c858b59040b5e0571d6565b1c252744394e5c91f3fc7666c081592746f8acff`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017336f8dfa381510251cf029e1e8b9068af186aec76d056f13f1bfd02c0cd3`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2` - unknown; unknown

```console
$ docker pull docker@sha256:a7811e3fe95592d83bd7ac50ab2e29193e551c1ef2f3174975161619ce5a7898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d4b79b678de90d818e106856c1da5f8f57a0df8d7bba87809610bef584af9e`

```dockerfile
```

-	Layers:
	-	`sha256:94845085a82ddc797095cf318c979066478d1a17fa05c408df973ec4c8f31fe3`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-cli`

```console
$ docker pull docker@sha256:1d6d751f1d68d1a5142c23c730ef5ecc976a8e050fa08c3cdb09f7e2e54a4439
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

### `docker:29.2-cli` - linux; amd64

```console
$ docker pull docker@sha256:0c04277b44d1d448d40238faa142c2edf21d4a90dc0d61486c32056bbf11572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70148082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fa388e81d5f66d9d9ee840c5375a0801629a980c3d9657463257b2c863f324`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c1620c41ed6e739f033f9e98a5bba1cb95e1ea6a093197beb216823c8c93ce72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f4666aeb7f994fb855d5fb4b289608e198a0a0b59b25161f28433aeb36364`

```dockerfile
```

-	Layers:
	-	`sha256:19b63918903a6b77f5af72e60038c44df3a84e5a4563b3db3d54ef79567b8195`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:cf09d93cea103396a11b1b12c36c15b6b93d367c0c80cce733f00214c71c92e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66235505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4367f8d4a4b3fc3d463d69bca54b902b58d4792ccf8967224e2ec3dd7aa4afb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:fbcdf3246eea54b7103bc19f384cd3f454538bd499af80a1566455c68e652971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63de4e3179da9faef11522e19444ae1387215588371c787a0b6852c464dcd77`

```dockerfile
```

-	Layers:
	-	`sha256:97d51d656e276dcee240923733068124918a337234be2ffb56edcdb70a458855`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ba03aff6e89a96861c91cbe97855b49f31e816c782afaa8225043cb76f7ae372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65192844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985b778ba8e60d8ceaa28fed60316b7c31c5ff3e18d6afb37619d388a8da92b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:725c7ed6fedc0c78099cca969de9d894742913605a635c1d1ae732d243e1f9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2b7afca7a73cadfc121038f2cb596614c4eff15299359ccc0fe5915a333dfa`

```dockerfile
```

-	Layers:
	-	`sha256:9fd463f063b0e999eee86b191492b64c48293c00436e4b777db697007872a8d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2bef500bc870e9a4eef5ac67cf6fef451c072f77b7351b207d74a3463c80e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65497196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffbe99c0e2eadb1b2dd8830a3ecddedf95c08183d497287cb048586c0c94905`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:22956d1b0f85ed3aaf3fbd162a232fd08241684704dc328c469298a7a60f924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0c6c28d5d6436cdecdceb1ee544bccb64c7a75c45b13de36e354116226cab3`

```dockerfile
```

-	Layers:
	-	`sha256:0c689b61e422b3962e7df2e52b56054a4e453d576da33fd3b1d6f7dca26d06b6`  
		Last Modified: Tue, 03 Feb 2026 17:26:45 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-dind`

```console
$ docker pull docker@sha256:8bcbad4b45f0bff9d3e809d85a7ac589390f0be8acbc526850c998c35c1243fd
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

### `docker:29.2-dind` - linux; amd64

```console
$ docker pull docker@sha256:2658fda9e8779b94ea1581f4d25214dac9ed144b407902842e5328cce8f861f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143806344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e53a1133dad326140cd3d234b76db232167ef01734e3b1a87cf3fbb1d18f2d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:14 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb3344ffbb9855e9e8c1fc885f05984fa42d8d5830e32df03e0d135ad8822e`  
		Last Modified: Tue, 03 Feb 2026 18:08:25 GMT  
		Size: 6.9 MB (6934690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678f9b57b1bc0e3be53c874c97da597f979a78c280ad71e6d7f63fcb8463911`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 92.5 KB (92473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b249709b45e2c9f5f73832f9cc1ec388f12b297e00d1171b7ce479df111ebd`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635e03777d6fa8913ee09d5abd54e7646e340b3aff6ce8ddff1d2e60f75e349`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 66.6 MB (66625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc6090a660e5dc2d63b3bcc09f50f8c36a471ae548571d43cf9b8a3cfe639c`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ebca63bb1cffa50e238c87876cbad00be5ca7084fa675f75225e8d1f03aeff`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5ca42eff6ef7d7c05200966f252adae0b699ece5fb2f8466eda35d7b36a890ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7670efdca26f8b1bcc0b988fb4f653a6376650ea58b34a100363b082bc6523`

```dockerfile
```

-	Layers:
	-	`sha256:04d995c70a723b002243db02983e46f08e29912414c5e73133bdb721b3f1e9b7`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:96c65c13341f1bd361681f0e10d68a466cb31465af3505c4ab11bb7e57b9f9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135639255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f4d60d48216741f772b218962de8bd12f6b4376c9b7d2d61945efe7de8af09`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:09:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:09:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:09:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:09:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589acbf83b02aefe4b74c88258659fbc3cbc808bca02b74d70fc84c2d85c1f0`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 7.3 MB (7271674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a1dc2d0150cb7d0d0ac4db0350de2ace99ddecbf13ede3f0852e989bee562`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e501e8c157d2cb65e85d675f7f62265ad6bf5403fd2fd5a82159dd013df16`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8a975a5a8a2c7f276059ed5b82c8d8fe03e3aa5f19fe35bfef977eb73f836a`  
		Last Modified: Tue, 03 Feb 2026 18:09:30 GMT  
		Size: 62.0 MB (62034292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b27e1927e65ff11d65fde3dbf30388e85fcddba8f24f5ed68c9556c7029e7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bf263325fbcf53d5d385378f5e9d50ebe967b108a54c4e71e1a21748ca0b7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6322cd1e6550fefe96c9648558e12551a32688528b16770636b40cfafa1a7518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38278b3e49b1412f16afef4b1389dd760ef2f1ec2117c02d9802fab93b7e0ec7`

```dockerfile
```

-	Layers:
	-	`sha256:b5e6e9bb35a96bbc52efdac8258e865ffa07b199e52e6c7be4fd1669bef4fce7`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:a1db2279111145cbcf1396c93955b81f5f2b7de52b32c9ba4859d020f36634f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133723354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284b3692652e58ba18acc63cf8b6e821364031b866cb6682f085149f779ab4ff`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:07:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:07:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:07:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:07:04 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6779a50db6dd09992adc4b403d5daf31daa7cfc8adf6350317537c2e3a7cb5f`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 6.6 MB (6573016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6e53c40bcc58f48835cdaa63c5a7022c93ff9df8c7106f139ce37baca30b5e`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 88.1 KB (88141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bd2d3709e6dab534375a42fc15c6065df38f73068c92ef2e76522924c25b7a`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f50af2801e8d40ff49c6a156103e37cab62872a4a79327fa5b346cfb48b9b`  
		Last Modified: Tue, 03 Feb 2026 18:07:17 GMT  
		Size: 61.9 MB (61863352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee9b22d2befaca7304238ebc8fd562d677a8b437d7f1d379ff801be543a6907`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eec5ef5f0a11840b0e7853071f5ca12064018f7d0d47f6101de217d79f484c7`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:c34ad6a1f7894d31642f2ece3bc56bb40c89621d5aca9042df85276dd5d91299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865285598aa081a112650828c916096f6c9d5b691cf04fe2c1fffca77a8e3dd3`

```dockerfile
```

-	Layers:
	-	`sha256:d8d51afa4a991b6fb7cc8cb5be95ab133da93d9f134e00e385b69c869b6bce03`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b5b3b18d8bb9d62276afb346b9392a9ca59fbf21e878c28d1a7694c847c49b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133253666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a395c8fe40dc997f59712d6616f1f5de99e5b87bd8652b1015f377bca5e2d60f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:04 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cdc8e2ada368f406368ddbc1a30cf5004317fe0d34e871c30de45de04f5555`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 7.2 MB (7213157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aabb19b2db370ae221b4a8c35a937d4c3ef464ab61a5cc640f4edd0ad27c`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 101.3 KB (101293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec0ca68a54a0c48f91559e549030d59a6ea57fe11e8c8f336d71203e30d4b`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359ce5f20066df79a2c2f15dfc2e4327391b52123711b1b932ba423d19dcd9d`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 60.4 MB (60436023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c858b59040b5e0571d6565b1c252744394e5c91f3fc7666c081592746f8acff`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017336f8dfa381510251cf029e1e8b9068af186aec76d056f13f1bfd02c0cd3`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a7811e3fe95592d83bd7ac50ab2e29193e551c1ef2f3174975161619ce5a7898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d4b79b678de90d818e106856c1da5f8f57a0df8d7bba87809610bef584af9e`

```dockerfile
```

-	Layers:
	-	`sha256:94845085a82ddc797095cf318c979066478d1a17fa05c408df973ec4c8f31fe3`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-dind-rootless`

```console
$ docker pull docker@sha256:68bb0d88ed4134f6cc41f04c62e5e49762051b16f628abf84db6f7c33994885c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:567ead5a15f1f97b9878eede0250d242c0ef27a19c0dd685d70c1c59e21d750c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164603487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e52a73bd06c9759bd4433c27b69afd58457bdb3174e0153ecf3089eea25736`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:14 GMT
CMD []
# Tue, 03 Feb 2026 18:56:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 03 Feb 2026 18:56:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 03 Feb 2026 18:56:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:56:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 03 Feb 2026 18:56:44 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 03 Feb 2026 18:56:44 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 03 Feb 2026 18:56:44 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb3344ffbb9855e9e8c1fc885f05984fa42d8d5830e32df03e0d135ad8822e`  
		Last Modified: Tue, 03 Feb 2026 18:08:25 GMT  
		Size: 6.9 MB (6934690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678f9b57b1bc0e3be53c874c97da597f979a78c280ad71e6d7f63fcb8463911`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 92.5 KB (92473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b249709b45e2c9f5f73832f9cc1ec388f12b297e00d1171b7ce479df111ebd`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635e03777d6fa8913ee09d5abd54e7646e340b3aff6ce8ddff1d2e60f75e349`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 66.6 MB (66625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc6090a660e5dc2d63b3bcc09f50f8c36a471ae548571d43cf9b8a3cfe639c`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ebca63bb1cffa50e238c87876cbad00be5ca7084fa675f75225e8d1f03aeff`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ae3e167984ddda59e327294c6376b950eea2c3ef31d27360612eac1daa1f0a`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 3.4 MB (3419941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d922f02e9320e8d0119111798e4061c241770bb012211f450efe2d517fd1a42a`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5687d1e84b0ee14d3c1995e61b0e4a68d506dd136ef95f02c8e2b6faaf863a33`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfdc02c4d88b47fb1008ea5191d51a35b34fca85278d2030e245268126bf6c8`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 17.4 MB (17375862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077f22d66325a95178fd420b08832727efb00c81b7c88dd48a131ccb5b1ce2d0`  
		Last Modified: Tue, 03 Feb 2026 18:56:51 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0d5c44c6470979f0c582d86f55d66e742e639e3a8fdc0a404c02021d4f43d416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e137c0f7f1699722fc735873de3ba73dd4cae21481ee991407f271300a01252`

```dockerfile
```

-	Layers:
	-	`sha256:ae18371d1afbd9ae2b2e2a148ace11a55c228a20017f500977180dec98bd30d8`  
		Last Modified: Tue, 03 Feb 2026 18:56:49 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c68e67b2934792c04cb7f598418b51467087009fcb45ca095e2b0e350705d699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154359925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b76823faed7a9fec13c67806e9f797ce9b03718d27e5e068ad293efc75410c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:04 GMT
CMD []
# Tue, 03 Feb 2026 18:55:45 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 03 Feb 2026 18:55:45 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 03 Feb 2026 18:55:45 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:55:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 03 Feb 2026 18:55:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 03 Feb 2026 18:55:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 03 Feb 2026 18:55:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cdc8e2ada368f406368ddbc1a30cf5004317fe0d34e871c30de45de04f5555`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 7.2 MB (7213157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aabb19b2db370ae221b4a8c35a937d4c3ef464ab61a5cc640f4edd0ad27c`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 101.3 KB (101293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec0ca68a54a0c48f91559e549030d59a6ea57fe11e8c8f336d71203e30d4b`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359ce5f20066df79a2c2f15dfc2e4327391b52123711b1b932ba423d19dcd9d`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 60.4 MB (60436023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c858b59040b5e0571d6565b1c252744394e5c91f3fc7666c081592746f8acff`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017336f8dfa381510251cf029e1e8b9068af186aec76d056f13f1bfd02c0cd3`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3efad4ea039a0085ac85140fdaff7b0901f77d844a3ced398908bed50280d3`  
		Last Modified: Tue, 03 Feb 2026 18:55:53 GMT  
		Size: 3.4 MB (3394383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad831014bf8990f5582f5d3e6722e27cfbba3529f3c04cfe9c6a949d88ac099d`  
		Last Modified: Tue, 03 Feb 2026 18:55:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fdeaa64fd5c21fb8b772c2d90c06e6775a9a4bb2843aced9f1875939c73f16`  
		Last Modified: Tue, 03 Feb 2026 18:55:52 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd2325131d24f7831871c339c38827915943cb61cb8728e71b867ad3ebd747e`  
		Last Modified: Tue, 03 Feb 2026 18:55:53 GMT  
		Size: 17.7 MB (17710536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29101bcbdf9cfd2edf02a50ce900b29e142538dd886a8ce77c5a95e1b429560e`  
		Last Modified: Tue, 03 Feb 2026 18:55:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c8832a8a4baba19861161896908a1fba0f16c66b34289e1d7587c4f6f4a2945d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3023e84e94ad559ac9f3b408469b4b362197ad68436d62ad001a7a64cb14b81c`

```dockerfile
```

-	Layers:
	-	`sha256:5b681b0886068572453781d5d67943bb963e404233a24ccd9b820c068524c523`  
		Last Modified: Tue, 03 Feb 2026 18:55:52 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2-windowsservercore`

```console
$ docker pull docker@sha256:79cb1793605b4f2d7317cea6706862e4b002e6ace6375912bab555eebfdf6ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.2-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:315827d701f9fef8731fca2a65b1c5960422bfb5d0e6f335995310b4c2c2bf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:ed671d3152d0f57a459cd9f0838f7e48071ccef5c71ad1188693f4540f24cf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29.2-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2.1`

```console
$ docker pull docker@sha256:8bcbad4b45f0bff9d3e809d85a7ac589390f0be8acbc526850c998c35c1243fd
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

### `docker:29.2.1` - linux; amd64

```console
$ docker pull docker@sha256:2658fda9e8779b94ea1581f4d25214dac9ed144b407902842e5328cce8f861f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143806344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e53a1133dad326140cd3d234b76db232167ef01734e3b1a87cf3fbb1d18f2d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:14 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb3344ffbb9855e9e8c1fc885f05984fa42d8d5830e32df03e0d135ad8822e`  
		Last Modified: Tue, 03 Feb 2026 18:08:25 GMT  
		Size: 6.9 MB (6934690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678f9b57b1bc0e3be53c874c97da597f979a78c280ad71e6d7f63fcb8463911`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 92.5 KB (92473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b249709b45e2c9f5f73832f9cc1ec388f12b297e00d1171b7ce479df111ebd`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635e03777d6fa8913ee09d5abd54e7646e340b3aff6ce8ddff1d2e60f75e349`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 66.6 MB (66625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc6090a660e5dc2d63b3bcc09f50f8c36a471ae548571d43cf9b8a3cfe639c`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ebca63bb1cffa50e238c87876cbad00be5ca7084fa675f75225e8d1f03aeff`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1` - unknown; unknown

```console
$ docker pull docker@sha256:5ca42eff6ef7d7c05200966f252adae0b699ece5fb2f8466eda35d7b36a890ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7670efdca26f8b1bcc0b988fb4f653a6376650ea58b34a100363b082bc6523`

```dockerfile
```

-	Layers:
	-	`sha256:04d995c70a723b002243db02983e46f08e29912414c5e73133bdb721b3f1e9b7`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:96c65c13341f1bd361681f0e10d68a466cb31465af3505c4ab11bb7e57b9f9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135639255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f4d60d48216741f772b218962de8bd12f6b4376c9b7d2d61945efe7de8af09`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:09:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:09:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:09:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:09:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589acbf83b02aefe4b74c88258659fbc3cbc808bca02b74d70fc84c2d85c1f0`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 7.3 MB (7271674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a1dc2d0150cb7d0d0ac4db0350de2ace99ddecbf13ede3f0852e989bee562`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e501e8c157d2cb65e85d675f7f62265ad6bf5403fd2fd5a82159dd013df16`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8a975a5a8a2c7f276059ed5b82c8d8fe03e3aa5f19fe35bfef977eb73f836a`  
		Last Modified: Tue, 03 Feb 2026 18:09:30 GMT  
		Size: 62.0 MB (62034292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b27e1927e65ff11d65fde3dbf30388e85fcddba8f24f5ed68c9556c7029e7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bf263325fbcf53d5d385378f5e9d50ebe967b108a54c4e71e1a21748ca0b7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1` - unknown; unknown

```console
$ docker pull docker@sha256:6322cd1e6550fefe96c9648558e12551a32688528b16770636b40cfafa1a7518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38278b3e49b1412f16afef4b1389dd760ef2f1ec2117c02d9802fab93b7e0ec7`

```dockerfile
```

-	Layers:
	-	`sha256:b5e6e9bb35a96bbc52efdac8258e865ffa07b199e52e6c7be4fd1669bef4fce7`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:a1db2279111145cbcf1396c93955b81f5f2b7de52b32c9ba4859d020f36634f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133723354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284b3692652e58ba18acc63cf8b6e821364031b866cb6682f085149f779ab4ff`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:07:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:07:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:07:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:07:04 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6779a50db6dd09992adc4b403d5daf31daa7cfc8adf6350317537c2e3a7cb5f`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 6.6 MB (6573016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6e53c40bcc58f48835cdaa63c5a7022c93ff9df8c7106f139ce37baca30b5e`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 88.1 KB (88141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bd2d3709e6dab534375a42fc15c6065df38f73068c92ef2e76522924c25b7a`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f50af2801e8d40ff49c6a156103e37cab62872a4a79327fa5b346cfb48b9b`  
		Last Modified: Tue, 03 Feb 2026 18:07:17 GMT  
		Size: 61.9 MB (61863352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee9b22d2befaca7304238ebc8fd562d677a8b437d7f1d379ff801be543a6907`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eec5ef5f0a11840b0e7853071f5ca12064018f7d0d47f6101de217d79f484c7`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1` - unknown; unknown

```console
$ docker pull docker@sha256:c34ad6a1f7894d31642f2ece3bc56bb40c89621d5aca9042df85276dd5d91299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865285598aa081a112650828c916096f6c9d5b691cf04fe2c1fffca77a8e3dd3`

```dockerfile
```

-	Layers:
	-	`sha256:d8d51afa4a991b6fb7cc8cb5be95ab133da93d9f134e00e385b69c869b6bce03`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b5b3b18d8bb9d62276afb346b9392a9ca59fbf21e878c28d1a7694c847c49b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133253666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a395c8fe40dc997f59712d6616f1f5de99e5b87bd8652b1015f377bca5e2d60f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:04 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cdc8e2ada368f406368ddbc1a30cf5004317fe0d34e871c30de45de04f5555`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 7.2 MB (7213157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aabb19b2db370ae221b4a8c35a937d4c3ef464ab61a5cc640f4edd0ad27c`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 101.3 KB (101293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec0ca68a54a0c48f91559e549030d59a6ea57fe11e8c8f336d71203e30d4b`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359ce5f20066df79a2c2f15dfc2e4327391b52123711b1b932ba423d19dcd9d`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 60.4 MB (60436023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c858b59040b5e0571d6565b1c252744394e5c91f3fc7666c081592746f8acff`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017336f8dfa381510251cf029e1e8b9068af186aec76d056f13f1bfd02c0cd3`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1` - unknown; unknown

```console
$ docker pull docker@sha256:a7811e3fe95592d83bd7ac50ab2e29193e551c1ef2f3174975161619ce5a7898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d4b79b678de90d818e106856c1da5f8f57a0df8d7bba87809610bef584af9e`

```dockerfile
```

-	Layers:
	-	`sha256:94845085a82ddc797095cf318c979066478d1a17fa05c408df973ec4c8f31fe3`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.1-alpine3.23`

```console
$ docker pull docker@sha256:8bcbad4b45f0bff9d3e809d85a7ac589390f0be8acbc526850c998c35c1243fd
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

### `docker:29.2.1-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:2658fda9e8779b94ea1581f4d25214dac9ed144b407902842e5328cce8f861f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143806344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e53a1133dad326140cd3d234b76db232167ef01734e3b1a87cf3fbb1d18f2d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:14 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb3344ffbb9855e9e8c1fc885f05984fa42d8d5830e32df03e0d135ad8822e`  
		Last Modified: Tue, 03 Feb 2026 18:08:25 GMT  
		Size: 6.9 MB (6934690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678f9b57b1bc0e3be53c874c97da597f979a78c280ad71e6d7f63fcb8463911`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 92.5 KB (92473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b249709b45e2c9f5f73832f9cc1ec388f12b297e00d1171b7ce479df111ebd`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635e03777d6fa8913ee09d5abd54e7646e340b3aff6ce8ddff1d2e60f75e349`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 66.6 MB (66625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc6090a660e5dc2d63b3bcc09f50f8c36a471ae548571d43cf9b8a3cfe639c`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ebca63bb1cffa50e238c87876cbad00be5ca7084fa675f75225e8d1f03aeff`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:5ca42eff6ef7d7c05200966f252adae0b699ece5fb2f8466eda35d7b36a890ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7670efdca26f8b1bcc0b988fb4f653a6376650ea58b34a100363b082bc6523`

```dockerfile
```

-	Layers:
	-	`sha256:04d995c70a723b002243db02983e46f08e29912414c5e73133bdb721b3f1e9b7`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:96c65c13341f1bd361681f0e10d68a466cb31465af3505c4ab11bb7e57b9f9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135639255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f4d60d48216741f772b218962de8bd12f6b4376c9b7d2d61945efe7de8af09`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:09:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:09:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:09:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:09:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589acbf83b02aefe4b74c88258659fbc3cbc808bca02b74d70fc84c2d85c1f0`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 7.3 MB (7271674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a1dc2d0150cb7d0d0ac4db0350de2ace99ddecbf13ede3f0852e989bee562`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e501e8c157d2cb65e85d675f7f62265ad6bf5403fd2fd5a82159dd013df16`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8a975a5a8a2c7f276059ed5b82c8d8fe03e3aa5f19fe35bfef977eb73f836a`  
		Last Modified: Tue, 03 Feb 2026 18:09:30 GMT  
		Size: 62.0 MB (62034292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b27e1927e65ff11d65fde3dbf30388e85fcddba8f24f5ed68c9556c7029e7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bf263325fbcf53d5d385378f5e9d50ebe967b108a54c4e71e1a21748ca0b7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:6322cd1e6550fefe96c9648558e12551a32688528b16770636b40cfafa1a7518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38278b3e49b1412f16afef4b1389dd760ef2f1ec2117c02d9802fab93b7e0ec7`

```dockerfile
```

-	Layers:
	-	`sha256:b5e6e9bb35a96bbc52efdac8258e865ffa07b199e52e6c7be4fd1669bef4fce7`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:a1db2279111145cbcf1396c93955b81f5f2b7de52b32c9ba4859d020f36634f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133723354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284b3692652e58ba18acc63cf8b6e821364031b866cb6682f085149f779ab4ff`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:07:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:07:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:07:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:07:04 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6779a50db6dd09992adc4b403d5daf31daa7cfc8adf6350317537c2e3a7cb5f`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 6.6 MB (6573016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6e53c40bcc58f48835cdaa63c5a7022c93ff9df8c7106f139ce37baca30b5e`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 88.1 KB (88141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bd2d3709e6dab534375a42fc15c6065df38f73068c92ef2e76522924c25b7a`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f50af2801e8d40ff49c6a156103e37cab62872a4a79327fa5b346cfb48b9b`  
		Last Modified: Tue, 03 Feb 2026 18:07:17 GMT  
		Size: 61.9 MB (61863352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee9b22d2befaca7304238ebc8fd562d677a8b437d7f1d379ff801be543a6907`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eec5ef5f0a11840b0e7853071f5ca12064018f7d0d47f6101de217d79f484c7`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:c34ad6a1f7894d31642f2ece3bc56bb40c89621d5aca9042df85276dd5d91299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865285598aa081a112650828c916096f6c9d5b691cf04fe2c1fffca77a8e3dd3`

```dockerfile
```

-	Layers:
	-	`sha256:d8d51afa4a991b6fb7cc8cb5be95ab133da93d9f134e00e385b69c869b6bce03`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b5b3b18d8bb9d62276afb346b9392a9ca59fbf21e878c28d1a7694c847c49b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133253666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a395c8fe40dc997f59712d6616f1f5de99e5b87bd8652b1015f377bca5e2d60f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:04 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cdc8e2ada368f406368ddbc1a30cf5004317fe0d34e871c30de45de04f5555`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 7.2 MB (7213157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aabb19b2db370ae221b4a8c35a937d4c3ef464ab61a5cc640f4edd0ad27c`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 101.3 KB (101293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec0ca68a54a0c48f91559e549030d59a6ea57fe11e8c8f336d71203e30d4b`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359ce5f20066df79a2c2f15dfc2e4327391b52123711b1b932ba423d19dcd9d`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 60.4 MB (60436023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c858b59040b5e0571d6565b1c252744394e5c91f3fc7666c081592746f8acff`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017336f8dfa381510251cf029e1e8b9068af186aec76d056f13f1bfd02c0cd3`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:a7811e3fe95592d83bd7ac50ab2e29193e551c1ef2f3174975161619ce5a7898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d4b79b678de90d818e106856c1da5f8f57a0df8d7bba87809610bef584af9e`

```dockerfile
```

-	Layers:
	-	`sha256:94845085a82ddc797095cf318c979066478d1a17fa05c408df973ec4c8f31fe3`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.1-cli`

```console
$ docker pull docker@sha256:1d6d751f1d68d1a5142c23c730ef5ecc976a8e050fa08c3cdb09f7e2e54a4439
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

### `docker:29.2.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:0c04277b44d1d448d40238faa142c2edf21d4a90dc0d61486c32056bbf11572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70148082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fa388e81d5f66d9d9ee840c5375a0801629a980c3d9657463257b2c863f324`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c1620c41ed6e739f033f9e98a5bba1cb95e1ea6a093197beb216823c8c93ce72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f4666aeb7f994fb855d5fb4b289608e198a0a0b59b25161f28433aeb36364`

```dockerfile
```

-	Layers:
	-	`sha256:19b63918903a6b77f5af72e60038c44df3a84e5a4563b3db3d54ef79567b8195`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:cf09d93cea103396a11b1b12c36c15b6b93d367c0c80cce733f00214c71c92e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66235505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4367f8d4a4b3fc3d463d69bca54b902b58d4792ccf8967224e2ec3dd7aa4afb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:fbcdf3246eea54b7103bc19f384cd3f454538bd499af80a1566455c68e652971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63de4e3179da9faef11522e19444ae1387215588371c787a0b6852c464dcd77`

```dockerfile
```

-	Layers:
	-	`sha256:97d51d656e276dcee240923733068124918a337234be2ffb56edcdb70a458855`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ba03aff6e89a96861c91cbe97855b49f31e816c782afaa8225043cb76f7ae372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65192844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985b778ba8e60d8ceaa28fed60316b7c31c5ff3e18d6afb37619d388a8da92b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:725c7ed6fedc0c78099cca969de9d894742913605a635c1d1ae732d243e1f9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2b7afca7a73cadfc121038f2cb596614c4eff15299359ccc0fe5915a333dfa`

```dockerfile
```

-	Layers:
	-	`sha256:9fd463f063b0e999eee86b191492b64c48293c00436e4b777db697007872a8d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2bef500bc870e9a4eef5ac67cf6fef451c072f77b7351b207d74a3463c80e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65497196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffbe99c0e2eadb1b2dd8830a3ecddedf95c08183d497287cb048586c0c94905`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:22956d1b0f85ed3aaf3fbd162a232fd08241684704dc328c469298a7a60f924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0c6c28d5d6436cdecdceb1ee544bccb64c7a75c45b13de36e354116226cab3`

```dockerfile
```

-	Layers:
	-	`sha256:0c689b61e422b3962e7df2e52b56054a4e453d576da33fd3b1d6f7dca26d06b6`  
		Last Modified: Tue, 03 Feb 2026 17:26:45 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.1-cli-alpine3.23`

```console
$ docker pull docker@sha256:1d6d751f1d68d1a5142c23c730ef5ecc976a8e050fa08c3cdb09f7e2e54a4439
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

### `docker:29.2.1-cli-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:0c04277b44d1d448d40238faa142c2edf21d4a90dc0d61486c32056bbf11572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70148082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fa388e81d5f66d9d9ee840c5375a0801629a980c3d9657463257b2c863f324`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:c1620c41ed6e739f033f9e98a5bba1cb95e1ea6a093197beb216823c8c93ce72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f4666aeb7f994fb855d5fb4b289608e198a0a0b59b25161f28433aeb36364`

```dockerfile
```

-	Layers:
	-	`sha256:19b63918903a6b77f5af72e60038c44df3a84e5a4563b3db3d54ef79567b8195`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-cli-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:cf09d93cea103396a11b1b12c36c15b6b93d367c0c80cce733f00214c71c92e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66235505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4367f8d4a4b3fc3d463d69bca54b902b58d4792ccf8967224e2ec3dd7aa4afb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:fbcdf3246eea54b7103bc19f384cd3f454538bd499af80a1566455c68e652971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63de4e3179da9faef11522e19444ae1387215588371c787a0b6852c464dcd77`

```dockerfile
```

-	Layers:
	-	`sha256:97d51d656e276dcee240923733068124918a337234be2ffb56edcdb70a458855`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-cli-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:ba03aff6e89a96861c91cbe97855b49f31e816c782afaa8225043cb76f7ae372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65192844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985b778ba8e60d8ceaa28fed60316b7c31c5ff3e18d6afb37619d388a8da92b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:725c7ed6fedc0c78099cca969de9d894742913605a635c1d1ae732d243e1f9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2b7afca7a73cadfc121038f2cb596614c4eff15299359ccc0fe5915a333dfa`

```dockerfile
```

-	Layers:
	-	`sha256:9fd463f063b0e999eee86b191492b64c48293c00436e4b777db697007872a8d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-cli-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2bef500bc870e9a4eef5ac67cf6fef451c072f77b7351b207d74a3463c80e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65497196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffbe99c0e2eadb1b2dd8830a3ecddedf95c08183d497287cb048586c0c94905`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-cli-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:22956d1b0f85ed3aaf3fbd162a232fd08241684704dc328c469298a7a60f924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0c6c28d5d6436cdecdceb1ee544bccb64c7a75c45b13de36e354116226cab3`

```dockerfile
```

-	Layers:
	-	`sha256:0c689b61e422b3962e7df2e52b56054a4e453d576da33fd3b1d6f7dca26d06b6`  
		Last Modified: Tue, 03 Feb 2026 17:26:45 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.1-dind`

```console
$ docker pull docker@sha256:8bcbad4b45f0bff9d3e809d85a7ac589390f0be8acbc526850c998c35c1243fd
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

### `docker:29.2.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:2658fda9e8779b94ea1581f4d25214dac9ed144b407902842e5328cce8f861f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143806344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e53a1133dad326140cd3d234b76db232167ef01734e3b1a87cf3fbb1d18f2d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:14 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb3344ffbb9855e9e8c1fc885f05984fa42d8d5830e32df03e0d135ad8822e`  
		Last Modified: Tue, 03 Feb 2026 18:08:25 GMT  
		Size: 6.9 MB (6934690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678f9b57b1bc0e3be53c874c97da597f979a78c280ad71e6d7f63fcb8463911`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 92.5 KB (92473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b249709b45e2c9f5f73832f9cc1ec388f12b297e00d1171b7ce479df111ebd`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635e03777d6fa8913ee09d5abd54e7646e340b3aff6ce8ddff1d2e60f75e349`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 66.6 MB (66625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc6090a660e5dc2d63b3bcc09f50f8c36a471ae548571d43cf9b8a3cfe639c`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ebca63bb1cffa50e238c87876cbad00be5ca7084fa675f75225e8d1f03aeff`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:5ca42eff6ef7d7c05200966f252adae0b699ece5fb2f8466eda35d7b36a890ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7670efdca26f8b1bcc0b988fb4f653a6376650ea58b34a100363b082bc6523`

```dockerfile
```

-	Layers:
	-	`sha256:04d995c70a723b002243db02983e46f08e29912414c5e73133bdb721b3f1e9b7`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:96c65c13341f1bd361681f0e10d68a466cb31465af3505c4ab11bb7e57b9f9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135639255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f4d60d48216741f772b218962de8bd12f6b4376c9b7d2d61945efe7de8af09`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:09:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:09:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:09:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:09:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589acbf83b02aefe4b74c88258659fbc3cbc808bca02b74d70fc84c2d85c1f0`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 7.3 MB (7271674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a1dc2d0150cb7d0d0ac4db0350de2ace99ddecbf13ede3f0852e989bee562`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e501e8c157d2cb65e85d675f7f62265ad6bf5403fd2fd5a82159dd013df16`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8a975a5a8a2c7f276059ed5b82c8d8fe03e3aa5f19fe35bfef977eb73f836a`  
		Last Modified: Tue, 03 Feb 2026 18:09:30 GMT  
		Size: 62.0 MB (62034292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b27e1927e65ff11d65fde3dbf30388e85fcddba8f24f5ed68c9556c7029e7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bf263325fbcf53d5d385378f5e9d50ebe967b108a54c4e71e1a21748ca0b7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6322cd1e6550fefe96c9648558e12551a32688528b16770636b40cfafa1a7518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38278b3e49b1412f16afef4b1389dd760ef2f1ec2117c02d9802fab93b7e0ec7`

```dockerfile
```

-	Layers:
	-	`sha256:b5e6e9bb35a96bbc52efdac8258e865ffa07b199e52e6c7be4fd1669bef4fce7`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:a1db2279111145cbcf1396c93955b81f5f2b7de52b32c9ba4859d020f36634f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133723354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284b3692652e58ba18acc63cf8b6e821364031b866cb6682f085149f779ab4ff`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:07:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:07:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:07:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:07:04 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6779a50db6dd09992adc4b403d5daf31daa7cfc8adf6350317537c2e3a7cb5f`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 6.6 MB (6573016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6e53c40bcc58f48835cdaa63c5a7022c93ff9df8c7106f139ce37baca30b5e`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 88.1 KB (88141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bd2d3709e6dab534375a42fc15c6065df38f73068c92ef2e76522924c25b7a`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f50af2801e8d40ff49c6a156103e37cab62872a4a79327fa5b346cfb48b9b`  
		Last Modified: Tue, 03 Feb 2026 18:07:17 GMT  
		Size: 61.9 MB (61863352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee9b22d2befaca7304238ebc8fd562d677a8b437d7f1d379ff801be543a6907`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eec5ef5f0a11840b0e7853071f5ca12064018f7d0d47f6101de217d79f484c7`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:c34ad6a1f7894d31642f2ece3bc56bb40c89621d5aca9042df85276dd5d91299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865285598aa081a112650828c916096f6c9d5b691cf04fe2c1fffca77a8e3dd3`

```dockerfile
```

-	Layers:
	-	`sha256:d8d51afa4a991b6fb7cc8cb5be95ab133da93d9f134e00e385b69c869b6bce03`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b5b3b18d8bb9d62276afb346b9392a9ca59fbf21e878c28d1a7694c847c49b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133253666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a395c8fe40dc997f59712d6616f1f5de99e5b87bd8652b1015f377bca5e2d60f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:04 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cdc8e2ada368f406368ddbc1a30cf5004317fe0d34e871c30de45de04f5555`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 7.2 MB (7213157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aabb19b2db370ae221b4a8c35a937d4c3ef464ab61a5cc640f4edd0ad27c`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 101.3 KB (101293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec0ca68a54a0c48f91559e549030d59a6ea57fe11e8c8f336d71203e30d4b`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359ce5f20066df79a2c2f15dfc2e4327391b52123711b1b932ba423d19dcd9d`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 60.4 MB (60436023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c858b59040b5e0571d6565b1c252744394e5c91f3fc7666c081592746f8acff`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017336f8dfa381510251cf029e1e8b9068af186aec76d056f13f1bfd02c0cd3`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a7811e3fe95592d83bd7ac50ab2e29193e551c1ef2f3174975161619ce5a7898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d4b79b678de90d818e106856c1da5f8f57a0df8d7bba87809610bef584af9e`

```dockerfile
```

-	Layers:
	-	`sha256:94845085a82ddc797095cf318c979066478d1a17fa05c408df973ec4c8f31fe3`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.1-dind-alpine3.23`

```console
$ docker pull docker@sha256:8bcbad4b45f0bff9d3e809d85a7ac589390f0be8acbc526850c998c35c1243fd
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

### `docker:29.2.1-dind-alpine3.23` - linux; amd64

```console
$ docker pull docker@sha256:2658fda9e8779b94ea1581f4d25214dac9ed144b407902842e5328cce8f861f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143806344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e53a1133dad326140cd3d234b76db232167ef01734e3b1a87cf3fbb1d18f2d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:14 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb3344ffbb9855e9e8c1fc885f05984fa42d8d5830e32df03e0d135ad8822e`  
		Last Modified: Tue, 03 Feb 2026 18:08:25 GMT  
		Size: 6.9 MB (6934690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678f9b57b1bc0e3be53c874c97da597f979a78c280ad71e6d7f63fcb8463911`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 92.5 KB (92473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b249709b45e2c9f5f73832f9cc1ec388f12b297e00d1171b7ce479df111ebd`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635e03777d6fa8913ee09d5abd54e7646e340b3aff6ce8ddff1d2e60f75e349`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 66.6 MB (66625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc6090a660e5dc2d63b3bcc09f50f8c36a471ae548571d43cf9b8a3cfe639c`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ebca63bb1cffa50e238c87876cbad00be5ca7084fa675f75225e8d1f03aeff`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:5ca42eff6ef7d7c05200966f252adae0b699ece5fb2f8466eda35d7b36a890ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7670efdca26f8b1bcc0b988fb4f653a6376650ea58b34a100363b082bc6523`

```dockerfile
```

-	Layers:
	-	`sha256:04d995c70a723b002243db02983e46f08e29912414c5e73133bdb721b3f1e9b7`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-dind-alpine3.23` - linux; arm variant v6

```console
$ docker pull docker@sha256:96c65c13341f1bd361681f0e10d68a466cb31465af3505c4ab11bb7e57b9f9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135639255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f4d60d48216741f772b218962de8bd12f6b4376c9b7d2d61945efe7de8af09`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:09:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:09:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:09:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:09:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589acbf83b02aefe4b74c88258659fbc3cbc808bca02b74d70fc84c2d85c1f0`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 7.3 MB (7271674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a1dc2d0150cb7d0d0ac4db0350de2ace99ddecbf13ede3f0852e989bee562`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e501e8c157d2cb65e85d675f7f62265ad6bf5403fd2fd5a82159dd013df16`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8a975a5a8a2c7f276059ed5b82c8d8fe03e3aa5f19fe35bfef977eb73f836a`  
		Last Modified: Tue, 03 Feb 2026 18:09:30 GMT  
		Size: 62.0 MB (62034292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b27e1927e65ff11d65fde3dbf30388e85fcddba8f24f5ed68c9556c7029e7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bf263325fbcf53d5d385378f5e9d50ebe967b108a54c4e71e1a21748ca0b7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:6322cd1e6550fefe96c9648558e12551a32688528b16770636b40cfafa1a7518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38278b3e49b1412f16afef4b1389dd760ef2f1ec2117c02d9802fab93b7e0ec7`

```dockerfile
```

-	Layers:
	-	`sha256:b5e6e9bb35a96bbc52efdac8258e865ffa07b199e52e6c7be4fd1669bef4fce7`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-dind-alpine3.23` - linux; arm variant v7

```console
$ docker pull docker@sha256:a1db2279111145cbcf1396c93955b81f5f2b7de52b32c9ba4859d020f36634f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133723354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284b3692652e58ba18acc63cf8b6e821364031b866cb6682f085149f779ab4ff`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:07:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:07:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:07:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:07:04 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6779a50db6dd09992adc4b403d5daf31daa7cfc8adf6350317537c2e3a7cb5f`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 6.6 MB (6573016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6e53c40bcc58f48835cdaa63c5a7022c93ff9df8c7106f139ce37baca30b5e`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 88.1 KB (88141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bd2d3709e6dab534375a42fc15c6065df38f73068c92ef2e76522924c25b7a`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f50af2801e8d40ff49c6a156103e37cab62872a4a79327fa5b346cfb48b9b`  
		Last Modified: Tue, 03 Feb 2026 18:07:17 GMT  
		Size: 61.9 MB (61863352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee9b22d2befaca7304238ebc8fd562d677a8b437d7f1d379ff801be543a6907`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eec5ef5f0a11840b0e7853071f5ca12064018f7d0d47f6101de217d79f484c7`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:c34ad6a1f7894d31642f2ece3bc56bb40c89621d5aca9042df85276dd5d91299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865285598aa081a112650828c916096f6c9d5b691cf04fe2c1fffca77a8e3dd3`

```dockerfile
```

-	Layers:
	-	`sha256:d8d51afa4a991b6fb7cc8cb5be95ab133da93d9f134e00e385b69c869b6bce03`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-dind-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b5b3b18d8bb9d62276afb346b9392a9ca59fbf21e878c28d1a7694c847c49b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133253666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a395c8fe40dc997f59712d6616f1f5de99e5b87bd8652b1015f377bca5e2d60f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:04 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cdc8e2ada368f406368ddbc1a30cf5004317fe0d34e871c30de45de04f5555`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 7.2 MB (7213157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aabb19b2db370ae221b4a8c35a937d4c3ef464ab61a5cc640f4edd0ad27c`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 101.3 KB (101293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec0ca68a54a0c48f91559e549030d59a6ea57fe11e8c8f336d71203e30d4b`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359ce5f20066df79a2c2f15dfc2e4327391b52123711b1b932ba423d19dcd9d`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 60.4 MB (60436023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c858b59040b5e0571d6565b1c252744394e5c91f3fc7666c081592746f8acff`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017336f8dfa381510251cf029e1e8b9068af186aec76d056f13f1bfd02c0cd3`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-dind-alpine3.23` - unknown; unknown

```console
$ docker pull docker@sha256:a7811e3fe95592d83bd7ac50ab2e29193e551c1ef2f3174975161619ce5a7898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d4b79b678de90d818e106856c1da5f8f57a0df8d7bba87809610bef584af9e`

```dockerfile
```

-	Layers:
	-	`sha256:94845085a82ddc797095cf318c979066478d1a17fa05c408df973ec4c8f31fe3`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.1-dind-rootless`

```console
$ docker pull docker@sha256:68bb0d88ed4134f6cc41f04c62e5e49762051b16f628abf84db6f7c33994885c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29.2.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:567ead5a15f1f97b9878eede0250d242c0ef27a19c0dd685d70c1c59e21d750c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164603487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e52a73bd06c9759bd4433c27b69afd58457bdb3174e0153ecf3089eea25736`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:14 GMT
CMD []
# Tue, 03 Feb 2026 18:56:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 03 Feb 2026 18:56:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 03 Feb 2026 18:56:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:56:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 03 Feb 2026 18:56:44 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 03 Feb 2026 18:56:44 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 03 Feb 2026 18:56:44 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb3344ffbb9855e9e8c1fc885f05984fa42d8d5830e32df03e0d135ad8822e`  
		Last Modified: Tue, 03 Feb 2026 18:08:25 GMT  
		Size: 6.9 MB (6934690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678f9b57b1bc0e3be53c874c97da597f979a78c280ad71e6d7f63fcb8463911`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 92.5 KB (92473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b249709b45e2c9f5f73832f9cc1ec388f12b297e00d1171b7ce479df111ebd`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635e03777d6fa8913ee09d5abd54e7646e340b3aff6ce8ddff1d2e60f75e349`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 66.6 MB (66625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc6090a660e5dc2d63b3bcc09f50f8c36a471ae548571d43cf9b8a3cfe639c`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ebca63bb1cffa50e238c87876cbad00be5ca7084fa675f75225e8d1f03aeff`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ae3e167984ddda59e327294c6376b950eea2c3ef31d27360612eac1daa1f0a`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 3.4 MB (3419941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d922f02e9320e8d0119111798e4061c241770bb012211f450efe2d517fd1a42a`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5687d1e84b0ee14d3c1995e61b0e4a68d506dd136ef95f02c8e2b6faaf863a33`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfdc02c4d88b47fb1008ea5191d51a35b34fca85278d2030e245268126bf6c8`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 17.4 MB (17375862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077f22d66325a95178fd420b08832727efb00c81b7c88dd48a131ccb5b1ce2d0`  
		Last Modified: Tue, 03 Feb 2026 18:56:51 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0d5c44c6470979f0c582d86f55d66e742e639e3a8fdc0a404c02021d4f43d416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e137c0f7f1699722fc735873de3ba73dd4cae21481ee991407f271300a01252`

```dockerfile
```

-	Layers:
	-	`sha256:ae18371d1afbd9ae2b2e2a148ace11a55c228a20017f500977180dec98bd30d8`  
		Last Modified: Tue, 03 Feb 2026 18:56:49 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29.2.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c68e67b2934792c04cb7f598418b51467087009fcb45ca095e2b0e350705d699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154359925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b76823faed7a9fec13c67806e9f797ce9b03718d27e5e068ad293efc75410c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:04 GMT
CMD []
# Tue, 03 Feb 2026 18:55:45 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 03 Feb 2026 18:55:45 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 03 Feb 2026 18:55:45 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:55:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 03 Feb 2026 18:55:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 03 Feb 2026 18:55:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 03 Feb 2026 18:55:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cdc8e2ada368f406368ddbc1a30cf5004317fe0d34e871c30de45de04f5555`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 7.2 MB (7213157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aabb19b2db370ae221b4a8c35a937d4c3ef464ab61a5cc640f4edd0ad27c`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 101.3 KB (101293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec0ca68a54a0c48f91559e549030d59a6ea57fe11e8c8f336d71203e30d4b`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359ce5f20066df79a2c2f15dfc2e4327391b52123711b1b932ba423d19dcd9d`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 60.4 MB (60436023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c858b59040b5e0571d6565b1c252744394e5c91f3fc7666c081592746f8acff`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017336f8dfa381510251cf029e1e8b9068af186aec76d056f13f1bfd02c0cd3`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3efad4ea039a0085ac85140fdaff7b0901f77d844a3ced398908bed50280d3`  
		Last Modified: Tue, 03 Feb 2026 18:55:53 GMT  
		Size: 3.4 MB (3394383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad831014bf8990f5582f5d3e6722e27cfbba3529f3c04cfe9c6a949d88ac099d`  
		Last Modified: Tue, 03 Feb 2026 18:55:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fdeaa64fd5c21fb8b772c2d90c06e6775a9a4bb2843aced9f1875939c73f16`  
		Last Modified: Tue, 03 Feb 2026 18:55:52 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd2325131d24f7831871c339c38827915943cb61cb8728e71b867ad3ebd747e`  
		Last Modified: Tue, 03 Feb 2026 18:55:53 GMT  
		Size: 17.7 MB (17710536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29101bcbdf9cfd2edf02a50ce900b29e142538dd886a8ce77c5a95e1b429560e`  
		Last Modified: Tue, 03 Feb 2026 18:55:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29.2.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c8832a8a4baba19861161896908a1fba0f16c66b34289e1d7587c4f6f4a2945d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3023e84e94ad559ac9f3b408469b4b362197ad68436d62ad001a7a64cb14b81c`

```dockerfile
```

-	Layers:
	-	`sha256:5b681b0886068572453781d5d67943bb963e404233a24ccd9b820c068524c523`  
		Last Modified: Tue, 03 Feb 2026 18:55:52 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:29.2.1-windowsservercore`

```console
$ docker pull docker@sha256:79cb1793605b4f2d7317cea6706862e4b002e6ace6375912bab555eebfdf6ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2.1-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29.2.1-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:315827d701f9fef8731fca2a65b1c5960422bfb5d0e6f335995310b4c2c2bf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:29.2.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:29.2.1-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:ed671d3152d0f57a459cd9f0838f7e48071ccef5c71ad1188693f4540f24cf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:29.2.1-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:1d6d751f1d68d1a5142c23c730ef5ecc976a8e050fa08c3cdb09f7e2e54a4439
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
$ docker pull docker@sha256:0c04277b44d1d448d40238faa142c2edf21d4a90dc0d61486c32056bbf11572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70148082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fa388e81d5f66d9d9ee840c5375a0801629a980c3d9657463257b2c863f324`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:c1620c41ed6e739f033f9e98a5bba1cb95e1ea6a093197beb216823c8c93ce72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f4666aeb7f994fb855d5fb4b289608e198a0a0b59b25161f28433aeb36364`

```dockerfile
```

-	Layers:
	-	`sha256:19b63918903a6b77f5af72e60038c44df3a84e5a4563b3db3d54ef79567b8195`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 38.1 KB (38056 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:cf09d93cea103396a11b1b12c36c15b6b93d367c0c80cce733f00214c71c92e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66235505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4367f8d4a4b3fc3d463d69bca54b902b58d4792ccf8967224e2ec3dd7aa4afb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:fbcdf3246eea54b7103bc19f384cd3f454538bd499af80a1566455c68e652971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63de4e3179da9faef11522e19444ae1387215588371c787a0b6852c464dcd77`

```dockerfile
```

-	Layers:
	-	`sha256:97d51d656e276dcee240923733068124918a337234be2ffb56edcdb70a458855`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:ba03aff6e89a96861c91cbe97855b49f31e816c782afaa8225043cb76f7ae372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65192844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985b778ba8e60d8ceaa28fed60316b7c31c5ff3e18d6afb37619d388a8da92b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:725c7ed6fedc0c78099cca969de9d894742913605a635c1d1ae732d243e1f9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2b7afca7a73cadfc121038f2cb596614c4eff15299359ccc0fe5915a333dfa`

```dockerfile
```

-	Layers:
	-	`sha256:9fd463f063b0e999eee86b191492b64c48293c00436e4b777db697007872a8d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 38.2 KB (38222 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:2bef500bc870e9a4eef5ac67cf6fef451c072f77b7351b207d74a3463c80e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65497196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffbe99c0e2eadb1b2dd8830a3ecddedf95c08183d497287cb048586c0c94905`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:22956d1b0f85ed3aaf3fbd162a232fd08241684704dc328c469298a7a60f924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0c6c28d5d6436cdecdceb1ee544bccb64c7a75c45b13de36e354116226cab3`

```dockerfile
```

-	Layers:
	-	`sha256:0c689b61e422b3962e7df2e52b56054a4e453d576da33fd3b1d6f7dca26d06b6`  
		Last Modified: Tue, 03 Feb 2026 17:26:45 GMT  
		Size: 38.3 KB (38258 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:8bcbad4b45f0bff9d3e809d85a7ac589390f0be8acbc526850c998c35c1243fd
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
$ docker pull docker@sha256:2658fda9e8779b94ea1581f4d25214dac9ed144b407902842e5328cce8f861f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143806344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e53a1133dad326140cd3d234b76db232167ef01734e3b1a87cf3fbb1d18f2d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:14 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb3344ffbb9855e9e8c1fc885f05984fa42d8d5830e32df03e0d135ad8822e`  
		Last Modified: Tue, 03 Feb 2026 18:08:25 GMT  
		Size: 6.9 MB (6934690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678f9b57b1bc0e3be53c874c97da597f979a78c280ad71e6d7f63fcb8463911`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 92.5 KB (92473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b249709b45e2c9f5f73832f9cc1ec388f12b297e00d1171b7ce479df111ebd`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635e03777d6fa8913ee09d5abd54e7646e340b3aff6ce8ddff1d2e60f75e349`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 66.6 MB (66625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc6090a660e5dc2d63b3bcc09f50f8c36a471ae548571d43cf9b8a3cfe639c`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ebca63bb1cffa50e238c87876cbad00be5ca7084fa675f75225e8d1f03aeff`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:5ca42eff6ef7d7c05200966f252adae0b699ece5fb2f8466eda35d7b36a890ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7670efdca26f8b1bcc0b988fb4f653a6376650ea58b34a100363b082bc6523`

```dockerfile
```

-	Layers:
	-	`sha256:04d995c70a723b002243db02983e46f08e29912414c5e73133bdb721b3f1e9b7`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:96c65c13341f1bd361681f0e10d68a466cb31465af3505c4ab11bb7e57b9f9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135639255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f4d60d48216741f772b218962de8bd12f6b4376c9b7d2d61945efe7de8af09`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:09:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:09:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:09:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:09:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589acbf83b02aefe4b74c88258659fbc3cbc808bca02b74d70fc84c2d85c1f0`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 7.3 MB (7271674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a1dc2d0150cb7d0d0ac4db0350de2ace99ddecbf13ede3f0852e989bee562`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e501e8c157d2cb65e85d675f7f62265ad6bf5403fd2fd5a82159dd013df16`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8a975a5a8a2c7f276059ed5b82c8d8fe03e3aa5f19fe35bfef977eb73f836a`  
		Last Modified: Tue, 03 Feb 2026 18:09:30 GMT  
		Size: 62.0 MB (62034292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b27e1927e65ff11d65fde3dbf30388e85fcddba8f24f5ed68c9556c7029e7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bf263325fbcf53d5d385378f5e9d50ebe967b108a54c4e71e1a21748ca0b7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:6322cd1e6550fefe96c9648558e12551a32688528b16770636b40cfafa1a7518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38278b3e49b1412f16afef4b1389dd760ef2f1ec2117c02d9802fab93b7e0ec7`

```dockerfile
```

-	Layers:
	-	`sha256:b5e6e9bb35a96bbc52efdac8258e865ffa07b199e52e6c7be4fd1669bef4fce7`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:a1db2279111145cbcf1396c93955b81f5f2b7de52b32c9ba4859d020f36634f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133723354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284b3692652e58ba18acc63cf8b6e821364031b866cb6682f085149f779ab4ff`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:07:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:07:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:07:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:07:04 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6779a50db6dd09992adc4b403d5daf31daa7cfc8adf6350317537c2e3a7cb5f`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 6.6 MB (6573016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6e53c40bcc58f48835cdaa63c5a7022c93ff9df8c7106f139ce37baca30b5e`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 88.1 KB (88141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bd2d3709e6dab534375a42fc15c6065df38f73068c92ef2e76522924c25b7a`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f50af2801e8d40ff49c6a156103e37cab62872a4a79327fa5b346cfb48b9b`  
		Last Modified: Tue, 03 Feb 2026 18:07:17 GMT  
		Size: 61.9 MB (61863352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee9b22d2befaca7304238ebc8fd562d677a8b437d7f1d379ff801be543a6907`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eec5ef5f0a11840b0e7853071f5ca12064018f7d0d47f6101de217d79f484c7`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:c34ad6a1f7894d31642f2ece3bc56bb40c89621d5aca9042df85276dd5d91299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865285598aa081a112650828c916096f6c9d5b691cf04fe2c1fffca77a8e3dd3`

```dockerfile
```

-	Layers:
	-	`sha256:d8d51afa4a991b6fb7cc8cb5be95ab133da93d9f134e00e385b69c869b6bce03`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b5b3b18d8bb9d62276afb346b9392a9ca59fbf21e878c28d1a7694c847c49b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133253666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a395c8fe40dc997f59712d6616f1f5de99e5b87bd8652b1015f377bca5e2d60f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:04 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cdc8e2ada368f406368ddbc1a30cf5004317fe0d34e871c30de45de04f5555`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 7.2 MB (7213157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aabb19b2db370ae221b4a8c35a937d4c3ef464ab61a5cc640f4edd0ad27c`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 101.3 KB (101293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec0ca68a54a0c48f91559e549030d59a6ea57fe11e8c8f336d71203e30d4b`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359ce5f20066df79a2c2f15dfc2e4327391b52123711b1b932ba423d19dcd9d`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 60.4 MB (60436023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c858b59040b5e0571d6565b1c252744394e5c91f3fc7666c081592746f8acff`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017336f8dfa381510251cf029e1e8b9068af186aec76d056f13f1bfd02c0cd3`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a7811e3fe95592d83bd7ac50ab2e29193e551c1ef2f3174975161619ce5a7898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d4b79b678de90d818e106856c1da5f8f57a0df8d7bba87809610bef584af9e`

```dockerfile
```

-	Layers:
	-	`sha256:94845085a82ddc797095cf318c979066478d1a17fa05c408df973ec4c8f31fe3`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:68bb0d88ed4134f6cc41f04c62e5e49762051b16f628abf84db6f7c33994885c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:567ead5a15f1f97b9878eede0250d242c0ef27a19c0dd685d70c1c59e21d750c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164603487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e52a73bd06c9759bd4433c27b69afd58457bdb3174e0153ecf3089eea25736`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:14 GMT
CMD []
# Tue, 03 Feb 2026 18:56:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 03 Feb 2026 18:56:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 03 Feb 2026 18:56:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:56:44 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 03 Feb 2026 18:56:44 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 03 Feb 2026 18:56:44 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 03 Feb 2026 18:56:44 GMT
USER rootless
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb3344ffbb9855e9e8c1fc885f05984fa42d8d5830e32df03e0d135ad8822e`  
		Last Modified: Tue, 03 Feb 2026 18:08:25 GMT  
		Size: 6.9 MB (6934690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678f9b57b1bc0e3be53c874c97da597f979a78c280ad71e6d7f63fcb8463911`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 92.5 KB (92473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b249709b45e2c9f5f73832f9cc1ec388f12b297e00d1171b7ce479df111ebd`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635e03777d6fa8913ee09d5abd54e7646e340b3aff6ce8ddff1d2e60f75e349`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 66.6 MB (66625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc6090a660e5dc2d63b3bcc09f50f8c36a471ae548571d43cf9b8a3cfe639c`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ebca63bb1cffa50e238c87876cbad00be5ca7084fa675f75225e8d1f03aeff`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ae3e167984ddda59e327294c6376b950eea2c3ef31d27360612eac1daa1f0a`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 3.4 MB (3419941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d922f02e9320e8d0119111798e4061c241770bb012211f450efe2d517fd1a42a`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5687d1e84b0ee14d3c1995e61b0e4a68d506dd136ef95f02c8e2b6faaf863a33`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfdc02c4d88b47fb1008ea5191d51a35b34fca85278d2030e245268126bf6c8`  
		Last Modified: Tue, 03 Feb 2026 18:56:50 GMT  
		Size: 17.4 MB (17375862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077f22d66325a95178fd420b08832727efb00c81b7c88dd48a131ccb5b1ce2d0`  
		Last Modified: Tue, 03 Feb 2026 18:56:51 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0d5c44c6470979f0c582d86f55d66e742e639e3a8fdc0a404c02021d4f43d416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e137c0f7f1699722fc735873de3ba73dd4cae21481ee991407f271300a01252`

```dockerfile
```

-	Layers:
	-	`sha256:ae18371d1afbd9ae2b2e2a148ace11a55c228a20017f500977180dec98bd30d8`  
		Last Modified: Tue, 03 Feb 2026 18:56:49 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:c68e67b2934792c04cb7f598418b51467087009fcb45ca095e2b0e350705d699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154359925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b76823faed7a9fec13c67806e9f797ce9b03718d27e5e068ad293efc75410c4`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:04 GMT
CMD []
# Tue, 03 Feb 2026 18:55:45 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 03 Feb 2026 18:55:45 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 03 Feb 2026 18:55:45 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:55:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 03 Feb 2026 18:55:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 03 Feb 2026 18:55:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 03 Feb 2026 18:55:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cdc8e2ada368f406368ddbc1a30cf5004317fe0d34e871c30de45de04f5555`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 7.2 MB (7213157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aabb19b2db370ae221b4a8c35a937d4c3ef464ab61a5cc640f4edd0ad27c`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 101.3 KB (101293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec0ca68a54a0c48f91559e549030d59a6ea57fe11e8c8f336d71203e30d4b`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359ce5f20066df79a2c2f15dfc2e4327391b52123711b1b932ba423d19dcd9d`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 60.4 MB (60436023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c858b59040b5e0571d6565b1c252744394e5c91f3fc7666c081592746f8acff`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017336f8dfa381510251cf029e1e8b9068af186aec76d056f13f1bfd02c0cd3`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3efad4ea039a0085ac85140fdaff7b0901f77d844a3ced398908bed50280d3`  
		Last Modified: Tue, 03 Feb 2026 18:55:53 GMT  
		Size: 3.4 MB (3394383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad831014bf8990f5582f5d3e6722e27cfbba3529f3c04cfe9c6a949d88ac099d`  
		Last Modified: Tue, 03 Feb 2026 18:55:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fdeaa64fd5c21fb8b772c2d90c06e6775a9a4bb2843aced9f1875939c73f16`  
		Last Modified: Tue, 03 Feb 2026 18:55:52 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd2325131d24f7831871c339c38827915943cb61cb8728e71b867ad3ebd747e`  
		Last Modified: Tue, 03 Feb 2026 18:55:53 GMT  
		Size: 17.7 MB (17710536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29101bcbdf9cfd2edf02a50ce900b29e142538dd886a8ce77c5a95e1b429560e`  
		Last Modified: Tue, 03 Feb 2026 18:55:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c8832a8a4baba19861161896908a1fba0f16c66b34289e1d7587c4f6f4a2945d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3023e84e94ad559ac9f3b408469b4b362197ad68436d62ad001a7a64cb14b81c`

```dockerfile
```

-	Layers:
	-	`sha256:5b681b0886068572453781d5d67943bb963e404233a24ccd9b820c068524c523`  
		Last Modified: Tue, 03 Feb 2026 18:55:52 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:8bcbad4b45f0bff9d3e809d85a7ac589390f0be8acbc526850c998c35c1243fd
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
$ docker pull docker@sha256:2658fda9e8779b94ea1581f4d25214dac9ed144b407902842e5328cce8f861f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143806344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e53a1133dad326140cd3d234b76db232167ef01734e3b1a87cf3fbb1d18f2d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:58 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:59 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:00 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:00 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:00 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:10 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:11 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:14 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:14 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:14 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:14 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:14 GMT
CMD []
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ffbc9e9d61a3a427749366541c9e55c1440658b296b288726282a7e3a200f3`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 8.4 MB (8399657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9130c567f6fc24a30ebaa5979b9c6700d6c174c3a52a1e753c42621bfb1a32d9`  
		Last Modified: Tue, 03 Feb 2026 17:26:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75aa627f4cd980f8d8c3e7be1834e54e286a6499508105b6f72c4a373c7a6e`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 18.8 MB (18773130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c979ccecd955439750b7f01789bf427e4c8d60acbf2b4a12100ff3173aea9b`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 28.3 MB (28311545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217f84c60501e3b3fb548f194b2861bfcb2a70aa12a9abe9b0d4ee342d75a7b5`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 10.8 MB (10799774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf8952411ee385ba36420d9b6bdcc36594a8be8bdace8fe62d7d97f81322411`  
		Last Modified: Tue, 03 Feb 2026 17:26:08 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f757cc0a441eaf36dbebd029cb42e59a8c463fb4ea19e2ec6bf557d5a981dc2`  
		Last Modified: Tue, 03 Feb 2026 17:26:09 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7358b0dc3398fd6f4c32455892c6ab6fbc099f1a8e62df04445dec7663a095`  
		Last Modified: Tue, 03 Feb 2026 17:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb3344ffbb9855e9e8c1fc885f05984fa42d8d5830e32df03e0d135ad8822e`  
		Last Modified: Tue, 03 Feb 2026 18:08:25 GMT  
		Size: 6.9 MB (6934690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5678f9b57b1bc0e3be53c874c97da597f979a78c280ad71e6d7f63fcb8463911`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 92.5 KB (92473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b249709b45e2c9f5f73832f9cc1ec388f12b297e00d1171b7ce479df111ebd`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5635e03777d6fa8913ee09d5abd54e7646e340b3aff6ce8ddff1d2e60f75e349`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 66.6 MB (66625104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dc6090a660e5dc2d63b3bcc09f50f8c36a471ae548571d43cf9b8a3cfe639c`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ebca63bb1cffa50e238c87876cbad00be5ca7084fa675f75225e8d1f03aeff`  
		Last Modified: Tue, 03 Feb 2026 18:08:26 GMT  
		Size: 3.3 KB (3296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:5ca42eff6ef7d7c05200966f252adae0b699ece5fb2f8466eda35d7b36a890ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7670efdca26f8b1bcc0b988fb4f653a6376650ea58b34a100363b082bc6523`

```dockerfile
```

-	Layers:
	-	`sha256:04d995c70a723b002243db02983e46f08e29912414c5e73133bdb721b3f1e9b7`  
		Last Modified: Tue, 03 Feb 2026 18:08:24 GMT  
		Size: 34.5 KB (34542 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:96c65c13341f1bd361681f0e10d68a466cb31465af3505c4ab11bb7e57b9f9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135639255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f4d60d48216741f772b218962de8bd12f6b4376c9b7d2d61945efe7de8af09`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:25:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:25:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:25:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:25:31 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:25:33 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:25:33 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:25:35 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:25:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:25:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:25:35 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:09:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:09:14 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:09:17 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:09:17 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:09:18 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:09:18 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:09:18 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:09:18 GMT
CMD []
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ed7f28a4b26e2736ceb8045d972a5f166880f3b93b1ce13d7cb7710819f7c0`  
		Last Modified: Tue, 03 Feb 2026 17:25:42 GMT  
		Size: 8.3 MB (8300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59982a56599ba445b45c1ff95a9bf2efe937cb3105d8107453c37e42aa96ab06`  
		Last Modified: Tue, 03 Feb 2026 17:25:41 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627db20a49a4f2be2d19fe161406f293a8b8804c985028e04c1cd95f0c40d96e`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 17.6 MB (17575014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acd42cfefd8cbfbea51ccc805027f78eefae1b3ad5cb91c207ebf9578a6a855`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 26.6 MB (26574500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac22564cea85937e49534e5ef435197d6c83fb053c5aa91ffddb70acae2ff81`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 10.2 MB (10213046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8735f9cb2ee8a9b930cd6b2bf3885083108a83a3707f302210e9bb0a138c15ec`  
		Last Modified: Tue, 03 Feb 2026 17:25:43 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf43e9302aee150c8b25e6f5c53d2eb8642dd7db31500f8f7e980a6639b3d75`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ca294aaca561ae37709af7d9406792302f6ac4cfe16d2068ba04176c0aa2a`  
		Last Modified: Tue, 03 Feb 2026 17:25:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589acbf83b02aefe4b74c88258659fbc3cbc808bca02b74d70fc84c2d85c1f0`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 7.3 MB (7271674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36a1dc2d0150cb7d0d0ac4db0350de2ace99ddecbf13ede3f0852e989bee562`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e501e8c157d2cb65e85d675f7f62265ad6bf5403fd2fd5a82159dd013df16`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8a975a5a8a2c7f276059ed5b82c8d8fe03e3aa5f19fe35bfef977eb73f836a`  
		Last Modified: Tue, 03 Feb 2026 18:09:30 GMT  
		Size: 62.0 MB (62034292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b27e1927e65ff11d65fde3dbf30388e85fcddba8f24f5ed68c9556c7029e7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bf263325fbcf53d5d385378f5e9d50ebe967b108a54c4e71e1a21748ca0b7`  
		Last Modified: Tue, 03 Feb 2026 18:09:29 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:6322cd1e6550fefe96c9648558e12551a32688528b16770636b40cfafa1a7518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38278b3e49b1412f16afef4b1389dd760ef2f1ec2117c02d9802fab93b7e0ec7`

```dockerfile
```

-	Layers:
	-	`sha256:b5e6e9bb35a96bbc52efdac8258e865ffa07b199e52e6c7be4fd1669bef4fce7`  
		Last Modified: Tue, 03 Feb 2026 18:09:28 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:a1db2279111145cbcf1396c93955b81f5f2b7de52b32c9ba4859d020f36634f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133723354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284b3692652e58ba18acc63cf8b6e821364031b866cb6682f085149f779ab4ff`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:11 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:11 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:15 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:19 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:19 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:20 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:20 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:20 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:07:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:07:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:07:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:07:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:07:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:07:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:07:04 GMT
CMD []
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb5af91453d1293030fbe90db4c6166609f99510d3fcec579be00a21249cbf2`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 7.6 MB (7597849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7fbe9447e7591ff3854f01ba9776952a93a9c4f22447067e6a9e1c3f93c760`  
		Last Modified: Tue, 03 Feb 2026 17:26:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc7844b3d362e6b692567d2587e4fd19b348dff44182f52019fdefe7ab344`  
		Last Modified: Tue, 03 Feb 2026 17:26:28 GMT  
		Size: 17.6 MB (17566404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9111fb63645fb502831d395247748514cc38c89a036c0c80ac0d68172af396`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 26.5 MB (26546121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17318896bc84227a623de0b09b1c19d9ba46473321e3c6ef037516d813f8da1`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 10.2 MB (10198592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58cddeebb4c56cedfe3c4d3406be79ac683f61f8d149db919627222cd847dae`  
		Last Modified: Tue, 03 Feb 2026 17:26:29 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cca7f5e3f5fc71d61ff7160fba4b5af52d1d5c1376ef27109056ee0bd35891`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68671e7ea5f72eebefa27db844dfc891bba0667adb87fda60be5a0a78a9e0af3`  
		Last Modified: Tue, 03 Feb 2026 17:26:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6779a50db6dd09992adc4b403d5daf31daa7cfc8adf6350317537c2e3a7cb5f`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 6.6 MB (6573016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6e53c40bcc58f48835cdaa63c5a7022c93ff9df8c7106f139ce37baca30b5e`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 88.1 KB (88141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bd2d3709e6dab534375a42fc15c6065df38f73068c92ef2e76522924c25b7a`  
		Last Modified: Tue, 03 Feb 2026 18:07:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f50af2801e8d40ff49c6a156103e37cab62872a4a79327fa5b346cfb48b9b`  
		Last Modified: Tue, 03 Feb 2026 18:07:17 GMT  
		Size: 61.9 MB (61863352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee9b22d2befaca7304238ebc8fd562d677a8b437d7f1d379ff801be543a6907`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eec5ef5f0a11840b0e7853071f5ca12064018f7d0d47f6101de217d79f484c7`  
		Last Modified: Tue, 03 Feb 2026 18:07:16 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:c34ad6a1f7894d31642f2ece3bc56bb40c89621d5aca9042df85276dd5d91299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865285598aa081a112650828c916096f6c9d5b691cf04fe2c1fffca77a8e3dd3`

```dockerfile
```

-	Layers:
	-	`sha256:d8d51afa4a991b6fb7cc8cb5be95ab133da93d9f134e00e385b69c869b6bce03`  
		Last Modified: Tue, 03 Feb 2026 18:07:14 GMT  
		Size: 34.7 KB (34722 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b5b3b18d8bb9d62276afb346b9392a9ca59fbf21e878c28d1a7694c847c49b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133253666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a395c8fe40dc997f59712d6616f1f5de99e5b87bd8652b1015f377bca5e2d60f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Feb 2026 17:26:35 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Feb 2026 17:26:35 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:26:37 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Feb 2026 17:26:37 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:26:38 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-amd64'; 			sha256='dc8eaffbf29138123b4874d852522b12303c61246a5073fa0f025e4220317b1e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v6'; 			sha256='0b661aa682eb421fb497e080b02f58357bc1f1e83744ffc6fb8de2671f330e93'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm-v7'; 			sha256='9a3cd7007611be95608a623b01ce9749b667450bf57f756e112770eeaa3cde8b'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-arm64'; 			sha256='963c674c558dad2eefd42304a09020329a196ed16819b72396e7657eb69f031b'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-ppc64le'; 			sha256='67016c06ceaaf076f852f07f6172f0edc6d71fb6f1436664f9877db68e2ffcfe'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-riscv64'; 			sha256='20ad44615fa09af8eccad4014040c0b59d5c83192337be0bd293b2cf732f606f'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.linux-s390x'; 			sha256='759b12386f3ec701b4255986193d339fad3093033d4786caab04bbdb9cc0d10a'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Feb 2026 17:26:38 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:26:39 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-x86_64'; 			sha256='2d880f723d3da7c779c54fdaea91a842fca8af55d1397f1ed8d7cbab3dd7af67'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv6'; 			sha256='6618f69bff2b9d2119164e4b44038e1b049c3cc9db39d49f8560db254b0a24b7'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-armv7'; 			sha256='d9a0742638f15bd91598ce465cca8718490d967cfb1a28305c388f214d09976b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-aarch64'; 			sha256='ac7810e0cd56a5b58576688196fafa843e07e8241fb91018a736d549ea20a3f3'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-ppc64le'; 			sha256='1e7ff60971411ffba30208c24c6f0988f8589b9d7bf7783c42f229e95f0648c3'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-riscv64'; 			sha256='745cc32f394cd68bb4f09124c43d5d4532277859b6c92efab619722af6eac686'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-linux-s390x'; 			sha256='d5a9fb6b035cf040fceecccca4892cf55f291e9bf1bb7dd5eb089923bc6e0aac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Feb 2026 17:26:39 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Feb 2026 17:26:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 17:26:39 GMT
CMD ["sh"]
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Feb 2026 18:08:01 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.2.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.2.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.2.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.2.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Tue, 03 Feb 2026 18:08:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 18:08:04 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Feb 2026 18:08:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Feb 2026 18:08:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Feb 2026 18:08:04 GMT
CMD []
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42a77f5fc93e1d6c642b2eb20bac67ddedc3fa614973ecad5d2425aa529cc7f`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 8.5 MB (8453512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9817403955ea5ea2eedc37cde61397fd369d7b07e3863286754b4989d443759a`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23c75ff3415b6637326f398bd112a7ec4373805d39318b94b65c8ff6ce7538`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 17.3 MB (17349111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfca817951310f1a68cb06e3fe0f27540e7d76c61b144cbbb1ebaa04308c8233`  
		Last Modified: Tue, 03 Feb 2026 17:26:46 GMT  
		Size: 25.5 MB (25540815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7af456c729c76507dbf99635546e893dd549241c3157a2a655f1a7472544d6`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 10.0 MB (9954516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72242c4fb87c9ebb62312863874911bfe531f06775fe6a90aa5c937db6274442`  
		Last Modified: Tue, 03 Feb 2026 17:26:47 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91b41b56d8ea2c6e69d6ed8a929177b21cc4e84b65284dd552f20cda40c3dd`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fa267764c487b75a914eae88e45afb0bdd82be8b4c090d4af5946454d79964`  
		Last Modified: Tue, 03 Feb 2026 17:26:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cdc8e2ada368f406368ddbc1a30cf5004317fe0d34e871c30de45de04f5555`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 7.2 MB (7213157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c58aabb19b2db370ae221b4a8c35a937d4c3ef464ab61a5cc640f4edd0ad27c`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 101.3 KB (101293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaec0ca68a54a0c48f91559e549030d59a6ea57fe11e8c8f336d71203e30d4b`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c359ce5f20066df79a2c2f15dfc2e4327391b52123711b1b932ba423d19dcd9d`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 60.4 MB (60436023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c858b59040b5e0571d6565b1c252744394e5c91f3fc7666c081592746f8acff`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9017336f8dfa381510251cf029e1e8b9068af186aec76d056f13f1bfd02c0cd3`  
		Last Modified: Tue, 03 Feb 2026 18:08:15 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:a7811e3fe95592d83bd7ac50ab2e29193e551c1ef2f3174975161619ce5a7898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d4b79b678de90d818e106856c1da5f8f57a0df8d7bba87809610bef584af9e`

```dockerfile
```

-	Layers:
	-	`sha256:94845085a82ddc797095cf318c979066478d1a17fa05c408df973ec4c8f31fe3`  
		Last Modified: Tue, 03 Feb 2026 18:08:14 GMT  
		Size: 34.8 KB (34776 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:79cb1793605b4f2d7317cea6706862e4b002e6ace6375912bab555eebfdf6ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `docker:windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:315827d701f9fef8731fca2a65b1c5960422bfb5d0e6f335995310b4c2c2bf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull docker@sha256:ba1e9a93d62651a48e0592e4a6010300708e2422e46df2b25d54b1d2f1e7fb47
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896494534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09c7520bcdba0cceb87d9e1fe705ea6641137be025705d09eaba1893561ddea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 03 Feb 2026 17:28:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:49 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:49 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:30:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:17 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:30:18 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:30:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:50 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:52 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:31:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1610c61d22cce1c0da1f89bcf2b2b93db5d1ee6703ddda8c50c992a55a3a3273`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35301633ca92d436f45505192a1ef4f18618178fd179a0275e79d55f1cdba61d`  
		Last Modified: Tue, 03 Feb 2026 17:31:19 GMT  
		Size: 502.0 KB (501985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc76ce47c4de88873c339dee382928f8c2afe957a1f67eaa1bc1745de35e796e`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c0a93da300b8f2017782995a21ddcc03360f0068884e95f2c90a34943b5a853`  
		Last Modified: Tue, 03 Feb 2026 17:31:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642a451e4aa3a689441cf53a384a5333b79045931964aecc32acb75dab6242f`  
		Last Modified: Tue, 03 Feb 2026 17:31:20 GMT  
		Size: 19.4 MB (19440499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80fcdb722aba8bdf0a57b047c109edce18d999e3bc1649781fa0d3de37c6e29`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52573eb20ed9e08365fa5f5e972f07f60f80fd44870b2c8c2e00435b86e529d7`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc93a0644ac21577feac91654ceef3e9cb714742257794765b8f41f26967f84e`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c020b7de7a60805f5e0f214c5933b5730ce1e22475c6c0637dbe59005c03baa4`  
		Last Modified: Tue, 03 Feb 2026 17:31:33 GMT  
		Size: 29.4 MB (29425091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538b00d976a03c45b55d387636033ba066f8d59660d195f26399a156232cb079`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8c0456ab18eeca4e06f6a4f1edc155807d2fd8565b3c71217f4895c0778536`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525c0f16947c0cc46484ca50b3cbe0be998327c9e218a8f15dd79b3752be1f84`  
		Last Modified: Tue, 03 Feb 2026 17:31:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29f86a605fc1d2ecf16f261c2beeb1261773d00bba4c7341e76d2363f15db4a`  
		Last Modified: Tue, 03 Feb 2026 17:31:16 GMT  
		Size: 11.5 MB (11456032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:ed671d3152d0f57a459cd9f0838f7e48071ccef5c71ad1188693f4540f24cf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull docker@sha256:c5d3ecbfcaeb424c90459ac8317405555d19b1b8b3e578390234d4a8e7c24c64
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1556599774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647b193ba9f5cb583f9fb294f2d532c6d85295880ef0649d60793cc309abcd1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 03 Feb 2026 17:28:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Feb 2026 17:29:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Feb 2026 17:29:30 GMT
ENV DOCKER_VERSION=29.2.1
# Tue, 03 Feb 2026 17:29:32 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.2.1.zip
# Tue, 03 Feb 2026 17:29:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:29:46 GMT
ENV DOCKER_BUILDX_VERSION=0.31.1
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.31.1/buildx-v0.31.1.windows-amd64.exe
# Tue, 03 Feb 2026 17:29:48 GMT
ENV DOCKER_BUILDX_SHA256=b49832d4ac46bde05006f7ad3506b9d5060b60e5c566545d8e10c1a80df08a4a
# Tue, 03 Feb 2026 17:29:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 03 Feb 2026 17:30:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.2
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.2/docker-compose-windows-x86_64.exe
# Tue, 03 Feb 2026 17:30:01 GMT
ENV DOCKER_COMPOSE_SHA256=e6281c7b906eafe8f39114e735f11fc276d8cce2cba93a54911ca15337ba6c49
# Tue, 03 Feb 2026 17:30:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3345d2727a1883e3d335172c07a1f0f478ed9c744e1aa4ec455219fd5b041b31`  
		Last Modified: Tue, 03 Feb 2026 17:30:17 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2b758f14303d714990de0fad8eacb8f18d18925809a064fa024e0a8203573a`  
		Last Modified: Tue, 03 Feb 2026 17:30:16 GMT  
		Size: 402.8 KB (402791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c544aebc260938057720752277d7e0b5a599ebf13c36d8be0403e694d8929db8`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54275eb139ff712b0a5f139cdba772a69cd2371fcb0b65f6371b8d8b22f92c19`  
		Last Modified: Tue, 03 Feb 2026 17:30:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff99eb3d4bee14899afa2383e60cfa18a0f63d88f5c759afcbfa0cef9bae50bb`  
		Last Modified: Tue, 03 Feb 2026 17:30:18 GMT  
		Size: 19.5 MB (19477937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a57f5276cfc049bae3b7a853039be549c9bada93ef2e8d868ea54e9c04236`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be178348f9fba72db323ad766660239b1363bbe80d1f01cf90cd2531b5f01b03`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77ca63bd7d4b72f07134cb3691a9edeba02acdb61fb8ff15a7f6c7f44734ce`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aa328a4c51fa2977445e97c24b485b2fbf132d207a9adfa58cf7406f3f8a1f`  
		Last Modified: Tue, 03 Feb 2026 17:30:30 GMT  
		Size: 29.5 MB (29453041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c300d10089e1c370f164537efd3c43df949644198f422eb4863dccfe9930a4f`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5356d434dcd14c58d539907321e96d2a0e794ac74a29c08aa2df1dbaa611e231`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b03bbb60e30cb160ee1c1c6844849f758718d7111a7cb510a1b0ec1702120fd`  
		Last Modified: Tue, 03 Feb 2026 17:30:12 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d04ad8db9950e63dbd9118d08d70484b5aed5cf9dadf9591e16f2a8339e8e`  
		Last Modified: Tue, 03 Feb 2026 17:30:14 GMT  
		Size: 11.5 MB (11493926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
