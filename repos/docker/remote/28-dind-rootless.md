## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:24f8d7d52a0929857ccefad85ac256f498a3cec347ab0ddab3912e15930e98c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:b3a65c98a8330e69bdcf5e6b938cdf8a9d82b58feab6f04389c655d04f7c8f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162799126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d4560ee9cf9fa438ecb6fddc66e1dd1f27610ca3028959f1597ce54ec88c44`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.2.2
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 30 May 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD []
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 30 May 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cc65efafcc08e79f71dae731e77e28d1d80b4e8ada17ff88b5734eddd8b2a5`  
		Last Modified: Tue, 24 Jun 2025 18:25:51 GMT  
		Size: 8.2 MB (8207465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d63cea5f093cb52e5db9c867ae989a06e7aa8da3e8b641acc40e3852a0b4a33`  
		Last Modified: Tue, 24 Jun 2025 18:25:51 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fb40a929fb94e74bfc7e12be73679efd7271a4a832ad71824a755c5fb98d52`  
		Last Modified: Tue, 24 Jun 2025 18:25:53 GMT  
		Size: 20.1 MB (20083032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4342d14bbc36cd4e7aca95e3da1601d37ac7d360ab3d1d2bc560921c779ac753`  
		Last Modified: Tue, 24 Jun 2025 18:25:53 GMT  
		Size: 21.7 MB (21664159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d7f0dca0e6ae8d3a54dc81a69eec3ed30d6f55304e7773186be2189f138654`  
		Last Modified: Tue, 24 Jun 2025 18:25:54 GMT  
		Size: 21.3 MB (21256113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33796bdf7104804d345eff4b4d83b52dfb7df5a630e8b745206114b8c3f0d83b`  
		Last Modified: Tue, 24 Jun 2025 18:25:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559fe81ecb98d50e6277594d9e182689dc4b1171a719ea5c67e66b714df0ac2e`  
		Last Modified: Tue, 24 Jun 2025 18:25:52 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34494de11e2361be041ad92d059656cb7c6769e655c88af2fea2a8ea9eb01f3f`  
		Last Modified: Tue, 24 Jun 2025 18:25:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f667be3e0ff8f4c28818d6f0525142b168bcbda9b76acf919e01ae972415dd6`  
		Last Modified: Tue, 24 Jun 2025 19:08:42 GMT  
		Size: 6.9 MB (6905603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14642f09a7eef7ea9bd9c186b71ea6e34202bbe820dea49f589afe1751bdbf8`  
		Last Modified: Tue, 24 Jun 2025 19:08:41 GMT  
		Size: 90.5 KB (90488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8442f8a96bd55582b3118587ab8eac4ddbf9bb9df2c6af59326acfc590ce163`  
		Last Modified: Tue, 24 Jun 2025 19:08:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d492bd36772d7d5a45f025052b03347b819f1be25e742ae76c39c74b7f288491`  
		Last Modified: Tue, 24 Jun 2025 19:08:51 GMT  
		Size: 62.2 MB (62206672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2b6397d8ae04439a856b225dd3824fe04b035aedf6402e8e4dd628529d7e9e`  
		Last Modified: Tue, 24 Jun 2025 19:08:43 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b59511e069b9e1b704d05c6a9cd72d042d1d1da6c1f755d9dce8ad8a771b5be`  
		Last Modified: Tue, 24 Jun 2025 19:21:05 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859499342ad159dd2ce959c5624fe22c016e29a0270150e81a8d2a9134e1b396`  
		Last Modified: Tue, 24 Jun 2025 20:08:15 GMT  
		Size: 993.3 KB (993284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a243d7b512b7006df7418ca5eccf2386d84490c14148b03e127633cd87671b34`  
		Last Modified: Tue, 24 Jun 2025 20:08:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629b274e29d1fd0ec4d5cc3ee17ce7bb1de1150b13c9499fea0316fc08fa6024`  
		Last Modified: Tue, 24 Jun 2025 20:08:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc21c6ee85925c53418c8e5a2297a35d4423904a16a1af78dee7465e5e3f7a5`  
		Last Modified: Tue, 24 Jun 2025 20:08:18 GMT  
		Size: 17.6 MB (17585966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b829b413d9ce175bdb2e9fb427eceb29120f2375484583b381f130ff4271cf4`  
		Last Modified: Tue, 24 Jun 2025 20:08:17 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:af39eef6ea89849b885164de65dfc48a417d43dd8e3ba1a648541bc56b07e95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70bfe6ca7fb8765c1491357beed3b9673ce8cc790d02aa2bc611b463d0cd07f`

```dockerfile
```

-	Layers:
	-	`sha256:56ef310a4c7097c2f6c59bc6838600021d0e16e5f09619351597fa9def2f12fe`  
		Last Modified: Tue, 24 Jun 2025 23:07:29 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:1ea35782946a090702895f3fc042c5fa0b16baeb47091f15cd7585f005c29ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154031432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722499bda8e9ce2751fc7f91ab80b36f761814abc0ff7ff0624dac9d959f9583`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.2.2
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.3
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-x86_64'; 			sha256='522181c447d831fb23134201d9cdc5cf365f913408124c678089ea62d6a2334c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv6'; 			sha256='06213b27bb8437f7bb306766a89adc8c6f0e39907b9e8774488f16efe4b580ce'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-armv7'; 			sha256='2abef7f6a59d5402206f11461b69b6314a5dfdcfdd235b9acfce661d9255f2be'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-aarch64'; 			sha256='15646d01e9291e69c9173a0d140d3ef44f912d26ffb2cbeeaf91aeb460dae59e'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-ppc64le'; 			sha256='1f7f9533bec72a38bc41afa0195189bd42d7be7374922fa40ea7424bab86f375'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-riscv64'; 			sha256='1b377c5857be66aa83e77182f83d5527b6c0a8baa30141dba1d8586e2b535baf'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.3/docker-compose-linux-s390x'; 			sha256='82549afc300c1318527ff693f22a41114bd7d5e787a63799c85bf511d8428cea'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.2.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.2.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 30 May 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 30 May 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 30 May 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 30 May 2025 17:04:15 GMT
CMD []
# Fri, 30 May 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.2.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.2.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 30 May 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 30 May 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 30 May 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c09c12dc876098db6faf127232f099623dbbbd3cf517f8246c8e5a8693e4f0`  
		Last Modified: Tue, 24 Jun 2025 18:27:47 GMT  
		Size: 8.2 MB (8228991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9495848de01826cc1e9f97b4397c76a8e5a50477e0ec7feb5d771d0911cc3918`  
		Last Modified: Tue, 24 Jun 2025 18:27:45 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a4c5587a885f488c1b2f7bd2d5d32c10b81adac78c6f4cae59b7d3ffacc4c0`  
		Last Modified: Tue, 24 Jun 2025 18:27:58 GMT  
		Size: 18.9 MB (18902603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0440c711470911bab6b20e4bff43ae46bc807cfb50baad00736c85ef6ee037`  
		Last Modified: Tue, 24 Jun 2025 18:27:59 GMT  
		Size: 19.8 MB (19819434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bfc89a1b69a15d2139349e50f73a98ddb63456d8d3b225411d135bea009a5b`  
		Last Modified: Tue, 24 Jun 2025 18:27:59 GMT  
		Size: 19.5 MB (19486365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7784f7f21537b654c4293cc583ba7c3d9a18e7acd718257c48d94bd517286fe`  
		Last Modified: Tue, 24 Jun 2025 18:27:58 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bf71c0421d5c63713f96809b651570077f7fc8485542df3ed287ba4166a3ad`  
		Last Modified: Tue, 24 Jun 2025 18:27:57 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854c48005dea8fe0d9b72fccbcd05edf5bce65fdd68e88de3341f581e3864b54`  
		Last Modified: Tue, 24 Jun 2025 18:27:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec98a5da319d161a21b78c776643d245448cd3cf6263408798dbd7230a6ced0`  
		Last Modified: Tue, 24 Jun 2025 20:07:44 GMT  
		Size: 7.1 MB (7141609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9463689252bcef2c2f0bd72219347662a2f636cd2fa7278cbcdb71d247d95c0d`  
		Last Modified: Tue, 24 Jun 2025 19:21:09 GMT  
		Size: 99.6 KB (99624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63f2016c38bb55bb58a699b9cc351277da1962be5b7e0fb63e15a4a2becd2d1`  
		Last Modified: Tue, 24 Jun 2025 19:22:15 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858b9c6f7d050584858e50e4866506c3437ac049885f67c2b65f103faeb7525b`  
		Last Modified: Tue, 24 Jun 2025 20:07:45 GMT  
		Size: 57.2 MB (57168201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2165fd945e91a19d72172d2047400d94969e0b62e250c31c96487df4fcfe8d54`  
		Last Modified: Tue, 24 Jun 2025 19:22:18 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff290852ce439256f869c129eefd252c207538bb2329ea0edfaefe24fe3e3de`  
		Last Modified: Tue, 24 Jun 2025 19:22:22 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b764990cb7c486c41c07f474e0505d88e5fc04584316b23371205ba8ac8e24f`  
		Last Modified: Tue, 24 Jun 2025 21:14:37 GMT  
		Size: 1.0 MB (1023001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8a119348331336a59cd165ee247637f49a0ebd7a6535ceabb4753557f0d81a`  
		Last Modified: Tue, 24 Jun 2025 21:14:41 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5566d4e79b8d1a822e82c87beec39c6bd89b55d78b3cdf477343a9812dde81`  
		Last Modified: Tue, 24 Jun 2025 21:14:44 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5369bf56ba7ffe92c2a88b9e7570ec85c1a89a12453c2c89fc68fa8dbb5b89`  
		Last Modified: Tue, 24 Jun 2025 23:07:45 GMT  
		Size: 18.0 MB (18016170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f56c4bfda7e9e61df44e59d3855d63cd782076bd6adc94367e0b5c6fde579f`  
		Last Modified: Tue, 24 Jun 2025 21:14:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6baabb6cd3f787552b8eb5114e8c81b0fcc95b8aa4ba65d0c51ede32737c1c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3236b3f82ac58ebe62cb6acec39e97dd557c8e59249b0108344165ff795884`

```dockerfile
```

-	Layers:
	-	`sha256:0f6dfef10b398f8d9bce2c61f2694864517b2dca2a765c00639a411b659c2f27`  
		Last Modified: Tue, 24 Jun 2025 23:07:33 GMT  
		Size: 30.6 KB (30620 bytes)  
		MIME: application/vnd.in-toto+json
