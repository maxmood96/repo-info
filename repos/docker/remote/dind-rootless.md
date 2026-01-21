## `docker:dind-rootless`

```console
$ docker pull docker@sha256:3f2db3470a9c852cb3493b458358ec3a170a710b68f699db161b7ed87ec8583a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:0243a4d78952d40df5bb0d0588c62079ee188b3fb42c260d50143cb74fc81fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156897816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd11b6e29c5be04e5fd396b251314fa0639890ee0b7375134e92b9f8e972ed00`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:30:45 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Jan 2026 23:30:45 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Jan 2026 23:30:45 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Jan 2026 23:30:48 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:30:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Jan 2026 23:30:48 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:30:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Jan 2026 23:30:48 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:30:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Jan 2026 23:30:49 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Jan 2026 23:30:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:30:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Jan 2026 23:30:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Jan 2026 23:30:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:30:49 GMT
CMD ["sh"]
# Fri, 16 Jan 2026 23:43:48 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 16 Jan 2026 23:43:48 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 16 Jan 2026 23:43:48 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 16 Jan 2026 23:43:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 16 Jan 2026 23:43:51 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 16 Jan 2026 23:43:51 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 16 Jan 2026 23:43:51 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:43:51 GMT
VOLUME [/var/lib/docker]
# Fri, 16 Jan 2026 23:43:51 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 16 Jan 2026 23:43:51 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 16 Jan 2026 23:43:51 GMT
CMD []
# Sat, 17 Jan 2026 00:14:46 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 17 Jan 2026 00:14:46 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 17 Jan 2026 00:14:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 17 Jan 2026 00:14:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 17 Jan 2026 00:14:47 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 17 Jan 2026 00:14:47 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 17 Jan 2026 00:14:47 GMT
USER rootless
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d08bf8475bf9e689c0d705f9b2b740fdc6f57fc7ea8522fa321e0407d5542a`  
		Last Modified: Fri, 16 Jan 2026 23:31:05 GMT  
		Size: 8.4 MB (8399670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e0a1bb1a714c3574763a4e79760a69a83b79cfeb1bed66e1183734cba512ea`  
		Last Modified: Fri, 16 Jan 2026 23:31:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f56b512895821ca11cd19fa0f3496f6b325efd5ad4006b5c4dec5828cfbb46`  
		Last Modified: Fri, 16 Jan 2026 23:30:56 GMT  
		Size: 18.7 MB (18749967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193ef8aa785fdc807d36f7842f2550fde47924a84196a0e8cae74d61c7ce918f`  
		Last Modified: Fri, 16 Jan 2026 23:31:06 GMT  
		Size: 22.9 MB (22905484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd266dff25ac5344bf8acdd83dd1d11a4d114b78e85830c712f55773276c565`  
		Last Modified: Fri, 16 Jan 2026 23:31:06 GMT  
		Size: 10.8 MB (10787419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c46e30e1e8ddc2abe93c818cbc340f93e0d470ba6d76e35a129274946a2191`  
		Last Modified: Fri, 16 Jan 2026 23:30:57 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd70625831c839f25752faf71a054de3bf972e39226d555c0c024a6bb1af04f`  
		Last Modified: Fri, 16 Jan 2026 23:31:03 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa84a26e75eabb10ad201c611a85dfeeda810506ca9d74cfcda13603e3667d5f`  
		Last Modified: Fri, 16 Jan 2026 23:43:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a227f237fe1cc495143034aa29d1f3bb34935624b3a1968387be3be9643afd`  
		Last Modified: Fri, 16 Jan 2026 23:44:09 GMT  
		Size: 6.9 MB (6934060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9e772224d42944940e5982b30cb03a21c31a9597a8266f2dd3b8ee81c921a4`  
		Last Modified: Fri, 16 Jan 2026 23:44:07 GMT  
		Size: 92.5 KB (92455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9840a05cb973e2d8b0c68b64a66746c6d190887c3dd23d828c49ce56fd762bb6`  
		Last Modified: Fri, 16 Jan 2026 23:44:07 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96e9a4646741eb4c737b5a5be006e0597cc26cef2276a4886f5fe1e3ba2288f`  
		Last Modified: Fri, 16 Jan 2026 23:44:17 GMT  
		Size: 64.4 MB (64367539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf27a6cf55bb7deeafc395d22479b56698da0c32ef86ab9e517d8d4ca1f33b41`  
		Last Modified: Fri, 16 Jan 2026 23:44:01 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6b1067e7e749c94b29fbcac41bc9d5ec545fb31d5b5ddb1f3a0b52ea357d41`  
		Last Modified: Fri, 16 Jan 2026 23:44:07 GMT  
		Size: 3.3 KB (3294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1557b2a406cc6f243f0171436f503bdb8e8d1e3e77bdcf36bc1b684311ed72`  
		Last Modified: Sat, 17 Jan 2026 00:15:00 GMT  
		Size: 3.4 MB (3419929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d8849e55ddf8f1caa5eaf086451cea763b8e9545dd3c3e97fdcdb59ef201a5`  
		Last Modified: Sat, 17 Jan 2026 00:15:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a94cff53939cdff88071fbd8e0fa9d0603580457bd6118ab08d88cf2201942`  
		Last Modified: Sat, 17 Jan 2026 00:15:00 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47d0dfc54602c4b9b436657ddff22108d34d2abee74a876828b8012a4c8e868`  
		Last Modified: Sat, 17 Jan 2026 00:14:54 GMT  
		Size: 17.4 MB (17371697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b922a090e96a69d521d8afb6527fa2cb7242cbf56626b59321174c38d81e858a`  
		Last Modified: Sat, 17 Jan 2026 00:15:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0fd9fbb62a639e7252d765f5048eb16278bc79dcb4f8d9d009d0865bbbee3f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806c70902187480fa7c1e67f5d2c797823edf7c685d7a8287068805b10700eac`

```dockerfile
```

-	Layers:
	-	`sha256:23843ead6c976efa05fb6d29fb376141c08d5d275ec15b7b1505a7f30b3d98dc`  
		Last Modified: Sat, 17 Jan 2026 03:07:51 GMT  
		Size: 30.6 KB (30589 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:14079d6dfc0f30439e105f43b71d745253f8da53ff591fc0c4376b8acb52b95c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147399701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6087b7c78ab28b0a866d9ea8abec22d95e2bfd23462b59ab08767164d9effb70`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:33:39 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 16 Jan 2026 23:33:39 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 16 Jan 2026 23:33:39 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 16 Jan 2026 23:33:41 GMT
ENV DOCKER_VERSION=29.1.5
# Fri, 16 Jan 2026 23:33:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 16 Jan 2026 23:33:41 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Fri, 16 Jan 2026 23:33:42 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 16 Jan 2026 23:33:42 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.1
# Fri, 16 Jan 2026 23:33:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64'; 			sha256='cdc1df64412ed009312afbc044b3625144d06c07736e2f7a77fb0460531b9327'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv6'; 			sha256='b19c5b17edfc2202921beaf0e672b3851276f414544b66dce354e3d613d00458'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-armv7'; 			sha256='f2262cc9e210bf6a01b054ffd96283996e3af66d5a117b70e1b573517c54f152'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-aarch64'; 			sha256='e3b36491a75f92c35ebfbbe6e4741bd2429664edf3971427983d67c0b21e7d1d'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-ppc64le'; 			sha256='e3f9031f60a31f3c6adff7c78f2ab654d462aab711699de53345139e27e91973'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-riscv64'; 			sha256='50f31386a62b77e95068573ac86d6f1be70fb1196ea92ae57757aa1d6fa2aa8d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-s390x'; 			sha256='7176f6a356ef0d764a9fe8f82873018e89e9f83008069c5252e0b3cf2beca634'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 16 Jan 2026 23:33:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 16 Jan 2026 23:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:33:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 16 Jan 2026 23:33:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 16 Jan 2026 23:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:33:43 GMT
CMD ["sh"]
# Fri, 16 Jan 2026 23:43:45 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 16 Jan 2026 23:43:45 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 16 Jan 2026 23:43:45 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 16 Jan 2026 23:43:48 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-29.1.5.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-29.1.5.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 16 Jan 2026 23:43:48 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 16 Jan 2026 23:43:48 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 16 Jan 2026 23:43:48 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:43:48 GMT
VOLUME [/var/lib/docker]
# Fri, 16 Jan 2026 23:43:48 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 16 Jan 2026 23:43:48 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 16 Jan 2026 23:43:48 GMT
CMD []
# Sat, 17 Jan 2026 00:15:09 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Sat, 17 Jan 2026 00:15:09 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Sat, 17 Jan 2026 00:15:10 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Sat, 17 Jan 2026 00:15:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-29.1.5.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-29.1.5.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Sat, 17 Jan 2026 00:15:12 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Sat, 17 Jan 2026 00:15:12 GMT
VOLUME [/home/rootless/.local/share/docker]
# Sat, 17 Jan 2026 00:15:12 GMT
USER rootless
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20aa2d791b8266f9dfa17d7927ad7bb695c7563923625c1f1b6b63d3e8a000b8`  
		Last Modified: Fri, 16 Jan 2026 23:33:58 GMT  
		Size: 8.5 MB (8453607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99f01766c5623ec5c29704949d2f9e78727351173fec312a472dda75bfe0fbc`  
		Last Modified: Fri, 16 Jan 2026 23:33:56 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cabe03379fd0715f8af4465bd60c20e0b9ff94b7b56d8ca8d804f4197a2302`  
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 17.3 MB (17329430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25675d97e9938547e8ec5252c02b0cf250b6e0f0c0e29a8c9d09b5cd2658f857`  
		Last Modified: Fri, 16 Jan 2026 23:33:50 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a994915892fc185bb6d8b8ca8d5fa8b7db988b37b0d8a0c01efc25df4f1fa3e8`  
		Last Modified: Fri, 16 Jan 2026 23:33:57 GMT  
		Size: 9.9 MB (9942176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f459c129e2df20f5a0b9d2cef232a2dcc43c1a744d94e95858ab5898896faead`  
		Last Modified: Fri, 16 Jan 2026 23:33:56 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cb42b654a8b7f6386af70afcfb18943c2b6ddfac3d25ac7663ad506613f927`  
		Last Modified: Fri, 16 Jan 2026 23:33:57 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985d6fb9c70efed7fba20dcfd74096bc1b34a04d71408695041842c10709c246`  
		Last Modified: Fri, 16 Jan 2026 23:33:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba14d49cf482ad8767be9715f12c32540f21afe52f5eeea827d7889eef9f4e5`  
		Last Modified: Fri, 16 Jan 2026 23:44:06 GMT  
		Size: 7.2 MB (7212983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869ecca31b7e4cb47dac3444670d9ac67935d4711faf1f4dc73c54448119f58`  
		Last Modified: Fri, 16 Jan 2026 23:44:05 GMT  
		Size: 101.3 KB (101282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07025eda5cadcd2aad50deee35f3f3e4ab0f3bd4d0bf30ede81de47cfdde90d6`  
		Last Modified: Fri, 16 Jan 2026 23:43:57 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9a4cc2ba717f8eaa4d250fcc460585a66fa48d9b640e570c448565b2ff4224`  
		Last Modified: Fri, 16 Jan 2026 23:44:12 GMT  
		Size: 58.4 MB (58406140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a638ecdb28d6f3ef84b8965d4d72c090a5fe9530f2ae82b504110a080dd6b6`  
		Last Modified: Fri, 16 Jan 2026 23:43:59 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2e1b9ff15531a4e7ef51a952d5340d1ffe0cb228d4ac9cf30b62de4d8578ac`  
		Last Modified: Fri, 16 Jan 2026 23:43:59 GMT  
		Size: 3.3 KB (3299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62989d71bec09d62584767340114f105a406f8384b68cf5433baa6e5de529e25`  
		Last Modified: Sat, 17 Jan 2026 00:15:18 GMT  
		Size: 3.4 MB (3394365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04e7033552d328933a1b36fbf42c05e189e12b2efd0dd322461f1dd9f27a921`  
		Last Modified: Sat, 17 Jan 2026 00:15:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12502433d4f521c091bf5f40e0a2f10c483376cd6cf491d5167d0d71255e93ae`  
		Last Modified: Sat, 17 Jan 2026 00:15:18 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028d45c1e6c47fa93138f7186507cc4c5173fce93755e0c753f472d31ca4449d`  
		Last Modified: Sat, 17 Jan 2026 00:15:29 GMT  
		Size: 17.7 MB (17709424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d784a5d534b102bd49b134cf1aa67620b01c91b045f85c4618fba5fa487ff05b`  
		Last Modified: Sat, 17 Jan 2026 00:15:24 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b70f9caf41eb196a2b6393247841ce3bf37d17ff2afa2c50bb06dd616d0bfdc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71ba866d349862b3bc3dfe53070a91544673fb4b1356f80edceb90836b17e7f`

```dockerfile
```

-	Layers:
	-	`sha256:93922cd50e5c74f53340ea243e39afeaf247cd99375d9e0311679382593e16c9`  
		Last Modified: Sat, 17 Jan 2026 03:07:54 GMT  
		Size: 30.8 KB (30753 bytes)  
		MIME: application/vnd.in-toto+json
