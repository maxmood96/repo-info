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
-	[`docker:28.3.2`](#docker2832)
-	[`docker:28.3.2-alpine3.22`](#docker2832-alpine322)
-	[`docker:28.3.2-cli`](#docker2832-cli)
-	[`docker:28.3.2-cli-alpine3.22`](#docker2832-cli-alpine322)
-	[`docker:28.3.2-dind`](#docker2832-dind)
-	[`docker:28.3.2-dind-alpine3.22`](#docker2832-dind-alpine322)
-	[`docker:28.3.2-dind-rootless`](#docker2832-dind-rootless)
-	[`docker:28.3.2-windowsservercore`](#docker2832-windowsservercore)
-	[`docker:28.3.2-windowsservercore-ltsc2022`](#docker2832-windowsservercore-ltsc2022)
-	[`docker:28.3.2-windowsservercore-ltsc2025`](#docker2832-windowsservercore-ltsc2025)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)
-	[`docker:windowsservercore-ltsc2025`](#dockerwindowsservercore-ltsc2025)

## `docker:28`

```console
$ docker pull docker@sha256:684bc226a69eb91582738f196e59e234355420ee592abea7685e4127afbce645
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
$ docker pull docker@sha256:2039571fb2946ea368779140c94dfbda3c7858b493c42dbbe8345d19500e6d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147544548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d269157efa5eebf6dbc86f558a80e2cb8016c6a9a39793526a4396a512f6d2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb387276c10661bba84fce126eed7b4ef9ef3622bbaf76fed5855a2f4712ce89`  
		Last Modified: Fri, 11 Jul 2025 23:08:13 GMT  
		Size: 9.5 MB (9506675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f8a93798fbae872851b58e72ef4b3bdace12203577685b3e52d5e94c24b42`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 90.5 KB (90506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f487a7a0e1532da82eb272ebcd78402bf76ee707c063da6f3f485326c3d403a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1f25172b8052f548668179a49f8d03408390b474e886f7afd40ce39007449`  
		Last Modified: Fri, 11 Jul 2025 23:08:15 GMT  
		Size: 62.5 MB (62517439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f23e14ee4f80c7f15ead5263837d831d43d4d8023341200c812784762d266a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c327638cbba730a460f516b7fca541b5b3543003eed01c494273d4afe84af`  
		Last Modified: Fri, 11 Jul 2025 23:08:09 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:1612ef52d558ce839416d05d730405b29142c973896aabc995f904e7ab473970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91d6a682e933349713bef3b27e24c6173ee392272ac25eb3fa024eaffdb3758`

```dockerfile
```

-	Layers:
	-	`sha256:f4f1bd41a1006eba393a7d70732b5d538b904f8edc1eea71cba3c25ee7102546`  
		Last Modified: Sat, 12 Jul 2025 02:07:33 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v6

```console
$ docker pull docker@sha256:3960ae5dceff97e2f1523fbadd2521995a9daf4d387a5480808a22b2c0899b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138138376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ee56a5d4421a9708d18d5433cfbbbe8d0327c86185361a95dc2e7fd2cf8b64`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7539813331bce9849eabb04feabc475057f406b6008e4ee8fe9cc34b09584181`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 9.5 MB (9461142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0883a2e698c28639f5e51239c30f623739e588758e46b282b4d86ca0696974e5`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd721e456a1abbd99a37541edfb801f174d50c67eb927d7d11c5f99171d47d62`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed9a7b148f299ea5bae85c09fc8c8f23d43bf689367f224453031283e72d0c8`  
		Last Modified: Fri, 11 Jul 2025 23:07:39 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b17794da37735f4238675dc8f08e3b997577476e766a2823c345f45dc6032`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272cd592cd54400557bde2759b815592c11caed1b9ab0f1e3fbf4c40d586a8ee`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:fba4e76c7a853c8ec14ed8001c3f8afbea81b47032255689ca70d6f5f3f2c9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa67ed505137fefa99d92897b086b45c84d8e36db4289bbea88b2c0eb844d0a`

```dockerfile
```

-	Layers:
	-	`sha256:7c9d7dc66552b1f6a8db09f35ffcedf83ab42a2e73c3233cfb147e16b92cf06f`  
		Last Modified: Sat, 12 Jul 2025 02:07:37 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm variant v7

```console
$ docker pull docker@sha256:5eb2289358e41707da0542f5777d08c6a252b8f0ded58903fcd72fe467703bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136289051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d930d302a73d55f2c350884eed98d79c117d882a7d599b564826bdb27828068`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c7a3c227e0d7b893835a896bf1421afe6c7a1bfe44b1141899c2a4ef2e889`  
		Last Modified: Fri, 11 Jul 2025 23:32:59 GMT  
		Size: 8.6 MB (8610408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33069b480d39ad0fd6e38090b30b043a73413afa7ca6ed1e0f3d1b54961669b0`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 86.5 KB (86504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129027ab9eb0b76ac3acd19b4198612a65e9c9f6f8b472a5d1bacb8583090852`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c185229dea08b37f2a81137ce8ea0b1455bbbdd9055c1ce9f9e1240066b71216`  
		Last Modified: Fri, 11 Jul 2025 23:33:02 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95881403c14969cffe472e4573c292f70ec294cd99406def97d5ff3e2208d8a9`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ba8c53288864cbc60a4a982c82dfc9c320157f56ad7cfcc7a049f0b3577864`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:407bfd26d03ddf54aca9656fac097643785152f2ae1042f160eb66253cb90812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9af45e0663098581e700831710f87e9f24f12a0e42213fb865f32ccecf9202a`

```dockerfile
```

-	Layers:
	-	`sha256:91475ec4af388e69220316d19fe0978aab6f0bfdc0d7adcb1be23f468d87f3f9`  
		Last Modified: Sat, 12 Jul 2025 02:07:41 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8a1c07af046d9b002e7d4eb623c39884512d3536d439abeaa725d0fae4c976b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138575154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698ae6cc2234b6bca2194e7639d01cc51f0d840a322887c06eefb9bf1a87446f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fed6fc4a68d5c71a2eb25262cb6ae103f5b4d17bc7af3066655e4038fa065`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 10.0 MB (10034378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37be3793d884a5c56f2ffc4899b108efdfb379d3412b94596889feeca6a4e19`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eefc3e025edefe52fa56cca59c462eff4688e14b7da94f1bb872ff684be9d96`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72138503f7c3515cce912ebff7c04ff9331b6f941114745557f8f3779bdfdbf`  
		Last Modified: Fri, 11 Jul 2025 23:34:45 GMT  
		Size: 57.5 MB (57464546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffed797ad64daff69c24cdc4b9b919cf829962a4c55474513ca6acbef6344e4`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ad5491b62b5a110e8c21811bbf035208ed68f752b71a1b2a848096c5c49201`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28` - unknown; unknown

```console
$ docker pull docker@sha256:a932864680893d42a6771d0ddeeb27e5bd50b731d9fd0e87c09aaaa29717e5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb27c8b2e82846d2b25aab8e29c2feb330ab2fa0d37efa5379c9f421b0f8485`

```dockerfile
```

-	Layers:
	-	`sha256:9fda5f788d0162b9af973bfde59e6c6abfc845820075a147bcab120322089c2c`  
		Last Modified: Sat, 12 Jul 2025 02:07:44 GMT  
		Size: 34.8 KB (34830 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-cli`

```console
$ docker pull docker@sha256:13f8f54e0410b262768c3f9ec6fb987abd385ef2b16d43cfe44b93f2042ba399
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
$ docker pull docker@sha256:ad955c02a8c8608a9a581c545b93b9d45023986553a9188da71ec2192ff9e2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75423937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29b7161492868d2bdab426c00ecf1a97e6d4249e4ce3e9e9ed98bae0dbbe7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1c4894165cfb9aaa1d2b37c50b551c31e17f71611b0ff43994110a9b460af8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236b9edd62480bf1994af5564b8ef182210d1336ff8892988f674ac27eaa5409`

```dockerfile
```

-	Layers:
	-	`sha256:fa1e8a11e4b8700fd3f91f6b363c3d23547ee308f1f0d69290d84031153575c7`  
		Last Modified: Fri, 11 Jul 2025 23:07:32 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:8b4a77177bb41dfbc484ffe2ca57773c9b8db3500a60596c0c259046d921d9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70384659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba833a381a4a0c18807371500fc2aba2f2538af694704e84f6be80a939ee3647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8d3de6ba8edd719f37c314ec9cb77ea92b3d9d7f3f43c4c8ccea5eab52d8bb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2de72b3b92515f3652b0c952bfd400180132ca92a98560966b78338b05a665b`

```dockerfile
```

-	Layers:
	-	`sha256:5d3aff152b821f9c64b37aa8c52a44adc9ee1104f48e48fc42bf63f8a0b7bf05`  
		Last Modified: Fri, 11 Jul 2025 23:07:22 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:2dfe76be879889721d4578609d8e57a681a1fb944f4ee8652de2f7b18fc04ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69389623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fa5a9d9861537caf7e62f6e3199c9cb97e9eb11907b3db24c2abb801d6e6f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f79f1a874c76d5e4b265a72dccb83bc513d7ff7f30bb0ba963bbfa5b82b9742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f65cbf035a05096f98a920c5dc0ba5979f0b9ce6ab023e58ca0ed9fe5f104c3`

```dockerfile
```

-	Layers:
	-	`sha256:6d694569211f0463fc2fa67fce30fbf7c91f557b6dc9aac14c0c6b9596e073fa`  
		Last Modified: Sat, 12 Jul 2025 02:07:45 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:29a155d2b64ee1f8ea9f51d52d109a94ad34178e8b4b9d62e645c96927a3119c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70970597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713cb7ebce506a192fd70fdda571e5ddf72f0815bed6363d998882208650b019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ca067feba0aa873cd74f3722c31ec7bf2065db5e8bad3bcbb2c0bbe4865da7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7747c774e4dc3eb0e4be57c7b98e8671a22cc51fcb182bc1a244be14f544cf30`

```dockerfile
```

-	Layers:
	-	`sha256:bbfb6f21e3789c8273c69cde35a76a93414d225c4f06c24482a778ab4dd42681`  
		Last Modified: Sat, 12 Jul 2025 02:07:48 GMT  
		Size: 38.3 KB (38321 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind`

```console
$ docker pull docker@sha256:684bc226a69eb91582738f196e59e234355420ee592abea7685e4127afbce645
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
$ docker pull docker@sha256:2039571fb2946ea368779140c94dfbda3c7858b493c42dbbe8345d19500e6d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147544548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d269157efa5eebf6dbc86f558a80e2cb8016c6a9a39793526a4396a512f6d2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb387276c10661bba84fce126eed7b4ef9ef3622bbaf76fed5855a2f4712ce89`  
		Last Modified: Fri, 11 Jul 2025 23:08:13 GMT  
		Size: 9.5 MB (9506675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f8a93798fbae872851b58e72ef4b3bdace12203577685b3e52d5e94c24b42`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 90.5 KB (90506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f487a7a0e1532da82eb272ebcd78402bf76ee707c063da6f3f485326c3d403a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1f25172b8052f548668179a49f8d03408390b474e886f7afd40ce39007449`  
		Last Modified: Fri, 11 Jul 2025 23:08:15 GMT  
		Size: 62.5 MB (62517439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f23e14ee4f80c7f15ead5263837d831d43d4d8023341200c812784762d266a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c327638cbba730a460f516b7fca541b5b3543003eed01c494273d4afe84af`  
		Last Modified: Fri, 11 Jul 2025 23:08:09 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1612ef52d558ce839416d05d730405b29142c973896aabc995f904e7ab473970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91d6a682e933349713bef3b27e24c6173ee392272ac25eb3fa024eaffdb3758`

```dockerfile
```

-	Layers:
	-	`sha256:f4f1bd41a1006eba393a7d70732b5d538b904f8edc1eea71cba3c25ee7102546`  
		Last Modified: Sat, 12 Jul 2025 02:07:33 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:3960ae5dceff97e2f1523fbadd2521995a9daf4d387a5480808a22b2c0899b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138138376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ee56a5d4421a9708d18d5433cfbbbe8d0327c86185361a95dc2e7fd2cf8b64`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7539813331bce9849eabb04feabc475057f406b6008e4ee8fe9cc34b09584181`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 9.5 MB (9461142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0883a2e698c28639f5e51239c30f623739e588758e46b282b4d86ca0696974e5`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd721e456a1abbd99a37541edfb801f174d50c67eb927d7d11c5f99171d47d62`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed9a7b148f299ea5bae85c09fc8c8f23d43bf689367f224453031283e72d0c8`  
		Last Modified: Fri, 11 Jul 2025 23:07:39 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b17794da37735f4238675dc8f08e3b997577476e766a2823c345f45dc6032`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272cd592cd54400557bde2759b815592c11caed1b9ab0f1e3fbf4c40d586a8ee`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:fba4e76c7a853c8ec14ed8001c3f8afbea81b47032255689ca70d6f5f3f2c9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa67ed505137fefa99d92897b086b45c84d8e36db4289bbea88b2c0eb844d0a`

```dockerfile
```

-	Layers:
	-	`sha256:7c9d7dc66552b1f6a8db09f35ffcedf83ab42a2e73c3233cfb147e16b92cf06f`  
		Last Modified: Sat, 12 Jul 2025 02:07:37 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:5eb2289358e41707da0542f5777d08c6a252b8f0ded58903fcd72fe467703bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136289051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d930d302a73d55f2c350884eed98d79c117d882a7d599b564826bdb27828068`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c7a3c227e0d7b893835a896bf1421afe6c7a1bfe44b1141899c2a4ef2e889`  
		Last Modified: Fri, 11 Jul 2025 23:32:59 GMT  
		Size: 8.6 MB (8610408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33069b480d39ad0fd6e38090b30b043a73413afa7ca6ed1e0f3d1b54961669b0`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 86.5 KB (86504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129027ab9eb0b76ac3acd19b4198612a65e9c9f6f8b472a5d1bacb8583090852`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c185229dea08b37f2a81137ce8ea0b1455bbbdd9055c1ce9f9e1240066b71216`  
		Last Modified: Fri, 11 Jul 2025 23:33:02 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95881403c14969cffe472e4573c292f70ec294cd99406def97d5ff3e2208d8a9`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ba8c53288864cbc60a4a982c82dfc9c320157f56ad7cfcc7a049f0b3577864`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:407bfd26d03ddf54aca9656fac097643785152f2ae1042f160eb66253cb90812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9af45e0663098581e700831710f87e9f24f12a0e42213fb865f32ccecf9202a`

```dockerfile
```

-	Layers:
	-	`sha256:91475ec4af388e69220316d19fe0978aab6f0bfdc0d7adcb1be23f468d87f3f9`  
		Last Modified: Sat, 12 Jul 2025 02:07:41 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8a1c07af046d9b002e7d4eb623c39884512d3536d439abeaa725d0fae4c976b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138575154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698ae6cc2234b6bca2194e7639d01cc51f0d840a322887c06eefb9bf1a87446f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fed6fc4a68d5c71a2eb25262cb6ae103f5b4d17bc7af3066655e4038fa065`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 10.0 MB (10034378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37be3793d884a5c56f2ffc4899b108efdfb379d3412b94596889feeca6a4e19`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eefc3e025edefe52fa56cca59c462eff4688e14b7da94f1bb872ff684be9d96`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72138503f7c3515cce912ebff7c04ff9331b6f941114745557f8f3779bdfdbf`  
		Last Modified: Fri, 11 Jul 2025 23:34:45 GMT  
		Size: 57.5 MB (57464546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffed797ad64daff69c24cdc4b9b919cf829962a4c55474513ca6acbef6344e4`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ad5491b62b5a110e8c21811bbf035208ed68f752b71a1b2a848096c5c49201`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a932864680893d42a6771d0ddeeb27e5bd50b731d9fd0e87c09aaaa29717e5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb27c8b2e82846d2b25aab8e29c2feb330ab2fa0d37efa5379c9f421b0f8485`

```dockerfile
```

-	Layers:
	-	`sha256:9fda5f788d0162b9af973bfde59e6c6abfc845820075a147bcab120322089c2c`  
		Last Modified: Sat, 12 Jul 2025 02:07:44 GMT  
		Size: 34.8 KB (34830 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:35198af02775d4862e97f6b8586ef506e389f61d114c1ac3118423cbed02daf4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6525ecd8e4c79837c9ee9aef0cc9fab291ba4e9992a21f1471e2f4487e495c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168528184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1c15ddae240606ea58ccceb878320b41b6c810d7bb6396f893d8ee214d2a4a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb387276c10661bba84fce126eed7b4ef9ef3622bbaf76fed5855a2f4712ce89`  
		Last Modified: Fri, 11 Jul 2025 23:08:13 GMT  
		Size: 9.5 MB (9506675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f8a93798fbae872851b58e72ef4b3bdace12203577685b3e52d5e94c24b42`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 90.5 KB (90506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f487a7a0e1532da82eb272ebcd78402bf76ee707c063da6f3f485326c3d403a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1f25172b8052f548668179a49f8d03408390b474e886f7afd40ce39007449`  
		Last Modified: Fri, 11 Jul 2025 23:08:15 GMT  
		Size: 62.5 MB (62517439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f23e14ee4f80c7f15ead5263837d831d43d4d8023341200c812784762d266a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c327638cbba730a460f516b7fca541b5b3543003eed01c494273d4afe84af`  
		Last Modified: Fri, 11 Jul 2025 23:08:09 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03112a04e52db6d13027e01dd6050144a8aee81e36d90b7ea023e739fe61172a`  
		Last Modified: Fri, 11 Jul 2025 23:33:14 GMT  
		Size: 3.4 MB (3398166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e447c93da945b8522da3e732002649cf9b6b639efdbc4a2d403f29148812a07f`  
		Last Modified: Fri, 11 Jul 2025 23:33:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16efbe21a8d03d3afe5f2cb9d60c580aa7be65b64f2d75f24f75f682648e3fcb`  
		Last Modified: Fri, 11 Jul 2025 23:33:14 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c859e61e7fd0651e4a8f254bb741a8e274162bbe21bbb29f89a027a6f11c8d9`  
		Last Modified: Fri, 11 Jul 2025 23:33:15 GMT  
		Size: 17.6 MB (17584130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f840bbaab3748e2feb91b659386024e4dd8371b44a84198551bde19f08eb69dd`  
		Last Modified: Fri, 11 Jul 2025 23:33:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3e9d03bae67266207ff9fc79e8c017ab171e1f7ec59b71e2e53f0ebad48e73fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea477fdfcdddb1bf12cc64d22107f292a356f128c8da309975205671d580f64`

```dockerfile
```

-	Layers:
	-	`sha256:0820f43a7d2b86f7ede683b82c6eb56ed10bae0e0892c219427e8b8b339c72b6`  
		Last Modified: Sat, 12 Jul 2025 02:07:55 GMT  
		Size: 30.6 KB (30635 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e113ae097663cf6428a12c793cddd2cf8ede3a895ef12468dece2036857c6594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159982139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f750db8fcf38249451e3f218882f1a8da997681207ad55fec24022d7187df2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fed6fc4a68d5c71a2eb25262cb6ae103f5b4d17bc7af3066655e4038fa065`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 10.0 MB (10034378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37be3793d884a5c56f2ffc4899b108efdfb379d3412b94596889feeca6a4e19`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eefc3e025edefe52fa56cca59c462eff4688e14b7da94f1bb872ff684be9d96`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72138503f7c3515cce912ebff7c04ff9331b6f941114745557f8f3779bdfdbf`  
		Last Modified: Fri, 11 Jul 2025 23:34:45 GMT  
		Size: 57.5 MB (57464546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffed797ad64daff69c24cdc4b9b919cf829962a4c55474513ca6acbef6344e4`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ad5491b62b5a110e8c21811bbf035208ed68f752b71a1b2a848096c5c49201`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da43fadc269459b75acd7de271e5a158d3571ab75c1ecc360602692e1ab07d0`  
		Last Modified: Sat, 12 Jul 2025 00:18:39 GMT  
		Size: 3.4 MB (3389661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4eb185ab4c980eb8b107c7bc3be6bbb124d73dafca5a67338af7189b1ab64`  
		Last Modified: Sat, 12 Jul 2025 00:18:38 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570abe49cfbd7a10502c8ab2552ff99ad64b6f334de551869c0b0127c8dccf3d`  
		Last Modified: Sat, 12 Jul 2025 00:18:38 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8f0e58928ea62c6fd1e569520de3775bc26384ab53f8281f34abff70fce620`  
		Last Modified: Sat, 12 Jul 2025 00:18:47 GMT  
		Size: 18.0 MB (18015982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e05691e4b87ef7aada1591b229cc9079e4ed99f8c9a452185b72aecb44b813`  
		Last Modified: Sat, 12 Jul 2025 00:18:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0fda9319fb82b510fc50a5faa2d8a2ba11fba00261d4ad6df71b162730508c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93d59bce5cc499c904a106fd8621a20e5ad797dd0b8c49e2276126a91a57213`

```dockerfile
```

-	Layers:
	-	`sha256:f883c406c3f247dcf965d3dcfbff08d54a48f5f246be6867c6ce1b830ea62fce`  
		Last Modified: Sat, 12 Jul 2025 02:07:58 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28-windowsservercore`

```console
$ docker pull docker@sha256:8af71f9bf2d9299f329b29664b8b03bc103d1ccfa95b6aa17e9ac2cc813b3f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `docker:28-windowsservercore` - windows version 10.0.26100.4652; amd64

```console
$ docker pull docker@sha256:1b56934c5d06028439690c1309eb9b88eb3622cf09b3c658d8eb414b4cc4e480
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3557253065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cff6279f7a6bb0448b10fd3cd887bc504f14bae6713de69b38dbd1aa2e7706`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Fri, 11 Jul 2025 23:11:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:52 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:12:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:05 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:12:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:12:08 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:12:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:12:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:12:20 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775c3cb412ef97cfd2e8fb3eb8b4ed4eb842eca9fc398d2532621e5c7ca35ece`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695218c842722d24657641ab6ebc81d25a63cdafa30de7cb49b776b367142f26`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 358.3 KB (358314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c1dbee4aeeef6e5fb1300fdb3bc18294e925cd09bbaaf1b15aa33e10ed8bd5`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8195ebb4a582faee7125a1f54b178e33d711e11f433d167ebb398bd3d7dadbb`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef092bafbfde0756ffc78f37df6a8535e86fc729053bca4043b4be37d30cdbd`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 20.8 MB (20833534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4946f34fbc3929b0bd1690efd11fde241fe49b422195a49a09396b88ea155603`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9f50c1a5652651e14e3c22d25b1481c335718752c4e07ac0542e78c7c3b328`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345a4650626a657dc7e6694018d735ab6606d22b47b705f8c09a7757e9015d43`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ed0744326d6c591698f832e08c6fa033c9e629de50f4c9483495c001fb2642`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 22.7 MB (22657124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b3a11825e8b21bb69b5c0384a182d6cdf8f1353b2bdb1442d4d16bce524e99`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe5aa15d97dd2804f78d9d8e369adabe4ea561c75eab7ad692dcd97967c33`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdfd59906a07f2c196fff6b67562e50e25b4afa4953e028029d2fc1e943dc43`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3376702d007e8b3dfce66cd8aad6d777423ed2c82d716767189aa3142e0522`  
		Last Modified: Fri, 11 Jul 2025 23:15:59 GMT  
		Size: 22.2 MB (22218765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28-windowsservercore` - windows version 10.0.20348.3932; amd64

```console
$ docker pull docker@sha256:274102f6fb709884e50fbd6385533222a64cfee86d1cd8cb2dd9252c89666d55
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346616670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ee854316da74807f41148421e20eaad374dffdc0c364ae90833d5ad07e2c8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Fri, 11 Jul 2025 23:11:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:23 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:11:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:37 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:11:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:11:39 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:11:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:11:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:11:51 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a169b055e688e9a95c597265e07131d5232287fba68b1423932d0e5a0d17994`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c1203248b3626938b2771becf28b8c6911cd9df9219ae520645531c0dbb70d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 345.2 KB (345190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c3435e2f8aaac8a675144ceb7549700537e00f4786f114c42491ee8383725d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1581baec19a91b283eefc934c91344d47afca0ea900b35da3f836b0b64a42865`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cff61016e6a9f50575ce34439e6a2c7178f3565df3b13a8fc1e83f5f851db74`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 20.8 MB (20818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ee52ae9d5dfdddd94c77625c32cf6d55ca38841bb7de45eca5317774463cb5`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24e1d00d64556954d1d53d6b8e8a34cb7d25586fe655167a48cf826509f45b9`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84d9071c54da8e2804485c068baa75a4fbad0a877fc958c33956da99ed71eab`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b3be0ea66255c0c1e37cf6ee05b2e8f428c56609247f49352a06e5515da63`  
		Last Modified: Fri, 11 Jul 2025 23:13:28 GMT  
		Size: 22.6 MB (22637804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c75de97c3645b05b277e0b519d48ebd131d07d48c07cd2cd90e6f980e2895f1`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839a8bfa777f817ee9a9e87de8fdffdb95c126c2755e19dbec8942b0bc99922`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56150ca8198cc556b583f4c58d8c4f50c7d478fdd3ad61a90be92fef4b92e31`  
		Last Modified: Fri, 11 Jul 2025 23:13:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9fc7429c59acba4f39458ab7209516b370cfb3caac581a87f6fd05712a7fbca`  
		Last Modified: Fri, 11 Jul 2025 23:13:34 GMT  
		Size: 22.2 MB (22200448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ee29d642afb6aaff1bcb9e6fb8f7035a5ac073aa673be20e95c8db1d7c5369a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `docker:28-windowsservercore-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull docker@sha256:274102f6fb709884e50fbd6385533222a64cfee86d1cd8cb2dd9252c89666d55
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346616670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ee854316da74807f41148421e20eaad374dffdc0c364ae90833d5ad07e2c8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Fri, 11 Jul 2025 23:11:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:23 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:11:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:37 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:11:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:11:39 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:11:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:11:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:11:51 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a169b055e688e9a95c597265e07131d5232287fba68b1423932d0e5a0d17994`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c1203248b3626938b2771becf28b8c6911cd9df9219ae520645531c0dbb70d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 345.2 KB (345190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c3435e2f8aaac8a675144ceb7549700537e00f4786f114c42491ee8383725d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1581baec19a91b283eefc934c91344d47afca0ea900b35da3f836b0b64a42865`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cff61016e6a9f50575ce34439e6a2c7178f3565df3b13a8fc1e83f5f851db74`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 20.8 MB (20818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ee52ae9d5dfdddd94c77625c32cf6d55ca38841bb7de45eca5317774463cb5`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24e1d00d64556954d1d53d6b8e8a34cb7d25586fe655167a48cf826509f45b9`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84d9071c54da8e2804485c068baa75a4fbad0a877fc958c33956da99ed71eab`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b3be0ea66255c0c1e37cf6ee05b2e8f428c56609247f49352a06e5515da63`  
		Last Modified: Fri, 11 Jul 2025 23:13:28 GMT  
		Size: 22.6 MB (22637804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c75de97c3645b05b277e0b519d48ebd131d07d48c07cd2cd90e6f980e2895f1`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839a8bfa777f817ee9a9e87de8fdffdb95c126c2755e19dbec8942b0bc99922`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56150ca8198cc556b583f4c58d8c4f50c7d478fdd3ad61a90be92fef4b92e31`  
		Last Modified: Fri, 11 Jul 2025 23:13:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9fc7429c59acba4f39458ab7209516b370cfb3caac581a87f6fd05712a7fbca`  
		Last Modified: Fri, 11 Jul 2025 23:13:34 GMT  
		Size: 22.2 MB (22200448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:58f55a64f3de77413f3e65abc364e070c041f64571fd689dba68f3708478979a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull docker@sha256:1b56934c5d06028439690c1309eb9b88eb3622cf09b3c658d8eb414b4cc4e480
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3557253065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cff6279f7a6bb0448b10fd3cd887bc504f14bae6713de69b38dbd1aa2e7706`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Fri, 11 Jul 2025 23:11:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:52 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:12:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:05 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:12:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:12:08 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:12:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:12:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:12:20 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775c3cb412ef97cfd2e8fb3eb8b4ed4eb842eca9fc398d2532621e5c7ca35ece`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695218c842722d24657641ab6ebc81d25a63cdafa30de7cb49b776b367142f26`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 358.3 KB (358314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c1dbee4aeeef6e5fb1300fdb3bc18294e925cd09bbaaf1b15aa33e10ed8bd5`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8195ebb4a582faee7125a1f54b178e33d711e11f433d167ebb398bd3d7dadbb`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef092bafbfde0756ffc78f37df6a8535e86fc729053bca4043b4be37d30cdbd`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 20.8 MB (20833534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4946f34fbc3929b0bd1690efd11fde241fe49b422195a49a09396b88ea155603`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9f50c1a5652651e14e3c22d25b1481c335718752c4e07ac0542e78c7c3b328`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345a4650626a657dc7e6694018d735ab6606d22b47b705f8c09a7757e9015d43`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ed0744326d6c591698f832e08c6fa033c9e629de50f4c9483495c001fb2642`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 22.7 MB (22657124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b3a11825e8b21bb69b5c0384a182d6cdf8f1353b2bdb1442d4d16bce524e99`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe5aa15d97dd2804f78d9d8e369adabe4ea561c75eab7ad692dcd97967c33`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdfd59906a07f2c196fff6b67562e50e25b4afa4953e028029d2fc1e943dc43`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3376702d007e8b3dfce66cd8aad6d777423ed2c82d716767189aa3142e0522`  
		Last Modified: Fri, 11 Jul 2025 23:15:59 GMT  
		Size: 22.2 MB (22218765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3`

```console
$ docker pull docker@sha256:684bc226a69eb91582738f196e59e234355420ee592abea7685e4127afbce645
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
$ docker pull docker@sha256:2039571fb2946ea368779140c94dfbda3c7858b493c42dbbe8345d19500e6d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147544548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d269157efa5eebf6dbc86f558a80e2cb8016c6a9a39793526a4396a512f6d2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb387276c10661bba84fce126eed7b4ef9ef3622bbaf76fed5855a2f4712ce89`  
		Last Modified: Fri, 11 Jul 2025 23:08:13 GMT  
		Size: 9.5 MB (9506675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f8a93798fbae872851b58e72ef4b3bdace12203577685b3e52d5e94c24b42`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 90.5 KB (90506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f487a7a0e1532da82eb272ebcd78402bf76ee707c063da6f3f485326c3d403a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1f25172b8052f548668179a49f8d03408390b474e886f7afd40ce39007449`  
		Last Modified: Fri, 11 Jul 2025 23:08:15 GMT  
		Size: 62.5 MB (62517439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f23e14ee4f80c7f15ead5263837d831d43d4d8023341200c812784762d266a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c327638cbba730a460f516b7fca541b5b3543003eed01c494273d4afe84af`  
		Last Modified: Fri, 11 Jul 2025 23:08:09 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:1612ef52d558ce839416d05d730405b29142c973896aabc995f904e7ab473970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91d6a682e933349713bef3b27e24c6173ee392272ac25eb3fa024eaffdb3758`

```dockerfile
```

-	Layers:
	-	`sha256:f4f1bd41a1006eba393a7d70732b5d538b904f8edc1eea71cba3c25ee7102546`  
		Last Modified: Sat, 12 Jul 2025 02:07:33 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3` - linux; arm variant v6

```console
$ docker pull docker@sha256:3960ae5dceff97e2f1523fbadd2521995a9daf4d387a5480808a22b2c0899b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138138376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ee56a5d4421a9708d18d5433cfbbbe8d0327c86185361a95dc2e7fd2cf8b64`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7539813331bce9849eabb04feabc475057f406b6008e4ee8fe9cc34b09584181`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 9.5 MB (9461142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0883a2e698c28639f5e51239c30f623739e588758e46b282b4d86ca0696974e5`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd721e456a1abbd99a37541edfb801f174d50c67eb927d7d11c5f99171d47d62`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed9a7b148f299ea5bae85c09fc8c8f23d43bf689367f224453031283e72d0c8`  
		Last Modified: Fri, 11 Jul 2025 23:07:39 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b17794da37735f4238675dc8f08e3b997577476e766a2823c345f45dc6032`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272cd592cd54400557bde2759b815592c11caed1b9ab0f1e3fbf4c40d586a8ee`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:fba4e76c7a853c8ec14ed8001c3f8afbea81b47032255689ca70d6f5f3f2c9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa67ed505137fefa99d92897b086b45c84d8e36db4289bbea88b2c0eb844d0a`

```dockerfile
```

-	Layers:
	-	`sha256:7c9d7dc66552b1f6a8db09f35ffcedf83ab42a2e73c3233cfb147e16b92cf06f`  
		Last Modified: Sat, 12 Jul 2025 02:07:37 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3` - linux; arm variant v7

```console
$ docker pull docker@sha256:5eb2289358e41707da0542f5777d08c6a252b8f0ded58903fcd72fe467703bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136289051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d930d302a73d55f2c350884eed98d79c117d882a7d599b564826bdb27828068`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c7a3c227e0d7b893835a896bf1421afe6c7a1bfe44b1141899c2a4ef2e889`  
		Last Modified: Fri, 11 Jul 2025 23:32:59 GMT  
		Size: 8.6 MB (8610408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33069b480d39ad0fd6e38090b30b043a73413afa7ca6ed1e0f3d1b54961669b0`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 86.5 KB (86504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129027ab9eb0b76ac3acd19b4198612a65e9c9f6f8b472a5d1bacb8583090852`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c185229dea08b37f2a81137ce8ea0b1455bbbdd9055c1ce9f9e1240066b71216`  
		Last Modified: Fri, 11 Jul 2025 23:33:02 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95881403c14969cffe472e4573c292f70ec294cd99406def97d5ff3e2208d8a9`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ba8c53288864cbc60a4a982c82dfc9c320157f56ad7cfcc7a049f0b3577864`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:407bfd26d03ddf54aca9656fac097643785152f2ae1042f160eb66253cb90812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9af45e0663098581e700831710f87e9f24f12a0e42213fb865f32ccecf9202a`

```dockerfile
```

-	Layers:
	-	`sha256:91475ec4af388e69220316d19fe0978aab6f0bfdc0d7adcb1be23f468d87f3f9`  
		Last Modified: Sat, 12 Jul 2025 02:07:41 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8a1c07af046d9b002e7d4eb623c39884512d3536d439abeaa725d0fae4c976b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138575154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698ae6cc2234b6bca2194e7639d01cc51f0d840a322887c06eefb9bf1a87446f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fed6fc4a68d5c71a2eb25262cb6ae103f5b4d17bc7af3066655e4038fa065`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 10.0 MB (10034378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37be3793d884a5c56f2ffc4899b108efdfb379d3412b94596889feeca6a4e19`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eefc3e025edefe52fa56cca59c462eff4688e14b7da94f1bb872ff684be9d96`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72138503f7c3515cce912ebff7c04ff9331b6f941114745557f8f3779bdfdbf`  
		Last Modified: Fri, 11 Jul 2025 23:34:45 GMT  
		Size: 57.5 MB (57464546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffed797ad64daff69c24cdc4b9b919cf829962a4c55474513ca6acbef6344e4`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ad5491b62b5a110e8c21811bbf035208ed68f752b71a1b2a848096c5c49201`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3` - unknown; unknown

```console
$ docker pull docker@sha256:a932864680893d42a6771d0ddeeb27e5bd50b731d9fd0e87c09aaaa29717e5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb27c8b2e82846d2b25aab8e29c2feb330ab2fa0d37efa5379c9f421b0f8485`

```dockerfile
```

-	Layers:
	-	`sha256:9fda5f788d0162b9af973bfde59e6c6abfc845820075a147bcab120322089c2c`  
		Last Modified: Sat, 12 Jul 2025 02:07:44 GMT  
		Size: 34.8 KB (34830 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-cli`

```console
$ docker pull docker@sha256:13f8f54e0410b262768c3f9ec6fb987abd385ef2b16d43cfe44b93f2042ba399
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
$ docker pull docker@sha256:ad955c02a8c8608a9a581c545b93b9d45023986553a9188da71ec2192ff9e2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75423937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29b7161492868d2bdab426c00ecf1a97e6d4249e4ce3e9e9ed98bae0dbbe7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1c4894165cfb9aaa1d2b37c50b551c31e17f71611b0ff43994110a9b460af8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236b9edd62480bf1994af5564b8ef182210d1336ff8892988f674ac27eaa5409`

```dockerfile
```

-	Layers:
	-	`sha256:fa1e8a11e4b8700fd3f91f6b363c3d23547ee308f1f0d69290d84031153575c7`  
		Last Modified: Fri, 11 Jul 2025 23:07:32 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:8b4a77177bb41dfbc484ffe2ca57773c9b8db3500a60596c0c259046d921d9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70384659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba833a381a4a0c18807371500fc2aba2f2538af694704e84f6be80a939ee3647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8d3de6ba8edd719f37c314ec9cb77ea92b3d9d7f3f43c4c8ccea5eab52d8bb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2de72b3b92515f3652b0c952bfd400180132ca92a98560966b78338b05a665b`

```dockerfile
```

-	Layers:
	-	`sha256:5d3aff152b821f9c64b37aa8c52a44adc9ee1104f48e48fc42bf63f8a0b7bf05`  
		Last Modified: Fri, 11 Jul 2025 23:07:22 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:2dfe76be879889721d4578609d8e57a681a1fb944f4ee8652de2f7b18fc04ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69389623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fa5a9d9861537caf7e62f6e3199c9cb97e9eb11907b3db24c2abb801d6e6f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f79f1a874c76d5e4b265a72dccb83bc513d7ff7f30bb0ba963bbfa5b82b9742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f65cbf035a05096f98a920c5dc0ba5979f0b9ce6ab023e58ca0ed9fe5f104c3`

```dockerfile
```

-	Layers:
	-	`sha256:6d694569211f0463fc2fa67fce30fbf7c91f557b6dc9aac14c0c6b9596e073fa`  
		Last Modified: Sat, 12 Jul 2025 02:07:45 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:29a155d2b64ee1f8ea9f51d52d109a94ad34178e8b4b9d62e645c96927a3119c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70970597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713cb7ebce506a192fd70fdda571e5ddf72f0815bed6363d998882208650b019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ca067feba0aa873cd74f3722c31ec7bf2065db5e8bad3bcbb2c0bbe4865da7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7747c774e4dc3eb0e4be57c7b98e8671a22cc51fcb182bc1a244be14f544cf30`

```dockerfile
```

-	Layers:
	-	`sha256:bbfb6f21e3789c8273c69cde35a76a93414d225c4f06c24482a778ab4dd42681`  
		Last Modified: Sat, 12 Jul 2025 02:07:48 GMT  
		Size: 38.3 KB (38321 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-dind`

```console
$ docker pull docker@sha256:684bc226a69eb91582738f196e59e234355420ee592abea7685e4127afbce645
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
$ docker pull docker@sha256:2039571fb2946ea368779140c94dfbda3c7858b493c42dbbe8345d19500e6d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147544548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d269157efa5eebf6dbc86f558a80e2cb8016c6a9a39793526a4396a512f6d2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb387276c10661bba84fce126eed7b4ef9ef3622bbaf76fed5855a2f4712ce89`  
		Last Modified: Fri, 11 Jul 2025 23:08:13 GMT  
		Size: 9.5 MB (9506675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f8a93798fbae872851b58e72ef4b3bdace12203577685b3e52d5e94c24b42`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 90.5 KB (90506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f487a7a0e1532da82eb272ebcd78402bf76ee707c063da6f3f485326c3d403a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1f25172b8052f548668179a49f8d03408390b474e886f7afd40ce39007449`  
		Last Modified: Fri, 11 Jul 2025 23:08:15 GMT  
		Size: 62.5 MB (62517439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f23e14ee4f80c7f15ead5263837d831d43d4d8023341200c812784762d266a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c327638cbba730a460f516b7fca541b5b3543003eed01c494273d4afe84af`  
		Last Modified: Fri, 11 Jul 2025 23:08:09 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1612ef52d558ce839416d05d730405b29142c973896aabc995f904e7ab473970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91d6a682e933349713bef3b27e24c6173ee392272ac25eb3fa024eaffdb3758`

```dockerfile
```

-	Layers:
	-	`sha256:f4f1bd41a1006eba393a7d70732b5d538b904f8edc1eea71cba3c25ee7102546`  
		Last Modified: Sat, 12 Jul 2025 02:07:33 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:3960ae5dceff97e2f1523fbadd2521995a9daf4d387a5480808a22b2c0899b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138138376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ee56a5d4421a9708d18d5433cfbbbe8d0327c86185361a95dc2e7fd2cf8b64`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7539813331bce9849eabb04feabc475057f406b6008e4ee8fe9cc34b09584181`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 9.5 MB (9461142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0883a2e698c28639f5e51239c30f623739e588758e46b282b4d86ca0696974e5`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd721e456a1abbd99a37541edfb801f174d50c67eb927d7d11c5f99171d47d62`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed9a7b148f299ea5bae85c09fc8c8f23d43bf689367f224453031283e72d0c8`  
		Last Modified: Fri, 11 Jul 2025 23:07:39 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b17794da37735f4238675dc8f08e3b997577476e766a2823c345f45dc6032`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272cd592cd54400557bde2759b815592c11caed1b9ab0f1e3fbf4c40d586a8ee`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:fba4e76c7a853c8ec14ed8001c3f8afbea81b47032255689ca70d6f5f3f2c9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa67ed505137fefa99d92897b086b45c84d8e36db4289bbea88b2c0eb844d0a`

```dockerfile
```

-	Layers:
	-	`sha256:7c9d7dc66552b1f6a8db09f35ffcedf83ab42a2e73c3233cfb147e16b92cf06f`  
		Last Modified: Sat, 12 Jul 2025 02:07:37 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:5eb2289358e41707da0542f5777d08c6a252b8f0ded58903fcd72fe467703bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136289051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d930d302a73d55f2c350884eed98d79c117d882a7d599b564826bdb27828068`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c7a3c227e0d7b893835a896bf1421afe6c7a1bfe44b1141899c2a4ef2e889`  
		Last Modified: Fri, 11 Jul 2025 23:32:59 GMT  
		Size: 8.6 MB (8610408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33069b480d39ad0fd6e38090b30b043a73413afa7ca6ed1e0f3d1b54961669b0`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 86.5 KB (86504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129027ab9eb0b76ac3acd19b4198612a65e9c9f6f8b472a5d1bacb8583090852`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c185229dea08b37f2a81137ce8ea0b1455bbbdd9055c1ce9f9e1240066b71216`  
		Last Modified: Fri, 11 Jul 2025 23:33:02 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95881403c14969cffe472e4573c292f70ec294cd99406def97d5ff3e2208d8a9`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ba8c53288864cbc60a4a982c82dfc9c320157f56ad7cfcc7a049f0b3577864`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:407bfd26d03ddf54aca9656fac097643785152f2ae1042f160eb66253cb90812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9af45e0663098581e700831710f87e9f24f12a0e42213fb865f32ccecf9202a`

```dockerfile
```

-	Layers:
	-	`sha256:91475ec4af388e69220316d19fe0978aab6f0bfdc0d7adcb1be23f468d87f3f9`  
		Last Modified: Sat, 12 Jul 2025 02:07:41 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8a1c07af046d9b002e7d4eb623c39884512d3536d439abeaa725d0fae4c976b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138575154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698ae6cc2234b6bca2194e7639d01cc51f0d840a322887c06eefb9bf1a87446f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fed6fc4a68d5c71a2eb25262cb6ae103f5b4d17bc7af3066655e4038fa065`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 10.0 MB (10034378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37be3793d884a5c56f2ffc4899b108efdfb379d3412b94596889feeca6a4e19`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eefc3e025edefe52fa56cca59c462eff4688e14b7da94f1bb872ff684be9d96`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72138503f7c3515cce912ebff7c04ff9331b6f941114745557f8f3779bdfdbf`  
		Last Modified: Fri, 11 Jul 2025 23:34:45 GMT  
		Size: 57.5 MB (57464546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffed797ad64daff69c24cdc4b9b919cf829962a4c55474513ca6acbef6344e4`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ad5491b62b5a110e8c21811bbf035208ed68f752b71a1b2a848096c5c49201`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a932864680893d42a6771d0ddeeb27e5bd50b731d9fd0e87c09aaaa29717e5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb27c8b2e82846d2b25aab8e29c2feb330ab2fa0d37efa5379c9f421b0f8485`

```dockerfile
```

-	Layers:
	-	`sha256:9fda5f788d0162b9af973bfde59e6c6abfc845820075a147bcab120322089c2c`  
		Last Modified: Sat, 12 Jul 2025 02:07:44 GMT  
		Size: 34.8 KB (34830 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-dind-rootless`

```console
$ docker pull docker@sha256:35198af02775d4862e97f6b8586ef506e389f61d114c1ac3118423cbed02daf4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.3-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6525ecd8e4c79837c9ee9aef0cc9fab291ba4e9992a21f1471e2f4487e495c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168528184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1c15ddae240606ea58ccceb878320b41b6c810d7bb6396f893d8ee214d2a4a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb387276c10661bba84fce126eed7b4ef9ef3622bbaf76fed5855a2f4712ce89`  
		Last Modified: Fri, 11 Jul 2025 23:08:13 GMT  
		Size: 9.5 MB (9506675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f8a93798fbae872851b58e72ef4b3bdace12203577685b3e52d5e94c24b42`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 90.5 KB (90506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f487a7a0e1532da82eb272ebcd78402bf76ee707c063da6f3f485326c3d403a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1f25172b8052f548668179a49f8d03408390b474e886f7afd40ce39007449`  
		Last Modified: Fri, 11 Jul 2025 23:08:15 GMT  
		Size: 62.5 MB (62517439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f23e14ee4f80c7f15ead5263837d831d43d4d8023341200c812784762d266a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c327638cbba730a460f516b7fca541b5b3543003eed01c494273d4afe84af`  
		Last Modified: Fri, 11 Jul 2025 23:08:09 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03112a04e52db6d13027e01dd6050144a8aee81e36d90b7ea023e739fe61172a`  
		Last Modified: Fri, 11 Jul 2025 23:33:14 GMT  
		Size: 3.4 MB (3398166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e447c93da945b8522da3e732002649cf9b6b639efdbc4a2d403f29148812a07f`  
		Last Modified: Fri, 11 Jul 2025 23:33:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16efbe21a8d03d3afe5f2cb9d60c580aa7be65b64f2d75f24f75f682648e3fcb`  
		Last Modified: Fri, 11 Jul 2025 23:33:14 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c859e61e7fd0651e4a8f254bb741a8e274162bbe21bbb29f89a027a6f11c8d9`  
		Last Modified: Fri, 11 Jul 2025 23:33:15 GMT  
		Size: 17.6 MB (17584130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f840bbaab3748e2feb91b659386024e4dd8371b44a84198551bde19f08eb69dd`  
		Last Modified: Fri, 11 Jul 2025 23:33:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3e9d03bae67266207ff9fc79e8c017ab171e1f7ec59b71e2e53f0ebad48e73fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea477fdfcdddb1bf12cc64d22107f292a356f128c8da309975205671d580f64`

```dockerfile
```

-	Layers:
	-	`sha256:0820f43a7d2b86f7ede683b82c6eb56ed10bae0e0892c219427e8b8b339c72b6`  
		Last Modified: Sat, 12 Jul 2025 02:07:55 GMT  
		Size: 30.6 KB (30635 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e113ae097663cf6428a12c793cddd2cf8ede3a895ef12468dece2036857c6594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159982139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f750db8fcf38249451e3f218882f1a8da997681207ad55fec24022d7187df2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fed6fc4a68d5c71a2eb25262cb6ae103f5b4d17bc7af3066655e4038fa065`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 10.0 MB (10034378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37be3793d884a5c56f2ffc4899b108efdfb379d3412b94596889feeca6a4e19`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eefc3e025edefe52fa56cca59c462eff4688e14b7da94f1bb872ff684be9d96`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72138503f7c3515cce912ebff7c04ff9331b6f941114745557f8f3779bdfdbf`  
		Last Modified: Fri, 11 Jul 2025 23:34:45 GMT  
		Size: 57.5 MB (57464546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffed797ad64daff69c24cdc4b9b919cf829962a4c55474513ca6acbef6344e4`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ad5491b62b5a110e8c21811bbf035208ed68f752b71a1b2a848096c5c49201`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da43fadc269459b75acd7de271e5a158d3571ab75c1ecc360602692e1ab07d0`  
		Last Modified: Sat, 12 Jul 2025 00:18:39 GMT  
		Size: 3.4 MB (3389661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4eb185ab4c980eb8b107c7bc3be6bbb124d73dafca5a67338af7189b1ab64`  
		Last Modified: Sat, 12 Jul 2025 00:18:38 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570abe49cfbd7a10502c8ab2552ff99ad64b6f334de551869c0b0127c8dccf3d`  
		Last Modified: Sat, 12 Jul 2025 00:18:38 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8f0e58928ea62c6fd1e569520de3775bc26384ab53f8281f34abff70fce620`  
		Last Modified: Sat, 12 Jul 2025 00:18:47 GMT  
		Size: 18.0 MB (18015982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e05691e4b87ef7aada1591b229cc9079e4ed99f8c9a452185b72aecb44b813`  
		Last Modified: Sat, 12 Jul 2025 00:18:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0fda9319fb82b510fc50a5faa2d8a2ba11fba00261d4ad6df71b162730508c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93d59bce5cc499c904a106fd8621a20e5ad797dd0b8c49e2276126a91a57213`

```dockerfile
```

-	Layers:
	-	`sha256:f883c406c3f247dcf965d3dcfbff08d54a48f5f246be6867c6ce1b830ea62fce`  
		Last Modified: Sat, 12 Jul 2025 02:07:58 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3-windowsservercore`

```console
$ docker pull docker@sha256:8af71f9bf2d9299f329b29664b8b03bc103d1ccfa95b6aa17e9ac2cc813b3f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `docker:28.3-windowsservercore` - windows version 10.0.26100.4652; amd64

```console
$ docker pull docker@sha256:1b56934c5d06028439690c1309eb9b88eb3622cf09b3c658d8eb414b4cc4e480
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3557253065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cff6279f7a6bb0448b10fd3cd887bc504f14bae6713de69b38dbd1aa2e7706`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Fri, 11 Jul 2025 23:11:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:52 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:12:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:05 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:12:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:12:08 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:12:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:12:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:12:20 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775c3cb412ef97cfd2e8fb3eb8b4ed4eb842eca9fc398d2532621e5c7ca35ece`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695218c842722d24657641ab6ebc81d25a63cdafa30de7cb49b776b367142f26`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 358.3 KB (358314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c1dbee4aeeef6e5fb1300fdb3bc18294e925cd09bbaaf1b15aa33e10ed8bd5`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8195ebb4a582faee7125a1f54b178e33d711e11f433d167ebb398bd3d7dadbb`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef092bafbfde0756ffc78f37df6a8535e86fc729053bca4043b4be37d30cdbd`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 20.8 MB (20833534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4946f34fbc3929b0bd1690efd11fde241fe49b422195a49a09396b88ea155603`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9f50c1a5652651e14e3c22d25b1481c335718752c4e07ac0542e78c7c3b328`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345a4650626a657dc7e6694018d735ab6606d22b47b705f8c09a7757e9015d43`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ed0744326d6c591698f832e08c6fa033c9e629de50f4c9483495c001fb2642`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 22.7 MB (22657124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b3a11825e8b21bb69b5c0384a182d6cdf8f1353b2bdb1442d4d16bce524e99`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe5aa15d97dd2804f78d9d8e369adabe4ea561c75eab7ad692dcd97967c33`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdfd59906a07f2c196fff6b67562e50e25b4afa4953e028029d2fc1e943dc43`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3376702d007e8b3dfce66cd8aad6d777423ed2c82d716767189aa3142e0522`  
		Last Modified: Fri, 11 Jul 2025 23:15:59 GMT  
		Size: 22.2 MB (22218765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.3-windowsservercore` - windows version 10.0.20348.3932; amd64

```console
$ docker pull docker@sha256:274102f6fb709884e50fbd6385533222a64cfee86d1cd8cb2dd9252c89666d55
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346616670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ee854316da74807f41148421e20eaad374dffdc0c364ae90833d5ad07e2c8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Fri, 11 Jul 2025 23:11:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:23 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:11:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:37 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:11:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:11:39 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:11:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:11:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:11:51 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a169b055e688e9a95c597265e07131d5232287fba68b1423932d0e5a0d17994`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c1203248b3626938b2771becf28b8c6911cd9df9219ae520645531c0dbb70d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 345.2 KB (345190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c3435e2f8aaac8a675144ceb7549700537e00f4786f114c42491ee8383725d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1581baec19a91b283eefc934c91344d47afca0ea900b35da3f836b0b64a42865`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cff61016e6a9f50575ce34439e6a2c7178f3565df3b13a8fc1e83f5f851db74`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 20.8 MB (20818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ee52ae9d5dfdddd94c77625c32cf6d55ca38841bb7de45eca5317774463cb5`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24e1d00d64556954d1d53d6b8e8a34cb7d25586fe655167a48cf826509f45b9`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84d9071c54da8e2804485c068baa75a4fbad0a877fc958c33956da99ed71eab`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b3be0ea66255c0c1e37cf6ee05b2e8f428c56609247f49352a06e5515da63`  
		Last Modified: Fri, 11 Jul 2025 23:13:28 GMT  
		Size: 22.6 MB (22637804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c75de97c3645b05b277e0b519d48ebd131d07d48c07cd2cd90e6f980e2895f1`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839a8bfa777f817ee9a9e87de8fdffdb95c126c2755e19dbec8942b0bc99922`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56150ca8198cc556b583f4c58d8c4f50c7d478fdd3ad61a90be92fef4b92e31`  
		Last Modified: Fri, 11 Jul 2025 23:13:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9fc7429c59acba4f39458ab7209516b370cfb3caac581a87f6fd05712a7fbca`  
		Last Modified: Fri, 11 Jul 2025 23:13:34 GMT  
		Size: 22.2 MB (22200448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ee29d642afb6aaff1bcb9e6fb8f7035a5ac073aa673be20e95c8db1d7c5369a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `docker:28.3-windowsservercore-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull docker@sha256:274102f6fb709884e50fbd6385533222a64cfee86d1cd8cb2dd9252c89666d55
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346616670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ee854316da74807f41148421e20eaad374dffdc0c364ae90833d5ad07e2c8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Fri, 11 Jul 2025 23:11:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:23 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:11:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:37 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:11:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:11:39 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:11:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:11:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:11:51 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a169b055e688e9a95c597265e07131d5232287fba68b1423932d0e5a0d17994`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c1203248b3626938b2771becf28b8c6911cd9df9219ae520645531c0dbb70d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 345.2 KB (345190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c3435e2f8aaac8a675144ceb7549700537e00f4786f114c42491ee8383725d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1581baec19a91b283eefc934c91344d47afca0ea900b35da3f836b0b64a42865`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cff61016e6a9f50575ce34439e6a2c7178f3565df3b13a8fc1e83f5f851db74`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 20.8 MB (20818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ee52ae9d5dfdddd94c77625c32cf6d55ca38841bb7de45eca5317774463cb5`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24e1d00d64556954d1d53d6b8e8a34cb7d25586fe655167a48cf826509f45b9`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84d9071c54da8e2804485c068baa75a4fbad0a877fc958c33956da99ed71eab`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b3be0ea66255c0c1e37cf6ee05b2e8f428c56609247f49352a06e5515da63`  
		Last Modified: Fri, 11 Jul 2025 23:13:28 GMT  
		Size: 22.6 MB (22637804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c75de97c3645b05b277e0b519d48ebd131d07d48c07cd2cd90e6f980e2895f1`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839a8bfa777f817ee9a9e87de8fdffdb95c126c2755e19dbec8942b0bc99922`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56150ca8198cc556b583f4c58d8c4f50c7d478fdd3ad61a90be92fef4b92e31`  
		Last Modified: Fri, 11 Jul 2025 23:13:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9fc7429c59acba4f39458ab7209516b370cfb3caac581a87f6fd05712a7fbca`  
		Last Modified: Fri, 11 Jul 2025 23:13:34 GMT  
		Size: 22.2 MB (22200448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:58f55a64f3de77413f3e65abc364e070c041f64571fd689dba68f3708478979a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `docker:28.3-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull docker@sha256:1b56934c5d06028439690c1309eb9b88eb3622cf09b3c658d8eb414b4cc4e480
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3557253065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cff6279f7a6bb0448b10fd3cd887bc504f14bae6713de69b38dbd1aa2e7706`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Fri, 11 Jul 2025 23:11:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:52 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:12:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:05 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:12:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:12:08 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:12:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:12:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:12:20 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775c3cb412ef97cfd2e8fb3eb8b4ed4eb842eca9fc398d2532621e5c7ca35ece`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695218c842722d24657641ab6ebc81d25a63cdafa30de7cb49b776b367142f26`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 358.3 KB (358314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c1dbee4aeeef6e5fb1300fdb3bc18294e925cd09bbaaf1b15aa33e10ed8bd5`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8195ebb4a582faee7125a1f54b178e33d711e11f433d167ebb398bd3d7dadbb`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef092bafbfde0756ffc78f37df6a8535e86fc729053bca4043b4be37d30cdbd`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 20.8 MB (20833534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4946f34fbc3929b0bd1690efd11fde241fe49b422195a49a09396b88ea155603`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9f50c1a5652651e14e3c22d25b1481c335718752c4e07ac0542e78c7c3b328`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345a4650626a657dc7e6694018d735ab6606d22b47b705f8c09a7757e9015d43`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ed0744326d6c591698f832e08c6fa033c9e629de50f4c9483495c001fb2642`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 22.7 MB (22657124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b3a11825e8b21bb69b5c0384a182d6cdf8f1353b2bdb1442d4d16bce524e99`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe5aa15d97dd2804f78d9d8e369adabe4ea561c75eab7ad692dcd97967c33`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdfd59906a07f2c196fff6b67562e50e25b4afa4953e028029d2fc1e943dc43`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3376702d007e8b3dfce66cd8aad6d777423ed2c82d716767189aa3142e0522`  
		Last Modified: Fri, 11 Jul 2025 23:15:59 GMT  
		Size: 22.2 MB (22218765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3.2`

```console
$ docker pull docker@sha256:684bc226a69eb91582738f196e59e234355420ee592abea7685e4127afbce645
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

### `docker:28.3.2` - linux; amd64

```console
$ docker pull docker@sha256:2039571fb2946ea368779140c94dfbda3c7858b493c42dbbe8345d19500e6d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147544548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d269157efa5eebf6dbc86f558a80e2cb8016c6a9a39793526a4396a512f6d2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb387276c10661bba84fce126eed7b4ef9ef3622bbaf76fed5855a2f4712ce89`  
		Last Modified: Fri, 11 Jul 2025 23:08:13 GMT  
		Size: 9.5 MB (9506675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f8a93798fbae872851b58e72ef4b3bdace12203577685b3e52d5e94c24b42`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 90.5 KB (90506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f487a7a0e1532da82eb272ebcd78402bf76ee707c063da6f3f485326c3d403a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1f25172b8052f548668179a49f8d03408390b474e886f7afd40ce39007449`  
		Last Modified: Fri, 11 Jul 2025 23:08:15 GMT  
		Size: 62.5 MB (62517439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f23e14ee4f80c7f15ead5263837d831d43d4d8023341200c812784762d266a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c327638cbba730a460f516b7fca541b5b3543003eed01c494273d4afe84af`  
		Last Modified: Fri, 11 Jul 2025 23:08:09 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2` - unknown; unknown

```console
$ docker pull docker@sha256:1612ef52d558ce839416d05d730405b29142c973896aabc995f904e7ab473970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91d6a682e933349713bef3b27e24c6173ee392272ac25eb3fa024eaffdb3758`

```dockerfile
```

-	Layers:
	-	`sha256:f4f1bd41a1006eba393a7d70732b5d538b904f8edc1eea71cba3c25ee7102546`  
		Last Modified: Sat, 12 Jul 2025 02:07:33 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2` - linux; arm variant v6

```console
$ docker pull docker@sha256:3960ae5dceff97e2f1523fbadd2521995a9daf4d387a5480808a22b2c0899b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138138376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ee56a5d4421a9708d18d5433cfbbbe8d0327c86185361a95dc2e7fd2cf8b64`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7539813331bce9849eabb04feabc475057f406b6008e4ee8fe9cc34b09584181`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 9.5 MB (9461142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0883a2e698c28639f5e51239c30f623739e588758e46b282b4d86ca0696974e5`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd721e456a1abbd99a37541edfb801f174d50c67eb927d7d11c5f99171d47d62`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed9a7b148f299ea5bae85c09fc8c8f23d43bf689367f224453031283e72d0c8`  
		Last Modified: Fri, 11 Jul 2025 23:07:39 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b17794da37735f4238675dc8f08e3b997577476e766a2823c345f45dc6032`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272cd592cd54400557bde2759b815592c11caed1b9ab0f1e3fbf4c40d586a8ee`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2` - unknown; unknown

```console
$ docker pull docker@sha256:fba4e76c7a853c8ec14ed8001c3f8afbea81b47032255689ca70d6f5f3f2c9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa67ed505137fefa99d92897b086b45c84d8e36db4289bbea88b2c0eb844d0a`

```dockerfile
```

-	Layers:
	-	`sha256:7c9d7dc66552b1f6a8db09f35ffcedf83ab42a2e73c3233cfb147e16b92cf06f`  
		Last Modified: Sat, 12 Jul 2025 02:07:37 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2` - linux; arm variant v7

```console
$ docker pull docker@sha256:5eb2289358e41707da0542f5777d08c6a252b8f0ded58903fcd72fe467703bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136289051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d930d302a73d55f2c350884eed98d79c117d882a7d599b564826bdb27828068`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c7a3c227e0d7b893835a896bf1421afe6c7a1bfe44b1141899c2a4ef2e889`  
		Last Modified: Fri, 11 Jul 2025 23:32:59 GMT  
		Size: 8.6 MB (8610408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33069b480d39ad0fd6e38090b30b043a73413afa7ca6ed1e0f3d1b54961669b0`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 86.5 KB (86504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129027ab9eb0b76ac3acd19b4198612a65e9c9f6f8b472a5d1bacb8583090852`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c185229dea08b37f2a81137ce8ea0b1455bbbdd9055c1ce9f9e1240066b71216`  
		Last Modified: Fri, 11 Jul 2025 23:33:02 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95881403c14969cffe472e4573c292f70ec294cd99406def97d5ff3e2208d8a9`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ba8c53288864cbc60a4a982c82dfc9c320157f56ad7cfcc7a049f0b3577864`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2` - unknown; unknown

```console
$ docker pull docker@sha256:407bfd26d03ddf54aca9656fac097643785152f2ae1042f160eb66253cb90812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9af45e0663098581e700831710f87e9f24f12a0e42213fb865f32ccecf9202a`

```dockerfile
```

-	Layers:
	-	`sha256:91475ec4af388e69220316d19fe0978aab6f0bfdc0d7adcb1be23f468d87f3f9`  
		Last Modified: Sat, 12 Jul 2025 02:07:41 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8a1c07af046d9b002e7d4eb623c39884512d3536d439abeaa725d0fae4c976b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138575154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698ae6cc2234b6bca2194e7639d01cc51f0d840a322887c06eefb9bf1a87446f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fed6fc4a68d5c71a2eb25262cb6ae103f5b4d17bc7af3066655e4038fa065`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 10.0 MB (10034378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37be3793d884a5c56f2ffc4899b108efdfb379d3412b94596889feeca6a4e19`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eefc3e025edefe52fa56cca59c462eff4688e14b7da94f1bb872ff684be9d96`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72138503f7c3515cce912ebff7c04ff9331b6f941114745557f8f3779bdfdbf`  
		Last Modified: Fri, 11 Jul 2025 23:34:45 GMT  
		Size: 57.5 MB (57464546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffed797ad64daff69c24cdc4b9b919cf829962a4c55474513ca6acbef6344e4`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ad5491b62b5a110e8c21811bbf035208ed68f752b71a1b2a848096c5c49201`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2` - unknown; unknown

```console
$ docker pull docker@sha256:a932864680893d42a6771d0ddeeb27e5bd50b731d9fd0e87c09aaaa29717e5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb27c8b2e82846d2b25aab8e29c2feb330ab2fa0d37efa5379c9f421b0f8485`

```dockerfile
```

-	Layers:
	-	`sha256:9fda5f788d0162b9af973bfde59e6c6abfc845820075a147bcab120322089c2c`  
		Last Modified: Sat, 12 Jul 2025 02:07:44 GMT  
		Size: 34.8 KB (34830 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.2-alpine3.22`

```console
$ docker pull docker@sha256:684bc226a69eb91582738f196e59e234355420ee592abea7685e4127afbce645
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

### `docker:28.3.2-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:2039571fb2946ea368779140c94dfbda3c7858b493c42dbbe8345d19500e6d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147544548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d269157efa5eebf6dbc86f558a80e2cb8016c6a9a39793526a4396a512f6d2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb387276c10661bba84fce126eed7b4ef9ef3622bbaf76fed5855a2f4712ce89`  
		Last Modified: Fri, 11 Jul 2025 23:08:13 GMT  
		Size: 9.5 MB (9506675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f8a93798fbae872851b58e72ef4b3bdace12203577685b3e52d5e94c24b42`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 90.5 KB (90506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f487a7a0e1532da82eb272ebcd78402bf76ee707c063da6f3f485326c3d403a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1f25172b8052f548668179a49f8d03408390b474e886f7afd40ce39007449`  
		Last Modified: Fri, 11 Jul 2025 23:08:15 GMT  
		Size: 62.5 MB (62517439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f23e14ee4f80c7f15ead5263837d831d43d4d8023341200c812784762d266a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c327638cbba730a460f516b7fca541b5b3543003eed01c494273d4afe84af`  
		Last Modified: Fri, 11 Jul 2025 23:08:09 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:1612ef52d558ce839416d05d730405b29142c973896aabc995f904e7ab473970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91d6a682e933349713bef3b27e24c6173ee392272ac25eb3fa024eaffdb3758`

```dockerfile
```

-	Layers:
	-	`sha256:f4f1bd41a1006eba393a7d70732b5d538b904f8edc1eea71cba3c25ee7102546`  
		Last Modified: Sat, 12 Jul 2025 02:07:33 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:3960ae5dceff97e2f1523fbadd2521995a9daf4d387a5480808a22b2c0899b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138138376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ee56a5d4421a9708d18d5433cfbbbe8d0327c86185361a95dc2e7fd2cf8b64`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7539813331bce9849eabb04feabc475057f406b6008e4ee8fe9cc34b09584181`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 9.5 MB (9461142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0883a2e698c28639f5e51239c30f623739e588758e46b282b4d86ca0696974e5`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd721e456a1abbd99a37541edfb801f174d50c67eb927d7d11c5f99171d47d62`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed9a7b148f299ea5bae85c09fc8c8f23d43bf689367f224453031283e72d0c8`  
		Last Modified: Fri, 11 Jul 2025 23:07:39 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b17794da37735f4238675dc8f08e3b997577476e766a2823c345f45dc6032`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272cd592cd54400557bde2759b815592c11caed1b9ab0f1e3fbf4c40d586a8ee`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:fba4e76c7a853c8ec14ed8001c3f8afbea81b47032255689ca70d6f5f3f2c9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa67ed505137fefa99d92897b086b45c84d8e36db4289bbea88b2c0eb844d0a`

```dockerfile
```

-	Layers:
	-	`sha256:7c9d7dc66552b1f6a8db09f35ffcedf83ab42a2e73c3233cfb147e16b92cf06f`  
		Last Modified: Sat, 12 Jul 2025 02:07:37 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:5eb2289358e41707da0542f5777d08c6a252b8f0ded58903fcd72fe467703bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136289051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d930d302a73d55f2c350884eed98d79c117d882a7d599b564826bdb27828068`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c7a3c227e0d7b893835a896bf1421afe6c7a1bfe44b1141899c2a4ef2e889`  
		Last Modified: Fri, 11 Jul 2025 23:32:59 GMT  
		Size: 8.6 MB (8610408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33069b480d39ad0fd6e38090b30b043a73413afa7ca6ed1e0f3d1b54961669b0`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 86.5 KB (86504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129027ab9eb0b76ac3acd19b4198612a65e9c9f6f8b472a5d1bacb8583090852`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c185229dea08b37f2a81137ce8ea0b1455bbbdd9055c1ce9f9e1240066b71216`  
		Last Modified: Fri, 11 Jul 2025 23:33:02 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95881403c14969cffe472e4573c292f70ec294cd99406def97d5ff3e2208d8a9`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ba8c53288864cbc60a4a982c82dfc9c320157f56ad7cfcc7a049f0b3577864`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:407bfd26d03ddf54aca9656fac097643785152f2ae1042f160eb66253cb90812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9af45e0663098581e700831710f87e9f24f12a0e42213fb865f32ccecf9202a`

```dockerfile
```

-	Layers:
	-	`sha256:91475ec4af388e69220316d19fe0978aab6f0bfdc0d7adcb1be23f468d87f3f9`  
		Last Modified: Sat, 12 Jul 2025 02:07:41 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8a1c07af046d9b002e7d4eb623c39884512d3536d439abeaa725d0fae4c976b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138575154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698ae6cc2234b6bca2194e7639d01cc51f0d840a322887c06eefb9bf1a87446f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fed6fc4a68d5c71a2eb25262cb6ae103f5b4d17bc7af3066655e4038fa065`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 10.0 MB (10034378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37be3793d884a5c56f2ffc4899b108efdfb379d3412b94596889feeca6a4e19`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eefc3e025edefe52fa56cca59c462eff4688e14b7da94f1bb872ff684be9d96`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72138503f7c3515cce912ebff7c04ff9331b6f941114745557f8f3779bdfdbf`  
		Last Modified: Fri, 11 Jul 2025 23:34:45 GMT  
		Size: 57.5 MB (57464546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffed797ad64daff69c24cdc4b9b919cf829962a4c55474513ca6acbef6344e4`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ad5491b62b5a110e8c21811bbf035208ed68f752b71a1b2a848096c5c49201`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:a932864680893d42a6771d0ddeeb27e5bd50b731d9fd0e87c09aaaa29717e5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb27c8b2e82846d2b25aab8e29c2feb330ab2fa0d37efa5379c9f421b0f8485`

```dockerfile
```

-	Layers:
	-	`sha256:9fda5f788d0162b9af973bfde59e6c6abfc845820075a147bcab120322089c2c`  
		Last Modified: Sat, 12 Jul 2025 02:07:44 GMT  
		Size: 34.8 KB (34830 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.2-cli`

```console
$ docker pull docker@sha256:13f8f54e0410b262768c3f9ec6fb987abd385ef2b16d43cfe44b93f2042ba399
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

### `docker:28.3.2-cli` - linux; amd64

```console
$ docker pull docker@sha256:ad955c02a8c8608a9a581c545b93b9d45023986553a9188da71ec2192ff9e2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75423937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29b7161492868d2bdab426c00ecf1a97e6d4249e4ce3e9e9ed98bae0dbbe7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1c4894165cfb9aaa1d2b37c50b551c31e17f71611b0ff43994110a9b460af8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236b9edd62480bf1994af5564b8ef182210d1336ff8892988f674ac27eaa5409`

```dockerfile
```

-	Layers:
	-	`sha256:fa1e8a11e4b8700fd3f91f6b363c3d23547ee308f1f0d69290d84031153575c7`  
		Last Modified: Fri, 11 Jul 2025 23:07:32 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:8b4a77177bb41dfbc484ffe2ca57773c9b8db3500a60596c0c259046d921d9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70384659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba833a381a4a0c18807371500fc2aba2f2538af694704e84f6be80a939ee3647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8d3de6ba8edd719f37c314ec9cb77ea92b3d9d7f3f43c4c8ccea5eab52d8bb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2de72b3b92515f3652b0c952bfd400180132ca92a98560966b78338b05a665b`

```dockerfile
```

-	Layers:
	-	`sha256:5d3aff152b821f9c64b37aa8c52a44adc9ee1104f48e48fc42bf63f8a0b7bf05`  
		Last Modified: Fri, 11 Jul 2025 23:07:22 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:2dfe76be879889721d4578609d8e57a681a1fb944f4ee8652de2f7b18fc04ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69389623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fa5a9d9861537caf7e62f6e3199c9cb97e9eb11907b3db24c2abb801d6e6f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f79f1a874c76d5e4b265a72dccb83bc513d7ff7f30bb0ba963bbfa5b82b9742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f65cbf035a05096f98a920c5dc0ba5979f0b9ce6ab023e58ca0ed9fe5f104c3`

```dockerfile
```

-	Layers:
	-	`sha256:6d694569211f0463fc2fa67fce30fbf7c91f557b6dc9aac14c0c6b9596e073fa`  
		Last Modified: Sat, 12 Jul 2025 02:07:45 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:29a155d2b64ee1f8ea9f51d52d109a94ad34178e8b4b9d62e645c96927a3119c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70970597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713cb7ebce506a192fd70fdda571e5ddf72f0815bed6363d998882208650b019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ca067feba0aa873cd74f3722c31ec7bf2065db5e8bad3bcbb2c0bbe4865da7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7747c774e4dc3eb0e4be57c7b98e8671a22cc51fcb182bc1a244be14f544cf30`

```dockerfile
```

-	Layers:
	-	`sha256:bbfb6f21e3789c8273c69cde35a76a93414d225c4f06c24482a778ab4dd42681`  
		Last Modified: Sat, 12 Jul 2025 02:07:48 GMT  
		Size: 38.3 KB (38321 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.2-cli-alpine3.22`

```console
$ docker pull docker@sha256:13f8f54e0410b262768c3f9ec6fb987abd385ef2b16d43cfe44b93f2042ba399
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

### `docker:28.3.2-cli-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:ad955c02a8c8608a9a581c545b93b9d45023986553a9188da71ec2192ff9e2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75423937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29b7161492868d2bdab426c00ecf1a97e6d4249e4ce3e9e9ed98bae0dbbe7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:1c4894165cfb9aaa1d2b37c50b551c31e17f71611b0ff43994110a9b460af8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236b9edd62480bf1994af5564b8ef182210d1336ff8892988f674ac27eaa5409`

```dockerfile
```

-	Layers:
	-	`sha256:fa1e8a11e4b8700fd3f91f6b363c3d23547ee308f1f0d69290d84031153575c7`  
		Last Modified: Fri, 11 Jul 2025 23:07:32 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-cli-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:8b4a77177bb41dfbc484ffe2ca57773c9b8db3500a60596c0c259046d921d9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70384659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba833a381a4a0c18807371500fc2aba2f2538af694704e84f6be80a939ee3647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:8d3de6ba8edd719f37c314ec9cb77ea92b3d9d7f3f43c4c8ccea5eab52d8bb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2de72b3b92515f3652b0c952bfd400180132ca92a98560966b78338b05a665b`

```dockerfile
```

-	Layers:
	-	`sha256:5d3aff152b821f9c64b37aa8c52a44adc9ee1104f48e48fc42bf63f8a0b7bf05`  
		Last Modified: Fri, 11 Jul 2025 23:07:22 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-cli-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:2dfe76be879889721d4578609d8e57a681a1fb944f4ee8652de2f7b18fc04ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69389623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fa5a9d9861537caf7e62f6e3199c9cb97e9eb11907b3db24c2abb801d6e6f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:f79f1a874c76d5e4b265a72dccb83bc513d7ff7f30bb0ba963bbfa5b82b9742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f65cbf035a05096f98a920c5dc0ba5979f0b9ce6ab023e58ca0ed9fe5f104c3`

```dockerfile
```

-	Layers:
	-	`sha256:6d694569211f0463fc2fa67fce30fbf7c91f557b6dc9aac14c0c6b9596e073fa`  
		Last Modified: Sat, 12 Jul 2025 02:07:45 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-cli-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:29a155d2b64ee1f8ea9f51d52d109a94ad34178e8b4b9d62e645c96927a3119c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70970597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713cb7ebce506a192fd70fdda571e5ddf72f0815bed6363d998882208650b019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-cli-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:ca067feba0aa873cd74f3722c31ec7bf2065db5e8bad3bcbb2c0bbe4865da7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7747c774e4dc3eb0e4be57c7b98e8671a22cc51fcb182bc1a244be14f544cf30`

```dockerfile
```

-	Layers:
	-	`sha256:bbfb6f21e3789c8273c69cde35a76a93414d225c4f06c24482a778ab4dd42681`  
		Last Modified: Sat, 12 Jul 2025 02:07:48 GMT  
		Size: 38.3 KB (38321 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.2-dind`

```console
$ docker pull docker@sha256:684bc226a69eb91582738f196e59e234355420ee592abea7685e4127afbce645
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

### `docker:28.3.2-dind` - linux; amd64

```console
$ docker pull docker@sha256:2039571fb2946ea368779140c94dfbda3c7858b493c42dbbe8345d19500e6d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147544548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d269157efa5eebf6dbc86f558a80e2cb8016c6a9a39793526a4396a512f6d2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb387276c10661bba84fce126eed7b4ef9ef3622bbaf76fed5855a2f4712ce89`  
		Last Modified: Fri, 11 Jul 2025 23:08:13 GMT  
		Size: 9.5 MB (9506675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f8a93798fbae872851b58e72ef4b3bdace12203577685b3e52d5e94c24b42`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 90.5 KB (90506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f487a7a0e1532da82eb272ebcd78402bf76ee707c063da6f3f485326c3d403a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1f25172b8052f548668179a49f8d03408390b474e886f7afd40ce39007449`  
		Last Modified: Fri, 11 Jul 2025 23:08:15 GMT  
		Size: 62.5 MB (62517439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f23e14ee4f80c7f15ead5263837d831d43d4d8023341200c812784762d266a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c327638cbba730a460f516b7fca541b5b3543003eed01c494273d4afe84af`  
		Last Modified: Fri, 11 Jul 2025 23:08:09 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1612ef52d558ce839416d05d730405b29142c973896aabc995f904e7ab473970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91d6a682e933349713bef3b27e24c6173ee392272ac25eb3fa024eaffdb3758`

```dockerfile
```

-	Layers:
	-	`sha256:f4f1bd41a1006eba393a7d70732b5d538b904f8edc1eea71cba3c25ee7102546`  
		Last Modified: Sat, 12 Jul 2025 02:07:33 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:3960ae5dceff97e2f1523fbadd2521995a9daf4d387a5480808a22b2c0899b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138138376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ee56a5d4421a9708d18d5433cfbbbe8d0327c86185361a95dc2e7fd2cf8b64`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7539813331bce9849eabb04feabc475057f406b6008e4ee8fe9cc34b09584181`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 9.5 MB (9461142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0883a2e698c28639f5e51239c30f623739e588758e46b282b4d86ca0696974e5`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd721e456a1abbd99a37541edfb801f174d50c67eb927d7d11c5f99171d47d62`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed9a7b148f299ea5bae85c09fc8c8f23d43bf689367f224453031283e72d0c8`  
		Last Modified: Fri, 11 Jul 2025 23:07:39 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b17794da37735f4238675dc8f08e3b997577476e766a2823c345f45dc6032`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272cd592cd54400557bde2759b815592c11caed1b9ab0f1e3fbf4c40d586a8ee`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:fba4e76c7a853c8ec14ed8001c3f8afbea81b47032255689ca70d6f5f3f2c9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa67ed505137fefa99d92897b086b45c84d8e36db4289bbea88b2c0eb844d0a`

```dockerfile
```

-	Layers:
	-	`sha256:7c9d7dc66552b1f6a8db09f35ffcedf83ab42a2e73c3233cfb147e16b92cf06f`  
		Last Modified: Sat, 12 Jul 2025 02:07:37 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:5eb2289358e41707da0542f5777d08c6a252b8f0ded58903fcd72fe467703bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136289051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d930d302a73d55f2c350884eed98d79c117d882a7d599b564826bdb27828068`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c7a3c227e0d7b893835a896bf1421afe6c7a1bfe44b1141899c2a4ef2e889`  
		Last Modified: Fri, 11 Jul 2025 23:32:59 GMT  
		Size: 8.6 MB (8610408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33069b480d39ad0fd6e38090b30b043a73413afa7ca6ed1e0f3d1b54961669b0`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 86.5 KB (86504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129027ab9eb0b76ac3acd19b4198612a65e9c9f6f8b472a5d1bacb8583090852`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c185229dea08b37f2a81137ce8ea0b1455bbbdd9055c1ce9f9e1240066b71216`  
		Last Modified: Fri, 11 Jul 2025 23:33:02 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95881403c14969cffe472e4573c292f70ec294cd99406def97d5ff3e2208d8a9`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ba8c53288864cbc60a4a982c82dfc9c320157f56ad7cfcc7a049f0b3577864`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:407bfd26d03ddf54aca9656fac097643785152f2ae1042f160eb66253cb90812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9af45e0663098581e700831710f87e9f24f12a0e42213fb865f32ccecf9202a`

```dockerfile
```

-	Layers:
	-	`sha256:91475ec4af388e69220316d19fe0978aab6f0bfdc0d7adcb1be23f468d87f3f9`  
		Last Modified: Sat, 12 Jul 2025 02:07:41 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8a1c07af046d9b002e7d4eb623c39884512d3536d439abeaa725d0fae4c976b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138575154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698ae6cc2234b6bca2194e7639d01cc51f0d840a322887c06eefb9bf1a87446f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fed6fc4a68d5c71a2eb25262cb6ae103f5b4d17bc7af3066655e4038fa065`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 10.0 MB (10034378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37be3793d884a5c56f2ffc4899b108efdfb379d3412b94596889feeca6a4e19`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eefc3e025edefe52fa56cca59c462eff4688e14b7da94f1bb872ff684be9d96`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72138503f7c3515cce912ebff7c04ff9331b6f941114745557f8f3779bdfdbf`  
		Last Modified: Fri, 11 Jul 2025 23:34:45 GMT  
		Size: 57.5 MB (57464546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffed797ad64daff69c24cdc4b9b919cf829962a4c55474513ca6acbef6344e4`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ad5491b62b5a110e8c21811bbf035208ed68f752b71a1b2a848096c5c49201`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a932864680893d42a6771d0ddeeb27e5bd50b731d9fd0e87c09aaaa29717e5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb27c8b2e82846d2b25aab8e29c2feb330ab2fa0d37efa5379c9f421b0f8485`

```dockerfile
```

-	Layers:
	-	`sha256:9fda5f788d0162b9af973bfde59e6c6abfc845820075a147bcab120322089c2c`  
		Last Modified: Sat, 12 Jul 2025 02:07:44 GMT  
		Size: 34.8 KB (34830 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.2-dind-alpine3.22`

```console
$ docker pull docker@sha256:684bc226a69eb91582738f196e59e234355420ee592abea7685e4127afbce645
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

### `docker:28.3.2-dind-alpine3.22` - linux; amd64

```console
$ docker pull docker@sha256:2039571fb2946ea368779140c94dfbda3c7858b493c42dbbe8345d19500e6d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147544548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d269157efa5eebf6dbc86f558a80e2cb8016c6a9a39793526a4396a512f6d2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb387276c10661bba84fce126eed7b4ef9ef3622bbaf76fed5855a2f4712ce89`  
		Last Modified: Fri, 11 Jul 2025 23:08:13 GMT  
		Size: 9.5 MB (9506675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f8a93798fbae872851b58e72ef4b3bdace12203577685b3e52d5e94c24b42`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 90.5 KB (90506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f487a7a0e1532da82eb272ebcd78402bf76ee707c063da6f3f485326c3d403a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1f25172b8052f548668179a49f8d03408390b474e886f7afd40ce39007449`  
		Last Modified: Fri, 11 Jul 2025 23:08:15 GMT  
		Size: 62.5 MB (62517439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f23e14ee4f80c7f15ead5263837d831d43d4d8023341200c812784762d266a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c327638cbba730a460f516b7fca541b5b3543003eed01c494273d4afe84af`  
		Last Modified: Fri, 11 Jul 2025 23:08:09 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:1612ef52d558ce839416d05d730405b29142c973896aabc995f904e7ab473970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91d6a682e933349713bef3b27e24c6173ee392272ac25eb3fa024eaffdb3758`

```dockerfile
```

-	Layers:
	-	`sha256:f4f1bd41a1006eba393a7d70732b5d538b904f8edc1eea71cba3c25ee7102546`  
		Last Modified: Sat, 12 Jul 2025 02:07:33 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-dind-alpine3.22` - linux; arm variant v6

```console
$ docker pull docker@sha256:3960ae5dceff97e2f1523fbadd2521995a9daf4d387a5480808a22b2c0899b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138138376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ee56a5d4421a9708d18d5433cfbbbe8d0327c86185361a95dc2e7fd2cf8b64`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7539813331bce9849eabb04feabc475057f406b6008e4ee8fe9cc34b09584181`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 9.5 MB (9461142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0883a2e698c28639f5e51239c30f623739e588758e46b282b4d86ca0696974e5`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd721e456a1abbd99a37541edfb801f174d50c67eb927d7d11c5f99171d47d62`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed9a7b148f299ea5bae85c09fc8c8f23d43bf689367f224453031283e72d0c8`  
		Last Modified: Fri, 11 Jul 2025 23:07:39 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b17794da37735f4238675dc8f08e3b997577476e766a2823c345f45dc6032`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272cd592cd54400557bde2759b815592c11caed1b9ab0f1e3fbf4c40d586a8ee`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:fba4e76c7a853c8ec14ed8001c3f8afbea81b47032255689ca70d6f5f3f2c9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa67ed505137fefa99d92897b086b45c84d8e36db4289bbea88b2c0eb844d0a`

```dockerfile
```

-	Layers:
	-	`sha256:7c9d7dc66552b1f6a8db09f35ffcedf83ab42a2e73c3233cfb147e16b92cf06f`  
		Last Modified: Sat, 12 Jul 2025 02:07:37 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-dind-alpine3.22` - linux; arm variant v7

```console
$ docker pull docker@sha256:5eb2289358e41707da0542f5777d08c6a252b8f0ded58903fcd72fe467703bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136289051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d930d302a73d55f2c350884eed98d79c117d882a7d599b564826bdb27828068`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c7a3c227e0d7b893835a896bf1421afe6c7a1bfe44b1141899c2a4ef2e889`  
		Last Modified: Fri, 11 Jul 2025 23:32:59 GMT  
		Size: 8.6 MB (8610408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33069b480d39ad0fd6e38090b30b043a73413afa7ca6ed1e0f3d1b54961669b0`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 86.5 KB (86504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129027ab9eb0b76ac3acd19b4198612a65e9c9f6f8b472a5d1bacb8583090852`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c185229dea08b37f2a81137ce8ea0b1455bbbdd9055c1ce9f9e1240066b71216`  
		Last Modified: Fri, 11 Jul 2025 23:33:02 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95881403c14969cffe472e4573c292f70ec294cd99406def97d5ff3e2208d8a9`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ba8c53288864cbc60a4a982c82dfc9c320157f56ad7cfcc7a049f0b3577864`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:407bfd26d03ddf54aca9656fac097643785152f2ae1042f160eb66253cb90812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9af45e0663098581e700831710f87e9f24f12a0e42213fb865f32ccecf9202a`

```dockerfile
```

-	Layers:
	-	`sha256:91475ec4af388e69220316d19fe0978aab6f0bfdc0d7adcb1be23f468d87f3f9`  
		Last Modified: Sat, 12 Jul 2025 02:07:41 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-dind-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8a1c07af046d9b002e7d4eb623c39884512d3536d439abeaa725d0fae4c976b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138575154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698ae6cc2234b6bca2194e7639d01cc51f0d840a322887c06eefb9bf1a87446f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fed6fc4a68d5c71a2eb25262cb6ae103f5b4d17bc7af3066655e4038fa065`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 10.0 MB (10034378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37be3793d884a5c56f2ffc4899b108efdfb379d3412b94596889feeca6a4e19`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eefc3e025edefe52fa56cca59c462eff4688e14b7da94f1bb872ff684be9d96`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72138503f7c3515cce912ebff7c04ff9331b6f941114745557f8f3779bdfdbf`  
		Last Modified: Fri, 11 Jul 2025 23:34:45 GMT  
		Size: 57.5 MB (57464546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffed797ad64daff69c24cdc4b9b919cf829962a4c55474513ca6acbef6344e4`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ad5491b62b5a110e8c21811bbf035208ed68f752b71a1b2a848096c5c49201`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-dind-alpine3.22` - unknown; unknown

```console
$ docker pull docker@sha256:a932864680893d42a6771d0ddeeb27e5bd50b731d9fd0e87c09aaaa29717e5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb27c8b2e82846d2b25aab8e29c2feb330ab2fa0d37efa5379c9f421b0f8485`

```dockerfile
```

-	Layers:
	-	`sha256:9fda5f788d0162b9af973bfde59e6c6abfc845820075a147bcab120322089c2c`  
		Last Modified: Sat, 12 Jul 2025 02:07:44 GMT  
		Size: 34.8 KB (34830 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.2-dind-rootless`

```console
$ docker pull docker@sha256:35198af02775d4862e97f6b8586ef506e389f61d114c1ac3118423cbed02daf4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28.3.2-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6525ecd8e4c79837c9ee9aef0cc9fab291ba4e9992a21f1471e2f4487e495c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168528184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1c15ddae240606ea58ccceb878320b41b6c810d7bb6396f893d8ee214d2a4a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb387276c10661bba84fce126eed7b4ef9ef3622bbaf76fed5855a2f4712ce89`  
		Last Modified: Fri, 11 Jul 2025 23:08:13 GMT  
		Size: 9.5 MB (9506675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f8a93798fbae872851b58e72ef4b3bdace12203577685b3e52d5e94c24b42`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 90.5 KB (90506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f487a7a0e1532da82eb272ebcd78402bf76ee707c063da6f3f485326c3d403a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1f25172b8052f548668179a49f8d03408390b474e886f7afd40ce39007449`  
		Last Modified: Fri, 11 Jul 2025 23:08:15 GMT  
		Size: 62.5 MB (62517439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f23e14ee4f80c7f15ead5263837d831d43d4d8023341200c812784762d266a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c327638cbba730a460f516b7fca541b5b3543003eed01c494273d4afe84af`  
		Last Modified: Fri, 11 Jul 2025 23:08:09 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03112a04e52db6d13027e01dd6050144a8aee81e36d90b7ea023e739fe61172a`  
		Last Modified: Fri, 11 Jul 2025 23:33:14 GMT  
		Size: 3.4 MB (3398166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e447c93da945b8522da3e732002649cf9b6b639efdbc4a2d403f29148812a07f`  
		Last Modified: Fri, 11 Jul 2025 23:33:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16efbe21a8d03d3afe5f2cb9d60c580aa7be65b64f2d75f24f75f682648e3fcb`  
		Last Modified: Fri, 11 Jul 2025 23:33:14 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c859e61e7fd0651e4a8f254bb741a8e274162bbe21bbb29f89a027a6f11c8d9`  
		Last Modified: Fri, 11 Jul 2025 23:33:15 GMT  
		Size: 17.6 MB (17584130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f840bbaab3748e2feb91b659386024e4dd8371b44a84198551bde19f08eb69dd`  
		Last Modified: Fri, 11 Jul 2025 23:33:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3e9d03bae67266207ff9fc79e8c017ab171e1f7ec59b71e2e53f0ebad48e73fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea477fdfcdddb1bf12cc64d22107f292a356f128c8da309975205671d580f64`

```dockerfile
```

-	Layers:
	-	`sha256:0820f43a7d2b86f7ede683b82c6eb56ed10bae0e0892c219427e8b8b339c72b6`  
		Last Modified: Sat, 12 Jul 2025 02:07:55 GMT  
		Size: 30.6 KB (30635 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28.3.2-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e113ae097663cf6428a12c793cddd2cf8ede3a895ef12468dece2036857c6594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159982139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f750db8fcf38249451e3f218882f1a8da997681207ad55fec24022d7187df2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fed6fc4a68d5c71a2eb25262cb6ae103f5b4d17bc7af3066655e4038fa065`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 10.0 MB (10034378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37be3793d884a5c56f2ffc4899b108efdfb379d3412b94596889feeca6a4e19`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eefc3e025edefe52fa56cca59c462eff4688e14b7da94f1bb872ff684be9d96`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72138503f7c3515cce912ebff7c04ff9331b6f941114745557f8f3779bdfdbf`  
		Last Modified: Fri, 11 Jul 2025 23:34:45 GMT  
		Size: 57.5 MB (57464546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffed797ad64daff69c24cdc4b9b919cf829962a4c55474513ca6acbef6344e4`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ad5491b62b5a110e8c21811bbf035208ed68f752b71a1b2a848096c5c49201`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da43fadc269459b75acd7de271e5a158d3571ab75c1ecc360602692e1ab07d0`  
		Last Modified: Sat, 12 Jul 2025 00:18:39 GMT  
		Size: 3.4 MB (3389661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4eb185ab4c980eb8b107c7bc3be6bbb124d73dafca5a67338af7189b1ab64`  
		Last Modified: Sat, 12 Jul 2025 00:18:38 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570abe49cfbd7a10502c8ab2552ff99ad64b6f334de551869c0b0127c8dccf3d`  
		Last Modified: Sat, 12 Jul 2025 00:18:38 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8f0e58928ea62c6fd1e569520de3775bc26384ab53f8281f34abff70fce620`  
		Last Modified: Sat, 12 Jul 2025 00:18:47 GMT  
		Size: 18.0 MB (18015982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e05691e4b87ef7aada1591b229cc9079e4ed99f8c9a452185b72aecb44b813`  
		Last Modified: Sat, 12 Jul 2025 00:18:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28.3.2-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0fda9319fb82b510fc50a5faa2d8a2ba11fba00261d4ad6df71b162730508c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93d59bce5cc499c904a106fd8621a20e5ad797dd0b8c49e2276126a91a57213`

```dockerfile
```

-	Layers:
	-	`sha256:f883c406c3f247dcf965d3dcfbff08d54a48f5f246be6867c6ce1b830ea62fce`  
		Last Modified: Sat, 12 Jul 2025 02:07:58 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:28.3.2-windowsservercore`

```console
$ docker pull docker@sha256:8af71f9bf2d9299f329b29664b8b03bc103d1ccfa95b6aa17e9ac2cc813b3f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `docker:28.3.2-windowsservercore` - windows version 10.0.26100.4652; amd64

```console
$ docker pull docker@sha256:1b56934c5d06028439690c1309eb9b88eb3622cf09b3c658d8eb414b4cc4e480
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3557253065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cff6279f7a6bb0448b10fd3cd887bc504f14bae6713de69b38dbd1aa2e7706`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Fri, 11 Jul 2025 23:11:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:52 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:12:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:05 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:12:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:12:08 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:12:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:12:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:12:20 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775c3cb412ef97cfd2e8fb3eb8b4ed4eb842eca9fc398d2532621e5c7ca35ece`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695218c842722d24657641ab6ebc81d25a63cdafa30de7cb49b776b367142f26`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 358.3 KB (358314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c1dbee4aeeef6e5fb1300fdb3bc18294e925cd09bbaaf1b15aa33e10ed8bd5`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8195ebb4a582faee7125a1f54b178e33d711e11f433d167ebb398bd3d7dadbb`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef092bafbfde0756ffc78f37df6a8535e86fc729053bca4043b4be37d30cdbd`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 20.8 MB (20833534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4946f34fbc3929b0bd1690efd11fde241fe49b422195a49a09396b88ea155603`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9f50c1a5652651e14e3c22d25b1481c335718752c4e07ac0542e78c7c3b328`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345a4650626a657dc7e6694018d735ab6606d22b47b705f8c09a7757e9015d43`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ed0744326d6c591698f832e08c6fa033c9e629de50f4c9483495c001fb2642`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 22.7 MB (22657124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b3a11825e8b21bb69b5c0384a182d6cdf8f1353b2bdb1442d4d16bce524e99`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe5aa15d97dd2804f78d9d8e369adabe4ea561c75eab7ad692dcd97967c33`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdfd59906a07f2c196fff6b67562e50e25b4afa4953e028029d2fc1e943dc43`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3376702d007e8b3dfce66cd8aad6d777423ed2c82d716767189aa3142e0522`  
		Last Modified: Fri, 11 Jul 2025 23:15:59 GMT  
		Size: 22.2 MB (22218765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:28.3.2-windowsservercore` - windows version 10.0.20348.3932; amd64

```console
$ docker pull docker@sha256:274102f6fb709884e50fbd6385533222a64cfee86d1cd8cb2dd9252c89666d55
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346616670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ee854316da74807f41148421e20eaad374dffdc0c364ae90833d5ad07e2c8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Fri, 11 Jul 2025 23:11:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:23 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:11:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:37 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:11:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:11:39 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:11:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:11:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:11:51 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a169b055e688e9a95c597265e07131d5232287fba68b1423932d0e5a0d17994`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c1203248b3626938b2771becf28b8c6911cd9df9219ae520645531c0dbb70d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 345.2 KB (345190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c3435e2f8aaac8a675144ceb7549700537e00f4786f114c42491ee8383725d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1581baec19a91b283eefc934c91344d47afca0ea900b35da3f836b0b64a42865`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cff61016e6a9f50575ce34439e6a2c7178f3565df3b13a8fc1e83f5f851db74`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 20.8 MB (20818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ee52ae9d5dfdddd94c77625c32cf6d55ca38841bb7de45eca5317774463cb5`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24e1d00d64556954d1d53d6b8e8a34cb7d25586fe655167a48cf826509f45b9`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84d9071c54da8e2804485c068baa75a4fbad0a877fc958c33956da99ed71eab`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b3be0ea66255c0c1e37cf6ee05b2e8f428c56609247f49352a06e5515da63`  
		Last Modified: Fri, 11 Jul 2025 23:13:28 GMT  
		Size: 22.6 MB (22637804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c75de97c3645b05b277e0b519d48ebd131d07d48c07cd2cd90e6f980e2895f1`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839a8bfa777f817ee9a9e87de8fdffdb95c126c2755e19dbec8942b0bc99922`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56150ca8198cc556b583f4c58d8c4f50c7d478fdd3ad61a90be92fef4b92e31`  
		Last Modified: Fri, 11 Jul 2025 23:13:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9fc7429c59acba4f39458ab7209516b370cfb3caac581a87f6fd05712a7fbca`  
		Last Modified: Fri, 11 Jul 2025 23:13:34 GMT  
		Size: 22.2 MB (22200448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3.2-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ee29d642afb6aaff1bcb9e6fb8f7035a5ac073aa673be20e95c8db1d7c5369a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `docker:28.3.2-windowsservercore-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull docker@sha256:274102f6fb709884e50fbd6385533222a64cfee86d1cd8cb2dd9252c89666d55
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346616670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ee854316da74807f41148421e20eaad374dffdc0c364ae90833d5ad07e2c8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Fri, 11 Jul 2025 23:11:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:23 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:11:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:37 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:11:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:11:39 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:11:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:11:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:11:51 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a169b055e688e9a95c597265e07131d5232287fba68b1423932d0e5a0d17994`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c1203248b3626938b2771becf28b8c6911cd9df9219ae520645531c0dbb70d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 345.2 KB (345190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c3435e2f8aaac8a675144ceb7549700537e00f4786f114c42491ee8383725d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1581baec19a91b283eefc934c91344d47afca0ea900b35da3f836b0b64a42865`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cff61016e6a9f50575ce34439e6a2c7178f3565df3b13a8fc1e83f5f851db74`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 20.8 MB (20818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ee52ae9d5dfdddd94c77625c32cf6d55ca38841bb7de45eca5317774463cb5`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24e1d00d64556954d1d53d6b8e8a34cb7d25586fe655167a48cf826509f45b9`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84d9071c54da8e2804485c068baa75a4fbad0a877fc958c33956da99ed71eab`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b3be0ea66255c0c1e37cf6ee05b2e8f428c56609247f49352a06e5515da63`  
		Last Modified: Fri, 11 Jul 2025 23:13:28 GMT  
		Size: 22.6 MB (22637804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c75de97c3645b05b277e0b519d48ebd131d07d48c07cd2cd90e6f980e2895f1`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839a8bfa777f817ee9a9e87de8fdffdb95c126c2755e19dbec8942b0bc99922`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56150ca8198cc556b583f4c58d8c4f50c7d478fdd3ad61a90be92fef4b92e31`  
		Last Modified: Fri, 11 Jul 2025 23:13:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9fc7429c59acba4f39458ab7209516b370cfb3caac581a87f6fd05712a7fbca`  
		Last Modified: Fri, 11 Jul 2025 23:13:34 GMT  
		Size: 22.2 MB (22200448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:28.3.2-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:58f55a64f3de77413f3e65abc364e070c041f64571fd689dba68f3708478979a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `docker:28.3.2-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull docker@sha256:1b56934c5d06028439690c1309eb9b88eb3622cf09b3c658d8eb414b4cc4e480
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3557253065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cff6279f7a6bb0448b10fd3cd887bc504f14bae6713de69b38dbd1aa2e7706`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Fri, 11 Jul 2025 23:11:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:52 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:12:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:05 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:12:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:12:08 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:12:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:12:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:12:20 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775c3cb412ef97cfd2e8fb3eb8b4ed4eb842eca9fc398d2532621e5c7ca35ece`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695218c842722d24657641ab6ebc81d25a63cdafa30de7cb49b776b367142f26`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 358.3 KB (358314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c1dbee4aeeef6e5fb1300fdb3bc18294e925cd09bbaaf1b15aa33e10ed8bd5`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8195ebb4a582faee7125a1f54b178e33d711e11f433d167ebb398bd3d7dadbb`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef092bafbfde0756ffc78f37df6a8535e86fc729053bca4043b4be37d30cdbd`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 20.8 MB (20833534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4946f34fbc3929b0bd1690efd11fde241fe49b422195a49a09396b88ea155603`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9f50c1a5652651e14e3c22d25b1481c335718752c4e07ac0542e78c7c3b328`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345a4650626a657dc7e6694018d735ab6606d22b47b705f8c09a7757e9015d43`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ed0744326d6c591698f832e08c6fa033c9e629de50f4c9483495c001fb2642`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 22.7 MB (22657124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b3a11825e8b21bb69b5c0384a182d6cdf8f1353b2bdb1442d4d16bce524e99`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe5aa15d97dd2804f78d9d8e369adabe4ea561c75eab7ad692dcd97967c33`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdfd59906a07f2c196fff6b67562e50e25b4afa4953e028029d2fc1e943dc43`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3376702d007e8b3dfce66cd8aad6d777423ed2c82d716767189aa3142e0522`  
		Last Modified: Fri, 11 Jul 2025 23:15:59 GMT  
		Size: 22.2 MB (22218765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:13f8f54e0410b262768c3f9ec6fb987abd385ef2b16d43cfe44b93f2042ba399
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
$ docker pull docker@sha256:ad955c02a8c8608a9a581c545b93b9d45023986553a9188da71ec2192ff9e2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75423937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29b7161492868d2bdab426c00ecf1a97e6d4249e4ce3e9e9ed98bae0dbbe7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:1c4894165cfb9aaa1d2b37c50b551c31e17f71611b0ff43994110a9b460af8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236b9edd62480bf1994af5564b8ef182210d1336ff8892988f674ac27eaa5409`

```dockerfile
```

-	Layers:
	-	`sha256:fa1e8a11e4b8700fd3f91f6b363c3d23547ee308f1f0d69290d84031153575c7`  
		Last Modified: Fri, 11 Jul 2025 23:07:32 GMT  
		Size: 38.1 KB (38116 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:8b4a77177bb41dfbc484ffe2ca57773c9b8db3500a60596c0c259046d921d9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70384659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba833a381a4a0c18807371500fc2aba2f2538af694704e84f6be80a939ee3647`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:8d3de6ba8edd719f37c314ec9cb77ea92b3d9d7f3f43c4c8ccea5eab52d8bb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2de72b3b92515f3652b0c952bfd400180132ca92a98560966b78338b05a665b`

```dockerfile
```

-	Layers:
	-	`sha256:5d3aff152b821f9c64b37aa8c52a44adc9ee1104f48e48fc42bf63f8a0b7bf05`  
		Last Modified: Fri, 11 Jul 2025 23:07:22 GMT  
		Size: 38.3 KB (38278 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:2dfe76be879889721d4578609d8e57a681a1fb944f4ee8652de2f7b18fc04ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69389623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fa5a9d9861537caf7e62f6e3199c9cb97e9eb11907b3db24c2abb801d6e6f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:f79f1a874c76d5e4b265a72dccb83bc513d7ff7f30bb0ba963bbfa5b82b9742d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f65cbf035a05096f98a920c5dc0ba5979f0b9ce6ab023e58ca0ed9fe5f104c3`

```dockerfile
```

-	Layers:
	-	`sha256:6d694569211f0463fc2fa67fce30fbf7c91f557b6dc9aac14c0c6b9596e073fa`  
		Last Modified: Sat, 12 Jul 2025 02:07:45 GMT  
		Size: 38.3 KB (38277 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:29a155d2b64ee1f8ea9f51d52d109a94ad34178e8b4b9d62e645c96927a3119c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70970597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713cb7ebce506a192fd70fdda571e5ddf72f0815bed6363d998882208650b019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:ca067feba0aa873cd74f3722c31ec7bf2065db5e8bad3bcbb2c0bbe4865da7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 KB (38321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7747c774e4dc3eb0e4be57c7b98e8671a22cc51fcb182bc1a244be14f544cf30`

```dockerfile
```

-	Layers:
	-	`sha256:bbfb6f21e3789c8273c69cde35a76a93414d225c4f06c24482a778ab4dd42681`  
		Last Modified: Sat, 12 Jul 2025 02:07:48 GMT  
		Size: 38.3 KB (38321 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:684bc226a69eb91582738f196e59e234355420ee592abea7685e4127afbce645
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
$ docker pull docker@sha256:2039571fb2946ea368779140c94dfbda3c7858b493c42dbbe8345d19500e6d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147544548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d269157efa5eebf6dbc86f558a80e2cb8016c6a9a39793526a4396a512f6d2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb387276c10661bba84fce126eed7b4ef9ef3622bbaf76fed5855a2f4712ce89`  
		Last Modified: Fri, 11 Jul 2025 23:08:13 GMT  
		Size: 9.5 MB (9506675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f8a93798fbae872851b58e72ef4b3bdace12203577685b3e52d5e94c24b42`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 90.5 KB (90506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f487a7a0e1532da82eb272ebcd78402bf76ee707c063da6f3f485326c3d403a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1f25172b8052f548668179a49f8d03408390b474e886f7afd40ce39007449`  
		Last Modified: Fri, 11 Jul 2025 23:08:15 GMT  
		Size: 62.5 MB (62517439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f23e14ee4f80c7f15ead5263837d831d43d4d8023341200c812784762d266a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c327638cbba730a460f516b7fca541b5b3543003eed01c494273d4afe84af`  
		Last Modified: Fri, 11 Jul 2025 23:08:09 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:1612ef52d558ce839416d05d730405b29142c973896aabc995f904e7ab473970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91d6a682e933349713bef3b27e24c6173ee392272ac25eb3fa024eaffdb3758`

```dockerfile
```

-	Layers:
	-	`sha256:f4f1bd41a1006eba393a7d70732b5d538b904f8edc1eea71cba3c25ee7102546`  
		Last Modified: Sat, 12 Jul 2025 02:07:33 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:3960ae5dceff97e2f1523fbadd2521995a9daf4d387a5480808a22b2c0899b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138138376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ee56a5d4421a9708d18d5433cfbbbe8d0327c86185361a95dc2e7fd2cf8b64`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7539813331bce9849eabb04feabc475057f406b6008e4ee8fe9cc34b09584181`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 9.5 MB (9461142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0883a2e698c28639f5e51239c30f623739e588758e46b282b4d86ca0696974e5`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd721e456a1abbd99a37541edfb801f174d50c67eb927d7d11c5f99171d47d62`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed9a7b148f299ea5bae85c09fc8c8f23d43bf689367f224453031283e72d0c8`  
		Last Modified: Fri, 11 Jul 2025 23:07:39 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b17794da37735f4238675dc8f08e3b997577476e766a2823c345f45dc6032`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272cd592cd54400557bde2759b815592c11caed1b9ab0f1e3fbf4c40d586a8ee`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:fba4e76c7a853c8ec14ed8001c3f8afbea81b47032255689ca70d6f5f3f2c9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa67ed505137fefa99d92897b086b45c84d8e36db4289bbea88b2c0eb844d0a`

```dockerfile
```

-	Layers:
	-	`sha256:7c9d7dc66552b1f6a8db09f35ffcedf83ab42a2e73c3233cfb147e16b92cf06f`  
		Last Modified: Sat, 12 Jul 2025 02:07:37 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:5eb2289358e41707da0542f5777d08c6a252b8f0ded58903fcd72fe467703bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136289051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d930d302a73d55f2c350884eed98d79c117d882a7d599b564826bdb27828068`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c7a3c227e0d7b893835a896bf1421afe6c7a1bfe44b1141899c2a4ef2e889`  
		Last Modified: Fri, 11 Jul 2025 23:32:59 GMT  
		Size: 8.6 MB (8610408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33069b480d39ad0fd6e38090b30b043a73413afa7ca6ed1e0f3d1b54961669b0`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 86.5 KB (86504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129027ab9eb0b76ac3acd19b4198612a65e9c9f6f8b472a5d1bacb8583090852`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c185229dea08b37f2a81137ce8ea0b1455bbbdd9055c1ce9f9e1240066b71216`  
		Last Modified: Fri, 11 Jul 2025 23:33:02 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95881403c14969cffe472e4573c292f70ec294cd99406def97d5ff3e2208d8a9`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ba8c53288864cbc60a4a982c82dfc9c320157f56ad7cfcc7a049f0b3577864`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:407bfd26d03ddf54aca9656fac097643785152f2ae1042f160eb66253cb90812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9af45e0663098581e700831710f87e9f24f12a0e42213fb865f32ccecf9202a`

```dockerfile
```

-	Layers:
	-	`sha256:91475ec4af388e69220316d19fe0978aab6f0bfdc0d7adcb1be23f468d87f3f9`  
		Last Modified: Sat, 12 Jul 2025 02:07:41 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8a1c07af046d9b002e7d4eb623c39884512d3536d439abeaa725d0fae4c976b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138575154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698ae6cc2234b6bca2194e7639d01cc51f0d840a322887c06eefb9bf1a87446f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fed6fc4a68d5c71a2eb25262cb6ae103f5b4d17bc7af3066655e4038fa065`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 10.0 MB (10034378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37be3793d884a5c56f2ffc4899b108efdfb379d3412b94596889feeca6a4e19`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eefc3e025edefe52fa56cca59c462eff4688e14b7da94f1bb872ff684be9d96`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72138503f7c3515cce912ebff7c04ff9331b6f941114745557f8f3779bdfdbf`  
		Last Modified: Fri, 11 Jul 2025 23:34:45 GMT  
		Size: 57.5 MB (57464546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffed797ad64daff69c24cdc4b9b919cf829962a4c55474513ca6acbef6344e4`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ad5491b62b5a110e8c21811bbf035208ed68f752b71a1b2a848096c5c49201`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a932864680893d42a6771d0ddeeb27e5bd50b731d9fd0e87c09aaaa29717e5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb27c8b2e82846d2b25aab8e29c2feb330ab2fa0d37efa5379c9f421b0f8485`

```dockerfile
```

-	Layers:
	-	`sha256:9fda5f788d0162b9af973bfde59e6c6abfc845820075a147bcab120322089c2c`  
		Last Modified: Sat, 12 Jul 2025 02:07:44 GMT  
		Size: 34.8 KB (34830 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:35198af02775d4862e97f6b8586ef506e389f61d114c1ac3118423cbed02daf4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6525ecd8e4c79837c9ee9aef0cc9fab291ba4e9992a21f1471e2f4487e495c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168528184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1c15ddae240606ea58ccceb878320b41b6c810d7bb6396f893d8ee214d2a4a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb387276c10661bba84fce126eed7b4ef9ef3622bbaf76fed5855a2f4712ce89`  
		Last Modified: Fri, 11 Jul 2025 23:08:13 GMT  
		Size: 9.5 MB (9506675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f8a93798fbae872851b58e72ef4b3bdace12203577685b3e52d5e94c24b42`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 90.5 KB (90506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f487a7a0e1532da82eb272ebcd78402bf76ee707c063da6f3f485326c3d403a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1f25172b8052f548668179a49f8d03408390b474e886f7afd40ce39007449`  
		Last Modified: Fri, 11 Jul 2025 23:08:15 GMT  
		Size: 62.5 MB (62517439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f23e14ee4f80c7f15ead5263837d831d43d4d8023341200c812784762d266a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c327638cbba730a460f516b7fca541b5b3543003eed01c494273d4afe84af`  
		Last Modified: Fri, 11 Jul 2025 23:08:09 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03112a04e52db6d13027e01dd6050144a8aee81e36d90b7ea023e739fe61172a`  
		Last Modified: Fri, 11 Jul 2025 23:33:14 GMT  
		Size: 3.4 MB (3398166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e447c93da945b8522da3e732002649cf9b6b639efdbc4a2d403f29148812a07f`  
		Last Modified: Fri, 11 Jul 2025 23:33:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16efbe21a8d03d3afe5f2cb9d60c580aa7be65b64f2d75f24f75f682648e3fcb`  
		Last Modified: Fri, 11 Jul 2025 23:33:14 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c859e61e7fd0651e4a8f254bb741a8e274162bbe21bbb29f89a027a6f11c8d9`  
		Last Modified: Fri, 11 Jul 2025 23:33:15 GMT  
		Size: 17.6 MB (17584130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f840bbaab3748e2feb91b659386024e4dd8371b44a84198551bde19f08eb69dd`  
		Last Modified: Fri, 11 Jul 2025 23:33:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3e9d03bae67266207ff9fc79e8c017ab171e1f7ec59b71e2e53f0ebad48e73fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea477fdfcdddb1bf12cc64d22107f292a356f128c8da309975205671d580f64`

```dockerfile
```

-	Layers:
	-	`sha256:0820f43a7d2b86f7ede683b82c6eb56ed10bae0e0892c219427e8b8b339c72b6`  
		Last Modified: Sat, 12 Jul 2025 02:07:55 GMT  
		Size: 30.6 KB (30635 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e113ae097663cf6428a12c793cddd2cf8ede3a895ef12468dece2036857c6594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159982139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f750db8fcf38249451e3f218882f1a8da997681207ad55fec24022d7187df2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fed6fc4a68d5c71a2eb25262cb6ae103f5b4d17bc7af3066655e4038fa065`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 10.0 MB (10034378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37be3793d884a5c56f2ffc4899b108efdfb379d3412b94596889feeca6a4e19`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eefc3e025edefe52fa56cca59c462eff4688e14b7da94f1bb872ff684be9d96`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72138503f7c3515cce912ebff7c04ff9331b6f941114745557f8f3779bdfdbf`  
		Last Modified: Fri, 11 Jul 2025 23:34:45 GMT  
		Size: 57.5 MB (57464546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffed797ad64daff69c24cdc4b9b919cf829962a4c55474513ca6acbef6344e4`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ad5491b62b5a110e8c21811bbf035208ed68f752b71a1b2a848096c5c49201`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da43fadc269459b75acd7de271e5a158d3571ab75c1ecc360602692e1ab07d0`  
		Last Modified: Sat, 12 Jul 2025 00:18:39 GMT  
		Size: 3.4 MB (3389661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c4eb185ab4c980eb8b107c7bc3be6bbb124d73dafca5a67338af7189b1ab64`  
		Last Modified: Sat, 12 Jul 2025 00:18:38 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570abe49cfbd7a10502c8ab2552ff99ad64b6f334de551869c0b0127c8dccf3d`  
		Last Modified: Sat, 12 Jul 2025 00:18:38 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8f0e58928ea62c6fd1e569520de3775bc26384ab53f8281f34abff70fce620`  
		Last Modified: Sat, 12 Jul 2025 00:18:47 GMT  
		Size: 18.0 MB (18015982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e05691e4b87ef7aada1591b229cc9079e4ed99f8c9a452185b72aecb44b813`  
		Last Modified: Sat, 12 Jul 2025 00:18:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0fda9319fb82b510fc50a5faa2d8a2ba11fba00261d4ad6df71b162730508c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93d59bce5cc499c904a106fd8621a20e5ad797dd0b8c49e2276126a91a57213`

```dockerfile
```

-	Layers:
	-	`sha256:f883c406c3f247dcf965d3dcfbff08d54a48f5f246be6867c6ce1b830ea62fce`  
		Last Modified: Sat, 12 Jul 2025 02:07:58 GMT  
		Size: 30.8 KB (30807 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:684bc226a69eb91582738f196e59e234355420ee592abea7685e4127afbce645
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
$ docker pull docker@sha256:2039571fb2946ea368779140c94dfbda3c7858b493c42dbbe8345d19500e6d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147544548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d269157efa5eebf6dbc86f558a80e2cb8016c6a9a39793526a4396a512f6d2f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b2c804715e1d2764c1b1055fc7555586e7f803131c5f3d9c4839b76f586ae4`  
		Last Modified: Fri, 11 Jul 2025 23:03:35 GMT  
		Size: 8.2 MB (8207387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508b10a70f04d35fbe618047c2025eef7fa0ad98635d78c2547f1d46d55c13f9`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f02761e25eda08b004b82e144d7c76335ff4256babedf23a3eddea680ec6`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 20.5 MB (20472150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b6d4364e33a7a961c982d9edb42cdd0d9576806cdc3c776bf64615b79b6f`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415fbc0e3f439bbec05203d17a509688636a6ce31398247243b6c7367cc1df3`  
		Last Modified: Fri, 11 Jul 2025 23:03:36 GMT  
		Size: 21.3 MB (21281243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fe8dfc194f850050fd54677d589ef6cda9456b15b70bd41a238045e8ab198`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6affb027fcae5f1b0d4d02d0da17a2cdc16e804a629d20c52ff885742083448`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e156e773c52b35a98addfbb063957a3c65ff935f38d2c9ee1254cfa820c069`  
		Last Modified: Fri, 11 Jul 2025 23:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb387276c10661bba84fce126eed7b4ef9ef3622bbaf76fed5855a2f4712ce89`  
		Last Modified: Fri, 11 Jul 2025 23:08:13 GMT  
		Size: 9.5 MB (9506675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2f8a93798fbae872851b58e72ef4b3bdace12203577685b3e52d5e94c24b42`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 90.5 KB (90506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f487a7a0e1532da82eb272ebcd78402bf76ee707c063da6f3f485326c3d403a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1f25172b8052f548668179a49f8d03408390b474e886f7afd40ce39007449`  
		Last Modified: Fri, 11 Jul 2025 23:08:15 GMT  
		Size: 62.5 MB (62517439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f23e14ee4f80c7f15ead5263837d831d43d4d8023341200c812784762d266a`  
		Last Modified: Fri, 11 Jul 2025 23:08:10 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7c327638cbba730a460f516b7fca541b5b3543003eed01c494273d4afe84af`  
		Last Modified: Fri, 11 Jul 2025 23:08:09 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:1612ef52d558ce839416d05d730405b29142c973896aabc995f904e7ab473970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91d6a682e933349713bef3b27e24c6173ee392272ac25eb3fa024eaffdb3758`

```dockerfile
```

-	Layers:
	-	`sha256:f4f1bd41a1006eba393a7d70732b5d538b904f8edc1eea71cba3c25ee7102546`  
		Last Modified: Sat, 12 Jul 2025 02:07:33 GMT  
		Size: 34.6 KB (34589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:3960ae5dceff97e2f1523fbadd2521995a9daf4d387a5480808a22b2c0899b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138138376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ee56a5d4421a9708d18d5433cfbbbe8d0327c86185361a95dc2e7fd2cf8b64`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9315e4ae003c4932b2d731f118ab95ba5e31da8693f2f37d8e5ccf35ce3a3834`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 8.1 MB (8114664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bcdb2cfea956eba0680481ec7bcec22748d82f9bfcd82f8fb7e079bdd8188c`  
		Last Modified: Thu, 05 Jun 2025 22:44:08 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562f8207b17ce00c8cf4cb27cf2fc8548690612dcef6fa5096412f41206bb02`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 18.5 MB (18457254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4347ab45d011f62c357724e01df8d14039c1be50f5a48af8afcdc0642ce1a12`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.3 MB (20295383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b286a00d84f0b75113c8155c710eefef598f9395684ba446beef14d5f1f2f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:12 GMT  
		Size: 20.0 MB (20014267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a7074d26f21d797ef18c088512fb9354ecd0d20ae6fe3b1d0479e8d52a6f7`  
		Last Modified: Fri, 11 Jul 2025 23:03:10 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66634cb978787ede2ba3551160194d26f11d78229f32df75fb27819360d69849`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db15fce538140fcb41d50f396088911ad53fa9535ea61a965e4e120f81b2bac`  
		Last Modified: Fri, 11 Jul 2025 23:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7539813331bce9849eabb04feabc475057f406b6008e4ee8fe9cc34b09584181`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 9.5 MB (9461142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0883a2e698c28639f5e51239c30f623739e588758e46b282b4d86ca0696974e5`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd721e456a1abbd99a37541edfb801f174d50c67eb927d7d11c5f99171d47d62`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed9a7b148f299ea5bae85c09fc8c8f23d43bf689367f224453031283e72d0c8`  
		Last Modified: Fri, 11 Jul 2025 23:07:39 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100b17794da37735f4238675dc8f08e3b997577476e766a2823c345f45dc6032`  
		Last Modified: Fri, 11 Jul 2025 23:07:33 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272cd592cd54400557bde2759b815592c11caed1b9ab0f1e3fbf4c40d586a8ee`  
		Last Modified: Fri, 11 Jul 2025 23:07:34 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:fba4e76c7a853c8ec14ed8001c3f8afbea81b47032255689ca70d6f5f3f2c9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa67ed505137fefa99d92897b086b45c84d8e36db4289bbea88b2c0eb844d0a`

```dockerfile
```

-	Layers:
	-	`sha256:7c9d7dc66552b1f6a8db09f35ffcedf83ab42a2e73c3233cfb147e16b92cf06f`  
		Last Modified: Sat, 12 Jul 2025 02:07:37 GMT  
		Size: 34.8 KB (34765 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:5eb2289358e41707da0542f5777d08c6a252b8f0ded58903fcd72fe467703bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136289051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d930d302a73d55f2c350884eed98d79c117d882a7d599b564826bdb27828068`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8744e27897a55eb08af859a97d9c03d6a74d08e092470ff034ebfe560d732ec4`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 7.4 MB (7440619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e300c45789036e097478e19f3431e50d26c74c192c75be446ad0ba6cd938e75`  
		Last Modified: Tue, 01 Jul 2025 22:39:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856ad1fb1fb1735c36c8233c8564b3d732aa8496f98cd36683e44689a04bb172`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 18.4 MB (18445976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45740b960dd7245fa002b4aeef7aa7ec2f2505e43d8dd43e44f3f0664bd00c94`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.3 MB (20282784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd4b99b797c8569171445449b2d0e696b171e848c75290bde33e42b62e8edf`  
		Last Modified: Fri, 11 Jul 2025 23:12:58 GMT  
		Size: 20.0 MB (19998903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b0dd01ce212617004ae66e8944482b8c70b2f7ca5ebe51613655b965eebfc4`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37334c5b7bf8bb853be9b7afa4b491daebfb2631752eeaff3d2b3c9c63be5c0`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe3bbe15417e8aab48ad09ffe920be4c0a82d9bfc2387ec763072b84e98bca`  
		Last Modified: Fri, 11 Jul 2025 23:12:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671c7a3c227e0d7b893835a896bf1421afe6c7a1bfe44b1141899c2a4ef2e889`  
		Last Modified: Fri, 11 Jul 2025 23:32:59 GMT  
		Size: 8.6 MB (8610408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33069b480d39ad0fd6e38090b30b043a73413afa7ca6ed1e0f3d1b54961669b0`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 86.5 KB (86504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129027ab9eb0b76ac3acd19b4198612a65e9c9f6f8b472a5d1bacb8583090852`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c185229dea08b37f2a81137ce8ea0b1455bbbdd9055c1ce9f9e1240066b71216`  
		Last Modified: Fri, 11 Jul 2025 23:33:02 GMT  
		Size: 58.2 MB (58196511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95881403c14969cffe472e4573c292f70ec294cd99406def97d5ff3e2208d8a9`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ba8c53288864cbc60a4a982c82dfc9c320157f56ad7cfcc7a049f0b3577864`  
		Last Modified: Fri, 11 Jul 2025 23:32:58 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:407bfd26d03ddf54aca9656fac097643785152f2ae1042f160eb66253cb90812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9af45e0663098581e700831710f87e9f24f12a0e42213fb865f32ccecf9202a`

```dockerfile
```

-	Layers:
	-	`sha256:91475ec4af388e69220316d19fe0978aab6f0bfdc0d7adcb1be23f468d87f3f9`  
		Last Modified: Sat, 12 Jul 2025 02:07:41 GMT  
		Size: 34.8 KB (34766 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:b8a1c07af046d9b002e7d4eb623c39884512d3536d439abeaa725d0fae4c976b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138575154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698ae6cc2234b6bca2194e7639d01cc51f0d840a322887c06eefb9bf1a87446f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_VERSION=28.3.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-x86_64'; 			sha256='486b3ffc0f806ca2efbc430cef89955386011662f0c76bad17c103d059cfa9cf'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv6'; 			sha256='3c572ab8554e37e08cd81850464380bfd276b70528d60dcc734d0934380a10c2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-armv7'; 			sha256='ec4786c5c33393d5e366fd6186cbfa116ae30a083666afefc428e4688a222c27'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-aarch64'; 			sha256='4d0f7678dd3338452beba4518e36a8e22b20cad79ba2535c687da554dc3997fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-ppc64le'; 			sha256='4d61ed3f0690c7415bdbe77acf2236121f5a560ff0e41022e2fabecc1690f5a6'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-riscv64'; 			sha256='67c65c4015db38b526b262cee9d98915f8fcb56b42be7926a21a7ec2ec0c3d2c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-linux-s390x'; 			sha256='e4aaad3a1a444d7e226ffda3df68795a562f9c3cb0b4805a74c2283036e6e7f0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 09 Jul 2025 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD ["sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 09 Jul 2025 23:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Jul 2025 23:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 09 Jul 2025 23:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 09 Jul 2025 23:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 09 Jul 2025 23:04:15 GMT
CMD []
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d7fcac09a3a401c2ac8e27ee557f271e642f965947da8c5bfa8b1ca238a1c9`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 8.2 MB (8229680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325d25a0ada27a36c2a50cf2995137cb2716a11bcdac9a133ecb8d8e818b033`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e366ef4b658acf3e8ea07d63c48991cf3e1e03d24909067b0e71b78834784886`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.3 MB (19272742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab73568b366cc1bd27f0afcf53c6f52e7fb043cc1c81bafa1428b6d50d6e42df`  
		Last Modified: Fri, 11 Jul 2025 23:24:30 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc992fdb53beed744a6154703e1d55034deaaa820e935188df3a80afbd7a49a`  
		Last Modified: Fri, 11 Jul 2025 23:24:31 GMT  
		Size: 19.5 MB (19510648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a85b97fceb0a4c890cea4d336d7f1fb7c697394cab5481fb7f53150958a3996`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3353b40514c275a6da3cc50c1b69d7549c752a0af52b0e06cd6f6c986683938`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e513651478931491a1dcd6cb0b01b599897472ef7edf1926694c4821dcf63b9a`  
		Last Modified: Fri, 11 Jul 2025 23:24:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fed6fc4a68d5c71a2eb25262cb6ae103f5b4d17bc7af3066655e4038fa065`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 10.0 MB (10034378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37be3793d884a5c56f2ffc4899b108efdfb379d3412b94596889feeca6a4e19`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 99.6 KB (99634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eefc3e025edefe52fa56cca59c462eff4688e14b7da94f1bb872ff684be9d96`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72138503f7c3515cce912ebff7c04ff9331b6f941114745557f8f3779bdfdbf`  
		Last Modified: Fri, 11 Jul 2025 23:34:45 GMT  
		Size: 57.5 MB (57464546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffed797ad64daff69c24cdc4b9b919cf829962a4c55474513ca6acbef6344e4`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ad5491b62b5a110e8c21811bbf035208ed68f752b71a1b2a848096c5c49201`  
		Last Modified: Fri, 11 Jul 2025 23:34:41 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:a932864680893d42a6771d0ddeeb27e5bd50b731d9fd0e87c09aaaa29717e5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb27c8b2e82846d2b25aab8e29c2feb330ab2fa0d37efa5379c9f421b0f8485`

```dockerfile
```

-	Layers:
	-	`sha256:9fda5f788d0162b9af973bfde59e6c6abfc845820075a147bcab120322089c2c`  
		Last Modified: Sat, 12 Jul 2025 02:07:44 GMT  
		Size: 34.8 KB (34830 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:8af71f9bf2d9299f329b29664b8b03bc103d1ccfa95b6aa17e9ac2cc813b3f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `docker:windowsservercore` - windows version 10.0.26100.4652; amd64

```console
$ docker pull docker@sha256:1b56934c5d06028439690c1309eb9b88eb3622cf09b3c658d8eb414b4cc4e480
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3557253065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cff6279f7a6bb0448b10fd3cd887bc504f14bae6713de69b38dbd1aa2e7706`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Fri, 11 Jul 2025 23:11:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:52 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:12:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:05 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:12:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:12:08 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:12:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:12:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:12:20 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775c3cb412ef97cfd2e8fb3eb8b4ed4eb842eca9fc398d2532621e5c7ca35ece`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695218c842722d24657641ab6ebc81d25a63cdafa30de7cb49b776b367142f26`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 358.3 KB (358314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c1dbee4aeeef6e5fb1300fdb3bc18294e925cd09bbaaf1b15aa33e10ed8bd5`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8195ebb4a582faee7125a1f54b178e33d711e11f433d167ebb398bd3d7dadbb`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef092bafbfde0756ffc78f37df6a8535e86fc729053bca4043b4be37d30cdbd`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 20.8 MB (20833534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4946f34fbc3929b0bd1690efd11fde241fe49b422195a49a09396b88ea155603`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9f50c1a5652651e14e3c22d25b1481c335718752c4e07ac0542e78c7c3b328`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345a4650626a657dc7e6694018d735ab6606d22b47b705f8c09a7757e9015d43`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ed0744326d6c591698f832e08c6fa033c9e629de50f4c9483495c001fb2642`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 22.7 MB (22657124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b3a11825e8b21bb69b5c0384a182d6cdf8f1353b2bdb1442d4d16bce524e99`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe5aa15d97dd2804f78d9d8e369adabe4ea561c75eab7ad692dcd97967c33`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdfd59906a07f2c196fff6b67562e50e25b4afa4953e028029d2fc1e943dc43`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3376702d007e8b3dfce66cd8aad6d777423ed2c82d716767189aa3142e0522`  
		Last Modified: Fri, 11 Jul 2025 23:15:59 GMT  
		Size: 22.2 MB (22218765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3932; amd64

```console
$ docker pull docker@sha256:274102f6fb709884e50fbd6385533222a64cfee86d1cd8cb2dd9252c89666d55
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346616670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ee854316da74807f41148421e20eaad374dffdc0c364ae90833d5ad07e2c8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Fri, 11 Jul 2025 23:11:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:23 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:11:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:37 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:11:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:11:39 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:11:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:11:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:11:51 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a169b055e688e9a95c597265e07131d5232287fba68b1423932d0e5a0d17994`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c1203248b3626938b2771becf28b8c6911cd9df9219ae520645531c0dbb70d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 345.2 KB (345190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c3435e2f8aaac8a675144ceb7549700537e00f4786f114c42491ee8383725d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1581baec19a91b283eefc934c91344d47afca0ea900b35da3f836b0b64a42865`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cff61016e6a9f50575ce34439e6a2c7178f3565df3b13a8fc1e83f5f851db74`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 20.8 MB (20818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ee52ae9d5dfdddd94c77625c32cf6d55ca38841bb7de45eca5317774463cb5`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24e1d00d64556954d1d53d6b8e8a34cb7d25586fe655167a48cf826509f45b9`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84d9071c54da8e2804485c068baa75a4fbad0a877fc958c33956da99ed71eab`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b3be0ea66255c0c1e37cf6ee05b2e8f428c56609247f49352a06e5515da63`  
		Last Modified: Fri, 11 Jul 2025 23:13:28 GMT  
		Size: 22.6 MB (22637804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c75de97c3645b05b277e0b519d48ebd131d07d48c07cd2cd90e6f980e2895f1`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839a8bfa777f817ee9a9e87de8fdffdb95c126c2755e19dbec8942b0bc99922`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56150ca8198cc556b583f4c58d8c4f50c7d478fdd3ad61a90be92fef4b92e31`  
		Last Modified: Fri, 11 Jul 2025 23:13:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9fc7429c59acba4f39458ab7209516b370cfb3caac581a87f6fd05712a7fbca`  
		Last Modified: Fri, 11 Jul 2025 23:13:34 GMT  
		Size: 22.2 MB (22200448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ee29d642afb6aaff1bcb9e6fb8f7035a5ac073aa673be20e95c8db1d7c5369a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull docker@sha256:274102f6fb709884e50fbd6385533222a64cfee86d1cd8cb2dd9252c89666d55
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346616670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ee854316da74807f41148421e20eaad374dffdc0c364ae90833d5ad07e2c8b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Fri, 11 Jul 2025 23:11:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:22 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:23 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:11:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:37 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:11:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:11:39 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:11:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:11:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:11:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:11:51 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a169b055e688e9a95c597265e07131d5232287fba68b1423932d0e5a0d17994`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c1203248b3626938b2771becf28b8c6911cd9df9219ae520645531c0dbb70d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 345.2 KB (345190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c3435e2f8aaac8a675144ceb7549700537e00f4786f114c42491ee8383725d`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1581baec19a91b283eefc934c91344d47afca0ea900b35da3f836b0b64a42865`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cff61016e6a9f50575ce34439e6a2c7178f3565df3b13a8fc1e83f5f851db74`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 20.8 MB (20818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ee52ae9d5dfdddd94c77625c32cf6d55ca38841bb7de45eca5317774463cb5`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24e1d00d64556954d1d53d6b8e8a34cb7d25586fe655167a48cf826509f45b9`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84d9071c54da8e2804485c068baa75a4fbad0a877fc958c33956da99ed71eab`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b3be0ea66255c0c1e37cf6ee05b2e8f428c56609247f49352a06e5515da63`  
		Last Modified: Fri, 11 Jul 2025 23:13:28 GMT  
		Size: 22.6 MB (22637804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c75de97c3645b05b277e0b519d48ebd131d07d48c07cd2cd90e6f980e2895f1`  
		Last Modified: Fri, 11 Jul 2025 23:13:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e839a8bfa777f817ee9a9e87de8fdffdb95c126c2755e19dbec8942b0bc99922`  
		Last Modified: Fri, 11 Jul 2025 23:13:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56150ca8198cc556b583f4c58d8c4f50c7d478fdd3ad61a90be92fef4b92e31`  
		Last Modified: Fri, 11 Jul 2025 23:13:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9fc7429c59acba4f39458ab7209516b370cfb3caac581a87f6fd05712a7fbca`  
		Last Modified: Fri, 11 Jul 2025 23:13:34 GMT  
		Size: 22.2 MB (22200448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:58f55a64f3de77413f3e65abc364e070c041f64571fd689dba68f3708478979a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull docker@sha256:1b56934c5d06028439690c1309eb9b88eb3622cf09b3c658d8eb414b4cc4e480
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3557253065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cff6279f7a6bb0448b10fd3cd887bc504f14bae6713de69b38dbd1aa2e7706`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Fri, 11 Jul 2025 23:11:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 11 Jul 2025 23:11:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 11 Jul 2025 23:11:52 GMT
ENV DOCKER_VERSION=28.3.2
# Fri, 11 Jul 2025 23:11:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.3.2.zip
# Fri, 11 Jul 2025 23:12:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:05 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 11 Jul 2025 23:12:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.windows-amd64.exe
# Fri, 11 Jul 2025 23:12:08 GMT
ENV DOCKER_BUILDX_SHA256=22baed7fdec17b429f4267d3ae388828dfea0c40622ef79ee6fb0a0d08d878fb
# Fri, 11 Jul 2025 23:12:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 11 Jul 2025 23:12:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.2
# Fri, 11 Jul 2025 23:12:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.38.2/docker-compose-windows-x86_64.exe
# Fri, 11 Jul 2025 23:12:20 GMT
ENV DOCKER_COMPOSE_SHA256=ba8f09d3873f7a9755b863ed2013a1276b96fcbbc074c69ff3d3cfbce3e0186f
# Fri, 11 Jul 2025 23:12:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775c3cb412ef97cfd2e8fb3eb8b4ed4eb842eca9fc398d2532621e5c7ca35ece`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695218c842722d24657641ab6ebc81d25a63cdafa30de7cb49b776b367142f26`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 358.3 KB (358314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c1dbee4aeeef6e5fb1300fdb3bc18294e925cd09bbaaf1b15aa33e10ed8bd5`  
		Last Modified: Fri, 11 Jul 2025 23:16:00 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8195ebb4a582faee7125a1f54b178e33d711e11f433d167ebb398bd3d7dadbb`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef092bafbfde0756ffc78f37df6a8535e86fc729053bca4043b4be37d30cdbd`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 20.8 MB (20833534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4946f34fbc3929b0bd1690efd11fde241fe49b422195a49a09396b88ea155603`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9f50c1a5652651e14e3c22d25b1481c335718752c4e07ac0542e78c7c3b328`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345a4650626a657dc7e6694018d735ab6606d22b47b705f8c09a7757e9015d43`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ed0744326d6c591698f832e08c6fa033c9e629de50f4c9483495c001fb2642`  
		Last Modified: Fri, 11 Jul 2025 23:16:04 GMT  
		Size: 22.7 MB (22657124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b3a11825e8b21bb69b5c0384a182d6cdf8f1353b2bdb1442d4d16bce524e99`  
		Last Modified: Fri, 11 Jul 2025 23:16:01 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfe5aa15d97dd2804f78d9d8e369adabe4ea561c75eab7ad692dcd97967c33`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdfd59906a07f2c196fff6b67562e50e25b4afa4953e028029d2fc1e943dc43`  
		Last Modified: Fri, 11 Jul 2025 23:15:57 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3376702d007e8b3dfce66cd8aad6d777423ed2c82d716767189aa3142e0522`  
		Last Modified: Fri, 11 Jul 2025 23:15:59 GMT  
		Size: 22.2 MB (22218765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
