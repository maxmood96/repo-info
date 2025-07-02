## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:2d478b8fee0330bc0fc56401fdf9df521281388a50401e4ea1d014ed440be124
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ce9ef5a87b9a9d60b895ca3b2488402119c9fb4ac402af3935b3babfc3e62e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165913942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f9193f50223ddaaf134b9d5c7926d086ed6f71f6aa3987c08519217ffa0e4e3`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.38.1
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-x86_64'; 			sha256='d94a60549c6916499ce41959941e6c88b67c23ed98d1c5eee2cfc4a2d58aa24b'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv6'; 			sha256='1025f08f0a91bac695376a118dc95c50bc8a7bb77558bd486a12eeff1aac63b9'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-armv7'; 			sha256='f9d95a3bf756be4c6be661ab5799e9cb62423d24fd4bf65d9c59fa6ffbc1a525'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-aarch64'; 			sha256='f7e9ed22cf330018cdc3e802e59cacb7fff3520d62aa111ac6640e00597a0ebc'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-ppc64le'; 			sha256='d4994e1b0d5d00c6f09f9f88a7ad135a96d8e48f8fc4238896a152def0a0c65b'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-riscv64'; 			sha256='316569c1e2fb518ea141a1995b4de475ae12332a7e72bfb5a2fe25fa2feaa46b'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.38.1/docker-compose-linux-s390x'; 			sha256='421afc85b17ad6ae4667f209db337d18a8c74f567f99fac6bca0aa0f787697db'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
# Tue, 01 Jul 2025 11:30:04 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Tue, 01 Jul 2025 11:30:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 01 Jul 2025 11:30:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 01 Jul 2025 11:30:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 01 Jul 2025 11:30:04 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 01 Jul 2025 11:30:04 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 01 Jul 2025 11:30:04 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd44dfd9ed005c75b2cb9a6c317864eb4368c58ae4b63c38b49fcef96744bb3d`  
		Last Modified: Tue, 01 Jul 2025 22:15:59 GMT  
		Size: 8.2 MB (8207456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af87fb31fb204b986a2ce24d6a6290a769e24244e9db397c1bbb1f5e25ea1f62`  
		Last Modified: Tue, 01 Jul 2025 22:15:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ba0d1476fc03a1254882d18ff825a820613a2f00f046c3f019e29eed558d77`  
		Last Modified: Tue, 01 Jul 2025 22:16:00 GMT  
		Size: 20.5 MB (20460129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6554ec0ba85c0894e2b7ceefee577e11d3196b43f4ac00d19601f4ebf8e056b1`  
		Last Modified: Tue, 01 Jul 2025 22:16:00 GMT  
		Size: 21.7 MB (21664158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb2482a56648c057e733df5ad11a730bf635646cfe2dbbbacc26b9e4e5f6750`  
		Last Modified: Tue, 01 Jul 2025 22:16:00 GMT  
		Size: 21.3 MB (21277560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8f41e8fb760475e415f7e10d472bcf110b277816449c514abd3d5768f3bcbf`  
		Last Modified: Tue, 01 Jul 2025 22:15:58 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c78189052135631fbdad76724fa4c1a058ea6a8e3e2acb40e64ee7007e6b7cb`  
		Last Modified: Tue, 01 Jul 2025 22:15:58 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661366313eb25141f764ddced9e982fdd56adec7e328a83a55879e9570f78fa5`  
		Last Modified: Tue, 01 Jul 2025 22:15:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3a8fbe75c9efeb94904d463ffd3e335519a12357524e99c4e2cf76aaf0fe23`  
		Last Modified: Tue, 01 Jul 2025 22:26:24 GMT  
		Size: 6.9 MB (6905555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b028c5428339f83803fd8f7b2988a7f4040251f9072b45c950db3a391711f333`  
		Last Modified: Tue, 01 Jul 2025 22:26:24 GMT  
		Size: 90.5 KB (90499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32b3776b8124b62e7ef3c1d0d1c7b466219b26f42d2acca4f19107b9a9283e1`  
		Last Modified: Tue, 01 Jul 2025 22:26:24 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c51f3f5fea654fdabf4645b5aa26901cf8430d9d6543f62677a370d79b2993`  
		Last Modified: Tue, 01 Jul 2025 22:26:48 GMT  
		Size: 62.5 MB (62517911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771c3a6a10c440deeb4e5e675cbc6e2b77c1717364a00c27a81063631c71780b`  
		Last Modified: Tue, 01 Jul 2025 22:26:23 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35972af5640865dcd01bcf9bcc6133fcae45e5151c88b9f5dca19fc9f99adba`  
		Last Modified: Tue, 01 Jul 2025 22:26:23 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dfd7b5c7e3ee3672a6b4fa4b350a5b456032c7dcfcb3a9415121fd10dc3c4d`  
		Last Modified: Tue, 01 Jul 2025 23:08:24 GMT  
		Size: 3.4 MB (3398178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9331c075b28ba6f074bd2c95d65f235071b8771f4801daf36fb5494c85e461a7`  
		Last Modified: Tue, 01 Jul 2025 23:08:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7227d997deff13e7d9bf3c2eb4d2bf77d75e3cd90032689ac57378a3d6dc1bf6`  
		Last Modified: Tue, 01 Jul 2025 23:08:23 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2b1b7444bd3ad686c01c2d6ca52b923641e7aeccd07cbfde8af4b0b51ba4b6`  
		Last Modified: Tue, 01 Jul 2025 23:08:26 GMT  
		Size: 17.6 MB (17586160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab2074ebaedca65e270404437883e3f038935f007fb8ecc4be6b73d86bc3c95`  
		Last Modified: Tue, 01 Jul 2025 23:08:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:2015e46afc8395fa59ae314aff4d19a97bb55e6adca732fcb6d474ac24372580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77e5da124bd3fd047b0abd74751451272b6af835ba990d29667f1a1130e1a69`

```dockerfile
```

-	Layers:
	-	`sha256:f4ad1fc3c28c4aafc02c16134b0812567ed4bfc75fa5af7b49fc12d8543189be`  
		Last Modified: Wed, 02 Jul 2025 02:07:28 GMT  
		Size: 30.6 KB (30637 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:a6bdd6495f432d9e77784f68f76efbbb3c1876f32f241af8ec504eb422370bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154690467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367b736522af6576dc89a15b7ee3c18b96c615d7e19acbcc7337fcc9e369d27c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_VERSION=28.3.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD ["sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/var/lib/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 25 Jun 2025 05:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 25 Jun 2025 05:04:15 GMT
CMD []
# Wed, 25 Jun 2025 05:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 25 Jun 2025 05:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 25 Jun 2025 05:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efdbf9d870140ba6962f37fb5c88bd7ff5a6edbecc246ad72a2fa05bf931215`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 8.2 MB (8229004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76080ff7919b6f2f983bad6e60d90dd09fe89ae23d5d4b1902e2401d5bdb4c3`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8fd166aa06a91e8aebc25ae41e6d6cc5e7c28d6ed8d80900bbbff954c25039`  
		Last Modified: Wed, 25 Jun 2025 19:19:16 GMT  
		Size: 19.3 MB (19267886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d06e85c1279ded07aa91a88084a5150f5cd8d2548264b21d31466a83fd0efbe`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b960b1bcb756bfb47a9d30ccd9d833fa804cd1937e49192e352282b3052fd`  
		Last Modified: Wed, 25 Jun 2025 19:19:15 GMT  
		Size: 19.5 MB (19486356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6a465a1f82d236a77e9d56a61a47a52f485772e7b3f15e106ce33e9c0122cc`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe8bd6221f77de746989b8fb7c2fd18258ebe95bed0552e77da29f8bfb7b283`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282c032f942aa616f0cf5d86e61b242a81cb9a5dbc3501a625ac9011a60bd97`  
		Last Modified: Wed, 25 Jun 2025 19:19:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e288846779cb65a12fa9317a7d0b83901dc1fc974c4897d70d99298b6d554`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 7.1 MB (7141528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f38badf3f4309571b4ba9b63d0081039a46caa66d30e139be5a99b3246f837`  
		Last Modified: Wed, 25 Jun 2025 23:41:49 GMT  
		Size: 99.6 KB (99646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deace05d4e2463a7802c79c319cc8c0efec0da8e7e7d0e3fc50cb892300e9202`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c07753a1e7611acc40ff993b6bb77ee28e1c38d51232fad653499eab0b852e`  
		Last Modified: Wed, 25 Jun 2025 23:41:53 GMT  
		Size: 57.5 MB (57460850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5409164ad4fffce29827dfd0997d723d4acbb80a4db2c10cae16882640caf580`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc224144c04ef3481a0325fe0397605a96a0b2cc32a11f2bb51ff0f02cf3b18`  
		Last Modified: Wed, 25 Jun 2025 23:41:50 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5b66d211d051c20b2b8fa072c573c801a3adfd1d5f78c9d8d98055034dc9e7`  
		Last Modified: Thu, 26 Jun 2025 03:49:19 GMT  
		Size: 1.0 MB (1022998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c908d2ebbfc7e6af38b4d76f325a249fa359e7f524e0316bbac900fa8f5537d9`  
		Last Modified: Thu, 26 Jun 2025 03:49:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e3f97ea27b30130cf4a126e578dc57f0c0083a14c56fd56f3f1c6b6fa5ac8c`  
		Last Modified: Thu, 26 Jun 2025 03:49:19 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287bf6b6e7ca52eb877ac8a25ac379d4dee7dfe8d860e93321e2bea6e071b8bb`  
		Last Modified: Thu, 26 Jun 2025 03:49:23 GMT  
		Size: 18.0 MB (18017325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2657fca26a04fb60ad2dd915fd0c4265b8be7854c9d68e19e05ec4372bbaa4d9`  
		Last Modified: Thu, 26 Jun 2025 03:49:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:88444b092967d974c32eb7853e9c4b5224d33ba1f1c8d0d57229afa39d1e4a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300e4e22e9b75ecb5b98766fb00c00d442bf16258821538c09572ea9c4121594`

```dockerfile
```

-	Layers:
	-	`sha256:8cf7d1bd28dd5d695964242d21c1d714fc4616311036c7fbf166b8c83e3d1403`  
		Last Modified: Thu, 26 Jun 2025 05:07:29 GMT  
		Size: 30.6 KB (30621 bytes)  
		MIME: application/vnd.in-toto+json
